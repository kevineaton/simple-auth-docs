# Simple Auth API Docs

Simple Auth is a stupidly simple authentication mechanism that was built to serve one very specific goal and flow. You can see the source code at the [Simple AUth Github Repo](https://github.com/kevineaton/simple-auth)

These docs were written according to the Open API Specification 3.

You can view the current docs at [https://docs.simpleauth.kevineaton.net/](https://docs.simpleauth.kevineaton.net/).

## Building

All of the documentation exists in the `docs` folder in YAML format. Checkout the repo, run `npm install`, and then you can use the following commands:

- `npm run lint`
  - Runs the `docs` folder through the linter
- `npm run combine`
  - Starting with the `docs/index.yaml` file, it combines all referenced YAML files into a single file
- `npm run preview`
  - Runs the `combine` command and serves a preview
  - NOTE: Requires a global installation of `serve` to be available
- `npm run generate`
  - Generates the API JSON file using the spec converter library
- `npm run build`
  - Runs `combine` and `generate` and then copies the resulting single file to the `build` directory

The output of the build will be an `api.json` file in the `/build` folder. It lives alongside a single `index.html` file, which uses a CDN copy of Redoc, parses the `api.json` file, and renders the output.
