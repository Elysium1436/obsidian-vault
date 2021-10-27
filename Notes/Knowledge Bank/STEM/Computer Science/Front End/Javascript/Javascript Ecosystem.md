## The Javascript Ecosystem

#### Build Tools
Any tool that is used to transform the development code to production is a build tool. They can be divided into three categories
- Package Manager
	These are what you use to install and manage dependencies. [[NPM]], Yarn
- Transpilers: Lets developers use updates, features, extensions, etc, while still maintaining browser compatibility. Example is [[Babel]]
- Bundlers: Used to read every import or require statement, finding libraries, put them in the appropriate scopes, and join them into one big js file. Common ones are Browserify, Webpack and Parcel
- Minifiers: Reduces the size of the code by removing white space and code comments. You can also use an obfuscate step that changes symbol names and make it even more optimized and less human redable. UglifyJS, Packer, Minify, etc.







##### An overview
![[Pasted image 20211025114142.png]]

