# Git project creation

```
Denis@DESKTOP-C9O29H2 MINGW64 /e/development-Web/svelte
$ git clone https://github.com/dvigouro/svelte-training.git
Cloning into 'svelte-training'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), 4.45 KiB | 1.11 MiB/s, done.
```

# Svelte template creation

```
Denis@DESKTOP-C9O29H2 MINGW64 /e/development-Web/svelte
$ cd svelte-training/

Denis@DESKTOP-C9O29H2 MINGW64 /e/development-Web/svelte/svelte-training (main)
$ npm create vite@latest .
√ Current directory is not empty. Remove existing files and continue? ... yes
√ Select a framework: » Svelte
√ Select a variant: » JavaScript

Scaffolding project in E:\development-Web\svelte\svelte-training...

Done. Now run:

npm install
npm run dev

$ npm install

added 26 packages, and audited 27 packages in 10s

5 packages are looking for funding
run `npm fund` for details

found 0 vulnerabilities
```

# Tailwindcss installation

```
Denis@DESKTOP-C9O29H2 MINGW64 /e/development-Web/svelte/svelte-training (main)
$ npm install -D tailwindcss@latest postcss@latest autoprefixer@latest

added 61 packages, and audited 88 packages in 16s

19 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

Denis@DESKTOP-C9O29H2 MINGW64 /e/development-Web/svelte/svelte-training (main)
$ npx tailwindcss init -p

Created Tailwind CSS config file: tailwind.config.cjs
Created PostCSS config file: postcss.config.cjs
```
