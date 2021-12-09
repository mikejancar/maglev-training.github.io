# Maglev Training

## About

Here's the idea: create an open-source reference application. Have the application be something that is actually _usable_ and _useful_. Let it grow over time. Let it grow with our ideas, our features, our increase in knowledge, and with the introduction of new technology that we want to explore.

## The Application

The application will to support the ongoing learning required to be a software developer. It will be publicly accessible, in continual "beta", and break often. A more thorough description of the application functionality, and speculative future functionality will be in the documentation.

The user-facing portion of this application will help provide a way for software developers to learn new skills, stay up to date on technology, get some feedback on good resources and helpful tips, etc. from other developers.

The source-code for this application will be another layer of reference, and will feed back into the user-facing portion of the site.

## The Stack

Preference will be given to cloud native technolgies. By "cloud native" we mean that we will lean on technologies that make it easy to develop, deploy, test, software that can be run on cloud providers, but also with the possibility to run with on-prem installations of that same software. Kubernetes and containerized applications will be the default. While we may use some "pure cloud" services as an expedient, there should be a plan to make a locally managed version of the same technology eventually. For example, we will start with using Github authentication, but will eventually move to something like our own hosted Hydra for OIDC.

The _initial_ front-end will be a monolithic Angular application, but we will explore alternative UI tools in the future, with particular emphasis on a composite, micro-front-end using Web Components. While not discounting creating a native UI in the future (Android, iOS, Maui, etc.), initial work will be done with url-deployable HTML5 apps.

The services will be implemented using HTTP-based web APIs, and WebSockets, using whatever server-side tools feel the best suited to our goals. We will start with some in Node (Nest.js) as a BFF, in a mono-repo with our front-end using NX, and we will have .NET APIs, Sockets, and will use other technologies for backend services, including Go.

## The Guidance

Some principles we will work within:

1. Open Source
   - Everything we create will be open source using the Apache 2.0 license. Everything we create will be available in public repos. The only exception will be "secrets" needed for whatever hosting provider we are using, and other administrative scripts/code.
   - We will gladly accept pull requests.
2. Up-To-Date
   - We will do our best to stay as close to the most recent releases of all frameworks, libraries, and dependencies.
   - This will allow this to be a "canary" for more _important_ work the members will be doing outside of this project.
3. Documentation
   - Technical choices will be discussed in issues and pull requests.
   - This site will be used and continually updated to show the current thinking and implementation details.
   - The purpose of this documentation site is to be a reference on how to actually _do_ this kind of work, not just what is happening in the project.
