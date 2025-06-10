# Multi-Agent Chatbot System 🤖

A powerful AI chatbot system that allows you to chat with multiple specialized AI assistants, each with unique personalities and expertise. Built with Streamlit and powered by OpenAI's GPT models.

<img width="312" alt="image" src="https://github.com/user-attachments/assets/511d9972-0da2-4966-bd19-852cdb837d98" />


## ✨ What This App Does

- **Multiple AI Assistants**: Chat with different AI agents, each specialized for different tasks
- **Smart Agent Switching**: Automatically suggests the best agent for your questions
- **Persistent Conversations**: All your chats are saved and can be resumed later
- **User Management**: Secure login system with admin controls
- **Easy Administration**: Manage users, agents, and system settings through a web interface

<img width="314" alt="image" src="https://github.com/user-attachments/assets/f28b9430-4467-41fa-b457-b0b9fd999775" />


## 🚀 Quick Start Guide

### Step 1: Prerequisites

Before you begin, make sure you have:
- **Python 3.8 or higher** installed on your computer
- **A code editor** (like VS Code, PyCharm, or even Notepad++)
- **Internet connection** for downloading packages and API access

#### Check Your Python Version
Open your terminal/command prompt and run:
```bash
python --version
```
If you see something like "Python 3.8.x" or higher, you're good to go!

### Step 2: Download the Project

1. Download all the project files to a folder on your computer
2. Open your terminal/command prompt and navigate to that folder:
```bash
cd path/to/your/project/folder
```

### Step 3: Install Required Packages

Install all necessary Python packages by running:
```bash
pip install -r requirements.txt
```

### Step 4: Set Up Your Database (Neon.tech)

This app uses a PostgreSQL database hosted on Neon.tech (free tier available).

#### 4.1 Create a Neon Account
1. Go to [neon.tech](https://neon.tech)
2. Sign up for a free account
3. Create a new project

<img width="1494" alt="image" src="https://github.com/user-attachments/assets/4e3c48b0-319e-474d-9426-3c752113837a" />


#### 4.2 Get Your Database Credentials
In your Neon dashboard, you'll find connection details like:
- **Host**: `ep-xxx-xxx.us-east-1.aws.neon.tech`
- **Database**: `neondb`
- **Username**: `your-username`
- **Password**: `your-password`

<img width="839" alt="image" src="https://github.com/user-attachments/assets/4e6f6e96-693f-42c2-8964-2be1f7528fb4" />


### Step 5: Configure Environment Variables

Create a file named `.env` in your project folder and add your credentials:

```env
# Database Configuration (from Neon.tech)
NEON_DB_USER=your-username-here
NEON_DB_PASSWORD=your-password-here
NEON_DB_HOST=your-host-here
NEON_DB_NAME=neondb

# OpenAI API Key (get from OpenAI website)
OPENAI_API_KEY=your-openai-key-here
```

#### Get Your OpenAI API Key
1. Go to [platform.openai.com](https://platform.openai.com)
2. Sign up/login to your account
3. Navigate to API Keys section
4. Create a new API key
5. Copy it to your `.env` file

<img width="795" alt="image" src="https://github.com/user-attachments/assets/aea96a38-6933-4dd1-853b-37f94916575a" />


### Step 6: Initialize the Database

Run this command to set up your database tables:
```bash
python models.py
```

If you see "Database setup completed successfully", you're ready to go!

### Step 7: Run the Application

Start the application with:
```bash
streamlit run app.py
```

Your browser should automatically open to `http://localhost:8501`

## 🎯 Using the Application

### First Time Setup

When you first open the app, you'll see a login screen:

<img width="1488" alt="image" src="https://github.com/user-attachments/assets/9fe05c11-c08a-47e3-b19d-2da39f4edf31" />


1. **Click the "Register" tab**
2. **Create your account** - the first user automatically becomes an admin
3. **Login with your new credentials**

### Main Interface Overview

Once logged in, you'll see the main chat interface:

<img width="1160" alt="image" src="https://github.com/user-attachments/assets/f6cdf41e-1517-4edb-93b9-3a9a69c70d7b" />


#### Sidebar Features:
- **Agent Selection**: Choose which AI assistant to chat with
- **Agent Info**: See what each agent specializes in
- **Conversation History**: Access your previous chats
- **New Conversation**: Start fresh conversations
- **Settings**: Configure API keys and preferences

#### Chat Area:
- **Message History**: See your conversation with the current agent
- **Agent Indicators**: Know which agent is responding
- **Input Box**: Type your messages here

### Chatting with Agents

1. **Select an agent** from the sidebar dropdown
2. **Type your message** in the input box at the bottom
3. **Press Enter** to send
4. **Wait for the response** - you'll see a thinking indicator

<img width="1079" alt="image" src="https://github.com/user-attachments/assets/d4b157a7-b861-41bd-846f-f5e1cdc2ff23" />


### Switching Agents

You can switch between agents at any time:
- Use the dropdown in the sidebar
- The system may suggest better agents for specific questions
- Each agent maintains its own conversation context

<img width="710" alt="image" src="https://github.com/user-attachments/assets/de300b50-8202-4629-a628-7a070f012713" />


### Managing Conversations

- **Start New**: Click "✨ New Conversation" to begin fresh
- **Continue Previous**: Click on any conversation in the history
- **Multi-Agent Indicator**: See 🔄 for conversations involving multiple agents


## 🔧 Admin Features

If you're an admin user, you'll see an "Admin" option in the sidebar navigation.

<img width="584" alt="image" src="https://github.com/user-attachments/assets/5b383ca4-0514-4a68-9ea3-560b412fb46d" />


### Managing Agents

In the "Manage Agents" tab:
- **View all agents** in an editable table
- **Edit descriptions** and system prompts
- **Add new agents** with custom personalities
- **Delete agents** you no longer need

<img width="1078" alt="image" src="https://github.com/user-attachments/assets/2a3a1f22-0d5b-46e5-8b30-44f7f793420f" />


### Managing Users

In the "Manage Users" tab:
- **View all users** and their roles
- **Change user roles** (admin/user)
- **Reset passwords** for users
- **Import/export users** via CSV

<img width="624" alt="image" src="https://github.com/user-attachments/assets/4f6aeaf5-ff27-44cf-97a7-94d204b955a0" />


### System Configuration

Configure system-wide settings:
- **Update OpenAI API key**
- **View database information**
- **Export chat history**

<img width="1040" alt="image" src="https://github.com/user-attachments/assets/ea2be1c7-ab3f-497a-8a17-f0763fe6d854" />


## 🛠️ Troubleshooting

### Common Issues and Solutions

#### "No OpenAI API key configured"
**Problem**: The app can't access OpenAI's services
**Solution**: 
1. Check your `.env` file has the correct `OPENAI_API_KEY`
2. Or configure it through the app: Sidebar → "🔑 OpenAI API Key"

#### "Database connection error"
**Problem**: Can't connect to your Neon database
**Solution**:
1. Verify your `.env` file has correct database credentials
2. Check your Neon.tech dashboard for the correct connection details
3. Ensure your database is not paused (Neon pauses inactive databases)

#### "Agents not loading"
**Problem**: No agents appear in the dropdown
**Solution**:
1. Run `python models.py` to reinitialize the database
2. Check the admin panel to add agents manually
3. Verify database connectivity

#### App won't start
**Problem**: `streamlit run app.py` fails
**Solution**:
1. Make sure all packages are installed: `pip install -r requirements.txt`
2. Check you're in the correct project directory
3. Verify Python version is 3.8+

### Enable Debug Mode

As an admin, you can enable debug mode for detailed error information:
1. Login as admin
2. In the sidebar, toggle "🐛 Debug Mode"
3. Look for additional error details in expandable sections


## 📝 Updating and Customizing the App

### Adding New Agents

1. **Login as admin**
2. **Go to Admin → Manage Agents**
3. **Scroll to "Add New Agent"**
4. **Fill in the form**:
   - **Name**: What to call your agent
   - **Description**: What it specializes in
   - **System Prompt**: Instructions for how it should behave

#### Example Agent Configurations:

**Creative Writer**
- Name: `Creative Writer`
- Description: `Helps with creative writing, storytelling, and content creation`
- System Prompt: `You are a creative writing assistant. Help users with stories, poems, creative content, and writing techniques. Be inspiring and imaginative.`

**Data Analyst**
- Name: `Data Analyst`
- Description: `Assists with data analysis, statistics, and business insights`
- System Prompt: `You are a data analysis expert. Help users understand data, create insights, and make data-driven decisions. Be analytical and precise.`

### Modifying Existing Agents

1. **Admin → Manage Agents**
2. **Edit the table directly** - just click in any cell
3. **Click "Save Changes"** when done

### Importing Users from CSV

If you need to add many users at once:
1. **Create a CSV file** with columns: `username`, `password`, `role`
2. **Admin → Manage Users → Import Users**
3. **Upload your CSV file**


### Updating the Code

If you want to modify the app's functionality:

#### Key Files to Know:
- `app.py` - Main application and user interface
- `agent.py` - How agents communicate with OpenAI
- `models.py` - Database structure
- `admin.py` - Admin panel functionality

#### Making Changes:
1. **Stop the running app** (Ctrl+C in terminal)
2. **Edit the files** in your code editor
3. **Save your changes**
4. **Restart with** `streamlit run app.py`


#### Database Changes:
If you modify `models.py`, run the update script:
```bash
python update_schema.py
```

## 📁 Project Structure

Understanding the project layout:

```
project-folder/
├── app.py              # Main application file
├── models.py           # Database models and setup
├── db_manager.py       # Database operations
├── agent.py            # AI agent communication
├── auth.py             # User authentication
├── admin.py            # Admin interface
├── chat.py             # Chat display functions
├── rag_system.py       # Agent recommendation system
├── csv_helper.py       # Import/export functions
├── requirements.txt    # Required Python packages
├── .env               # Your configuration (create this)
├── readme.md          # This guide
└── screenshots/       # Screenshots for this guide
```

## 🆘 Getting Help

### If You're Stuck:

1. **Check the debug mode** (admin users only)
2. **Look at the terminal** where you ran `streamlit run app.py` for error messages
3. **Verify your `.env` file** has correct credentials
4. **Try restarting the app** - sometimes fixes temporary issues

### Error Messages to Look For:

- **"No module named 'streamlit'"** → Run `pip install -r requirements.txt`
- **"Authentication error"** → Check your OpenAI API key
- **"Database connection failed"** → Verify Neon.tech credentials
- **"Port 8501 is already in use"** → Close other Streamlit apps or use `streamlit run app.py --server.port 8502`

## 🚀 Going Live (Optional)

To share your app with others, you can deploy it using Streamlit Community Cloud:

1. **Push your code to GitHub** (without the `.env` file!)
2. **Go to [share.streamlit.io](https://share.streamlit.io)**
3. **Connect your GitHub repository**
4. **Add your environment variables** in the deployment settings
5. **Deploy!**

---

## 🎉 You're All Set!

You now have a fully functional multi-agent chatbot system! Experiment with different agents, invite team members, and customize it to fit your needs.

**Remember**: 
- Keep your `.env` file secure and never share it
- Monitor your OpenAI API usage to avoid unexpected charges
- Regularly backup your chat history if it's important

Happy chatting! 🤖✨
