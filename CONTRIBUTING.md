# Contributing to D-OneCash

Thank you for your interest in contributing to D-OneCash! This document provides guidelines and information for contributors.

## 🚀 Getting Started

### Prerequisites
- Node.js 18 or higher
- PostgreSQL database
- Git
- Basic knowledge of React, TypeScript, and Express.js

### Development Setup
1. Fork the repository
2. Clone your fork:
   ```bash
   git clone https://github.com/your-username/d-onecash.git
   cd d-onecash
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Copy environment variables:
   ```bash
   cp .env.example .env
   ```
5. Configure your `.env` file with database connection
6. Set up database:
   ```bash
   npm run db:push
   ```
7. Start development server:
   ```bash
   npm run dev
   ```

## 🎯 How to Contribute

### Reporting Bugs
- Use the GitHub issue tracker
- Include detailed description and steps to reproduce
- Provide system information and screenshots if helpful
- Check if the issue already exists before creating new one

### Suggesting Features
- Open an issue with `enhancement` label
- Describe the feature and its benefits
- Include mockups or examples if possible
- Discuss implementation approach

### Code Contributions
1. Pick an issue or create one for your contribution
2. Create a feature branch:
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. Make your changes following our coding standards
4. Test your changes thoroughly
5. Commit with descriptive messages
6. Push to your fork and create a pull request

## 📝 Coding Standards

### TypeScript/JavaScript
- Use TypeScript for all new code
- Follow ESLint configuration
- Use meaningful variable and function names
- Add JSDoc comments for complex functions
- Prefer functional programming patterns

### React Components
- Use functional components with hooks
- Keep components small and focused
- Use proper prop typing with TypeScript
- Follow the established file structure
- Use Tailwind CSS for styling

### Database
- Use Drizzle ORM for all database operations
- Follow the schema patterns in `shared/schema.ts`
- Add proper relations between tables
- Use transactions for multi-step operations

### API Design
- Follow RESTful conventions
- Use proper HTTP status codes
- Validate input with Zod schemas
- Handle errors gracefully
- Document new endpoints

## 🏗 Project Structure

```
d-onecash/
├── client/           # React frontend
│   ├── src/
│   │   ├── components/   # Reusable UI components
│   │   ├── pages/        # Page components
│   │   ├── hooks/        # Custom React hooks
│   │   └── lib/          # Utility functions
├── server/           # Express backend
│   ├── routes.ts     # API routes
│   ├── storage.ts    # Data access layer
│   └── db.ts         # Database configuration
├── shared/           # Shared code
│   └── schema.ts     # Database schema and types
└── public/           # Static assets
```

## 🧪 Testing

### Running Tests
```bash
# Run all tests
npm test

# Run tests in watch mode
npm run test:watch

# Run tests with coverage
npm run test:coverage
```

### Writing Tests
- Add tests for new features and bug fixes
- Use meaningful test descriptions
- Test both success and error cases
- Mock external dependencies
- Aim for good test coverage

## 🎨 UI/UX Guidelines

### Design Principles
- Mobile-first responsive design
- Consistent with D-OneCash branding (green/black)
- Accessible to all users
- Intuitive navigation
- Fast loading times

### Component Guidelines
- Use Radix UI components when possible
- Follow Tailwind CSS conventions
- Ensure keyboard navigation works
- Add proper ARIA labels
- Test on multiple screen sizes

## 📋 Pull Request Process

### Before Submitting
- [ ] Code follows project standards
- [ ] Tests pass locally
- [ ] New features have tests
- [ ] Documentation updated if needed
- [ ] No console errors or warnings
- [ ] Mobile responsiveness verified

### PR Description
Include:
- Clear description of changes
- Link to related issue
- Screenshots for UI changes
- Breaking changes noted
- Testing instructions

### Review Process
1. Automated checks must pass
2. Code review by maintainers
3. Address feedback if requested
4. Final approval and merge

## 🐛 Debugging

### Common Issues
- **Database connection**: Check `DATABASE_URL` format
- **Session issues**: Verify `SESSION_SECRET` is set
- **Build failures**: Clear `node_modules` and reinstall
- **Type errors**: Run `npm run type-check`

### Development Tools
- Use browser dev tools for frontend debugging
- Check server logs for backend issues
- Use Drizzle Studio for database inspection
- Utilize TypeScript strict mode

## 📖 Documentation

### Code Documentation
- Add JSDoc comments for public APIs
- Document complex algorithms
- Include usage examples
- Keep README up to date

### User Documentation
- Update user guides for new features
- Include screenshots in documentation
- Write clear setup instructions
- Document configuration options

## 🔐 Security

### Best Practices
- Never commit secrets or API keys
- Validate all user inputs
- Use parameterized queries
- Implement proper authentication
- Follow OWASP guidelines

### Reporting Security Issues
- Email security issues privately
- Do not open public issues for vulnerabilities
- Allow reasonable time for fixes
- Coordinate disclosure timeline

## 🎉 Recognition

Contributors will be:
- Listed in project credits
- Mentioned in release notes
- Invited to contributor discussions
- Eligible for special recognition

## 📞 Getting Help

- Open an issue for questions
- Join community discussions
- Check existing documentation
- Review similar projects

## 📄 License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

Thank you for helping make D-OneCash better! 🚀