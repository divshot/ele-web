# Ele Web

This is the web client for [Ele](https://ele.io/). It's built using Polymer and
hosted on (and developed by) [Divshot](http://www.divshot.com/). Ele is an
in-browser editor for Web Components.

## Local Development

Ele is separated into two pieces: the static front-end web client (this repo)
and [ele-api](https://github.com/divshot/ele-api), the Node.js back-end. You'll
need both repositiories, Node.js, and MongoDB to get local development up and
running.

### Cloning

    mkdir ele && cd ele
    git clone https://github.com/divshot/ele-web.git
    git clone https://github.com/divshot/ele-api.git
    
### API Up and Running

You should follow the instructions in the [API README](https://github.com/divshot/ele-api)
to get it up and running. Once that's done, head back here to get the web client
properly set up.

### Running the Web Client

Divshot allows for client-side environment variables. To develop locally, you'll
need to create a `.env.json` file that looks like this:

```json
{
  "API_ORIGIN":"http://url.of.your.api.server"
}
```

Where `API_ORIGIN` is set to whatever host and port on which you're running the
Node.js API (for instance, `http://localhost:3000`).

Then you just need to install the bower components and you're up and running:

    bower install
    npm install -g divshot-cli
    divshot server -p 4000
    
That's it! You should now be able to visit `http://localhost:4000` and see the
Ele landing page.