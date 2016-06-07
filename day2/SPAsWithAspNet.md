# Creating SPAs with ASP.NET

## What is a SPA?
- Single Page Application
- More fluid user experience akin to a desktop app
- Browser based
- Rich UI
- Thick client
- View composition on the client side
- Server primarily used for retrieving/persisting data

## Hallmarks
- No URL change
  - Other than hash
- Back button still works as expected
- Bookmark-able links
- Rich interaction between UI components
- Single full-page refresh from server, other content loaded using JS
- Uses web services, especially RESTful ones

## Advantages
- Faster UI
- Better UX
- Less server loading
- Less need for caching

## Disadvantages
- SEO
- Can be more work
- Modern web skills

## Routers
- '#' is used because they can then internally key off of hash change event

## Modularizing Code
- Keeps variables off global scop
- Separation of concerns
- ECMAScript 6 import/export feature

## What is left for server-side?
- Data Services
  - Database Access
  - CRUD
  - Validation
- SEO
  - Hash-Bang
- Security
  - Service-As-UI Rule
  - Authentication
- Other
  - Delivering views
  - Different views for different device agents
  - Preprocessing
  - Mixing dynamic and static content
  
- Build utilities
  - Task Runner (with gulp or grunt)
  - Minification
  - Bundling
  - ts -> js
  
  ## Hash-bang
  - Allow server to deliver a crawlable (pre-rendered) page