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

## Data Fetching

## Rendering

## Caching

## Styling

## Optimizing

## Configuring

## Testing

## Authentication

## ✅ Deploying

- [ ] docker docker

### Checklist

### Static Exports
