# Getting Started with Create React App

## AWS CLI setup
* [Download](https://awscli.amazonaws.com/AWSCLIV2.msi)
* [Reference video](https://www.youtube.com/watch?v=BzzCIsjrE7U)
* Check if it installed
```
C:\Users\nhlanhla>aws --version
aws-cli/2.15.25 Python/3.11.8 Windows/10 exe/AMD64 prompt/off
```
* Go to AWS console and create a group
* Create an IAM user and assign a group
* Go the user to assign security credentials, by creating access keys
* After creating access key go to CMD and do the following
`aws configure`
```
C:\Users\nhlanhla>aws configure
AWS Access Key ID [None]: AKIAZ*********
AWS Secret Access Key [None]: JKQSEag********
Default region name [None]: us-east-1
Default output format [None]: json
```
* Test your settings
`aws iam list-users`
```
{
    "Users": [
        {
            "Path": "/",
            "UserName": "nhlanhla",
            "UserId": "AIDAZQ3D******",
            "Arn": "arn:aws:iam::65465****:user/nhlanhla",
            "CreateDate": "2024-03-05T21:19:36+00:00"
        }
    ]
}
```

## Create AWS S3 Bucket
* [Reference video](https://www.youtube.com/watch?v=SHN48wTEQ5I)

## Build react project
* `npm run build` this will create a build folder with artifacts to deploy
* Test your build `serve -s build`, this will need you to have installed `serve` globally in your workstation. To install it run `npm install -g serve`

## Deploy react project to AWS using CLI
* Note that you can also deploy this by drag and dropping the files.
* For this POC we focusing on using CLI `aws s3 sync <build folder> s3://<bucket name>` -> `aws s3 sync .\build\* s3://react-website-test-nhlanhla-01`

## AWS CI/CD Code Pipeline
* [Reference Video](https://www.youtube.com/watch?v=D2p2nwKvqHs)
* Search for `code pipeline` in the AWS console search box
* `buildspec.yml` command yml file needed


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
