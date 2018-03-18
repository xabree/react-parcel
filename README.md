# setting up react and parcel bunlder with zero config

install dependencies from scratch in one command

```
mkdir learn && cd learn && npm init -y && git init && npm i -D parcel-bundler && npm i -S react@next react-dom@next && touch index.html && touch client.js && touch server.js && touch README.md && mkdir src && touch src/app.js && code . && ./node_modules/.bin/parcel index.html --open
```

this command will create folder -> open folder -> init npm -> init git -> install parcel-bundler as devDependencies -> install react, react-dom as dependencies -> create file index.html, index.js and README.md -> create folder src -> create app.js file && running parcel bundle -> open vscode to start coding :)

edit `src/app.js`
```
import React from "react";
const App = () => <div>hello world</div>;
export default App;

```

edit `client.js`
```
import React from "react";
import ReactDom from "react-dom";
import App from "./src/app";

ReactDom.render(<App />, document.getElementById("app"));
```

edit `index.html`

```
<html>

<head>
    <title>setting up react and parcel bunlder with zero config</title>
</head>

<body>
    <div id="app" />
    <script src="./client.js"></script>
</body>

</html>
