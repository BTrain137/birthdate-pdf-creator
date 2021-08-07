# Birthdate PDF Creator

[Original README](./docs/README.md)
Project forked from [url-to-pdf-api](https://github.com/alvarcarto/url-to-pdf-api)

#### Local development

First, clone the repository and cd into it.

* `cp .env.sample .env`
* Fill in the blanks in `.env`

* `npm install`
* `npm start` Start express server locally
* Server runs at http://localhost:9000 or what `$PORT` env defines

#### Local CURL Commands

```bash
curl -o ./html.pdf -XPOST -d'{"html": "<body>test</body>"}' -H"content-type: application/json" http://localhost:9000/api/render
```

```bash
curl -o ./google.pdf http://localhost:9000/api/render?url=http://google.com
```

#### Production CURL Commands

```bash
curl -o ./html.pdf -XPOST -d'{"html": "<body>test</body>"}' -H"content-type: application/json"  https://birthdate-pdf-creator.herokuapp.com/api/render
```

```bash
curl -o ./google.pdf https://birthdate-pdf-creator.herokuapp.com/api/render?url=http://google.com
```
