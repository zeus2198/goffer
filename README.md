# Goffer
This is a file manager, with a beautiful and easy to use UI, that lets you segregate files based on categories and tags. The main segregation is done based on categories and you can add tags to each file. Then later on you can search based on either file name or tag. 

This app does not actually create a copy of file or move it to other location, this app just indexes the files.

This is just a mini-app that I made as a project for college.

## Demo
Video:
<div align="center">
<a href="https://www.youtube.com/watch?v=eTJQIwUQvhc"><img src="https://img.youtube.com/vi/eTJQIwUQvhc/0.jpg" alt="IMAGE ALT TEXT"></a>
</div>


## Features
- Simple and beautiful UI based on material design:
![Image](https://i.gyazo.com/a51602199c922349257d2cc72d07243a.png)

- Various UI related customization for adding new categories:
![Image](https://i.gyazo.com/9a5fd17679c74e558fdf5d401173dd4d.png)

- Beautiful file explorer for each category, with file typing(different icons for different types of files):
![Image](https://i.gyazo.com/774abe579d739ca3a8608a66f9423908.png)

- Search based on file name and tags with file typing:
![Image](https://i.gyazo.com/ef7fc5b06c50d107379b3ea70c28c5dc.png)

- Ability to add files by dragging and dropping them directly into the category.
- Ability to add tags to be associated with a file.

## Editing Source Code 
Clone the repo, then install using:
```
yarn
```
or
```
npm install
```
#### Building
Build for current platform:
````
yarn run build
````
Build for Windows:
```
yar run build_windows
```
Build for MacOS:
```
yar run build_mac
```
Build for Linux:
```
yar run build_linux
```

All the builds will be made in a folder named `build`.

#### Enabling developer tools console
Uncomment the following line from `main.js` file:
```
// mainWindow.webContents.openDevTools()
```
Do not forget to comment this line while building. 
#### Adding files to file type recognition used in file explorer and search result of app
Find the following lines and add the type of file you want in the array:
```
fileTypes = {
    'default': { icon: 'help', color: 'amber darken-3' },
    'doc': { icon: 'edit', color: 'blue' },
    'docx': { icon: 'edit', color: 'blue' },
    'xls': { icon: 'grid_on', color: 'green' },
    'xlsx': { icon: 'grid_on', color: 'green' },
    'pdf': { icon: 'picture_as_pdf', color: 'red' },
    'txt': { icon: 'short_text', color: 'grey lighten-3' },
    'jpg': { icon: 'image', color: 'deep-purple' },
    'jpeg': { icon: 'image', color: 'deep-purple' },
    'png': { icon: 'image', color: 'deep-purple' },
    'ppt': { icon: 'slideshow', color: 'pink' },
    'pptx': { icon: 'slideshow', color: 'pink' },
    'zip': { icon: 'library_books', color: 'deep-orange' },
    'rar': { icon: 'library_books', color: 'deep-orange' }
};
```
# Libraries used
- https://jquery.com/
- http://lesscss.org/
- https://materializecss.com/
- https://pouchdb.com/
- https://twitter.github.io/hogan.js/

# Todo
- Add filter and sorting option in search
- Add prebuilt script to compile the `.less` file into `.css` file and inject it into the build automatically. The prebuild script will also disable developer tools if it is enabled while building.
