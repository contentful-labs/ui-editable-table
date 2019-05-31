# Contentful Editable Table UI Extension

An editable table to handle tabular data as a [Contentful UI Extension](https://www.contentful.com/developers/docs/concepts/uiextensions/).

![figure](https://raw.githubusercontent.com/contentful-developer-relations/ui-editable-table/master/demo.gif "Editable table as Contentful UI Extension demo")

## Installation

```sh
git clone git@github.com:contentful-labs/ui-editable-table.git
cd ui-editable-table
npm install
```

### Configure

Create a configuration file with your credentials for Contentful.

```sh
cp .env.example .env
```

Open `.env` in a editor of your liking and add your Contentful space ID, and management token. [Learn how to obtain a token](https://www.contentful.com/developers/docs/references/authentication/#getting-an-oauth-token).

Load environment variables

```sh
source .env
```

Adjust the table configuration. Open `index.html`.

Update the `<title>` tag with the table name.
Update the `tableData` object with the desired table format.

```
  tableData : getInitialData({
    rows: 3,
    header: ['FOO', 'BAR', 'BAZ']
  })
```

### Create

```sh
npm run create
```

Create task will register the extension in your space on Contentful.

### Update

```sh
npm run update
```

Update task will upload the extension to your space on Contentful.

## License

Copyright &copy; Contentful Developer Relations

Licensed under the [MIT license](https://github.com/contentful-labs/ui-editable-table/blob/master/LICENSE).
