# App

TODO: links to origin docs

## 👁️ Configuring

### ✅ TS

- plugin
  - command shift p
  - typescript: select typescript version
  - use workspace version
- minimum version v4.5.2
- statically typed links
  - `experimental: {typedRoutes: true}`
- end-to-end type safety
- async server component TS error
  - TS 5.1.3 
  - @types/react 18.2.8
- path aliases and baseUrl
- custom type declarations
  - not in next-env.d.ts
  - new-types.d.ts
  - tsconfig.json includes the above

### ✅ ESlint

- config 
  - default (eslint-config-next)
- plugin
- custom directories
- disabling rules
- with other tools
  - prettier (eslint-config-prettier)

### .env

- loading environment variables
  - `process.env.XX`
  - referencing other variables `$VARIABLE`
  - @next/env
- for browser `NEXT_PUBLIC_XX`
- default environment variables
  - .env
  - .env.development
  - .env.production
- test environment
  - .env.test
- load order
  1. process.env
  2. .env.$(NODE_ENV).local
  3. .env.local
  4. .env.$(NODE_ENV)
  5. .env

### Path Aliases

- absolute imports
- module aliases

### MDX

- @next/mdx
- remote mdx
  - next-mdx-remote
- layouts
- Remark and Rehype plugins
- frontmatter
- custom elements

### src

### ? Draft Mode

### ? Content Security Policy

- nonce

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

## 👁️ Caching

### Request Memoization

- duration 
  - in the same render
- revalidating
  - no need
- GET only

### Data Cache

- duration
  - unless revalidate / opt-out
- revalidating
  - time-based / on-demand
- opt-out

### Full Route Cache

1. react rending on the server
2. next.js caching on the server(full route cache)
3. react hydration and reconciliation on the client
4. next.js caching on the client(route cache)
5. subsequent navigation

- static and dynamic rendering

- duration
- invalidation
  - revalidating data
  - redeploying
- opt-out

### Router Cache

- duration
  - session
  - automatic invalidation period
- invalidation
  - revalidatePath revalidateTag
  - router.refresh
- opt-out

## 👁️ Authentication

### Authentication

- sign up / login

1. capture user credentials
2. validate form fields on the server
3. create a user or check user credentials

### Session Management

#### stateless

1. generating a secret key
2. encrypting and decrypting
3. setting cookies
4. updating session
5. deleting session

#### database

1. table
2. functions
3. encrypt

### Authorization

- Optimistic checks middleware

- ⭐️ Data Access Layer
- Data Transfer Object
- Server Components
- Layouts and auth checks
- server actions
- route handlers

### Resources

...







## Optimizing

## Testing

## ✅ Deploying

- [ ] docker docker

### Checklist

### Static Exports
