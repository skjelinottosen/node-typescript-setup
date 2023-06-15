# Node.js with TypeScript 


To set up a Node.js project with TypeScript, follow the steps below:

## Step 1: Initialize the project

Run the following command to initialize a new Node.js project with a default package.json file:
````
npm init -y
````
The npm init -y command initializes the project without interactive prompts, automatically accepting default values for the package.json file.

## Step 2: Install TypeScript and type definitions for Node.js
To install TypeScript and the type definitions for Node.js, use the following command:

````
npm install -D typescript @types/node
````
The command npm install -D typescript @types/node is used to install TypeScript and the TypeScript type definitions for Node.js as dev dependencies in your Node.js project.


## Step 3: Update the package.json file
Update the package.json file to include a build script and specify the module type as "module". Open the package.json file and modify it as follows:

````
{
  "type": "module",
  "scripts": {
    "build": "tsc"
  }
}
`````
"type": "module": This line sets the module type to module. This indicates that your code will be using ES modules instead of CommonJS modules.
"scripts": { "build": "tsc" }: This adds a build script named build that executes the tsc command. tsc is the TypeScript compiler, and running this script will compile your TypeScript code into JavaScript.


## Step 4: Create a tsconfig.json file
Create a tsconfig.json file in the root directory of your project and add the following configuration:

````
{
  "compilerOptions": {
    "module": "NodeNext",
    "moduleResolution": "NodeNext",
    "target": "ES2022",
    "sourceMap": true,
    "outDir": "dist"
  },
  "include": ["src/**/*"]
}
`````

"compilerOptions": This section specifies the compiler options for TypeScript.\
<br/>
"module": "NodeNext": This option enables compatibility with ES modules and CommonJS modules in Node.js.\
<br/>
"moduleResolution": "NodeNext": This option tells TypeScript to use Node.js-style module resolution when resolving module imports.\
<br/>
"target": "ES2022": This option sets the ECMAScript target version to ES2022, which is the version of JavaScript that TypeScript will compile your code to.\
<br/>
"sourceMap": true: This option generates source map files alongside the compiled JavaScript code. Source maps help with debugging by mapping the compiled code back to the original TypeScript code.
<br/>
<br/>
"outDir": "dist": This option specifies the output directory for the compiled JavaScript files.\
<br/>
"include": ["src/**/*"]: This specifies the files that should be included for compilation. In this case, it includes all files in the src directory and its subdirectories.
