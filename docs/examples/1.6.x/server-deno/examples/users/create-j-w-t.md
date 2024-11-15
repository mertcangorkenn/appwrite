import { Client, Users } from "https://deno.land/x/appwrite/mod.ts";

const client = new Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('<YOUR_PROJECT_ID>') // Your project ID
    .setKey('<YOUR_API_KEY>'); // Your secret API key

const users = new Users(client);

const response = await users.createJWT(
    '<USER_ID>', // userId
    '<SESSION_ID>', // sessionId (optional)
    0 // duration (optional)
);