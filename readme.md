1] download node js
2] run below command to check whether node js is installed or not
```bash
node -v
```

3] we'll use express JS to connect computer and server
4] We'll use routes
5] open terminal in VS code
use following command
```bash
npm init
package name: chaibackend
version : 
description : 
entry point: index.js
test command : 
git repo : 
keywords : 
author : 
license : 
Yes
```

6] There is a file package.json : 

"scripts" is important to run index.js .

```bash
"scripts":{
    "start" : "node index.js"
}
```

Run it using following command : 
```bash
npm run start
```

7] Install express js
```bash 
npm install express
```

8] Go to express js website and copy the code given in "Hello world" section . Copy and paste it in index.js section . 

```JS
const express = require(`express`)
const app = express()
const port = 3000

// Response on home route
app.get('/',(req,res)=>{
    res.send(`Hello world`)
})

// Response on xyz route
app.get('/xyz',(req,res)=>{
    res.send(`Response on xyz`)
})

// Response to login 
app.get('/login',(req,res)=>{
    res.send(`<h1>Hello user login</h1>`)
})


app.listen(port,()=>{
    console.log(`Example app listening on port ${port} .`)
})
```

Run this file using following command : 
```bash 
npm run start
```

9] Install dot env
```bash
npm i dotnev
```

Create a file .env in worksapce . 
-- Remember 'All the sensitive variables , data name is stored in .env file so that no one can access them directly .'

Follow the steps to use sensitive variables : 
```JS 
// in index.js
require('dotenv').config()

// Suppose PORT is stored in the .env file
// access it as below
process.env.PORT // You will access the port
```


10] Deploying at production level
- Before deploying code , deploy it to github : 
    - Dont deploy files which have sensitive info . Add those files to .gitignore . 
    ```git
        name_of_folder/file1
        name_of_folder/file2
        name_of_folder/file3
        .
        .
        .
        .
    ```
- Now open `Digital Ocean` 
- Click on 'create'
- choose 'app'
- choose github and reposiratory .