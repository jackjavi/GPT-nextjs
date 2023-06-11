# [twitterbio.io](https://www.twitterbio.io/)

This project generates Twitter bios for you using AI.

[![Twitter Bio Generator](./public/screenshot.png)](https://www.twitterbio.io)

## How it works

This project uses the [ChatGPT API](https://openai.com/api/) and [Vercel Edge functions](https://vercel.com/features/edge-functions) with streaming. It constructs a prompt based on the form and user input, sends it to the ChatGPT API via a Vercel Edge function, then streams the response back to the application.

If you'd like to see how I built this, check out the [video](https://youtu.be/JcE-1xzQTE0) or [blog post](https://vercel.com/blog/gpt-3-app-next-js-vercel-edge-functions).

## Running Locally

After cloning the repo, go to [OpenAI](https://beta.openai.com/account/api-keys) to make an account and put your API key in a file called `.env`.

Then, run the application in the command line, and it will be available at `http://localhost:3000`.

```bash
npm run dev
```

## One-Click Deploy

Deploy the example using [Vercel](https://vercel.com?utm_source=github&utm_medium=readme&utm_campaign=vercel-examples):

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/Nutlope/twitterbio&env=OPENAI_API_KEY&project-name=twitter-bio-generator&repo-name=twitterbio)

Notes
Task 3: Develop smartsheet.ts CRUD template
To interact with an external API (Smartsheets), I can create a file called smartsheet.ts to handle basic CRUD operations. Here's a pseudocode template for the CRUD operations:

// Function to create a new record in Smartsheet
function createRecord(recordData: any): Promise<any> {
// Implement the logic to create a record using the Smartsheet API
}

// Function to read a record from Smartsheet by ID
function getRecordById(recordId: string): Promise<any> {
// Implement the logic to get a record by ID using the Smartsheet API
}

// Function to update a record in Smartsheet by ID
function updateRecord(recordId: string, updatedData: any): Promise<any> {
// Implement the logic to update a record by ID using the Smartsheet API
}

// Function to delete a record from Smartsheet by ID
function deleteRecord(recordId: string): Promise<any> {
// Implement the logic to delete a record by ID using the Smartsheet API
}
Task 4: Define example user schema for Precision services
Define an example user schema in your codebase to represent the structure of user data for Precision services. For example:

interface User {
id: string;
name: string;
email: string;
}
Task 5: User Functions
In a file called userFunctions.ts, I can define functions to interact with user data in Smartsheet. Here are some example functions:

import { createRecord, getRecordById, updateRecord, deleteRecord } from './smartsheet';

// Function to get a user from Smartsheet by ID
export function getUser(userId: string): Promise<User> {
return getRecordById(userId);
}

// Function to get all users from Smartsheet
export function getAllUsers(): Promise<User[]> {
// Implement the logic to retrieve all users using the Smartsheet API
}

// Function to update a specific property of user with ID 34 in Smartsheet
export function updateUserProperty(userId: string, property: string, value: any): Promise<any> {
// Implement the logic to update a specific property of a user with ID 34 using the Smartsheet API
}

// Function to update a group of users in Smartsheet
export function updateGroupOfUsers(userIds: string[], updatedData: any): Promise<any> {
// Implement the logic to update a group of users using the Smartsheet API
}

// Function to update all users in Smartsheet
export function updateAllUsers(updatedData: any): Promise<any> {
// Implement the logic to update all users using the Smartsheet API
}
