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

Configure the application with the correct back-end:

```
src/feathers-client.js
```

To upload the static front-end to the Google Cloud Bucket, run the following
after having built the application:

```
$ gcloud config set project my-gcp-project
$ gsutil -h "Cache-Control:private, max-age=0" rsync -d -r ./dist gs://my-gcp-bucket
```

> All files will be uploaded with a "no cache" policy.
