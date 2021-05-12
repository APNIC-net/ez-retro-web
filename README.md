# ez-retro-web

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

### Upload to bucket

To upload the static front-end to the Google Cloud Bucket, run:

```
$ gcloud config set project my-gcp-project
$ gsutil -h "Cache-Control:private, max-age=0" rsync -d -r ./dist gs://my-gcp-bucket
```

> All files will be uploaded with a "no cache" policy.
