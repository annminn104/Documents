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
