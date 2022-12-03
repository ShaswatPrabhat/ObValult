*  [[Vite]] targets 2 bottle necks in a traditional web development server
* Slow server start: [[Bundler]] based web server has to eagerly crawl and build the entire application before it can be served
* [[Vite]] divides the code into [[dependencies]] and source code
* [[dependencies]] do not often change
* [[Vite]] pre bundles these using [[esbuild]]
* the source code often contains rapidly changing code and often will need bundling - CSS, non plain JS etc
* [[Vite]] serves source code over native ESM - letting the browser take over part of rendering process
* [[Vite]] only needs to server code on demand from the browser
* in [[Vite]] hot module replacement [[HMR]] is done over native ESM hence only the effected files and the files which depend on it need to updated
* Hence [[HMR]] is much faster than [[Bundler]] based HMR where the full app needs to be rebundled
* [[Vite]] requires wayy less [[dependencies]] than a CRA or Vue-Cli based project
* 