# Deployment Guide for D-OneCash

This guide will help you deploy D-OneCash to various hosting platforms.

## 🚀 Quick Deployment Options

### Option 1: Replit (Recommended)
1. Import your GitHub repository to Replit
2. Set environment variables in Secrets tab
3. Run `npm install` and `npm run dev`
4. Enable Replit Auth for authentication

### Option 2: Vercel
1. Connect your GitHub repository to Vercel
2. Set environment variables in project settings
3. Build command: `npm run build`
4. Output directory: `dist`

### Option 3: Railway
1. Connect GitHub repository to Railway
2. Set environment variables
3. Railway will auto-detect and deploy

### Option 4: DigitalOcean App Platform
1. Create new app from GitHub repository
2. Configure environment variables
3. Set build and run commands

## 🔧 Environment Variables

Copy `.env.example` to `.env` and configure:

```bash
# Required
DATABASE_URL=your_postgresql_connection_string
SESSION_SECRET=your_secure_random_string

# Optional (for Replit Auth)
REPL_ID=your_replit_app_id
ISSUER_URL=https://replit.com/oidc
REPLIT_DOMAINS=your-domain.com
```

## 🗄️ Database Setup

### PostgreSQL on Neon (Recommended)
1. Create account at [neon.tech](https://neon.tech)
2. Create new project
3. Copy connection string to `DATABASE_URL`
4. Run `npm run db:push` to create tables

### PostgreSQL on Railway
1. Add PostgreSQL service to your Railway project
2. Copy connection string from service details
3. Set as `DATABASE_URL` environment variable

### PostgreSQL on Supabase
1. Create project at [supabase.com](https://supabase.com)
2. Go to Settings > Database
3. Copy connection string to `DATABASE_URL`

## 📋 Pre-deployment Checklist

- [ ] All environment variables configured
- [ ] Database connection working
- [ ] Session secret set to secure random string
- [ ] Dependencies installed (`npm install`)
- [ ] Database tables created (`npm run db:push`)
- [ ] Build successful (`npm run build`)
- [ ] HTTPS enabled for production
- [ ] Domain configured (if using custom domain)

## 🔐 Security Considerations

### Production Environment
- Use strong, unique `SESSION_SECRET`
- Enable HTTPS/SSL certificates
- Configure CORS properly
- Use environment variables for all secrets
- Enable database connection pooling
- Set up monitoring and logging

### Database Security
- Use connection pooling
- Enable SSL for database connections
- Regular database backups
- Implement proper access controls

## 🚀 Build Commands

```bash
# Development
npm run dev

# Production build
npm run build

# Database operations
npm run db:push    # Push schema changes
npm run db:studio  # Open Drizzle Studio
```

## 🌐 Custom Domain Setup

### Vercel
1. Add domain in project settings
2. Configure DNS records as instructed
3. SSL certificates auto-generated

### Railway
1. Add custom domain in project settings
2. Point CNAME to Railway endpoint
3. SSL certificates auto-generated

### Replit
1. Link custom domain in deployment settings
2. Configure DNS as instructed
3. SSL included automatically

## 📊 Monitoring & Analytics

### Recommended Tools
- **Error Tracking**: Sentry
- **Analytics**: Google Analytics or Plausible
- **Uptime Monitoring**: Uptime Robot
- **Performance**: Web Vitals

### Health Checks
Set up health check endpoints:
- Database connectivity
- Session store status
- Memory usage
- Response times

## 🔄 CI/CD Pipeline

### GitHub Actions Example
```yaml
name: Deploy
on:
  push:
    branches: [main]
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
      - run: npm install
      - run: npm run build
      - run: npm test
```

## 🆘 Troubleshooting

### Common Issues
1. **Database Connection Failed**
   - Check `DATABASE_URL` format
   - Verify database is accessible
   - Check firewall settings

2. **Session Issues**
   - Verify `SESSION_SECRET` is set
   - Check session store connection
   - Ensure HTTPS in production

3. **Build Failures**
   - Check Node.js version compatibility
   - Verify all dependencies installed
   - Review build logs for errors

4. **Authentication Problems**
   - Verify auth provider configuration
   - Check redirect URLs
   - Confirm environment variables

### Support
- Check deployment platform documentation
- Review application logs
- Test database connectivity
- Verify environment variable configuration

## 📈 Scaling Considerations

### Database
- Enable connection pooling
- Consider read replicas for heavy loads
- Monitor query performance
- Implement caching strategies

### Application
- Use load balancers for multiple instances
- Implement Redis for session storage
- Consider CDN for static assets
- Monitor memory and CPU usage

---

**Note**: Always test deployments in staging environment before production release.