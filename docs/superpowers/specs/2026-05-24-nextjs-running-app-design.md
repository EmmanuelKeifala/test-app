# Next.js Running App Design

## Goal

Create a new public GitHub repository containing a minimal deployable Next.js application. The application should render the message `we are running` on its homepage and include a Dockerfile suitable for production deployment.

## Repository

- Repository name: `nextjs-running-app`
- Visibility: public
- Owner: authenticated GitHub CLI user
- Initial code will be pushed from `/home/emmanuel/work/test-app`

## Application

Use a standard Next.js App Router project with TypeScript and npm. The homepage will be implemented in `app/page.tsx` and will display only the required message in a simple centered layout.

The app should keep the default Next.js conventions where possible so it remains easy to build, run, and deploy.

## Docker Deployment

Add a multi-stage `Dockerfile` based on Node.js Alpine images:

- Install dependencies with `npm ci`
- Build the Next.js app with `npm run build`
- Run the production server with `npm start`
- Expose port `3000`

The Dockerfile will prioritize clear, conventional deployment over extra optimization.

## Verification

Before pushing, verify that the app builds successfully with `npm run build`. If feasible, also build the Docker image to confirm the Dockerfile works.

## Out Of Scope

- Authentication
- API routes
- Custom styling system
- CI/CD configuration
- Hosting-provider-specific deployment files
