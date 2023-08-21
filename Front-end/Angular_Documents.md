# Documents Angular Template

This is a comprehensive Angular application which is designed to be scalable, maintainable and robust. The application follows a clear directory structure along with a set of predefined scripts for build, development, testing and formatting. This application has been enhanced with a range of libraries such as Husky, Commitlint, AutoChangelog, Bootstrap, and ng-bootstrap.

## Getting Started

To get started, clone the repository to your local machine and install the dependencies:

```shell
git clone <repo_url>
cd <project_name>
yarn
```

## Scripts

The `package.json` file includes the following scripts:

- `yarn start`: Runs the app in development mode on `http://localhost:4200`
- `yarn build`: Builds the app for production in the `dist/` folder
- `yarn build:dev`, `yarn build:qc`, `yarn build:uat`, `yarn build:prod`: Builds the app with different configurations
- `yarn watch`: Builds the app in development mode and watches for changes
- `yarn test`: Runs unit tests via [Karma](https://karma-runner.github.io)
- `yarn format`: Formats the code using Prettier
- `yarn prepare`: Sets up Husky for Git hooks
- `yarn changelog`: Generates a changelog based on git commits
- `yarn changelog:commit`: Generates a changelog and amends the current commit with the new changelog

## Local Testing of Builds

After running the build script, you may want to test the resulting build in a local environment. To do this, you can use a simple, zero-configuration command-line HTTP server, such as `http-server`.

If you haven't installed it yet, you can do so globally by running:

```shell
npm install --global http-server
```

Then, navigate to your build directory and start the server:

```shell
cd dist/<project_name>
http-server
```

By default, this will start the server on port 8080. You can then navigate to `http://localhost:8080` in your browser to view your application.

## Project Structure

This application follows a particular structure:

```shell
.
├── src/                                               # Source files (alternatively `lib` or `app`)
│   ├── app/                                           # Main app module and components
│   │   ├── containers/                                # Components that make up your application's screens, pages, dialogs, forms
│   │   │   └── module-name/                           # Specific module in the containers
│   │   │       ├── component-name/                    # Specific feature or type within the module
│   │   │       │   ├── component-name.type.html       # HTML template for the type-specific feature
│   │   │       │   ├── component-name.type.scss       # SCSS styles for the type-specific feature
│   │   │       │   └── component-name.type.ts         # Angular component for the type-specific feature
│   │   │       └── module-name.module.ts              # Module declaration file
│   │   ├── core/                                      # Core features used throughout the application
│   │   │   ├── enums/                                 # Enumerations
│   │   │   │   └── name.enum.ts                       # Enumeration files
│   │   │   ├── guards/                                # Route guards (services that control navigation access)
│   │   │   │   ├── auth.guard.ts                      # Guard to prevent unauthenticated users
│   │   │   │   └── non-auth.guard.ts                  # Guard to prevent authenticated users
│   │   │   ├── interfaces/                            # TypeScript interfaces
│   │   │   │   └── interface-name.ts                  # Interface declaration files
│   │   │   ├── interceptors/                          # Interceptors
│   │   │   │   ├── api.interceptor.ts                 # Interceptor for handling API interactions
│   │   │   │   ├── auth.interceptor.ts                # Interceptor for handling authentication
│   │   │   │   ├── data.interceptor.ts                # Interceptor for handling data processing
│   │   │   │   ├── error.interceptor.ts               # Interceptor for handling HTTP errors
│   │   │   │   └── refresh-token.interceptor.ts       # Interceptor for refreshing tokens
│   │   │   ├── models/                                # Application models
│   │   │   │   └── model-name.ts                      # Model declaration files
│   │   │   ├── services/                              # Services for API communication and business logic
│   │   │   │   ├── api.service.ts                     # Service for making API calls
│   │   │   │   ├── jwt.service.ts                     # Service for handling JWTs
│   │   │   │   └── logging.service.ts                 # Service for application logging
│   │   │   └── tokens/                                # Tokens for user authentication handling
│   │   │       ├── api.ts                             # API configuration token
│   │   │       ├── interceptor.ts                     # Interceptor configuration token
│   │   │       ├── logging.ts                         # Logging service configuration token
│   │   │       └── jwt.ts                             # JWT configuration token
│   │   ├── enums/                                     # Enums used in the app module
│   │   │   └── enums-name.ts                          # Enumeration files for the app module
│   │   ├── interfaces/                                # Interfaces used in the app module
│   │   │   └── interface-name.ts                      # Interface declaration files for the app module
│   │   ├── layouts/                                   # Layouts used in the app module
│   │   │   └── name-layout/                           # A specific layout
│   │   │       ├── components/                        # Components specific to this layout
│   │   │       ├── name-layout-routing.module.ts      # Routing module for the layout
│   │   │       ├── name-layout.component.html         # HTML template for the layout
│   │   │       ├── name-layout.component.scss         # SCSS styles for the layout
│   │   │       ├── name-layout.component.ts           # Angular component for the layout
│   │   │       └── name-layout.module.ts              # Angular module for the layout
│   │   ├── models/                                    # Models specific to the app module
│   │   │   └── model-name.ts                          # Model declaration files for the app module
│   │   ├── services/                                  # Services specific to the app module
│   │   │   └── module-name.service.ts                 # Service files for the app module
│   │   ├── shared/                                    # Shared utilities, modules, data, pipes
│   │   │   ├── mocks/                                 # Mock data files
│   │   │   ├── modules/                               # Shared modules (e.g., icons, toasts, common components)
│   │   │   ├── pipes/                                 # Angular Pipes
│   │   │   └── utils/                                 # Utility files (e.g., helper functions, small services, config files)
│   │   ├── views/                                     # Pages as per modules
│   │   │   ├── pages/                                 # Page components grouped by modules
│   │   │   ├── name-routing.module.ts                 # Routing definitions for 'name' module
│   │   │   └── name.module.ts                         # Main module file for 'name' module
│   │   ├── app-routing.module.ts                      # Main routing definitions for the app
│   │   ├── app.component.html                         # Main HTML template for the app
│   │   ├── app.component.scss                         # SCSS styles for the main app component
│   │   ├── app.component.ts                           # TypeScript class for the main app component
│   │   └── app.module.ts                              # Main module for the app
│   ├── assets/                                        # All static assets
│   │   ├── fonts/                                     # Font files
│   │   ├── icons/                                     # Icon files
│   │   ├── images/                                    # Image files
│   │   └── styles/                                    # Global SCSS stylesheets
│   │       ├── base/                                  # Base styles such as resets, typography, etc.
│   │       ├── components/                            # Styles for specific components
│   │       ├── layouts/                               # Styles for specific layouts
│   │       ├── libs/                                  # Styles from external libraries or CSS plugins
│   │       ├── modules/                               # Styles for specific modules
│   │       ├── pages/                                 # Styles for specific pages
│   │       ├── utilities/                             # Utility and helper styles, variables, mixins, etc.
│   │       └── index.scss                             # Entry point file for SCSS, importing all other SCSS files
│   └── environments/                                  # Files for different environment variables
```

## Additional Documentation

You can refer to the following resources to better understand the libraries used:

- [Angular](https://angular.io/docs)
- [Husky](https://typicode.github.io/husky/#/)
- [Commitlint](https://commitlint.js.org/#/)
- [AutoChangelog](https://github.com/CookPete/auto-changelog)
- [Bootstrap](https://getbootstrap.com/docs/)
- [Mdbootstrap](https://mdbootstrap.com/docs/angular/)

## CSS Standards (SCSS with ABEM)

This project uses SCSS with the [ABEM](https://css-tricks.com/abem-useful-adaptation-bem/) methodology. Color variables should be named according to [Hexcol](https://hexcol.com/) standards.

## Commit Rules & Rebase Process

This project uses [Commitlint](https://commitlint.js.org/#/) to enforce a standard format for commit messages. Here are the basic rules:

- `build`: Changes that affect the build system or external dependencies.
- `chore`: Updates tasks unrelated to the application's source code or tests.
- `ci`: Changes to our CI configuration files and scripts.
- `docs`: Marks a commit that updates the documentation.
- `feat`: Marks a commit that adds a new feature to the application.
- `fix`: Marks a commit that fixes a bug in your code.
- `perf`: A code change that improves performance.
- `refactor`: Marks a commit that modifies the source code but neither fixes a bug nor adds a feature.
- `revert`: Reverts a previous commit.
- `style`: Marks a commit that does not affect the meaning of the code (whitespace, formatting, missing semi-colons, etc.)
- `test`: Marks a commit that adds or modifies tests.
- `translation`: Marks a commit that adds or updates translations.
- `security`: Marks a commit that improves application security.
- `changeset`: Marks a commit that brings several changes bundled together.

Rebase is a git process that allows you to modify and optimize your commit history. This is very useful when you want to keep your commit history clean and clear. Here is the basic rebase process:

1. Fetch the latest changes from the branch you want to rebase onto (usually `develop` or `stagging`): `git fetch origin develop`
2. Switch to the branch you want to rebase: `git checkout <your_branch>`
3. Start the rebase process: `git rebase origin/develop`
4. Resolve any conflicts that might arise during the rebase.
5. Once all conflicts have been resolved, continue the rebase process using: `git rebase --continue`
6. Push your changes to the remote branch, you might need to use the `--force` option: `git push origin <your_branch> --force`

## Contribution

Contributions to this project are welcomed. Please ensure to follow the guidelines when making a commit, husky and commitlint will ensure that all your commits follow the correct pattern. When making a pull request, make sure you have updated the Changelog accordingly.

## Docker Build and Run

**See-more:** <https://docs.docker.com/get-started/overview/>
