# Synthetic homepage for a WIP project

[![Deploy to Fastly](https://deploy.edgecompute.app/button)](https://deploy.edgecompute.app/deploy)

✨ **Spin up a temp homepage for a project you're working on.** ✨

This project returns a synthetic homepage for an app or site you haven't built yet, but have perhaps bought a domain for. Return some info about your project if you aren't ready to figure out hosting yet.

## How to use this project

* Sign into GitHub
* Sign into / up for [Fastly](https://www.fastly.com/signup/) and [grab an API key](https://docs.fastly.com/en/guides/using-api-tokens)
* Click the __Deploy to Fastly__ button in this repo
* The [Cloud Deploy](https://developer.fastly.com/learning/tools/cloud-deploy/) flow will walk you through cloning the repo and deploying it to a Fastly Compute service
* Edit the `/src/homepage.html` content to include your own details, let people know about your project or how to get in touch with you
* When you push to the main branch, the GitHub actions in the repo will use Fastly CLI to deploy your changes to the [Compute service](https://developer.fastly.com/learning/compute/)

### Optional:

* Set your domain to [point at your Fastly service](https://dev.to/fastly/point-a-domain-at-your-site-with-fastly-1khm)
* When your project is ready to publish at the domain, update your Fastly service origin or edge compute logic to show it!

[**Example deploy**](https://homepage.edgecompute.app/)

![Homepage preview](https://cdn.glitch.global/c60940d7-2acc-4570-9bdc-97168aa9d35b/homepage.png?v=1702921290416)

## Understanding the code

_This project is a remix of the default Fastly Compute starter kit._

This starter is intentionally lightweight, and requires no dependencies aside from the [`@fastly/js-compute`](https://www.npmjs.com/package/@fastly/js-compute) npm package. It will help you understand the basics of processing requests at the edge using Fastly. This starter includes implementations of common patterns explained in our [using Compute](https://developer.fastly.com/learning/compute/javascript/) and [VCL migration](https://developer.fastly.com/learning/compute/migrate/) guides.

The starter doesn't require the use of any backends. Once deployed, you will have a Fastly service running on Compute that can generate synthetic responses at the edge.

The template uses webpack to bundle `index.js` and its imports into a single JS file, `bin/index.js`, which is then wrapped into a `.wasm` file, `bin/index.wasm` using the `js-compute-runtime` CLI tool bundled with the `@fastly/js-compute` npm package, and bundled into a `.tar.gz` file ready for deployment to Compute.

**For more details about other starter kits for Compute, see the [Fastly developer hub](https://developer.fastly.com/solutions/starters)**
