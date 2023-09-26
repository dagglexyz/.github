<p align="center">
  <a href="https://beta.daggle.xyz">
    <img src="https://i.ibb.co/4JLkjfQ/Group-5.png" alt="Daggle logo" />
  </a>
  </p>

<h1 align="center">Daggle 🦈<br>Compute Over Data Platform</h1>

Our platform lets users offload their extensive CPU workloads to Bacalhau, an off-chain compute network closely packed to IPFS storage, making file retrieval faster. Users can use several features our platform offers, like training Tensorflow models, uploading data from web2 to web3 storage using Spheron, running Python or Node.js scripts and many more in just a matter of clicks.

Easy-to-use marketplace allows users to upload their Actions in the future and even monetise them if needed. Actions are CLI commands that can be fed into Bacalhau.

They can manage their bacalhau jobs, check the status or results, redeploy jobs, and many more.

## How it's Made

Contains several modules, which includes server, client, car-archiver, Lilypad and BacalhauJS.

The server is written using Node.js which interacts with several SDKs and libraries to power the platform.

1. **BacalhauJS** Node.js wrapper for the Bacalhau API module to interact with server. [\[know more\]](https://github.com/dagglexyz/bacalhau-js)
2. **car-archiver** A web3 CDN, https://saturn.tech/ to retrieve and download results faster. [\[know more\]](https://github.com/dagglexyz/car)
3.  **Bacalhau:** Node interacts with Bacalhau using [BacalhauJS](https://github.com/dagglexyz/bacalhau-js). A simple REST API wrapper around the network.
4. **Lilypad** Lilypad to create anonymous jobs in the platform, it free as of writing this, but might be monetized in the future! [\[know more\]](https://docs.lilypadnetwork.org/)
5.  **Spheron Storage SDK:** Used to convert mass web2 data into web3.
6.  **Spheron Compute:** Node.js application is containerized and hosted on Spheron Compute.
7.  **Polybase:** A decentralized database powered by zero-knowledge proofs, users, jobs, authentication and other records are stored in Polybase.
8.  **Push Notification:** Bacalhau job status is communicated to clients via Push Notification.

The client is built using React.js, Material components and other client-based SDKs. Hosted on Spheron.

1.  **FVM:** Payments and Credit system is maintained on Smart contracts hosted on FVM, and interacted via web3.js.
2.  **Spheron Hosting:** The client is hosted on the Spheron cloud, an infrastructure to build a faster, more personalized web.
3.  **Push Notification Embed:** Notifications related to bacalhau jobs are displayed with the help of Push Notification Embed.
4.  **ENS:** Names and avatars are resolved using ENS, which uses an ethers provider in the background.


## **Follow the below steps to run it locally.**
### Server⚙️

1. Clone Repo.
> $ git clone https://github.com/leostelon/dagglexyz/server server
>  $ cd server
2. Add the .env file in the root directory. Add the below variables and replace them with your tokens, respectively.

		  SPHERON_TOKEN= < spheron-webapp-token > [Know More](https://docs.spheron.network/rest-api/#creating-an-access-token)
		  MONGODB_URL=mongodb://127.0.0.1:27017/daggle
		  ALLOWED_DOMAINS="http://localhost:3002"
		  JWT_SECRET= < your-secret >
	  

3. Run server!
> $ npm run start

### Client💻

1. Clone Repo.
> $ git clone https://github.com/dagglexyz/client client
>  $ cd client
2. Add the .env file in the root directory. Replace the value accordingly.

		  REACT_APP_SERVER_URL=http://localhost:3000
		  REACT_APP_QUICK_NODE= < quick-node-key >
		  REACT_APP_CHAIN=FVM_MAINNET
	  
4. Run the client!
> $ npm run start

Note: It may prompt to run on a different port, hit enter.

## Demos

> Make sure your browser supports video encoding or click the link for
> respective sections to watch the video.

<div align="center">
  <h2>Demo Lilypad🍃</h2>
  <p>See how it work!</p>
<video width="320" height="240" controls>
  <source src="https://github.com/dagglexyz/.github/assets/53221136/f6693936-e68b-4754-83c2-2a5398d8a4ff" type="video/mp4">
</video>
<div>

[check out the full video here.](https://github.com/dagglexyz/.github/assets/53221136/f6693936-e68b-4754-83c2-2a5398d8a4ff)

<div align="center">
  <h2>Demo BacalhauJS🐟</h2>
  <p>See how it work!</p>
<video width="320" height="240" controls>
  <source src="https://github.com/dagglexyz/.github/assets/53221136/f6693936-e68b-4754-83c2-2a5398d8a4ff" type="video/mp4">
</video>
<div>

[check out the full video here.](https://github.com/dagglexyz/.github/assets/53221136/f6693936-e68b-4754-83c2-2a5398d8a4ff)
