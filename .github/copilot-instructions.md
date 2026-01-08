# Copilot Instructions for congenial-spork

## Project Overview
A full-stack Node.js/Python application with PostgreSQL database, configured for Replit hosting. The project uses modern JavaScript tooling and supports multiple integrations including Twilio, SendGrid, and Resend.

## Tech Stack
- **Runtime**: Node.js 20, Python 3.11
- **Database**: PostgreSQL 16
- **Frontend**: Development server on port 5000 (`npm run dev`)
- **Build**: `npm run build` for production builds
- **Deployment**: Auto-scale on Replit with `npm start`

## Development Workflow
- **Local Dev**: Run `npm run dev` - starts frontend server on port 5000
- **Production Build**: Run `npm run build` 
- **Start Server**: Run `npm start` - used for deployment
- **IDE Setup**: VS Code Chrome debugger configured to launch against `localhost:8080`

## Replit Configuration (replit)
- **Expert Mode**: Enabled for AI agent workflows
- **Key Integrations**: OpenAI, Twilio, SendGrid, Resend, Replit authentication
- **Workflow**: Primary "Project" workflow runs "Frontend Server" in parallel mode
- **Port Mapping**: 
  - Port 5000 → External port 80 (main web interface)
  - Port 5001 → External port 3001 (secondary service)
- **System Packages**: FreeFont, glibc locales, Graphviz, unzip, xdg-utils

## Conventions & Patterns
- Use npm scripts defined in package.json for all development tasks
- Follow Replit nix-based environment configuration for reproducible setups
- Leverage Replit integrations when adding email/SMS/communication features
- Database migrations and initialization should work with PostgreSQL 16

## Integration Points
- **Replit Auth**: Built-in login available via `javascript_log_in_with_replit` integration
- **Email**: SendGrid for transactional emails
- **SMS/Voice**: Twilio for communications
- **Modern Email**: Resend API for email delivery
- **AI**: OpenAI integrations available

## Common Tasks
- **Add Dependencies**: Modify package.json or use `npm install` in dev environment
- **Database Setup**: PostgreSQL available in Replit environment - configure connection string in environment
- **Deploy**: Commit changes; Replit automatically runs `npm run build && npm start`
- **Debug**: Use VS Code Chrome debugger or Replit's built-in console

## Notes
- Repository structure suggests early-stage project - may need to establish src/ and other directories
- .gitignore includes AL language patterns (likely leftover template) - may need cleanup
- Ensure environment variables are configured in Replit for API keys (Twilio, SendGrid, Resend)
