**# Project Overview**

I have a basic Next JS project setup with shadcn/ui...

**# Core Functionality**


**# Doc**


**# Current File Structure**


**# Additional Requirements**
1. Project Setup
	- All new components should go in `/src/components` at the root (not in the `/src/app` folder) and be named like `ExampleComponent.tsx` unless otherwise specified
	- All new pages go in `/src/app`
	- Use the Next.js App router
	- All data fetching should be done in a server component and pass the data down as props
	- Client components (useState, hooks, etc) require that `use client` is set at the top of the file

2. Server-side API Calls
	- All interactions with external APIs (e.g. Youtube, Twitter/X, Reddit, OpenAI) should be performed server-side
	- Create dedicated API routes in the `/src/app/api` directory for each external API interaction
	- Client-side components should fetch data through these API routes, not directly from external APIs

3. Environment Variables
	- Store all sensitive information (API keys, credentials) in environment variables
	- Use a `.env.local` files for local development and ensure it's listed in `.gitignore`
	- For production, set environment variables in the deployment platform (e.g. Vercel)
	- Access environment variables only in server-side code or API routes

4. Error Handling and Logging
	- Implement comprehensive error handling in both client-side components and server-side API routes
	- Log errors on the server-side for debugging purposes
	- Display user-friendly error messages on the client-side

5. Type Safety
	- Use Typescript interfaces for all data structures, especially API responses
	- Avoid using `any` type; instead, define proper types for all variables and function parameters

6. API Client Initializations
	- Initialize API clients (e.g. Snoowrap for Rddit, OpenAi) in server-side code only
	- Implement checks to ensure API clients are properly initialized before use

7. Data Fetching in Components
	- User React hooks (e.g. `useEffect`) for data fetching in client-side components
	- Implement loading states and error handling for all data fetching operations

8. Next.js Configuration
	- Utilize `next.config.mjs` for environment-specific configurations
	- Use the `env` property in `next.config.mjs` to make environment variables available to the application

9. CORS and API Routes
	- Use Next.js API routes to avoid CORS issues when interacting with external APIs
	- Implement proper request validation in API routes

10. Component Structure
	- Separate concerns between client and server components
	- Use server components for initial data fetching and pass data as props to client components

11. Security
	- Never expose API keys
	- 