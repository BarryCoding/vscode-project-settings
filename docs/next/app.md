# App

## Routing

### 👁️ Defining Routes

### 👁️ Pages

### 👁️ Layouts and Templates

### 👁️ Linking and Navigation

### 👁️ Error Handing

### 👁️ Loading UI and Streaming

### ✅ Redirecting

- NextResponse.redirect in middleware
- redirects in next.config.mjs
- redirect
- permanentRedirect
- useRouter

- advanced (in what case?)

### ✅ Route Groups

- convention: (folderName)

### ✅ Project Organization

- features
  - private folder `_folderName`
  - route groups `(folderName)`
  - `src` directory
  - module path aliases `@/`

- strategies
  - outside of app
  - inside of app

### ✅ Dynamic Routes

- convention `[folderName]`
- ? generating static params
- catch-all segments `[...folderName]`
- optional catch-all segments `[[...folderName]]`
- TS table

### ⛔️ Parallel Routes

- slots `@folderName`
- active state and navigation

### ⛔️ Intercepting Routes

- convention `(.)` `(..)` `(..)(..)` `(...)`

### ✅ Route Handlers

- convention `route.ts`
  - GET POST PUT PATCH DELETE HEAD OPTIONS
  - NextRequest NextResponse
- Behavior
  - Caching
  - Opting out of caching
  - Route Resolution
- Examples ...

### ⛔️ Middleware

- use cases
  - Authentication and Authorization
  - Server-Side Redirects
  - Path Rewriting
  - Bot Detection
  - Logging and Analytics
  - Feature Flagging
- convention `middleware.ts`
- matching paths
  - matcher
  - conditional statements
- NextResponse
- cookies
- headers
  - CORS
- producing a response
  - waitUntil and NextFetchEvent
- advanced middleware flags
- runtime: edge

### ✅ i18n

- localization
- static generation

## Styling

- not NextJS related topics
- integration part

### ✅ Tailwind CSS

- install
  - `pnpm add -D tailwindcss postcss autoprefixer`
  - `npx tailwindcss init -p`
- tailwind.config.ts
- globals.css `@tailwind`

### 👁️ CSS Module

- extensions `.module.css`

### 👁️ Sass

- install `pnpm add -D sass`


## Rendering

- environment
  - client
  - server
- request-response lifecycle
  - user action
  - http request
  - server
  - http response
  - client
- network boundary
  - use client
  - use server

### ✅ Server Components

- benefits
  - data fetching
  - security
  - caching
  - performance
  - initial page load and first contentful paint
  - SEO and social network shareability
  - streaming

- How?

- strategies
  - static `build time`
  - dynamic `request time`
    - cookies() headers()
    - searchParams
  - streaming
    - loading.tsx
    - Suspense

### ✅ Client Components

- benefits
  - interactivity
  - browser APIs
- use `'use client'`
- how?
  - full page load
  - subsequent

### Composition Patterns

- when table!
- Server Components
  - share data
  - server only
  - 3rd party package | Providers
    - reexport under 'use client'
- Client Components
  - Move down the tree
  - serialize props from sever to client
- Interleaving
  - client not support: import server component
  - client support: server component as props

### 👁️ Runtime

- node.js
  - rendering
- edge
  - middleware

## Data Fetching

### ✅ Patterns and Best Practices

- fetching data on server
- fetching data where it's needed
- streaming
- sequential data fetching
- parallel data fetching
- preloading data
  - cache, server-only, preload pattern
- sensitive data

### ✅ Fetching Caching and Revalidating

1. server fetch
   - caching data
   - revalidating data
     - on-demand
     - time-based
   - not cached
     - individual (recommend)
     - multiple
2. server 3rd party lib
   - cache()
3. client routeHandler
4. client 3rd party lib
   - react-query or SWR

### ✅ Server Actions and Mutations

- convention `use server`
  - server component
  - client component
- behavior
- examples
  - form non-form
  - error handling
  - revalidating
  - redirecting
  - cookies
- security
  - authentication and authorization
  - closures
  - overwriting encryption keys
  - allowed origins

## Caching

### Request Memoization

### Data Cache

### Full Route Cache

### Router Cache

### Cache Interaction

### APIs






## Optimizing

## Configuring

## Testing

## Authentication

## ✅ Deploying

- [ ] docker docker

### Checklist

### Static Exports
