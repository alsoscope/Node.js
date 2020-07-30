tdl.js

    var http = require('http');
    var fs = require('fs');

    http.createServer(function(request, response){
        fs.readFile(`./tdl.html`, 'utf8', function(err, data){
            response.writeHead(200);
            response.end(data);
        });
    }).listen(3000);

    console.log("Server running ...");
