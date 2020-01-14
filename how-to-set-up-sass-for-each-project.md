# Set up SASS for your project

0. Create a project folder. Start with a basic `index.html` linked to an empty `style.css`.

1. Open this folder in your terminal, and run `$ npm init`. Keep hitting enter to accept all the defaults. This will create `package.json`.

2. From the same project directory, install SASS as a **dev dependency** by running `$ npm i -D dart-sass`

    - Open `package.json` and check that `dart-sass` appears under `"devDependencies"`.
    - If you're in a git repo, **make sure that node_modules is in your `.gitignore`**

3. Create a directory called `scss` and a file inside it called `style.scss`. Add some SASS or CSS code in there just to test. (Though later you should build out file structure for your SASS, instead of including styles directly in this file)

4. In `package.json`, add this new line (one line) in the `"scripts"` section (you'll also need a comma on the previous line to separate them):
```json
    "watch-css": "dart-sass --watch scss/style.scss style.css --style compressed"
```

5. In your terminal, run `$npm run watch-css` (note: that final argument needs to match the script we defined above).

    -  Check that your project folder now includes `style.css` and `style.css.map`. **We will not be editing these files directly.** They will be overwritten every time we update our `scss` files.

6. Open your site in a browser. With your compile script running in the background, Edit your `scss` and check that the changes are visible in the browser.

7. Now you can set up your file structure and start styling your project. Here's an example to use as a guide:

scss/
│   style.scss      (This file's one job is to import other files. Don't write styles in here.)
│
├── third-party/    (code you didn't write)
│   └── normalize.css (Feel free to rename it to _normalize.scss if you like. Both work)
│
├── variables/      (values you will use throughout your project)
│   ├── _color.scss
│   ├── _typography.scss
│   └── _sizing.scss
│
└── modules/        (small parts of your project)
    ├── _header.scss
    ├── _footer.scss
    └── _forms.scss
