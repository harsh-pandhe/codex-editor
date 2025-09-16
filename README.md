# Codex Editor - Real-Time Collaborative Code Editor

A powerful, modern collaborative code editor built with Next.js, Monaco Editor, and Liveblocks. Designed for seamless real-time collaboration, perfect for pair programming, code reviews, team development, and educational environments.

🚀 **Live Demo**: [https://collabcodex.vercel.app/](https://collabcodex.vercel.app/)  
📂 **Repository**: [https://github.com/harsh-pandhe/codex-editor](https://github.com/harsh-pandhe/codex-editor)

## ✨ Key Features

### Real-Time Collaboration
- **Live Multi-User Editing**: Multiple developers can code simultaneously with instant synchronization
- **Live Cursors & Presence**: See teammates' cursors, selections, and online status in real-time
- **Conflict-Free Editing**: Y.js CRDT technology ensures seamless collaborative editing without conflicts
- **Instant Synchronization**: Powered by Liveblocks for lightning-fast real-time updates

### Advanced Code Editor
- **Monaco Editor Integration**: Full VS Code editor experience with syntax highlighting and IntelliSense
- **Multi-Language Support**: Comprehensive syntax highlighting for popular programming languages
- **Code Intelligence**: Auto-completion, error detection, and code formatting
- **Flexible Layout**: Golden Layout system for customizable multi-panel interface

### Organization & Board Management
- **Secure Authentication**: Clerk-powered authentication with organization support
- **Board System**: Create and manage multiple coding projects with custom layouts
- **Team Workspaces**: Organization-based board sharing and access control
- **Persistent State**: Automatic saving ensures no code is ever lost

### Modern User Experience
- **Responsive Design**: Beautiful, mobile-friendly interface built with Tailwind CSS
- **Intuitive UI**: Clean, distraction-free coding environment
- **Performance Optimized**: Built on Next.js 14 with App Router for optimal performance

## 🛠️ Technology Stack

### Core Framework
- **Next.js 14** - React framework with App Router for optimal performance
- **TypeScript** - Type-safe development for reliability and maintainability
- **Tailwind CSS** - Modern, utility-first CSS framework

### Editor & Collaboration
- **Monaco Editor** - Industry-standard code editor (VS Code for the web)
- **Liveblocks** - Real-time collaboration infrastructure and presence
- **Y.js** - Conflict-free replicated data types for collaborative editing
- **Y-Monaco** - Monaco Editor bindings for Y.js integration
- **Golden Layout** - Flexible multi-panel interface management

### Backend & Services
- **Convex** - Real-time backend as a service with instant database sync
- **Clerk** - Complete authentication and user management platform
- **Y-Protocols** - Awareness and synchronization protocols

### UI & Design
- **Radix UI** - Headless, accessible UI component primitives
- **Lucide React** - Beautiful, customizable icon library
- **Perfect Freehand** - Smooth drawing and annotation capabilities

## 🚀 Quick Start

### Prerequisites

Ensure you have the following installed:
- **Node.js 18+** 
- **Package manager**: npm, yarn, or pnpm
- **Service Accounts**: Convex, Liveblocks, and Clerk

### Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/harsh-pandhe/codex-editor.git
   cd codex-editor
   ```

2. **Install Dependencies**
   ```bash
   npm install
   # or
   yarn install
   # or  
   pnpm install
   ```

3. **Environment Configuration**
   
   Create `.env.local` in the project root:
   ```env
   # Convex Configuration
   CONVEX_DEPLOYMENT=your_convex_deployment_id
   NEXT_PUBLIC_CONVEX_URL=https://your_deployment.convex.cloud

   # Clerk Authentication
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_your_clerk_key
   CLERK_SECRET_KEY=sk_test_your_clerk_secret

   # Liveblocks Real-time Collaboration
   LIVEBLOCKS_SECRET_KEY=sk_your_liveblocks_secret
   NEXT_PUBLIC_LIVEBLOCKS_PUBLIC_KEY=pk_your_liveblocks_public_key
   ```

4. **Initialize Convex Backend**
   ```bash
   npx convex dev
   ```

5. **Start Development Server**
   ```bash
   npm run dev
   # or
   yarn dev  
   # or
   pnpm dev
   ```

6. **Access the Application**
   
   Open [http://localhost:3000](http://localhost:3000) in your browser

## 📁 Project Architecture

```
codex-editor/
├── app/                          # Next.js App Router
│   ├── (dashboard)/             # Protected dashboard routes
│   │   ├── _components/         # Dashboard-specific components
│   │   └── page.tsx            # Main dashboard interface
│   ├── api/                    # API route handlers
│   ├── board/                  # Board management routes
│   │   └── [boardId]/          # Dynamic board pages
│   ├── globals.css             # Global styles
│   └── layout.tsx              # Root application layout
├── components/                  # Reusable React components
│   ├── auth/                   # Authentication components
│   ├── modals/                 # Modal dialog components
│   └── ui/                     # Base UI components (Radix)
├── convex/                     # Convex backend functions
│   ├── board.ts               # Board CRUD operations
│   ├── boards.ts              # Board query functions
│   └── schema.ts              # Database schema definitions
├── hooks/                      # Custom React hooks
├── lib/                        # Utility functions and helpers
├── providers/                  # React context providers
├── store/                      # Zustand state management
├── types/                      # TypeScript type definitions
└── public/                     # Static assets and images
```

## 🎯 Usage Guide

### Getting Started with Boards

1. **Authentication**: Sign in using Clerk authentication
2. **Organization Setup**: Create or join an organization for team collaboration
3. **Create Board**: Click "New Board" to create a collaborative coding workspace
4. **Invite Collaborators**: Share board access with team members
5. **Start Coding**: Begin real-time collaborative development!

### Collaboration Features

- **Real-Time Editing**: Watch as teammates edit code with live cursors and selections
- **Presence Awareness**: See who's online and actively editing
- **Automatic Conflict Resolution**: Y.js handles simultaneous edits seamlessly
- **Persistent Sessions**: All changes auto-save for uninterrupted workflow

### Advanced Features

- **Multi-Panel Layout**: Organize multiple code files with Golden Layout
- **Organization Management**: Team-based board organization and access control
- **Search & Discovery**: Quick board search and filtering capabilities
- **Favorites System**: Bookmark frequently accessed boards

## 🤝 Contributing

We welcome contributions! Help make Codex Editor even better.

### Contribution Workflow

1. **Fork** the repository on GitHub
2. **Clone** your fork locally
3. **Create** a feature branch: `git checkout -b feature/awesome-feature`
4. **Commit** your changes: `git commit -m 'Add awesome feature'`
5. **Push** to your branch: `git push origin feature/awesome-feature`
6. **Submit** a Pull Request with detailed description

### Development Guidelines

- Follow TypeScript best practices
- Write meaningful commit messages
- Test your changes thoroughly
- Update documentation as needed

## 📄 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for complete details.

## 🙏 Acknowledgments

Built with amazing open-source technologies:

- **[Monaco Editor](https://microsoft.github.io/monaco-editor/)** - Powerful web-based code editor
- **[Liveblocks](https://liveblocks.io/)** - Real-time collaboration platform
- **[Y.js](https://yjs.dev/)** - Conflict-free replicated data types
- **[Convex](https://convex.dev/)** - Real-time backend as a service  
- **[Clerk](https://clerk.com/)** - Complete authentication platform
- **[Golden Layout](https://golden-layout.com/)** - Multi-panel interface framework

## 📞 Support & Community

- **Issues**: Report bugs on [GitHub Issues](https://github.com/harsh-pandhe/codex-editor/issues)
- **Discussions**: Join conversations in [GitHub Discussions](https://github.com/harsh-pandhe/codex-editor/discussions)
- **Documentation**: Visit our [Wiki](https://github.com/harsh-pandhe/codex-editor/wiki) for detailed guides

---

**🚀 Ready to revolutionize collaborative coding? Try Codex Editor today!**

**Live App**: [https://collabcodex.vercel.app/](https://collabcodex.vercel.app/)  
**Source Code**: [https://github.com/harsh-pandhe/codex-editor](https://github.com/harsh-pandhe/codex-editor)