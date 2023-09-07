# How to make API requests with Axios and React JS.

## Technologies to be used.

▶️ React JS (v.18)

▶️ Vite JS

▶️ TypeScript

▶️ Axios

▶️ CSS vanilla (You can find the styles in the repository at the end of this post)

## [Creating the project](https://dev.to/franklin030601/how-to-make-api-requests-with-axios-and-react-js-5a07)

<code>npm init vite@latest

cd axios-react

npm install

code .
</code>


##  First steps

Inside the [src/App.tsx](src/App.tsx) file we delete everything and create a component that displays a hello world.


We create the folder src/components and inside we create 4 files:

[src/components/CreatePost.tsx](src/components/CreatePost.tsx)

[src/components/GetPost.tsx](src/components/GetPost.tsx)

[src/components/UpdatePost.tsx](src/components/UpdatePost.tsx)

[src/components/DeletePost.tsx](src/components/DeletePost.tsx)

## Creating a new instance of axios.

<code>npm install axios</code>

## [Let's create the src/api folder and create the client.ts file.](src/api/client.ts)


## [🕯️ Creating GET request.](src/App.tsx)

Then, we are going to create a new folder [src/utils](src/utils) where we will create several files, the first one is [getData.ts](src/utils/getData.ts).


## [🕯️ Creating POST request.](src/components/CreatePost.tsx)

Now we go to the [src/components/CreatePost.tsx](src/components/CreatePost.tsx) file and create a new component similar to the previous one.

Next, let's create a new file in src/utils named [createPost.ts](src/utils/createPost.ts).

Ready, we have our function to create a new post, now we are going to use it in [src/components/CreatePost.tsx](src/components/CreatePost.tsx).

We probably won't see anything, but remember to comment out the old component and place the new one, in [src/App.tsx](src/App.tsx).


## 🕯️ Creating PUT request.

First we will change the component in [src/App.tsx](src/App.tsx).

Then we go to [src/components/UpdatePost.tsx](src/components/UpdatePost.tsx) to create a new functional component that is the same as [GetPost.tsx](GetPost.tsx). since we need a list of existing posts in order to update any of them.

Then, we go to src/utils and create a new [updatePost.ts](src/utils/updatePost.ts) file.

Now we are going to use our function, in [src/components/UpdatePost.tsx](src/components/UpdatePost.tsx).

## 🕯️ Creating DELETE request.

First let's change the component in [src/App.tsx](src/App.tsx)

Then we need to create a new src/utils file named [deletePost.ts](src/utils/deletePost.ts) that inside will have an asynchronous function that will just return a promise resolving a boolean value to indicate if the post deletion was successful.

Now we are going to use this function in [src/components/DeletePost.tsx](src/components/DeletePost.tsx).

## 🕯️ Handling errors.

[src/utils/](src/utils/)


## I want to extend my heartfelt thanks to [Franklin Martinez](https://github.com/Franklin361/) for creating and maintaining this fantastic project.



# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
   parserOptions: {
    ecmaVersion: 'latest',
    sourceType: 'module',
    project: ['./tsconfig.json', './tsconfig.node.json'],
    tsconfigRootDir: __dirname,
   },
```

- Replace `plugin:@typescript-eslint/recommended` to `plugin:@typescript-eslint/recommended-type-checked` or `plugin:@typescript-eslint/strict-type-checked`
- Optionally add `plugin:@typescript-eslint/stylistic-type-checked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and add `plugin:react/recommended` & `plugin:react/jsx-runtime` to the `extends` list
