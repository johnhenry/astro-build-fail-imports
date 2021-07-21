Build fails when importing a javascript that is in the "./public" directory.

Note: this works properly on the dev server -- just not when building for production.

Note: importing CSS files in the same way does not cause a similar issue.

1. Init generic astro project
2. Run `npm install`
3. Add basic javascript file at /public/index.js
4. Add basic astro html file at /src/pages/indes.astro that references the above javascript file.
5. Run `npm run build`
6. Error! Build fails with message 'Error: file:///.../src/pages/index.astro: could not find "index.js"
   at file:///.../node_modules/astro/src/build.ts:140:25'
7. Run `npm start`
8. Visit http://localhost:3000/
9. Open console. Note the javascript file has bee pulled in to /src/pages/index.astro.
