# node-rest-express

This example demonstrates how to implement a **REST API** using [Express.JS](https://expressjs.com/de/) and Prisma.

## Get started

### 1. Install the Prisma CLI

You need to have the Prisma CLI installed on your machine to run this example. If you don't have it yet, execute the following command to install it globally on your machine:

```
npm install -g prisma
# or `yarn global add prisma`
```

### 2. Download example & Install dependencies

Clone the repository:

```
git clone git@github.com:prisma/prisma-examples.git
```

Install Node dependencies:

```
cd prisma-examples/node-rest-express
yarn install # or `npm install`
```

### 3. Deploy the Prisma API

You will now deploy the Prisma API that's backing this example. This requires you to have [Docker](https://www.docker.com) installed on your machine (if you don't have Docker follow the collapsed instructions below the code block):

Launch Prisma via Docker:

```
docker-compose up -d
```

Navigate into the `prisma` directory and deploy the Prisma API:

```
cd prisma
prisma deploy
```

<details>
 <summary><strong>I don't have Docker installed on my machine</strong></summary>

To deploy your service to a demo server (rather than locally with Docker), follow these steps:

- Run the following command:
  ```
  cd prisma
  prisma deploy --new
  ```
- In the interactive CLI wizard:
  - Select the **Demo server**
  - For all following questions, choose the suggested values by just hitting **Enter**

</details>

### 4. Start the server

```
yarn start
```

The server is now running on `http://localhost:3000`. You can send the API requests implemented in `index.js`, e.g. [`http://localhost:3000/houses`](http://localhost:3000/houses).
