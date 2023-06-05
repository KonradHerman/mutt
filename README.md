# Website using SvelteKit (V1.5.0) for Mutt Ad Agency Company
Resources:
- [Tailwind](https://tailwindcss.com/docs/grid-row)
- [Svelte]([https://](https://svelte.dev))

Commands
```
    npm i 
    npm run dev
```

Notes / Tips:
- ```+layout``` is the entry point where you can add things that are common to all pages
- ```+page``` is the root page, you can have ```+page``` files inside sub folders of src and it'll automatically make a route with the same name as the folder name. For example if you made ```/about/+page.svelte``` it would create a ```/about``` route automagically
- ```lang="postcss``` enables ```@apply``` for tailwind classes