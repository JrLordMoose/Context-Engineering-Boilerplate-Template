# Project Setup & File Organization Guide

## 🎯 Quick Answer: Where Do Generated Files Go?

**Simple Rule**: Create a **NEW folder** for each project you build. Put ALL generated files (Step 0 config + Step 3 code) in that folder.

```
your-workspace/
├── Context-Engineering-Boilerplate-Template/    # This template (keep it separate!)
├── my-task-manager/                             # Your first project
├── my-ecommerce-store/                          # Your second project  
└── my-analytics-dashboard/                      # Your third project
```

**Never mix**: Template files and your project files should stay completely separate.

---

## Complete Setup Process (5 Minutes)

### Before You Start Any Project

**Step 1: Choose Your Workspace Location**
Pick where you want to create projects. Common choices:
- `C:\Users\YourName\Projects\` (Windows)
- `/Users/YourName/Projects/` (Mac)
- `/home/YourName/projects/` (Linux)
- `~/workspace/` (Any system)

**Step 2: Keep Template Separate**
The Context Engineering Template should stay in its own folder:
- **✅ Good**: `~/workspace/Context-Engineering-Boilerplate-Template/` (template)
- **✅ Good**: `~/workspace/my-awesome-app/` (your project)
- **❌ Bad**: Mixing template files with your project files

---

## For Each New Project You Build

### Step-by-Step File Management

#### Before Step 0: Create Project Folder

**1. Decide on project name** (use simple, lowercase names):
- `my-task-manager`
- `team-chat-app`  
- `expense-tracker`
- `ecommerce-store`

**2. Create the folder**:

**Windows (File Explorer)**:
- Right-click in your workspace folder → New → Folder
- Name it your project name (e.g., `my-task-manager`)

**Mac/Linux (Terminal)**:
```bash
cd ~/workspace
mkdir my-task-manager
cd my-task-manager
```

**Any System (VS Code)**:
- File → Open Folder → Navigate to workspace
- Right-click → New Folder → Name it your project name

#### During Step 0: Save Configuration Files

**Step 0 generates these files**:
- `CLAUDE.md` (AI configuration for your project)
- `context-sources.md` (technology-specific information sources)
- `.claude/subagents/` folder (specialized AI helpers)

**Where to save them**: In your project folder (`my-task-manager/`)

**How to save**:
1. **Copy the generated CLAUDE.md content** from AI chat
2. **Create file**: `my-task-manager/CLAUDE.md`
3. **Paste the content** into the file
4. **Repeat for all generated files**

**Final structure after Step 0**:
```
my-task-manager/
├── CLAUDE.md              # Your project's AI configuration
├── context-sources.md     # Technology information sources
└── .claude/               # AI helper configurations
    └── subagents/
        ├── code-generator.md
        ├── project-planner.md
        └── tech-advisor.md
```

#### During Steps 1-2: Save Planning Documents

**Step 1 generates**: Project requirements and user stories
**Step 2 generates**: Technical architecture and file structure plan

**Where to save**: Keep in chat history OR create planning files:
- `my-task-manager/planning/requirements.md` (Step 1 output)
- `my-task-manager/planning/architecture.md` (Step 2 output)

**Optional but helpful**:
```
my-task-manager/
├── CLAUDE.md
├── planning/              # Optional: save planning documents
│   ├── requirements.md    # Step 1 output
│   └── architecture.md    # Step 2 output
└── .claude/
```

#### During Step 3: Save All Application Code

**Step 3 generates**: Complete application (20-50 files typically)

**Example application structure** (AI will tell you exactly what to create):
```
my-task-manager/
├── CLAUDE.md              # From Step 0
├── package.json           # From Step 3
├── README.md              # From Step 3
├── src/                   # From Step 3
│   ├── components/
│   ├── pages/
│   ├── utils/
│   └── App.js
├── tests/                 # From Step 3
├── public/                # From Step 3
└── .claude/               # From Step 0
```

**How to create files**:
1. **AI provides structured output** like this:
   ```
   File: src/components/TaskList.js
   ```javascript
   [code content here]
   ```
   
   File: src/App.js
   ```javascript
   [code content here]
   ```
   ```

2. **Create each file** in your project folder following the exact structure
3. **Copy the code** from AI output into each file

---

## Development Environment Integration

### VS Code / Cursor Setup

**1. Open your project folder**:
- File → Open Folder → Select `my-task-manager`
- All your files (Step 0 config + Step 3 code) are in one place

**2. Use the generated CLAUDE.md**:
- If using Claude Code extension, it automatically uses your project's CLAUDE.md
- Enhanced AI collaboration with your project-specific configuration

### Replit Setup

**1. Create new Repl**:
- Choose your technology stack (React, Node.js, Python, etc.)
- Name it your project name

**2. Upload generated files**:
- Drag and drop files from your local project folder
- Or manually create files and copy/paste code content

### GitHub Integration

**1. Initialize Git in your project folder**:
```bash
cd my-task-manager
git init
git add .
git commit -m "Initial project setup with Context Engineering"
```

**2. Create GitHub repository**:
- Name it the same as your project folder
- Push your complete project (config + code)

### Claude Code Integration

**1. Navigate to your project**:
```bash
cd ~/workspace/my-task-manager
```

**2. Use project-specific configuration**:
- Claude Code automatically uses your project's CLAUDE.md
- Enhanced AI collaboration with specialized agents

---

## Multiple Projects Management

### Workspace Organization

**Recommended structure**:
```
your-workspace/
├── Context-Engineering-Boilerplate-Template/    # Template (never modify)
├── personal-projects/                           # Your personal apps
│   ├── task-manager/
│   ├── expense-tracker/
│   └── recipe-organizer/
├── work-projects/                               # Work-related apps
│   ├── team-dashboard/
│   ├── inventory-system/
│   └── customer-portal/
├── learning-projects/                           # Practice/learning apps
│   ├── todo-app/
│   ├── weather-app/
│   └── chat-app/
└── experimental/                                # Testing new ideas
    ├── ai-experiment/
    └── complex-system-test/
```

### Project Naming Conventions

**Good Names** (clear, descriptive, lowercase with hyphens):
- `task-manager`
- `ecommerce-store`
- `team-chat-app`
- `expense-tracker`
- `inventory-system`

**Avoid** (confusing, generic, spaces):
- `New Folder`
- `app`
- `project1`
- `My App With Spaces`

### Reusing Template for Multiple Projects

**Each project gets**:
- Its own folder
- Its own Step 0 configuration (custom CLAUDE.md)
- Its own generated code (Step 3 output)

**Template folder**:
- Keep the original template unchanged
- Copy prompts from template for each new project
- Reference documentation from template

---

## Step-by-Step Visual Guide

### Creating Your First Project

**1. Starting Point** - You have the template:
```
📁 your-workspace/
└── 📁 Context-Engineering-Boilerplate-Template/
    ├── 📄 CLAUDE.md (template)
    ├── 📁 prompts/
    └── 📁 docs/
```

**2. Create Project Folder**:
```
📁 your-workspace/
├── 📁 Context-Engineering-Boilerplate-Template/  # Template
└── 📁 my-task-manager/                          # Your project (NEW!)
```

**3. After Step 0** - Configuration generated:
```
📁 my-task-manager/
├── 📄 CLAUDE.md              # Custom config for your project
├── 📄 context-sources.md     # Technology info sources
└── 📁 .claude/              # AI helpers for your project
    └── 📁 subagents/
```

**4. After Step 3** - Complete application:
```
📁 my-task-manager/
├── 📄 CLAUDE.md              # Your AI config
├── 📄 package.json           # App dependencies
├── 📄 README.md              # App documentation
├── 📁 src/                   # App source code
│   ├── 📄 App.js
│   ├── 📁 components/
│   └── 📁 pages/
├── 📁 tests/                 # App tests
├── 📁 public/                # App assets
└── 📁 .claude/              # AI helpers
```

**5. Ready to develop**:
```bash
cd my-task-manager
npm install    # Install dependencies
npm start      # Run your app!
```

---

## Common Mistakes & Solutions

### ❌ Common Mistakes

**Mistake 1**: Putting project files in template folder
```
📁 Context-Engineering-Boilerplate-Template/
├── 📁 prompts/
├── 📄 my-app-files.js  # ❌ Wrong! Don't put project files here
└── 📄 CLAUDE.md        # ❌ This gets overwritten
```

**Mistake 2**: Not creating project folder before Step 0
- Running Step 0 without knowing where to put the generated files
- Getting confused about which CLAUDE.md to use

**Mistake 3**: Mixing multiple projects in one folder
```
📁 my-projects/
├── 📄 task-app.js      # ❌ Files from different projects mixed together
├── 📄 store-app.js     # ❌ Confusing and hard to manage
└── 📄 CLAUDE.md        # ❌ Which project does this configure?
```

### ✅ Correct Approach

**Step-by-step for each project**:
1. **Create project folder first**: `mkdir my-specific-project-name`
2. **Run Step 0**: Generate config files for this specific project
3. **Save Step 0 files**: In your project folder (not template folder)
4. **Run Steps 1-3**: Continue with same project context
5. **Save Step 3 code**: In same project folder with Step 0 config
6. **Develop and deploy**: Everything is organized and ready

---

## Development Environment Workflows

### VS Code Workflow
```bash
# 1. Create project
mkdir my-task-manager
cd my-task-manager

# 2. Generate and save Step 0 config
# [Copy Step 0 prompt to AI chat, save generated files here]

# 3. Generate and save Step 3 code  
# [Copy Steps 1-3 prompts to AI chat, save generated code here]

# 4. Open in VS Code
code .

# 5. Install and run
npm install
npm start
```

### Replit Workflow
```
# 1. Complete Steps 0-3 in AI chat
# 2. Create new Repl with your project name
# 3. Upload/create all generated files in Repl
# 4. Run in Replit environment
```

### Claude Code Workflow
```bash
# 1. Complete Steps 0-3 in ChatGPT/Claude Desktop
# 2. Create project directory
mkdir my-task-manager && cd my-task-manager

# 3. Use Claude Code to create files:
# "Create CLAUDE.md with the following content: [paste Step 0 output]"
# "Create src/App.js with the following content: [paste Step 3 code]"
# [Repeat for all files]

# 4. Install and run through Claude Code
```

---

## Project Templates & Naming Guide

### Project Naming Best Practices

**For Personal Projects**:
- `task-manager` (personal productivity)
- `expense-tracker` (personal finance)
- `recipe-organizer` (personal lifestyle)
- `workout-planner` (personal health)

**For Business Projects**:
- `customer-portal` (client-facing)
- `inventory-system` (internal operations)
- `team-dashboard` (team productivity)
- `sales-tracker` (business metrics)

**For Learning Projects**:
- `react-todo-app` (learning React)
- `python-data-analyzer` (learning Python)
- `nodejs-api-server` (learning backend)
- `flutter-mobile-app` (learning mobile)

**For Complex Projects**:
- `enterprise-crm-system`
- `microservices-ecommerce`
- `real-time-analytics-platform`
- `ai-document-processor`

### Project Folder Structure Templates

**Simple App Structure** (after Step 3):
```
my-simple-app/
├── CLAUDE.md              # AI config from Step 0
├── package.json           # Dependencies
├── README.md              # Setup instructions
├── index.html             # Main page
├── src/
│   ├── app.js            # Main application
│   ├── components/       # UI components
│   └── utils/            # Helper functions
├── tests/                # Test files
├── styles/               # CSS/styling
└── assets/               # Images, fonts, etc.
```

**Medium App Structure** (after Step 3):
```
my-medium-app/
├── CLAUDE.md              # AI config from Step 0
├── package.json           # Frontend dependencies
├── server/package.json    # Backend dependencies
├── README.md              # Complete setup guide
├── frontend/              # React/Vue frontend
│   ├── src/
│   ├── public/
│   └── tests/
├── backend/               # Node.js/Python backend
│   ├── src/
│   ├── tests/
│   └── config/
├── database/              # Database scripts
├── docs/                  # API documentation
└── deployment/            # Docker, config files
```

**Complex App Structure** (after Step 3):
```
my-complex-app/
├── CLAUDE.md              # Enhanced AI config from Step 0
├── docker-compose.yml     # Multi-service setup
├── README.md              # Comprehensive guide
├── services/              # Microservices
│   ├── user-service/
│   ├── order-service/
│   ├── payment-service/
│   └── notification-service/
├── shared/                # Shared libraries
├── tests/                 # Integration tests
├── docs/                  # System documentation
├── monitoring/            # Observability setup
├── deployment/            # Kubernetes configs
└── scripts/               # Build and deploy scripts
```

---

## Development Environment Setup

### Option 1: Local Development (VS Code/Cursor)

**Complete Setup Process**:

**Step 1: Create Workspace Structure**
```bash
# Create main workspace
mkdir ~/projects
cd ~/projects

# Keep template separate
git clone https://github.com/JrLordMoose/Context-Engineering-Boilerplate-Template.git

# Create your first project
mkdir my-awesome-app
cd my-awesome-app
```

**Step 2: Generate Project Configuration**
1. **Open AI chat** (ChatGPT, Claude Desktop)
2. **Copy Step 0 prompt** from template
3. **Paste and complete** Step 0 in chat
4. **Save generated files** in `my-awesome-app/`:
   - Create `CLAUDE.md` and paste content
   - Create `context-sources.md` and paste content
   - Create `.claude/subagents/` folder and files

**Step 3: Generate Application Code**
1. **Continue in same chat** or start new chat with Step 1 prompt
2. **Complete Steps 1-3** following the workflow
3. **Save generated code** in `my-awesome-app/`:
   - Create exact folder structure AI specifies
   - Create each file and paste corresponding code
   - Follow the structure precisely

**Step 4: Development and Testing**
```bash
cd my-awesome-app
npm install        # Install dependencies
npm start          # Run development server
npm test           # Run tests
```

**Step 5: Version Control**
```bash
git init
git add .
git commit -m "Initial project setup with Context Engineering"
git remote add origin https://github.com/yourusername/my-awesome-app.git
git push -u origin main
```

### Option 2: Cloud Development (Replit)

**Complete Setup Process**:

**Step 1: Generate Code First**
1. **Complete Steps 0-3** in AI chat (ChatGPT/Claude Desktop)
2. **Save all outputs** (copy to text files temporarily)

**Step 2: Create Replit Project**
1. **Go to Replit.com** → Create Repl
2. **Choose template** based on your technology (React, Node.js, Python, etc.)
3. **Name your Repl** (same as your project name)

**Step 3: Upload Generated Files**
1. **Delete default files** Replit created (keep package.json if it exists)
2. **Create folder structure** exactly as AI specified in Step 3
3. **Create each file** and paste code from Step 3 output
4. **Upload CLAUDE.md** from Step 0 (for future development)

**Step 4: Run Your Application**
- Click **Run** button
- Replit automatically installs dependencies and starts your app
- Your application should work immediately

### Option 3: GitHub Codespaces

**Complete Setup Process**:

**Step 1: Create GitHub Repository**
1. **Go to GitHub** → New Repository
2. **Name it** your project name (`my-awesome-app`)
3. **Initialize** with README (you'll replace it)

**Step 2: Open in Codespaces**
1. **Click Code** → Codespaces → Create codespace
2. **Wait for environment** to load

**Step 3: Generate and Upload Files**
1. **Complete Steps 0-3** in AI chat
2. **Create files in Codespaces** following exact structure from Step 3
3. **Copy/paste code** from AI output into each file

**Step 4: Develop and Deploy**
```bash
npm install    # Install dependencies
npm start      # Run in cloud environment
```

### Option 4: Claude Code Terminal

**Important**: Claude Code is different! Use it AFTER generating code with chat AI.

**Step 1: Generate Code with Chat AI**
- **Use ChatGPT or Claude Desktop** for Steps 0-3
- **Save all outputs** (you'll need them for Claude Code)

**Step 2: Transfer to Claude Code**
```bash
# Navigate to your project directory
cd ~/projects/my-awesome-app

# Use Claude Code to create files:
# "Create package.json with the following content:" [paste Step 3 content]
# "Create src/App.js with the following content:" [paste Step 3 content]
# [Repeat for all files from Step 3]
```

**Step 3: Development in Claude Code**
- All files are created with Claude Code's help
- Use your custom CLAUDE.md for enhanced collaboration
- Install dependencies and run through Claude Code

---

## File Management Best Practices

### Organization Tips

**1. One Project = One Folder**
- Never mix multiple projects in the same folder
- Each project gets its own complete file structure
- Keep projects completely separate

**2. Consistent Naming**
- Use lowercase with hyphens: `my-project-name`
- Be descriptive: `task-manager` not `app1`
- Avoid spaces and special characters

**3. Backup Your Projects**
- Use Git for version control
- Push to GitHub for cloud backup
- Keep your workspace organized

**4. Template Separation**
- Keep the original template in its own folder
- Never modify the template directly
- Copy prompts from template to use them

### File Creation Order

**Always follow this order**:
1. **Create project folder** (before anything else)
2. **Run Step 0** → Save config files in project folder
3. **Run Steps 1-3** → Save code files in same project folder
4. **Install dependencies** → Run your application

**Never**:
- Create code files before project folder
- Mix Step 0 config with template files
- Put multiple projects in one folder

---

## Quick Reference: File Locations

### Where Files Come From & Where They Go

| Step | Generated Files | Where to Save | Purpose |
|------|----------------|---------------|---------|
| **Step 0** | `CLAUDE.md`, `context-sources.md`, `.claude/` | `your-project/` | AI configuration for your project |
| **Step 1** | Requirements text | Chat history or `your-project/planning/` | Project requirements |
| **Step 2** | Architecture plan | Chat history or `your-project/planning/` | Technical architecture |
| **Step 3** | Complete codebase | `your-project/` | Your application files |

### Template vs Project Files

| File Type | Template Location | Your Project Location | Notes |
|-----------|------------------|---------------------|--------|
| **Prompts** | `template/prompts/step1-prompt.md` | Copy to AI chat | Use but don't modify |
| **Docs** | `template/docs/How-to-Use.md` | Reference only | Read for instructions |
| **CLAUDE.md** | `template/CLAUDE.md` | `your-project/CLAUDE.md` | Generate custom version |
| **App Code** | Not in template | `your-project/src/` | Generated by Steps 1-3 |

### Quick Setup Checklist

For each new project:
- [ ] **Create project folder** with descriptive name
- [ ] **Run Step 0** in AI chat
- [ ] **Save Step 0 files** in project folder
- [ ] **Run Steps 1-3** in AI chat (same chat or new)
- [ ] **Save Step 3 code** in project folder with exact structure
- [ ] **Open project folder** in your development environment
- [ ] **Install dependencies** and run application
- [ ] **Initialize Git** and push to GitHub (optional)

---

## Frequently Asked Questions - File Management

**Q: Where exactly do I put the CLAUDE.md file generated in Step 0?**
A: In your new project folder (e.g., `my-task-manager/CLAUDE.md`), NOT in the template folder. Each project gets its own custom CLAUDE.md.

**Q: Can I reuse the same CLAUDE.md for multiple projects?**
A: You can, but it's better to generate a custom one for each project using Step 0. This optimizes AI collaboration for your specific project needs.

**Q: What if I forget to create a project folder before Step 0?**
A: No problem! Create the folder now and save the Step 0 output there. You can run Step 0 again if needed.

**Q: Should I keep the template folder after creating my project?**
A: Yes! Keep it for future projects. You'll copy the prompts from it each time you start a new project.

**Q: Can I modify the template folder?**
A: It's better not to. Keep the template pristine and create project-specific configurations through Step 0 instead.

**Q: What if my project gets really large with hundreds of files?**
A: The folder structure will grow naturally. The neural field and agents in Step 5 help manage complexity. Consider breaking very large projects into multiple modules.

**Q: How do I share my project with team members?**
A: Push your entire project folder (including CLAUDE.md) to GitHub. Team members can clone and use the same Context Engineering configuration.

**Q: Can I use different development environments for the same project?**
A: Yes! Your project folder works with VS Code, Replit, Claude Code, etc. The files are standard and portable.

---

**Bottom Line**: Create a new folder for each project, save ALL generated files there (Step 0 config + Step 3 code), and keep everything organized. Simple rule: One project = One folder = Complete independence.