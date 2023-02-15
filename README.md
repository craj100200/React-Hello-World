# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)

### STEPS TO CREATE THE PROJECT 

=====================================================================
STEP 1 : Create React App in a container
=====================================================================
docker run  -it -p 7000:3000 --name reactContainer -v "D:\Docker-Volumes\react:/my-app"  alpine 

apk add --update nodejs
apk add --update npm 
npx create-react-app my-app
cd my-app
npm start

apk add --update curl
======================================================================


=====================================================================
STEP 2 : Create a new component HelloWorld.js
=====================================================================
1. Navidate to my-app/src folder. This is the folder where App.js and 
index.js files are located. 

2. Create a new file HelloWorld.js in this folder. Write the following 
code in the file: 

----------------------------------------------------------------------
HelloWorld.js
----------------------------------------------------------------------
import React from "react";

class HelloWorld extends React.Component { 

	render() {
		return (
			<div>
				<h1>Hello World From React</h1>
			</div>
		); 
		} 
} 

export default HelloWorld;
----------------------------------------------------------------------

3. Save this file. 
======================================================================

======================================================================
STEP 3 : Change index.js
======================================================================
1. The existing index.js file in my-app/src folder renders <App /> in 
its render method: 

	const root = ReactDOM.createRoot(document.getElementById('root'));
	root.render(
	<React.StrictMode>
		<App />
	</React.StrictMode>
	);

2. Remove the <App /> tag from the above code and replace it with 
<HelloWorld /> : 

	root.render(
	<React.StrictMode>
		<HelloWorld />
	</React.StrictMode>
	);	

3. Add an import for HelloWorld component: 
import HelloWorld from './HelloWorld.js';

4. Save index.js file. 

5. Run the project: 
	npm start

6. From your local computer browse to the url localhost:7000
You should see the text "Hello World From React" in H1 format. 

NOTE: Since you are using unix container, note that filenames are 
case sensitive. So if you change the casing of file name in the 
import statement ( suppose you write Helloworld.js instead of HelloWorld.js)
you will get a "Module not found: Error : Can't resolve './Helloworld.js'; 
======================================================================

