# Udagram Image Filtering Microservice

Udagram is a simple cloud application developed alongside the Udacity Cloud Engineering Nanodegree. It allows users to register and log into a web client, post photos to the feed, and process photos using an image filtering microservice.

The project is split into three parts:
1. [The Simple Frontend](https://github.com/udacity/cloud-developer/tree/master/course-02/exercises/udacity-c2-frontend)
A basic Ionic client web application which consumes the RestAPI Backend. [Covered in the course]
2. [The RestAPI Backend](https://github.com/udacity/cloud-developer/tree/master/course-02/exercises/udacity-c2-restapi), a Node-Express server which can be deployed to a cloud service. [Covered in the course]
3. [The Image Filtering Microservice](https://github.com/udacity/cloud-developer/tree/master/course-02/project/image-filter-starter-code), the final project for the course. It is a Node-Express application which runs a simple script to process images. [Your assignment]

## Tasks

### Setup Node Environment

You'll need to create a new node server. Open a new terminal within the project directory and run:

1. Initialize a new project: `npm i`
2. run the development server with `npm run dev`

### Create a new endpoint in the server.ts file

The starter code has a task for you to complete an endpoint in `./src/server.ts` which uses query parameter to download an image from a public URL, filter the image, and return the result.

We've included a few helper functions to handle some of these concepts and we're importing it for you at the top of the `./src/server.ts`  file.

```typescript
import {filterImageFromURL, deleteLocalFiles} from './util/util';
```

### Deploying your system

Follow the process described in the course to `eb init` a new application and `eb create` a new environment to deploy your image-filter service! Don't forget you can use `eb deploy` to push changes.

### Endpoint url for running beanstalk
[http://udagramjaindev-dev2.ap-south-1.elasticbeanstalk.com](http://udagramjaindev-dev2.ap-south-1.elasticbeanstalk.com)

#### example url

[http://udagramjaindev-dev2.ap-south-1.elasticbeanstalk.com/filteredimage?image_url=https://www.jacksonandperkins.com/images/xxl/v1780.jpg](http://udagramjaindev-dev2.ap-south-1.elasticbeanstalk.com/filteredimage?image_url=https://www.jacksonandperkins.com/images/xxl/v1780.jpg)

### Health Check Screenshot for eb deployement

<img width="1342" alt="Screenshot 2020-04-01 at 1 16 16 PM" src="https://user-images.githubusercontent.com/25522394/78114782-6b3a1c00-741f-11ea-95de-24ef96bfafe4.png">

<img width="1672" alt="Screenshot 2020-04-01 at 1 16 09 PM" src="https://user-images.githubusercontent.com/25522394/78114793-6ffed000-741f-11ea-8d9e-edbfcca2368e.png">

