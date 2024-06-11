# AGE Fitness

click here to visit the live webpage👉👉 [https://pallabofficial.github.io/sun-studios/]<br><br>  


## About

TakeNote is a note-taking app for the web. You can use the demo app at [takenote.dev](https://takenote.dev). It is a static site without a database and does not sync your notes to the cloud. The notes are persisted temporarily in local storage, but you can download all notes in markdown format as a zip.

Hidden within the code is an alternate version that contain a Node/Express server and integration with GitHub. This version involves creating an OAuth application for GitHub and signing up to it with private repository permissions. Instead of backing up to local storage, your notes will back up to a private repository in your account called `takenote-data`. Due to the following reasons I'm choosing not to deploy or maintain this portion of the application:

- I do not want to maintain a free app with users alongside my career and other commitments
- I do not want to request private repository permissions from users
- I do not want to maintain an active server
- I do not want to worry about GitHub rate limiting from the server
- There is no way to batch create many files from the GitHub API, leading to a suboptimal GitHub storage solution

However, I'm leaving the code available so you can feel free to host your own TakeNote instance or study the code for learning purposes. I do not provide support or guidance for these purposes.

TakeNote was created with TypeScript, React, Redux, Node, Express, Codemirror, Webpack, Jest, Cypress, Feather Icons, ESLint, and Mousetrap, among other awesome open-source software.<br><br> 


## Features

- **Plain text notes** - take notes in an IDE-like environment that makes no assumptions
- **Markdown preview** - view rendered HTML
- **Linked notes** - use `{{uuid}}` syntax to link to notes within other notes
- **Syntax highlighting** - light and dark mode available (based on the beautiful [New Moon theme](https://taniarascia.github.io/new-moon/))
- **Keyboard shortcuts** - use the keyboard for all common tasks - creating notes and categories, toggling settings, and other options
- **Drag and drop** - drag a note or multiple notes to categories, favorites, or trash
- **Multi-cursor editing** - supports multiple cursors and other [Codemirror](https://codemirror.net/) options
- **Search notes** - easily search all notes, or notes within a category
- **Prettify notes** - use Prettier on the fly for your Markdown
- **No WYSIWYG** - made for developers, by developers
- **No database** - notes are only stored in the browser's local storage and are available for download and export to you alone
- **No tracking or analytics** - 'nuff said
- **GitHub integration** - self-hosted option is available for auto-syncing to a GitHub repository (not available in the demo)<br><br> 



## Tech Stack

- Next.js
- Three.js
- Framer Motion
- Tailwind CSS<br><br>




## Demo Development

Clone and install.

```bash
git clone git@github.com:taniarascia/takenote
cd takenote
npm i
```

Run a development server.

```bash
npm run client
```
<br><br> 


### Pre-Installation

Before working on TakeNote locally, you must create a GitHub OAuth app for development.

Go to your GitHub profile settings, and click on **Developer Settings**.

Click the **New OAuth App** button.

- **Application name**: TakeNote Development
- **Homepage URL**: `http://localhost:3000`
- **Authorization callback URL**: `http://localhost:3000/api/auth/callback`

Create a `.env` file in the root of the project, and add the app's client ID and secret. Remove `DEMO` variable to enable GitHub integration.

```bash
CLIENT_ID=xxx
CLIENT_SECRET=xxxx
DEMO=true
```

> Change the URLs to port `5000` in production mode or Docker.<br><br> 

### Installation

```bash
git clone git@github.com:taniarascia/takenote
cd takenote
npm i
```

#### Development mode

In the development environment, an Express server is running on port `5000` to handle all API calls, and a hot Webpack dev server is running on port `3000` for the React frontend. To run both of these servers concurrently, run the `dev` command.

```bash
npm run dev
```

Go to `localhost:3000` to view the app.

> API requests will be proxied to port `5000` automatically.<br><br> 

#### Production mode

In the production environment, the React app is built, and Express redirects all incoming requests to the `dist` directory on port `5000`.

```bash
npm run build && npm run start
```

Go to `localhost:5000` to view the app.<br><br> 


## Contributing

TakeNote is an open source project, and contributions of any kind are welcome and appreciated. Open issues, bugs, and feature requests are all listed on the [issues](https://github.com/taniarascia/takenote/issues) tab and labeled accordingly. Feel free to open bug tickets and make feature requests. Easy bugs and features will be tagged with the `good first issue` label.
<br><br> 


## Acknowledgements

- AI tools (chatGPT, Gemini)
- official documentations
- online free tutorials<br><br> 

## Author

- Pallab Mondal<br><br> 

## License

This project is open source.
