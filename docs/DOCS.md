# cbmc.py Documentation

## Where do I start?

Please look at the pages below to find out where to go.

- [Quickstart](#installing)
- [API Reference](/docs/API.md)
- [Frequently Asked Questions](/docs/FAQ.md)

## Installing

**cbmc.py** is a python library for 麥塊匿名發文平台 API. A library in Python has to be installed with pip. Run the following in your terminal/command line to install the library.

```py
pip install -U cbmc.py
```

## Initializing an API Instance

### First, let's create the api instance.

```py
import cbmc

api = cbmc.SyncCbmc() # synchronous

# or

api = cbmc.AsyncCbmc() # asynchronous
```

And that's it! You should be able to interact with the API with the instance now.

Let's take a look at what is happening:

- `import cbmc` - This is the import line. If this returns a `ModuleNotFoundError`, please look at the section on how to install [here](#installing).
- `api = cbmc.SyncCbmc()` - This is the `api` variable that holds the api instance.
- `api = cbmc.AsyncCbmc()` - This is the `api` variable that holds the async api instance, where you can call the api asynchronously.

Note:  
All methods can be called directly from the class, so you can also do `cbmc.SyncCbmc.get_post()` instead of `api.get_post()`.  
Creating an instance is not required, but it is recommended for future updates (some planned new features will require that).
