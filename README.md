# i-app Language Support for Visual Studio Code
This extension adds support for the i-app programming language to Visual Studio Code.

[![Discord Chat](https://img.shields.io/badge/chat-discord-blue.svg)](https://discord.gg/N5Z7Z8NF)

[![Contribute](https://img.shields.io/badge/help-contribute-551A8B.svg)](https://github.com/MWN-S/i-app)

[<img src="https://i-app.org/img/i-app.gif" width="128"/>](https://i-app.org)

#   i-app

## Welcome To  i-app Revolution
### `Build the Future  Build the Next Big Thing`
i-app is a revolutionary new open-source programming language that aims to help developers improve their productivity by providing them with a working environment and a library of tools to build front-end and back-end applications.

> Easy and Fast use .app
## Learn i-app
```
{
    /* No cote ',' or ';'  */ 
    /*you can easy render any componet app by i_root:"filename" 
    anther keys will return false in that case
    */
    i_root:"menu"
    /** i: its element key its like id in html but its not
     *  render atterbute for security you can also use id: insted for
     *  public use in DOM 
     * */
    i:'app'
    
    /*typ: if you dont write type key = typ it will back as default as layout and layout in web version = </div> return or choose typ:( tx=</p> | ti=</h1> or use html tag  a | p | b | img etc..) */
     typ:"ly"
     /*
     cls 
     
     bassic css class
     iapp.min.css
     auto css class 
     B_"colorkey" = background:var(--color)
     P_5 = padding:5px
     F_W = color:#fff
     connected with colors
     1-colors balet 
     colors.json 
     2-theme ballet 
     to switch between dark and light mode 
     style.json  
     */
     cls:["WW","HH","F_W"]
     /**
      * you can write html style
      * with all it power if you need
      */
     
     style:{
        minWidth:"50px"
    }
     /* txt can be string as next example or it can be array 
     of txt object [{t:"d" d:"hello world"}]
      and theres a lot of kind of object like auto text
       translate or query text and many of anther functions you can under stand 
       from the next code
       text render before any anther elm in innerHtml
       */
       
      txt:"hello world"
      /**
       * 
       * you can easy render anther  elements to make 
       * any your dream app tree 
       */
      elm:[{
        typ:"t"/** t= table */
        elm:[{
            typ:"tr"
            elm:[{
                typ:"th"
                txt:"No"
            },{
                typ:"th"
                txt:"Name"
            },{
                typ:"th"
                txt:"Title"
            }]

        }]
      }]
    /*data: you can write a  query  to database and connect to i-app-server [mysql]*/
    data:[
        {
                    a: "get"
                    n: "emploees"
                    s: ["A"]
                    l: 0
                    q: [
                        [
                            [1, 0, "uneq"]
                        ]
                    ]
                }
    ]
   
    before:[{
       
        txt: "element text before render query "
    }]
    /** model: 
     * render your query inside the etement or 
     * anther and you control every index
     *  by q:{s:static string i: index data you chose to key with}
     *  wich generte uniqe i 
     * every model will parse one index data

     * */
    model: [{
        typ: "tr"
        q: {
            s: "id_",
            i: "id"
        },
        elm:[
            {
                typ:"td"
                txt: { t: "d", c: "q", d: "no" }
            }, {
                typ:"td"
                txt: { t: "d", c: "q", d: "name" }
            },
            {
                typ:"td"
                txt: { t: "d", c: "qtx", d: "title" }
            }
        ]
       
    }]
    /** if query back FALSE or [] it will render else */
    else:[{
       
        txt: {t:"s",d:"no-data-error" }
    }]
    after:[{
       
        txt: "element text after render query "
    }]

    /* if you insert function it will be default onclick function you can choose between all function types */
    fn["fn name"](){}
    }
```
---
## Read More ... https://i-app.org

---



## Features
* Syntax highlighting for i-app files
* Auto-indentation for i-app code
* Code snippets for common i-app constructs
* Basic code completion for keywords and functions
* Integration with Visual Studio Code's built-in debugger
## Requirements
This extension requires Visual Studio Code version 1.50.0 or later.

## Usage
To use this extension, simply open a file with the ".app" extension in Visual Studio Code. The syntax highlighting, auto-indentation, and code snippets will be available automatically. Code completion is triggered by pressing Ctrl+Space.

Debugging support is provided through the use of a launch configuration in the ".vscode/launch.json" file. An example launch configuration is provided below:
```
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "iapp",
            "request": "launch",
            "name": "Debug i-app Program",
            "program": "${workspaceFolder}/main.i",
            "args": [],
            "cwd": "${workspaceFolder}",
            "preLaunchTask": "build",
            "runtimeExecutable": "/path/to/iapp-interpreter",
            "runtimeArgs": ["-debug"]
        }
    ]
}

```
To use this launch configuration, you will need to replace "/path/to/iapp-interpreter" with the path to the i-app interpreter on your system. You may also need to modify the "program" field to specify the path to the i-app file you wish to debug.

> Contributing

If you encounter any bugs or issues with this extension, please report them on the GitHub repository: https://github.com/MWN-S/i-app-vscode-ex

If you would like to contribute to this extension, feel free to fork the repository and submit pull requests with your changes.

### License
This extension is licensed under the MIT License. See the LICENSE file for details.