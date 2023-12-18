# Synthetic homepage for a WIP project

[![Deploy to Fastly](https://deploy.edgecompute.app/button)](https://deploy.edgecompute.app/deploy)

This project returns a synthetic homepage for a project or site you haven't built yet, but perhaps have bought a domain for.

**For more details about other starter kits for Compute, see the [Fastly developer hub](https://developer.fastly.com/solutions/starters)**

## Features

* Spin up a temp homepage for a project you've bought a domain for
* Pop in your own details so that people know how to find out about the project or get in touch
* Set your domain to [point at your Fastly service](https://dev.to/fastly/point-a-domain-at-your-site-with-fastly-1khm)
* When your project is ready to publish at the domain, update your Fastly service origin or edge compute logic to show it!

[**Example deploy**](https://homepage.edgecompute.app/)

![Homepage preview](https://cdn.glitch.global/c60940d7-2acc-4570-9bdc-97168aa9d35b/homepage.png?v=1702921290416)

## Understanding the code

_This project is a remix of the default Fastly Compute starter kit._

This starter is intentionally lightweight, and requires no dependencies aside from the [`@fastly/js-compute`](https://www.npmjs.com/package/@fastly/js-compute) npm package. It will help you understand the basics of processing requests at the edge using Fastly. This starter includes implementations of common patterns explained in our [using Compute](https://developer.fastly.com/learning/compute/javascript/) and [VCL migration](https://developer.fastly.com/learning/compute/migrate/) guides.

The starter doesn't require the use of any backends. Once deployed, you will have a Fastly service running on Compute that can generate synthetic responses at the edge.

The template uses webpack to bundle `index.js` and its imports into a single JS file, `bin/index.js`, which is then wrapped into a `.wasm` file, `bin/index.wasm` using the `js-compute-runtime` CLI tool bundled with the `@fastly/js-compute` npm package, and bundled into a `.tar.gz` file ready for deployment to Compute.
