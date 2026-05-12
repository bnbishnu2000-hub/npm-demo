# npm-demo

🧰 Prerequisites
Make sure you have:

✅ Check installations
node -v
npm -v
If not installed:

Install Node.js from https://nodejs.org (npm comes with it)
📁 Step 1: Create Project Folder
mkdir my-node-app
cd my-node-app
⚙️ Step 2: Initialize npm Project
npm init -y
👉 This creates:

package.json
🧠 What is package.json?
👉 It is like pom.xml in Maven

It contains:

Project info
Dependencies
Scripts (commands to run app)
📦 Step 3: Install Dependency
npm install express
👉 This will:

Download Express framework
Create:
node_modules/
package-lock.json
✍️ Step 4: Create Application
Create a file:

touch index.js
Add this code:

const express = require('express');
const app = express();

app.get('/', (req, res) => {
  res.send("Hello from Node + npm!");
});

app.listen(3000, () => {
  console.log("Server running on port 3000");
});
▶️ Step 5: Run the Application
node index.js
👉 Open browser:

http://localhost:3000
👉 Output:

Hello from Node + npm!
🧪 Step 6: Add Scripts (Important)
Open package.json and add:

"scripts": {
  "start": "node index.js"
}
Run using npm:
npm start
🔨 Step 7: Build the Application (Concept)
👉 In simple apps, no build step is required 👉 In real apps, we use:

npm run build
👉 This creates:

dist/
(only if build tool like webpack is configured)

📦 Step 8: What is Artifact in JS?
👉 In Java:

.jar
👉 In Node.js:

dist/ folder OR compiled JS bundle
📥 Step 9: Dependency Management
👉 Save dependencies:

npm install express
👉 Install from package.json:

npm install
🔁 Step 10: npm Lifecycle (Simple)
install → start → build → test
🎯 What You Learned
What is npm
What is package.json
How to install dependencies
How to run app
What is artifact in JS
🚀 Summary
👉 npm installs dependencies and helps run/build your JavaScript application






how to add docker file 

FROM node:20
WORKDIR /my-app
COPY package*.json ./
RUN npm install
COPY . .  
EXPOSE 3000
CMD ["node", "index.js"]



