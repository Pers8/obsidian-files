
To set up your Discord bot and database to run 24/7 on Pebblehost, you'll need to follow several steps to ensure everything is configured correctly. Here’s a step-by-step guide to help you get started:

### 1. Setting Up Your Pebblehost Account

1. **Create an Account:** If you haven't already, sign up for an account on [Pebblehost](https://pebblehost.com/).
2. **Choose a Plan:** Select a plan that suits your needs under the "Game VPS" section, which offers more flexibility for running a Discord bot and a database.
3. **Purchase and Set Up the Server:** Once you've chosen your plan, follow the instructions to set up your server. You will receive credentials and server access information.

### 2. Preparing Your Bot and Database

1. **Upload Your Bot Code:**
    - Connect to your server via SSH (using a tool like PuTTY or Terminal).
    - Upload your bot files to the server. You can use SFTP (with a client like FileZilla) to transfer files from your local machine to the server.
2. **Install Node.js:**
    
    - Install Node.js on your server. You can download it from [Node.js official website](https://nodejs.org/) or use a package manager like `apt` for Linux.
    
    `curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash - sudo apt-get install -y nodejs`
    
3. **Set Up Dependencies:**
    - Navigate to your bot's directory and run `npm install` to install all required npm packages.
4. **Install and Configure SQLite:**
    - Ensure SQLite is installed on your server. If not, you can install it using your package manager.
    - Make sure your database file (`mydatabase.db`) is correctly set up in your project folder.

### 3. Running the Bot

1. **Start Your Bot:**
    - You can start your bot by running `node yourBotFile.js` (replace `yourBotFile.js` with the entry point of your bot).
2. **Use PM2 for Process Management:**
    - Install PM2 via npm to keep your bot running continuously:
        
        `npm install pm2 -g pm2 start yourBotFile.js pm2 save pm2 startup`
        
    - This will ensure your bot automatically restarts if it crashes or the server reboots.

### 4. Setting Up Webhooks or API for Order Handling

- Ensure your website can communicate with your Discord bot. This might involve setting up webhooks or an API endpoint on your server that listens for requests from your website and interacts with the Discord bot accordingly.

### 5. Automatic Discord Server Link

- To open a Discord server link automatically when an order is created, ensure that the order creation process on your website triggers a bot notification that sends a message containing the Discord invite link to the appropriate channel or user.

### 6. Monitoring and Maintenance

- Regularly check your bot and server for any issues. Use logs to troubleshoot problems. Keep your system updated with the latest security patches.

### 7. Final Testing

- Before going live, thoroughly test the entire flow from order creation on the website to the handling by the Discord bot to ensure everything works seamlessly.

By following these steps, you should be able to set up your Discord bot and database on Pebblehost and ensure it runs smoothly 24/7. If you encounter any specific issues during setup, consulting Pebblehost's support or community forums can be beneficial.