# Website using SvelteKit (V1.5.0) for Mutt Ad Agency Company
#### Resources:
- [Tailwind](https://tailwindcss.com/docs/grid-row)
- [Svelte]([https://](https://svelte.dev))

#### Scripts
Dev commands
```
    npm i 
    npm run dev
```

Build command for deployment
```
    npm run build
```
Svelte is a compiler and this creates a build in a directory.


#### Notes / Tips:
- ```+layout``` is the entry point where you can add things that are common to all pages. the ```<slot/>``` is where each page is injected. The ```<slot/>``` works the same way in ```snapSection.svelte```
- ```+page``` is the root page, you can have ```+page``` files inside sub folders of src and it'll automatically make a route with the same name as the folder name. For example if you made ```/about/+page.svelte``` it would create a ```/about``` route automagically
- ```lang="postcss``` enables ```@apply``` for tailwind classes
- If you don't add ```scoped``` to styles like ```<styles lang="postcss" scoped>``` all styles are global by default (I think).