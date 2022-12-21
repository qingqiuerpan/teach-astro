# Welcome to [Astro](https://astro.build)

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/withastro/astro/tree/latest/examples/basics)
[![Open with CodeSandbox](https://assets.codesandbox.io/github/button-edit-lime.svg)](https://codesandbox.io/s/github/withastro/astro/tree/latest/examples/basics)

> 🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

![basics](https://user-images.githubusercontent.com/4677417/186188965-73453154-fdec-4d6b-9c34-cb35c248ae5b.png)


## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```
/
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   └── Card.astro
│   ├── layouts/
│   │   └── Layout.astro
│   └── pages/
│       └── index.astro
└── package.json
```

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

Any static assets, like images, can be placed in the `public/` directory.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                | Action                                             |
| :--------------------- | :------------------------------------------------- |
| `npm install`          | Installs dependencies                              |
| `npm run dev`          | Starts local dev server at `localhost:3000`        |
| `npm run build`        | Build your production site to `./dist/`            |
| `npm run preview`      | Preview your build locally, before deploying       |
| `npm run astro ...`    | Run CLI commands like `astro add`, `astro preview` |
| `npm run astro --help` | Get help using the Astro CLI                       |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).

## Node 17.1.0
## 集成tailwind：pnpx astro add tailwind, 
会自动将配置写入astro.config.mjs，生成tailwind.config.cjs
# github上创建项目
- Your repositories- new一个代码库
- 上传代码，先clone git地址，然后add、commit
- 没有看到dist文件，修改gitignore之后再上传
- 点击settings-pages-static html Configure-Start commit, 可以看到会生成static.yml文件
- 点击Actions，可以看到一条操作记录 Create static.yml, 点击进去 deploy是部署过程，下面的链接就是访问地址了，但这个地址是404，因为默认是访问项目的index.html，但我们需要让它访问dist
- git pull ,把 static.yml拉到本地, 将jobs-deploy-steps-name: Upload artifact width 中 [path: '.'] 改成 [path: './dist']
- 再次点击deploy 下链接，页面可以访问了，但是样式没有出来, 因为css路径没有项目名
- 给astro.config.mjs defineConfig加上 base: "teach-astro",

