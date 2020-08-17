# Pureport Python Client

The Pureport Python Client provides a Python programmatic interface to the 
Pureport REST API.  The Pureport Python Client is predominately a session and 
transport library designed to making interfacing with the API simple.  For 
more information about Pureport or to sign up for an account please visit the
[website](http://www.pureport.com).

## Installing

You can install the Pureport Python Client using `pip`.

```
   $ pip install pureport-client
```

This project can be run directly from source as well using `pipenv`.  To 
get started with running this from source, be sure you have `pipenv` 
installed on your local system.  For information about `pipenv` please see 
their website [here](https://pipenv.pypa.io/en/latest/)

```
   $ git clone https://github.com/pureport/pureport-python
   $ cd pureport-python
   $ pipenv shell
   $ pipenv install -d
   $ python setup.py develop
```

### Supported Python Versions

The Pureport Python Client supports Python 3.5+

## Getting Started

In order to use this SDK, you must first have a valid Pureport acccount 
and have created and downloaded API keys.  Once you have obtained your
Pureport API keys, simply create environment variables for the API
key and API secret.

To get started, either sign up or login to your existing Pureport account at 
https://console.pureport.com and generate your API keys.

Once the keys are generated, set the required environment variables.


```
   export PUREPORT_API_KEY="<your api key here>"
   export PUREPORT_API_SECRET="<your api secret here>"
```

With the credentials set properly, you can using the Pureport Python
SDK to interact with the Pureport Fabric API.

```
   import pureport
   pureport.get("/accounts")
   <output omitted>
```

When consuming the Pureport Python Client in your own projects, the easiest
way to embed this library is to create a Session object as shown below.

```
   from pureport.session import Session
   from pureport.credentials import default

   session = Session(*default())
   response = session.get("/accounts")
   print(response.json)
```

For details and documentation of the Pureport Fabric API, please check 
the API section of the [Pureport Console](https://console.pureport.com)

## Contributing

This project provides an easy to use implementation for consuming the 
Pureport Fabric API for building and managing multicloud networks.  We 
gladly accept contributions to this project from open source community
contributors. 

There are many ways to contribute to this project from opening issues, 
providing documentation updates and, of course, providing code.  If you 
are considering contributing to this project, please review the 
guidlines for contributing to this project found [here](CONTRIBUTING.md).

Also please be sure to review our open source community Code of Conduct
found [here](CODE_OF_CONDUCT.md).

## License

This project is licenses under the MIT open source license.