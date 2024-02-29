## How to setup Tailwind CSS

Step 1 : Run the following command

```
npm install -D tailwindcss
npx tailwindcss init
```

Step 2 : Update taiwind.config.js file to include this line:

```
content:["*.html"]
```

Step 3 : create src/input.css to include:

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Step 4 : Run the following command

```
npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
```

Step 5 : include the src/output.css file to your html

Step 6 : Set Package.json in script add this :

```
"build" : "npx tailwindcss -i ./src/input.css -o ./src/output.css --watch"
```

Step 7 : Run this command to not run every time Step 5

```
npm run build
```

# Explain command

Step 5 : This command is use because this command watching ./src/input.css and also watch the file which was set in taiwind.config.js at content : and this will decide that which utility classes will compile which are used in watch file

### if we dont do this all then :

all the utility classes will shift in browser and it will increse the load time of the website
