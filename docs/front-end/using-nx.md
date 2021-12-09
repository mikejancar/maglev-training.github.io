# Using NX

This is an Angular 13.x app running in a (an?) Nx Workspace.

Read about Nx here: [https://nx.dev/](https://nx.dev/)

I'll post some links and videos/gifs of how to use this here.

Right now it has one app in the `apps` folder called `frontend`.

It has one library in the `libs` folder called `darkmode`.

## Using Nx

> TODO: Details Coming

## The Projects

### Applications

#### Frontend (`apps/frontend`)

This is an Angular 13 application. I've added support for [Tailwind](https://tailwindcss.com/) and added to the already existent support for es-lint the [Ngrx ES-Lint Plugin](https://ngrx.io/guide/eslint-plugin). I took the default recommendations.

Right now the `app.module.ts` has a reference to the store and the effects module. I'd like to have _zero_ branches defined directly on this state. We will use NGRX feature modules. Sample code coming.

### Libraries

#### DarkMode (`libs/darkmode`)

This is a library with (currently) a single Module (DarkModeModule) and a single service it exports (DarkModeService).

It provides an observable to watch if the user is using dark mode, and a `toggle()` method that let's the user decide if they want to use darkmode.

That functionality is exposed from the `app.component` in the Frontend with the handy toggle button in the upper-right corner. I'm not sure if we are going to allow that in the future, but I thought it would be cool to have it, and the library for reference.

This module is set up to be imported into the project from NPM from the `@maglev-training/darkmode` library, but I have not published it there yet (I will do a CI/CD set of actions for this, coming soon.) That means for right now you really can't do a full build of this, only run it in developer mode.

But that's pretty cool because NX takes care of that stuff for you. It resolves the path and all that until you are ready to publish, which, for me, is a super compelling reason to use NX - it makes creating libraries super easy, so you do it more.
