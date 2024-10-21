## Electron and Hybrids framework boilerplate

This boilerplate was created to serve as a basis for creating webapps. It has integrated some technologies that will facilitate development, such as Electron, Vite, Hybrids, Bootstrap and Capacitor.

Each one will serve a function: Vite for packaging the application, Hybrids is a reactive framework that facilitates the creation of web components, Bootstrap for grid UI and components and Electron to generate native aplication.


### Running this example

To run this boilerplate you need `bun` or `node` installed. If you prefer to use `bun`, it will be much faster, so it is recommended!

To install dependencies `bun install` or `npm install`.
To run the provided example, you can use `bun electron-dev` or `npm electron-dev` command.
Don't forget that this project is html in nature, so you can run it in the web environment as well, so you can use the `bun dev` command to use the local server and see the application in your browser.

```bash
bun electron-dev
```

```bash
npm electron-dev
```

### Packaging and distribute native application

To create a executable and distribute the application, run:

```bash
bun electron-build
```

In linux this command will generate .deb and AppImage in electron/dist directory. In Windows will generate .exe application.

### Optional to create a mobile application

You can create a mobile application from this boilerplate, because the Capacitor lib is installed too. You first need to generate a build with `vite`, and then create the android project:

1. Generate the build:

```bash
bunx vite build
```

2. Add the android folder:

```bash
bunx cap add android
```

3. Open the project in Android Studio:

```bash
bunx cap open android
```

4. If there is a change in the build, just synchronize it with the android folder:

```bash
bunx cap sync
```

Now, you can execute this application in Android Studio, and send to mobile.
Capacitor can create applications for iOS as well, in which case you need to add an additional library for it. See Capacitor documentation for more details.
