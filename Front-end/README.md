# FRONT-END DOCUMENTS

## Roadmap 2024
- https://dev.to/dragosnedelcu/senior-frontend-developer-roadmap-2024-5-clear-steps-to-next-level-2m5c

## Angular

<details>
  <summary>Document template</summary>

# Documents Angular Template

This is a comprehensive Angular application which is designed to be scalable, maintainable and robust. The application follows a clear directory structure along with a set of predefined scripts for build, development, testing and formatting. This application has been enhanced with a range of libraries such as Husky, Commitlint, AutoChangelog, Bootstrap, and ng-bootstrap.

## Learn
**https://github.com/angular-vietnam/100-days-of-angular**

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

</details>

## Nextjs

<details>
 <summary>Learning</summary>

**Init Source**: https://dev.to/alexeagleson/how-to-build-scalable-architecture-for-your-nextjs-project-2pb7

**Docker Nextjs**: https://medium.com/geekculture/optimally-dockerizing-nextjs-application-and-lessons-learned-af1833e7da46

**Dockerfile and Docker-compose:** https://medium.com/@elifront/best-next-js-docker-compose-hot-reload-production-ready-docker-setup-28a9125ba1dc

**React-Query for Nextjs:** https://codevoweb.com/setup-react-query-in-nextjs-13-app-directory/#google_vignette

</details>

## Payments

**Stripe:** https://github.com/stripe-samples/accept-a-payment/tree/main/custom-payment-flow

## React

<details>
 <summary>Document template</summary>

# Example React Vite (Basic setup)

### Libraries, dependencies and tools

- Node v16.20.\* / Gallium
- React v18
- TypeScript
- React router dom v6.14
- React Helmet v6.1
- Axios v1.4
- React Redux
- Ant Design **Notes: `Depending on the project`**
- React Query (TanStack Query v3)
- Redux-toolkit
- React Hook Form
- Yup / Yup Resolvers
- Socket.io (Socket client)
- SCSS (sass)
- Storybook v7
- ESLint
- Hygen

### Files / Directories

| Path               | Purpose                                                            |
| ------------------ | ------------------------------------------------------------------ |
| /.storybook/       | contains Storybook config files                                    |
| /.eslintrc         | settings for `ESLint`                                              |
| /.hygen.js         | settings for `Hygen`                                               |
| /\_templates/      | contains scaffolding templates based on `Hygen`                    |
| /.vscode/          | settings for `Visual Studio Code` workspace                        |
| /package.json      | manifest file for Node.js projects                                 |
| /tsconfig.json     | settings for `TypeScript`                                          |
| /dist/             | contains production build codes                                    |
| /public/           | root folder that gets served up as our react app.                  |
| /src/@types/       | contains global interfaces, enums, contains                        |
| /src/components/   | contains Atomic Design components                                  |
| /src/containers/   | contains containers / layout                                       |
| /src/pages/        | contains pages                                                     |
| /src/assets/       | contains images, icons, fonts, videos                              |
| /src/stores/       | contains shared stores                                             |
| /src/services/     | contains shared services                                           |
| /src/styles/       | contains common styles: breakpoints, colors, font, mixin, function |
| /src/utils/        | contains common utils: utils, helper, contains, enums              |
| /src/index.tsx/    | contains root file                                                 |
| /src/App.tsx       | contains application page index                                    |
| /src/vite-env.d.ts | contains shared types                                              |

---

### Source Tree

```shell
.
├── _templates/                               # Hygen templates
│   ├── components/                           # Generates new components
│   ├── containers/                           # Generates new containers
│   └── pages/                                # Generates new pages
├── .storybook/                               # Storybook configuration
├── public/                                   # Static files
├── src/                                      # Main application source code
│   ├── assets/                               # Static resources
│   │   ├── fonts/
│   │   ├── icons/
│   │   └── images/
│   ├── @types/                               # @Types define enums, interfaces, contains
│   │   ├── contains/
│   │   ├── enums/
│   │   └── interfaces/
│   ├── components/                           # Reusable components
│   │   ├── atoms/                            # Atomic components
│   │   │   ├── [ComponentName]/
│   │   │   │   ├── index.scss
│   │   │   │   ├── index.stories.tsx
│   │   │   │   └── index.tsx
│   │   │   └── more.../
│   │   ├── molecules/                        # Molecule components
│   │   ├── organisms/                        # Organism components
│   │   ├── templates/                        # Templates components
│   │   └── types.d.ts                        # Component TypeScript definitions
│   ├── containers/                           # Stateful components / containers layout
│   │   ├── [NameLayout]/
│   │   │   │   ├── index.scss
│   │   │   │   └── index.tsx
│   │   │   └── more.../
│   ├── hooks/                                # Custom React hooks
│   │   ├── store.ts
│   │   ├── use[HookName].tsx
│   │   └── .../
│   ├── pages/                                # Application pages (if using a page-based architecture)
│   │   ├── [NamePage]/
│   │   │   │   ├── index.scss
│   │   │   │   └── index.tsx
│   │   │   └── more.../
│   ├── routes/                               # Routing related files
│   │   ├── app.route.tsx
│   │   ├── protected.guard.tsx
│   │   ├── protected.routing.tsx
│   │   ├── rejected.guard.tsx
│   │   └── rejected.routing.tsx
│   ├── services/                             # Services, e.g., API call
│   │   ├── [module-name]/
│   │   │   │   ├── [module-name].service.ts
│   │   │   │   ├── [useModuleNameQuery].ts
│   │   │   │   └── type.d.ts
│   │   ├── common/                           # Common services such as API service and interceptors
│   │   │   │   ├── api.service.ts
│   │   │   │   ├── request.interceptor.ts
│   │   │   │   ├── response.interceptor.ts
│   │   │   │   └── type.d.ts
│   │   │   └──type.d.ts
│   ├── socket/                               # Socket related files (if used)
│   ├── stores/                               # Directory containing data stores (if using a state management architecture)
│   │   ├── [moduleName].slice.ts
│   │   └── index.ts
│   ├── styles/                               # Global styles
│   ├── utils/                                # Utils/helper/contains/enums functions
│   ├── App.tsx                               # Main application component
│   ├── main.tsx                              # Application entry point
│   └── vite-env.d.tsx                        # Vite environment TypeScript definitions
```

### Command Line

| Path                 | Purpose                           |
| -------------------- | --------------------------------- |
| yarn dev             | start the project                 |
| yarn build           | build the project                 |
| gen:component        | generate new `atomic` component   |
| gen:page             | generate new page                 |
| gen:container        | generate new container            |
| yarn storybook       | run the storybook                 |
| yarn build-storybook | build the storybook               |
| yarn lint            | run `Eslint` to check the syntax  |
| yarn prettier        | check format code with `prettier` |
| yarn prettier:fix    | run format code with `prettier`   |

---

### `Abem`

<https://css-tricks.com/abem-useful-adaptation-bem/>

**Note: Use only the `lowercase` format for `className`.**

```tsx
//GOOD 🏆🏆🏆
export const Sample: React.FC = ({ children }) => <div className='a-sample'>{children}</div>;

//NOT GOOD 💩💩💩
export const Sample: React.FC = ({ children }) => <div className='a-Sample'>{children}</div>;
```

**Note: Use only the `Single_Underscore(_) && Single-Dash(-)` format for `className`.**

```tsx
//GOOD 🏆🏆🏆
export const Sample = () => (
  <div className='a-sample'>
    <span className='a-sample_title'>Title</span>
  </div>
);

//NOT GOOD 💩💩💩
export const Sample = () => (
  <div className='a--sample'>
    <span className='a--sample__title'>Title</span>
  </div>
);
```

**Note: The `className` must be formatted as `block_element-modifier`. But `Sometimes` it will be formatted as `block_element_element-modifier`.**

```tsx
//GOOD 🏆🏆🏆
export const Sample = () => (
  <div className='a-sample'>
    <span className='a-sample_element'>One Element</span>
  </div>
);

export const Sample = () => (
  <div className='a-sample'>
    <span className='a-sample_element1_element2'>Two elements</span>
  </div>
);

//NOT GOOD 💩💩💩
export const Sample = () => (
  <div className='a-sample'>
    <span className='a-sample_element1_element2_element3'>Greater than 2 elements</span>
  </div>
);
```

### `Atomic`

<https://bradfrost.com/blog/post/atomic-web-design/>

### `Components`

- Use only `React-Hook`
- Follow the `rules of hook` (<https://reactjs.org/docs/hooks-rules.html>)

### `Custom Hooks`

- Example: <https://usehooks-ts.com/introduction>

**Note: Use `ModifierUtils` to generate `modifiers` `className`.**

```tsx
export const Component: React.FC<Props> = (props) => (
  <div className={ModifierUtils.map('a-sample', props.modifiers)}>{props.children}</div>
);
```

**Note: Use `// eslint-disable-next-line react-hooks/exhaustive-deps` when you want to avoid checking of the `useEffect` syntax (also on `useMemo & useCallback`)**

```tsx
  useEffect(() => {
    Todo Something...
  // eslint-disable-next-line react-hooks/exhaustive-deps
  }, []);
```

**Note: Use simple syntax when the component has no properties.**

```tsx
//GOOD 🏆🏆🏆
export const Component = () => <div>Without children...</div>;

export const Component: React.FC = ({ children }) => <div>{children}</div>;

//NOT GOOD 💩💩💩
export const Component: React.FC = () => <div>Without children...</div>;
```

**Note: Clearly define the data type of the property.**

```tsx
//GOOD 🏆🏆🏆
interface Props {
  title: string;
}

//NOT GOOD 💩💩💩
interface Props {
  title: any;
}
```

**Note: Please leave TODO when you encounter some unresolved issues immediately.**

```tsx
export const Component = () => {
  // TODO: bla...bla...bla
  const Problems = 'Problems';

  return <div>Todo Something...</div>;
};
```

**Note: Use the filename as the component name. For example, Example.tsx should have a reference name of Example. However, for root components of a directory, use index.jsx as the filename and use the directory name as the component name:**

```tsx
//GOOD 🏆🏆🏆
import Example from 'components/atoms/Example';

//NOT GOOD 💩💩💩
import Example from 'components/atoms/Example/index';
```

### `CSS/SCSS`

**Note: Instead of using `Color Variables`, do `NOT` use `Color Codes`. If the color code has not been defined. Please leave `TODO` about that.**

```css
.a-sample {
  // TODO: Replace with color variable
  color: rgb(0, 0, 0);
}
```

**Note: Instead of using `Color Variable` defined at `styles/colors.scss` and you can get name of color at <https://hexcol.com/> , do `NOT` use `Color Names | Color Hexs | ...`.**

```css
/* GOOD 🏆🏆🏆*/
.a-sample {
  // TODO: Replace with color variable
  color: $black;
}

/* NOT GOOD 💩💩💩 */
.a-sample {
  // TODO: Replace with color variable
  color: black; /* stylelint-disable-line color-named */
}
```

**Note: Please Use `font-family: $font-family-variable`, not Use `font-family: 'Font Name'` .**

```css
/* GOOD 🏆🏆🏆*/
.a-sample {
  // TODO: Replace with font-family variable
  font-family: $anotherFont;
}

/* NOT GOOD 💩💩💩 */
.a-sample {
  font-family: 'AnotherFont';
}
```

**Note: Please use `@function rem` with the properties have dynamic values (Scale-up and Scale-down). rem($SizeOnDesign)**

```css
/* GOOD 🏆🏆🏆*/
.a-sample {
  border-radius: 4px;
  font-size: rem(16);
}

/* NOT GOOD 💩💩💩 */
.a-sample {
  border-radius: 4px;
  font-size: 16px;
}
```

**Note: Instead of using `z-index: $variables`, do `NOT` use `z-index value`. Please define the `zIndex variable` before using that function. Please follow the instructions at `styles/variables.scss`**

```css
/* GOOD 🏆🏆🏆*/
.a-sample {
  z-index: $z-sample;
}

/* NOT GOOD 💩💩💩 */
.a-sample {
  z-index: 4;
}
```

### `React Hook Form + Yup Resolvers`

`Set controlId with Form Control`

```tsx
<div className='c-module'>
  <Form onSubmit={handleSubmit(onSubmit)}>
    <Form.Group controlId='c-module_input-fieldName'>
      <Form.Label>fieldName</Form.Label>
      <Form.Control type='text' {...register('fieldName')} placeholder='...' />
    </Form.Group>
  </Form>
</div>
```

### `Storybook`

**Note: Make sure that you have included all instances of the component in the storybook when building it.**

### `Typescript`

**See more:**

- <https://www.typescriptlang.org/docs/>

- <https://www.typescriptlang.org/docs/handbook/utility-types.html>

### `Redux`

**See more:**

- redux: <https://redux.js.org/>
- redux-toolkit: <https://redux-toolkit.js.org/>
- react-redux: <https://react-redux.js.org/>

### `React-router-dom`

**See more: <https://reactrouter.com/en/main>**

### `Naming`

**1. Service:** `[moduleName].service.ts`

```ts
export const moduleNameService = {
  crud: async (args): Promise<unknown> => {
    const res = await ....
    return res.data;
  };
  // or
  method[Module][Action]: async (): Promise<unknown> => {
    const res = await ....
    return res.data;
  };
}
```

**2. Interfaces, Enum, Types, Contains:** `types.d.ts`

```ts
// IUser, IProfile, ILoginRequest, ILoginResponse

interface I[Module][Action][Request]{}

interface I[Module]Item {}

interface I[Module][Action][Response] extends IPaginationResponse<I[Module]Item[]> {
}

// enum naming UPPER_SNAKE_CASE
enum USER_STATUS {
  ACTIVE = 'ACTIVE',
  INACTIVE = 'INACTIVE',
  SUSPENDED = 'SUSPENDED',
}

// Type Aliases PascalCase
type Color = 'A' | 'B'

// used for contains which is considered as mock data or default value `UPPER_SNAKE_CASE`
const MAX_LOGIN_ATTEMPTS = 3
```

**3. Stores:**

- Reducer: `[moduleName][Reducer]`
- Action: `[actionName][Action]`
- Action Prefix: `[moduleName][Reducer]/[actionName][Action]`
- Slice: `[moduleName][Slice]`

```ts
export const getExampleAction = createAsyncThunk<IExampleResponse>(
  'exampleReducer/getExampleAction',
  async (_, { rejectWithValue }) => {
    // ...
  }
);

export const exampleSlice = createSlice({
  // ...
});
```

**4. Handy Naming Conventions for Event Handler Functions, variables & Props in React:**

`Naming your functions, variables`

- **Convention**

  - handleEvent // function
  - isVariables, hasVariables, shouldVariables // boolean
  - camelCaseExample // variables

- **Example**
  - handleEvent
  - isLoggedIn, hasAdminAccess
  - camelCaseExample

`Naming your props`

- **Convention**
  - onEvent
  - isVariables, hasVariables, shouldVariables
  - camelCaseExample

```tsx
<SomeComponent onEvent={handleEvent} isChecked={isChecked} textExample={textExample} />
```

**5. Colors:** <https://hexcol.com/> Enter code => Get `color_name`

**6. Break the UI into a Hierarchy Component:**

![image](./public/HierarchyComponent.png)

You'll see in the image above that we have five components in our app. We've listed the data each component represents.

- `TweetSearchResults (orange):` container for the full component
- `SearchBar (blue):` user input for what to search for
- `TweetList (green):` displays and filters tweets based on user input
- `TweetCategory (turquoise):` displays a heading for each category
- `TweetRow (red):` displays a row for each tweet

Now that the components in the mock have been identified, the next thing to do would be to sort them into a hierarchy. Components that are found within another component in the mock should appear as a child in the hierarchy. Like this:

```shell
├── TweetSearchResults        # Call API
│   ├── SearchBar             # Event Search/Filter
│   ├── TweetList             # Render List/Table
│   │   ├── TweetCategory
│   │   └── TweetRow
```

### `Git`

- Rebase: <https://git-scm.com/docs/git-rebase>
- Git branch format: <http://karma-runner.github.io/5.0/dev/git-commit-msg.html>

**Note: When create a new branch. The `type` will include `feature | bugfix | hotfix | release | support`**

```ssh
  git checkout -b type/feature-name
```

**Note: When committed. The `type` will include `build | chore | ci | docs | feat | fix | perf | refactor | revert | style | test`**

```ssh
  git commit -m 'type(:emoji: | feature-name): messages'
```

**The type must be one of the following:**

| Type         | Emoji                    | Description                                                                                                 |
| ------------ | ------------------------ | ----------------------------------------------------------------------------------------------------------- |
| **build**    | 📦 :package:             | Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)         |
| **chore**    |                          | Updating grunt tasks etc.; no production code change                                                        |
| **ci**       | 👷 :construction_worker: | Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs) |
| **docs**     | 📚 :books:               | Documentation only changes                                                                                  |
| **feat**     | ✨ :sparkles:            | A new feature                                                                                               |
| **fix**      | 🐛 :bug:                 | A bug fix                                                                                                   |
| **perf**     | 🐎 :racehorse:           | A code change that improves performance                                                                     |
| **refactor** | 🔨 :hammer:              | A code change that neither fixes a bug nor adds a feature                                                   |
| **revert**   |                          |                                                                                                             |
| **style**    | 💄 :lipstick:            | Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)      |
| **test**     | 🚨 :rotating_light:      | Adding missing tests or correcting existing tests                                                           |
| **draft**    | 🚧 :construction:        | Work In Progress                                                                                            |

**Emoji** <https://gist.github.com/parmentf/035de27d6ed1dce0b36a>

### Generate Template

- Generate component: `yarn gen:component → select level → enter component's name`
- Generate page: `yarn gen:page → enter page's name`
- Generate container: `yarn gen:container → enter container's name`

## Rebase Process

### Why Rebase?

- It's an alternative to merge, but approached differently.
- Helps resolve conflicts.
- Pulls the latest code from the main branch.

### Why choose rebase over merge?

- Merging resolves all conflicts in a single commit, which may complicate conflict resolution.
- Rebasing addresses conflicts at the exact commit that introduced them, making it easier to handle them.
- If conflicts arise during rebase, you can always checkout and rewrite the commit from scratch based on the commit message.
- Merging makes the secondary branch's code the primary, risking overwriting. Rebasing takes the main branch's code as the primary.
- Rebasing results in a cleaner and more intuitive git tree.
- Rebase is also helpful for other management tasks.

### When should you rebase?

- Rebase when you want to get the code from the develop branch to your own branch.
- Conflicts should be resolved with rebase.
- Regularly rebase (when new commits are added to develop) and always rebase before creating a pull request. This prevents complications from rebasing multiple commits.

### Rebase Procedure

**1.** get the latest code from the remote and rebase on the main branch

> `git fetch` -> `git rebase origin/develop`

**2.** handle conflict if any

> In the worst case, checkout the conflicted file and re-code it according to the old commit, rebase on the branch with only 1 person coding at the same time, it will be simple, but if 2 people code at the same time, it will add more cases to handle , but according to git-flow, I have limited the case of 1 branch with many people coding at the same time

**3.** need to check the current code carefully after rebase, make sure it is equivalent to the old code, no errors, ...

**4.** run the following command to officially override your code on remote `git push --force-with-lease` or `git push -f`

### Hotfix procedure

**1.** When will hotfix be needed

> When you urgently need to fix 'fatal errors', it is not possible to merge the development branch into the production branch.

> Can be used to develop a folding feature for production, `but should not be abused`

**2.** Implementation steps

> Hotfix branch must be forked from production branch (will be different for each project), branch name is hotfix/`branch-name`

> Create 2 PRs from 1 hotfix branch into production and develop again, must merge into production first

> The next steps must be performed in the following order:

> - Handling conflicts of PR in production (if any)

> - Merge PR into production, but don't delete branch

> - Handle conflict of PR in development (if any)

> - Merge PR into development, tick the box to delete branch

### Branching procedure

- All branches are forked from the main branch `develop`
- In case the sub-branch has more sub-branches, then checkout from the sub-branch, do and merge into the sub-branch. Then merge the sub branch into the main branch `develop`


</details>

<details>
 <summary>Learning</summary>

**React Query**: https://medium.com/@kvs.sankar23/react-query-is-the-best-thing-that-happened-to-react-abd92553e953

**React AuthGuard**: https://romik-mk.medium.com/authguard-react-router-v6-764f049e172d

**React Table + Chakra**: https://codesandbox.io/p/sandbox/react-table-chakra-ui-pagination-example-fxx0v?file=%2Fsrc%2FApp.js%3A77%2C18-77%2C31

**Next React Table + Chakra**: https://codesandbox.io/s/chakra-ui-react-table-nextjs-lxvru

**Theme**: https://github.com/creativetimofficial/material-dashboard-react

- https://medium.com/bitsrc/clean-frontend-architecture-2995c68702fb

- https://dev.to/react-admin/documentation-the-key-enabler-for-open-source-success-3d4bn

</details>

## Deploy
<details>
  <summary>Nextjs + nginx</summary>

# How to setup next.js app on nginx with letsencrypt
> next.js, nginx, reverse-proxy, ssl

### 1. Install nginx and letsencrypt
```bash
$ sudo apt-get update
$ sudo apt-get install nginx letsencrypt
```
#### Also enable nginx in ufw
```bash
# after installing nginx!
$ sudo ufw allow 'Nginx Full'
```

### 2. Edit our default nginx site file
```bash
$ sudo vim /etc/nginx/sites-available/default
```
##### Content
```
# *q is our domain
server {
  listen 80 default_server;
  listen [::]:80 default_server;

  root /var/www/html;
  index index.html index.htm index.nginx-debian.html;

  server_name q*;

  location / {
    try_files $uri $uri/ =404;
  }
  
  # for letsencrypt
  location ~ /.well-known {
    allow all;
  }
}
```
#### Restart nginx
```bash
$ sudo nginx -t # check syntax errors
$ sudo systemctl restart nginx
```

### 3. Setup letsencrypt
```bash
# *q is our domain
$ sudo letsencrypt certonly -a webroot --webroot-path=/var/www/html -d *q -d www.q*
```

#### Generate Strong DH Group
```bash
$ sudo openssl dhparam -dsaparam -out /etc/ssl/certs/dhparam.pem 2048
```

#### Create nginx config file with Strong Encryption Settings
```bash
$ sudo vim /etc/nginx/snippets/ssl-params.conf
```
##### Content
```
ssl_protocols TLSv1.3; 
ssl_prefer_server_ciphers on;
ssl_ciphers "EECDH+AESGCM:EDH+AESGCM:AES256+EECDH:AES256+EDH";
ssl_ecdh_curve secp384r1;
ssl_session_cache shared:SSL:10m;
ssl_session_tickets off;
ssl_stapling on;
ssl_stapling_verify on;

resolver 8.8.8.8 8.8.4.4 valid=300s;
resolver_timeout 5s;

add_header Strict-Transport-Security "max-age=63072000; includeSubdomains";
add_header X-Frame-Options DENY;
add_header X-Content-Type-Options nosniff;

ssl_dhparam /etc/ssl/certs/dhparam.pem;
```

#### Edit our nginx file
```
# *q is our domain

# redirect http to https
server {
  listen 80 default_server;
  listen [::]:80 default_server;
  server_name *q www.*q;
  return 301 https://$server_name$request_uri;
}

server {
  # listen on *:443 -> ssl; instead of *:80
  listen 443 ssl http2 default_server;
  listen [::]:443 ssl http2 default_server;

  server_name q*;
  
  ssl_certificate /etc/letsencrypt/live/example.com/fullchain.pem;
  ssl_certificate_key /etc/letsencrypt/live/example.com/privkey.pem;
  include snippets/ssl-params.conf;

  location / {
    # reverse proxy for next server
    proxy_pass http://localhost:3000;
    proxy_http_version 1.1;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection 'upgrade';
    proxy_set_header Host $host;
    proxy_cache_bypass $http_upgrade;
  
    # we need to remove this 404 handling
    # because next's _next folder and own handling
    # try_files $uri $uri/ =404;
  }
  
  location ~ /.well-known {
    allow all;
  }
}
```

#### Restart nginx again
```bash
$ sudo systemctl restart nginx
```

### 4. Setup next.js app
```bash
$ yarn build # build our app for production (npm build script: next build)
$ yarn global add pm2 # install pm2 to keep next app alive forever*

# run start/stop
$ pm2 start npm --name "next" -- start # start next app (npm start script: next start)
$ pm2 stop next # for stopping app
```

# We are done
Now you have next.js app up and running on nginx reverse proxy with ssl!


```shell
server {
  server_name   <domain_name>;

  location / {
    proxy_pass             http://127.0.0.1:<PORT>;
    proxy_read_timeout     60;
    proxy_connect_timeout  60;
    proxy_redirect         off;

    # Allow the use of websockets
    proxy_http_version 1.1;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection 'upgrade';
    proxy_set_header Host $host;
    proxy_cache_bypass $http_upgrade;
  }
  
  location /_next/static {
        add_header Cache-Control "public, max-age=3600, immutable";
        proxy_pass http://127.0.0.1:<PORT>/_next/static;
  }

}
```

</details>

## More

<details>
 <summary>Tricks and tips</summary>

# TRICKS & TIPS

### Front-end
- `Pattern:` https://demo.patternlab.io/?p=all

- `BEM cheat-sheet:` https://bem-cheat-sheet.9elements.com

- `Front-end Resources:` https://dev.to/aycanogut/front-end-resources-1jk2

### AI Tools:
- `Design:` https://ideogram.ai/login - https://www.recraft.ai

### Useful
- `Web-code:` https://webcode.tools
- `Layout:` https://layout.bradwoods.io
- `Button, loading, input..:` https://uiverse.io
- `Border-radius Blob:` https://app.haikei.app
- `Loading-spiner:` https://10015.io/tools/css-loader-generator
- `Animations:` https://animista.net - https://www.transition.style
- `CSS Grid:` https://cssgrid-generator.netlify.app
- `Glassmorphism:` https://hype4.academy/tools/glassmorphism-generator
- `Generate CORS:` https://cors.sh

### Libs
- `Carousel (Slides):` https://splidejs.com - https://swiperjs.com

### Assests
- `Illustration:` https://storyset.com 
- `Icons:` https://iconbuddy.app - https://unicornicons.com
- `Design UI:` https://hype4.academy - https://pixcap.com

### Styled-component
- `selector`: https://viblo.asia/p/huong-dan-styled-components-co-ban-V3m5WRgwlO7

### FCM firebase
- FCM: https://viblo.asia/p/reactjs-push-notification-su-dung-firebase-cloud-messaging-yZjJYE9XJOE

### Trick lỏ tiếng ba tư RTL
- https://codepen.io/2undercover/pen/jOYRgM

### Front-end community 
- https://github.com/webuild-community/advent-of-sharing

</details>
