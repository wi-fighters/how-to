# How to set up Autoprefixer with Post-CSS

1. In your project directory, run `$ npm i -D postcss-cli autoprefixer` (this installs two dev dependencies at once)

2. Add this to your package.json scripts: `"prefix": "postcss *.css --use autoprefixer -d build/"` (where `*.css` will match the files to use as inputs, and `build/` is the destination dir for the output stylesheet)

3. From your project directory, run `$ npm run prefix`. This should create the `build` directory if you didn't have one already.

4. Connect your new output file to your html (if you had an older non-prefixed version, replace it with the prefixed one)
