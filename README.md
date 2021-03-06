# nfvo-client
NFVO module service for the NI project.

This Python package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Package version: 1.0.0
- Build package: io.swagger.codegen.languages.PythonClientCodegen

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage
### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install git+https://github.com//.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com//.git`)

Then import the package:
```python
import nfvo_client 
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import nfvo_client
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python
from __future__ import print_function
import time
import nfvo_client
from nfvo_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = nfvo_client.RouteApi(nfvo_client.ApiClient(configuration))
id = 'id_example' # str | route id

try:
    # Delete a Route.
    api_instance.del_route(id)
except ApiException as e:
    print("Exception when calling RouteApi->del_route: %s\n" % e)

```

## Documentation for API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*RouteApi* | [**del_route**](docs/RouteApi.md#del_route) | **DELETE** /routes/{id} | Delete a Route.
*RouteApi* | [**get_routes**](docs/RouteApi.md#get_routes) | **GET** /routes | Get current route information, i.e., list of all active SFCRs including their paths.
*RouteApi* | [**set_route**](docs/RouteApi.md#set_route) | **POST** /routes | Route a request via the provided route. Return route id if success (which also means input route id is ommitted).
*RouteApi* | [**update_route**](docs/RouteApi.md#update_route) | **PUT** /routes/{id} | Update a new route path or new sfcrs.
*SfcrApi* | [**add_sfcr**](docs/SfcrApi.md#add_sfcr) | **POST** /sfcrs | Add new SFC request. id field is optional
*SfcrApi* | [**del_sfcr**](docs/SfcrApi.md#del_sfcr) | **DELETE** /sfcrs/{id} | Delete a sfcr.
*SfcrApi* | [**get_sfcrs**](docs/SfcrApi.md#get_sfcrs) | **GET** /sfcrs | Get currently active SFC requests.
*VnfApi* | [**deploy_vnf**](docs/VnfApi.md#deploy_vnf) | **POST** /vnfs | Instantiate an instance of a VNF flavor on a given node.
*VnfApi* | [**destroy_vnf**](docs/VnfApi.md#destroy_vnf) | **DELETE** /vnfs/{id} | Destroy a VNF instance.
*VnfApi* | [**shutdown_vnf**](docs/VnfApi.md#shutdown_vnf) | **POST** /vnfs/{id}/shutdown | Shut down a VNF instance.


## Documentation For Models

 - [Body](docs/Body.md)
 - [Route](docs/Route.md)
 - [RouteUpdate](docs/RouteUpdate.md)
 - [SFCR](docs/SFCR.md)


## Documentation For Authorization

 All endpoints do not require authorization.


## Author

vantu.bkhn@gmail.com

