

npm init -y


npm install -D tailwindcss postcss postcss-cli autoprefixer


npx tailwindcss init


in tailwind.config.js

```
module.exports = {
  purge: [
    './public/**/*.html',
    './src/**/*.{js,jsx,ts,tsx,vue}',
  ],
  mode: 'jit',
  theme: {
    extend: {},
  },
  plugins: [],
}

```


in postcss.config.js

module.exports = {
    plugins: {
      tailwindcss: {},
      autoprefixer: {},
    }
  }


in css/tailwind.css


add


```
@tailwind base;
@tailwind components;
@tailwind utilities;

```


then add scrip in package.json

  "scripts": {
    "tailwind": "postcss css/tailwind.css -o public/build/tailwind.css"
  },


  run the scrip  using
  
   npm run tailwind


import the stylesheet 'public/build/tailwind.css' in you html page 

