# Personal-Dev-Manifesto

Personal Dev Notes for the future

## Project Planning

- GitHub Projects/ Jira - Sprint Board
- Confluence/ Notion - Project Documentation

## API Testing

- Postman - Testing Endpoints
- Swagger - Declarative API Documentation

## Web Application Framework

- Model-View-Controller (MVC)

## Infrastructure as Code (IaC)

- Terraform

## CI/CD Pipeline

- Github Actions

## Webdev Project Workflow

1. Create the GitHub repo with the project skeleton and push the initial code
2. Set up GitHub continuous deployment with Vercel/Netlify (or any other hosting service)
3. Create branches in the repository to implement features or fix bugs
4. Hosting services will create a deployable build, deploy it on a CDN, and provide us a preview URL for each branch.
5. Use this URL to test the feature. We can also share this URL publicly with our stakeholders.
6. Merge the PR, and the changes in the master or main branch are also built and deployed automatically.

## Git Commit Types

- feat – feature addition
- fix – bug fix
- chore – improvements/ tech debt
- refactor – improvements/ tech debt
- docs – documentation
- style – code format
- test – including new or correcting previous tests
- perf – performance improvements
- ci – continuous integration related
- build – changes that affect the build system or external dependencies
- revert – reverts a previous commit

## General Project Structure

└───.github/workflows - CI/CD with Github Actions
└───src/ - Frontend
└───api/ - Backend
└───infrastructure - Cloud Resource Provisioning

## React Best Practices (adapt as per application size)

- kebab-case naming convention for folders

```
message-item/
```

- Maintanable import structure at the top of files

```
Built-In (like 'react') --> External (third-party node modules) --> Internal
```

- Set up Linter (ESLint)
- Lazy loading/ Code Splitting for better bundle management (WebPack)
- Error Handling (try/catch, react-error-boundary library as appropriate, 3rd Party/ custom logging utilities)
- useReducer hook for components where useState hooks > 4 for better code readability
- Folder Structure

```
src
└───feature (Non-reusable Components)
    └───user/
    └───message/
        └───message-item/
        └───message-list/
    └───payment/
└───components (Reusable Components)
│   └───app/
│   │       App.js
|   |       App.test.js
│   │       App.style.css
│   └───button/
│   └───list/
└───hooks/
└───context/
└───services/
```

## Useful Tricks

- Sometimes it will required to delete ./node_modules folder to resolve random errors related to 3rd party libraries. Use the following command instead of manual deletion because it will be way faster
  ```
  rm -rf node_modules
  ```
