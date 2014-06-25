# Ele Web

This is the web client for [Ele](https://ele.io/). It's built using Polymer.

## Local Development

You'll need to create a `.env.json` file that looks like this:

```json
{
  "API_ORIGIN":"http://url.of.your.api.server"
}
```

Then you just need to install the bower components and you're up and running:

    bower install
    npm install -g divshot-cli
    divshot server -p 4000