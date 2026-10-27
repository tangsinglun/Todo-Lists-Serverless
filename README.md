# AWS Serverless Project - Todo Lists App

## Table of Contents

- [OverView](#OverView)
- [Setup Environment](#Setting-Environment)
- [Deploy Back-End Production](#Deploy-BackEnd-Production)
- [Installation Front-End](#Installation-FrontEnd)
- [Run the App](#Run-App)
- [Config Auth0](#Config-Auth0)
- [Project Reference Sources Or Links](#references)

## OverView

In this project, we will apply the skills we have acquired in this cloud engineering course to design, deploy and operate a AWS Serverless todo lists application. The App consist of two parts, a backend which is written in Nodejs and enitirely a `Labmda` serverless architecture. We will use the `Serverless` framework to deploy our Lambda fucntions. And the other part is the front-end which is written in React TypeScript. The main use of this App is to allow users to add and delete item to the todo lists.


For this project we will uses Oracle Vitualbox Virtual Machine for simulating the Linux development Environment. If you personally has a Linux Environment you can skip to part.

## Setting-Environment

- VirtaulBox Machine For Download

  - To install please follow the this link: https://www.virtualbox.org/wiki/Downloads.

- Ubuntu OS Dowload

  - Download the Ubuntu from the Ubuntu website: https://ubuntu.com/download, we will download the Ubuntu 18.0.4 desktop version.

- Add Ubuntu OS to the Virtual Machine.

  1. From the VirtualBox click the `New` Button.
  2. For the name type in `todo-lists`. For the type field select `Linux` and `Ubuntu 64-bit` for the Version.
  3. Leave Everthing as default. (You can adjust the Storage Space according to your needs).
  4. Then Click the `Setting` Button.
  5. Go to the `Storage` Section => For the `Controller IDE`, Select the Ubuntu OS Image you download.
  6. Click the `Start` button to begin install the Ubuntu OS. Follow the setup instructions and install.

- Install Nodejs.
  when you sucessfully install Nodejs, `npm (Node Package Manager)` will be installed as well.

  - To install Nodjs, please follow this link: https://nodejs.org/en/download/

- Install git

  - sudo apt install git-all

- Install Serverless FrameWork

  - npm install -g serverless
  - Config Serverless FrameWork. Type in the following command
    - `serverless config credentials --provider aws --key AKIAIOSFODNN7EXAMPLE --secret wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY`
      Please substitute the --key and --secret with you own values.

- Clone the Project
  - Type in the following command to clone the Project.
    `git clone https://github.com/tangsinglun/Todo-Lists-Serverless.git`

And that is it! We have setup an environment for the Todo Lists App. Next we will config the project and deploy it to the AWS.


## Deploy-BackEnd-Production

`Please Note you need to Config the settings for Production!`, please follow the above procedures.

- Install All the Dependencies
  - Browser to the location `Todo-Lists-Serverless/backend`
  - Type in the following command `npm install`. Wait till the installation completes
- Deploy the App to the AWS.
  - Browser to the location `Todo-Lists-Serverless/backend`
  - Type in the following command `sls deploy --stage prod -v`. Wait till the deployment completes.

## Installation-FrontEnd

- Install All the Dependencies
  - Browser to the location `Todo-Lists-Serverless/client`
  - Type in the following command `npm install`. Wait till the installation completes

## Run-App

- For Production

  As the Backend is deploy to AWS. In-order to run the app. All we need is start-up the Front-End.

  - Browser to the location `Todo-Lists-Serverless/client`
  - type in the following command `npm run start`
  - In the Browser type in the URL `http://localhost:3000/prod/login`.


## Config-Auth0

* We are using Auth0 for our login services. To config Auth0 please goto the website `https://auth0.com/`. 
    1. You just need to fill in the "domain" and "clientId". (change in the program client/src/config.ts accordingly)
    2. For the certificate, you can find it in the advance section which is at the bottom of the menu, if everything remains the same the certificate item should be on the last tab. (change in the program "\backend\src\lambda\auth\rs256Auth0Authorizer.ts"
    and "\backend\src\lambda\utils.ts" accordingly)

## References

- Code References
  - [Udacity](https://www.udacity.com/)
  - [GitHub](https://github.com/)
  - [Serverless](https://serverless.com/)
  - [Binary responses with Serverless Framework and API Gateway](https://medium.com/nextfaze/binary-responses-with-serverless-framework-and-api-gateway-5fde91376b76)
  - [Serverless S3 Local](https://www.npmjs.com/package/serverless-s3-local)
  - [Serverless Apigw Binary](https://serverless.com/plugins/serverless-apigw-binary/)
  - [Express](https://expressjs.com/)
  - [Auth0](https://auth0.com/)
  - [JSON Web Tokens](https://jwt.io/)
