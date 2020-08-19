# fastdocs

Automatically generated [Docsify](https://docsify.js.org/#/) flavored documentation sites for your markdown files! We are a README-as-a-Service project, spin up beautiful versions of your documentation in seconds! And the best part? We are completely free and open-source!

# Getting Started

## Compile your docs

To add your repo documentation to FastDocs, you would need to visit `/:user/:repo/compile` first. This allows us to store your `README.md` and add [Docsify](https://docsify.js.org/#/) to render it.

You need to visit this compile endpoint everytime you would like your fastdocs to be updated.

## View your docs

Once you have compiled your docs, you can view and share the pretty version of your docs at `/:user/:repo/`!

That's it, it's that simple and fast!

# Configuration

To add a `description` for SEO purposes, or to add plugins to your documentation, you need to create a `.fastdocs.json` file in the root of your repo.

_Example repo file structure_ :

```text
├── .fastdocs.json
├── build/
├── src/
└── README.md
```

## Config Schema

Once you have made the `.fastdocs.json` file, the currently supported options are:

```json
{
  "description": "Description",
  "plugins": [],
  "gaCode": ""
}
```

### description

The description of your project. Mainly for SEO purposes when docs are linked on platforms like facebook, twitter, linkedin, etc.

- type: string
- default: `"Description"`
- example usage: `"App that sends hello world every 2 seconds"`

### plugins

List of plugins you would like added to your docs. Supported plugins right now:

#### full-text-search

Adds a search bar on the top of the sidebar to quickly search docs.

#### docsify-copy-code

Adds a "Copy to Clipboard" next to code blocks.

#### google-analytics

Support for google analytics. Pass in the google analytics code to [gaCode](#gaCode)

#### emoji

Renders emoji's in your documentation. (Ex: `:100:` would render to :100:)

#### zoom-image

Adds subtle zooming to images cursor is hovering.

---

- type: string array
- default: `[""]`
- example usage: `["docsify-copy-code", "full-text-search"]`

### gaCode

Pass in your google analytics code if you have specified `google-analytics` in the plugins array. This field is optional and can be ignored if it does not apply to you.

- type: string
- default: `""`
- example usage: `"UA-GXXXY"`

# Contribution

Everyone is encouraged to contribute to this project, there are no restrictions other than following the `semantic-commit` conventions. If you want to contribute by reporting bugs, or suggesting new features you are welcome to do so on our [Issue Tracker](https://github.com/MLH-Fellowship/docsify-up/issues)