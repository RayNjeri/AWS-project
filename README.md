This repo is for the serverless backend API 
#### Steps

- [Set up the Serverless Framework]
- [Add Support for ES6/ES7 JavaScript]
- [Add a Create Note API]
- [Add a Get Note API]
- [Add a List All the Notes API]
- [Add an Update Note API]
- [Add a Delete Note API]


#### Usage

To use this repo locally you need to have the [Serverless framework](https://serverless.com) installed.

``` bash
$ npm install serverless -g
```

Clone this repo and install the NPM packages.

``` bash
$ git clone https://github.com/RayNjeri/AWS-project.git
$ npm install
```

Run a single API on local.

``` bash
$ serverless webpack invoke --function list --path event.json
```

Where, `event.json` contains the request event info and looks something like this.

``` json
{
  "requestContext": {
    "authorizer": {
      "claims": {
        "sub": "USER-SUB-1234"
      }
    }
  }
}
```

Finally, run this to deploy to your AWS account.

``` bash
$ serverless deploy
```