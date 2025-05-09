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

# Loan Sense Frontend Deployment Guide

## Prerequisites
- Node.js (v14 or higher)
- npm (Node Package Manager)

## Local Development Setup
1. Install dependencies:
```bash
npm install
```

2. Start the development server:
```bash
npm start
```

## Production Deployment

### Option 1: Deploy to Vercel
1. Create a Vercel account
2. Install Vercel CLI:
```bash
npm install -g vercel
```

3. Deploy to Vercel:
```bash
vercel
```

### Option 2: Deploy to Netlify
1. Create a Netlify account
2. Install Netlify CLI:
```bash
npm install -g netlify-cli
```

3. Build the project:
```bash
npm run build
```

4. Deploy to Netlify:
```bash
netlify deploy
```

### Option 3: Deploy to GitHub Pages
1. Install gh-pages:
```bash
npm install --save gh-pages
```

2. Add homepage to package.json:
```json
"homepage": "https://yourusername.github.io/loan-sense"
```

3. Add deploy scripts to package.json:
```json
"scripts": {
  "predeploy": "npm run build",
  "deploy": "gh-pages -d build"
}
```

4. Deploy to GitHub Pages:
```bash
npm run deploy
```

## Environment Variables
Create a `.env` file with the following variables:
```
REACT_APP_API_URL=https://your-backend-url.com
```

## Production Build
1. Create a production build:
```bash
npm run build
```

2. The build files will be in the `build` directory

## Production Considerations
- Update API endpoints to use production URLs
- Implement proper error handling
- Set up proper CORS configuration
- Use environment variables for configuration
- Implement proper security measures
- Set up proper caching
- Configure proper build optimization
