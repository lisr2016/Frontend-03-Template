学习笔记
浏览器工作原理第二课


HTML解析
server.js

const http = require('http');

http.createServer((request, response) => {
    let body = [];
    request.on('error', (err) => {
        console.error(err);
    }).on('data', (chunk) => {
        body.push(chunk.toString());
    }).on('end', () => {
        body = Buffer.concat(body).toString();
        console.log('body:', body);
        response.writeHead(200, {'Content-Type': 'text/html'});
        response.end(' Hello World\n');
    });
}).listen(8088);

console.log('server started');

client.js

const net = require('net');

class Request {
    constructor (options) {
        this.method = options.method || 'GET';
        this.host = options.host;
        this.port = options.port || 80;
        this.path = options.path || '/';
        this.body = options.body || {};
        this.headers = options.headers || {};
        if (!this.headers['Content-Type']) {
            this.headers['Content-Type'] = 'application/x-www-form-urlencoded';
        }
        
        if(this.headers['Content-Type'] === 'application/json')
            this.bodyText = JSON.stringify(this.body);
        else if(this.headers['Content-Type'] === 'application/x-www-form-urlencoded')
            this.bodyText = Object.keys(this.body).map(key => `${key}=${encodeURIComponent()}`)
        this.headers['Content-Length'] = this.bodyText.length;
    }
    
    send() {
        return new Promise((resolve, reject) => {
            const parser = new ResponseParser;
            resolve('');
        })
    }
}

class ResponseParser {
    constructor () {
    }
    
    receive(string) {
        for (let i = 0; i < string.length; i++) {
            this.receive(Char(string.charAt(i)));
        }
    }
    
    receiveChar(char) {
    
    }
}



CSS计算




课程总结

HTML解析
parse模块的文件拆分
 parser接受HTML文本作为参数，返回一棵DOM树

用FSM实现HTML的分析
 创建状态机
 HTML已经有设计好的状态机
 创建一个Symbol， 'EOF'，作为最后一个输入给到状态机
解析标签
 HTML tag: 1.开始标签 2.结束标签 3.自封闭标签
 
创建元素

处理属性

用token构建DOM树

将文本节点加到DOM树

CSS计算
收集CSS规则

添加调用

获取父元素序列

选择器与元素的匹配

计算选择器与元素匹配

生成computed属性

specificity的计算逻辑


