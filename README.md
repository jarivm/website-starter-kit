# Website Starter Kit

[![Netlify Status](https://api.netlify.com/api/v1/badges/4927a76f-f3dc-4bba-8e3f-d402d668733d/deploy-status)](https://app.netlify.com/sites/vanmenxel-website-starter-kit/deploys)

Starter kit for custom websites, initiated and used by [Van Menxel Solutions](https://vanmenxel.nl). This starter kit uses static site generator [Zola](https://getzola.org), [Decap CMS](https://decapcms.org/) for the admin environment and [SCSS](https://sass-lang.com/documentation/syntax/) for CSS preprocessing.

## Running locally

Download repository and install dependencies.

```
git clone git@github.com:jarivm/website-starter-kit

npm i
```

Open `static/admin/config.yml` and look for the following section:

```yml
backend:
    name: git-gateway
    branch: main
```

Replace the above with:

```yml
backend:
    name: proxy
    proxy_url: http://localhost:8081/api/v1
    branch: main
```

Run.

```
npm start
```
