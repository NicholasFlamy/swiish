Firstly, thank you for considering contributing to Swiish. This started as a personal learning project to create something I wanted and needed and has grown into a project that I hope others will find useful.

Swiish is an open-source, self-hostable platform for digital business cards. My goal is to provide a professional, privacy-focused, and offline-tolerant solution for sharing your details while networking, both in person and digitally.

## (No) Code of Conduct

Generally follow the same minimal guidance as set forth by Devuan: <https://dev1galaxy.org/viewtopic.php?id=17>
I went ahead and put the following in the `CODE_OF_CONDUCT.md` file: <https://nocodeofconduct.com/>

## How Can I Contribute?

### Reporting Bugs

If you find a bug, please open an issue on GitHub. Include as much detail as possible:

* Use the template provided.
* A clear, descriptive title.
* Steps to reproduce the bug.
* What you expected to happen vs. what actually happened.
* Screenshots or screen recordings if applicable.
* Your environment (Browser, OS, Swiish version).

### Suggesting Features

We love ideas. If you have a feature request:

* Use the template provided.
* Check if the feature has already been suggested.
* Open an issue and describe the feature, why it's useful, and how it might work.

### Improving Documentation

Documentation is easily as important as code - and for the user more so. If you see a typo, a confusing section, or something missing in the README or other docs, feel free to submit an issue or fix it and submit a PR.

## Development Workflow

### Branching Strategy

We use a `develop` branch model to keep the `master` branch stable while allowing for continuous development.

1. **Master Branch**: Represents the latest stable, production-ready release.
2. **Develop Branch**: The main integration branch for development. All new features and bug fixes should target this branch.
3. **Feature Branches**: Create your feature or bugfix branch off the **`develop` branch**.
    * Naming convention: `feature/your-feature-name` or `fix/your-fix-name`.
4. **Pull Requests**: Submit your PR into the **`develop` branch**.
5. **Releases**: When we are ready for a new release, the `develop` branch is merged into `master` and tagged with a version number (e.g., `v0.5.0`).

### Conventional Commits

We use [Conventional Commits](https://www.conventionalcommits.org/) to keep our history clean and automate changelogs. Please format your commit messages as follows:

* `feat: add new theme support`
* `fix: resolve alignment issue on mobile`
* `docs: update contributing guidelines`
* `style: fix linting errors`
* `refactor: simplify card rendering logic`

You can also include a commit body with more details if needed - but don't feel obliged, just if it's helpful to 'future you' or others.

### Local Setup

1. Fork the repository.
2. Clone your fork: `git clone https://github.com/your-username/swiish.git`
3. Install dependencies: `npm install`
4. Set up your environment: `cp .env.example .env`
5. Run the development server: `npm run dev`

## Pull Request Process

1. Ensure your code follows the existing style.
2. Update the documentation if you're adding or changing features.
3. Make sure your PR title follows Conventional Commits.
4. Provide a clear description of the changes in the PR body.
5. Wait for a review.

## Coding Standards

* **Frontend**: We currently use a monolithic structure in [`src/App.js`](src/App.js). While we plan to modularize this in the future, please stick to the current pattern for now to maintain consistency.
* **Styling**: Use Tailwind CSS for all styling.
* **Backend**: Keep logic in [`server.js`](server.js) or appropriate modules if we start breaking it out.
* **Database**: Use migrations for any schema changes (`npm run migrate`).

## Future: Testing

We don't have a comprehensive test suite yet, but we're looking to add one. If you're interested in helping set up a testing framework (like Vitest or Jest), please open an issue to discuss!

---

Thank you for helping make Swiish better!
