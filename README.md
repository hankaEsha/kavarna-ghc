# A responsive multipage website of a fictional coffee shop based on a provided graphic design. 

Built on Bootstrap 5, using SASS and Nunjucks templates.


Includes these technologies and services:

-   **Bootstrap 5**
-   **Gulp 4**: task runner for running all of the following
-   **Sass compilation**: leverage the power of the most popular CSS extension language
-   **Sourcemaps** generation for easier Sass debugging
-   **Browsersync**: automatically reloads (or injects in case of CSS), browsers when you change files
-   **Autoprefixer**: parses CSS and adds vendor prefixes according to [caniuse.com]()
-   **UnCSS**: removes unused styles from CSS
-   **CSSO**: CSS minifier with structural optimizations
-   **Nunjucks**: templating language by Mozilla
-   **Vercel**: deploy static websites easily and for free

## Vercel deployment set up
- set up an account on https://vercel.com (if you do not have one)
**CLI**
- instal Vercel: npm i vercel 
- npm audit fix (if needed)
- npm run vercel
    * log in to Vercel
    * ? Set up and deploy > Y
    * ? Which scope do you want to deploy to? > your Vercel account (e.g. hankaesha)
    * ? Link to existing project? > N
    * ? What's your project's name? > choose one (ghc - for example, case sensitive!)
    * ? In which directory is your code located? > ./dist
    * Upload runs ... Default Project Settings:
        - Build Command: `npm run vercel-build` or `npm run build`
        - Output Directory: `public` if it exists, or `.`
        - Development Command: None
        - ? Want to override the settings? [y/N] > n
        - Set up finished (e.g.:
            - 🔗  Linked to hankaesha/ghc (created .vercel and added it to .gitignore)
            - 🔍  Inspect: https://vercel.com/hankaesha/ghc/S2vV8nZbqLssNxeGQJiN3XRZvrZu [2s]
            - ✅  Production: https://ghc-nine.vercel.app [copied to clipboard] [12s]
            - 📝  Deployed to production. Run `vercel --prod` to overwrite later (https://vercel.link/2F).
            - 💡  To change the domain or build command, go to https://vercel.com/hankaesha/ghc/settings)
- `npx vercel` (can be used for running the deployment) 
- BUT
- go to the file "package.json", find "scripts" and amend to read `"deploy": "gulp build && vercel && vercel --prod"`
- next time run deployment using `npm run deploy`

- setting up Vercel affects these three files:
    modified:   .gitignore
    modified:   package-lock.json
    modified:   package.json
    