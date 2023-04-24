# API Reference

This page outlines the API wrapper of cbmc.py

## API Instances

- [SyncCbmc](#synccbmc)
- [AsyncCbmc](#asynccbmc)

## Post Object

- [Post](#post)

---

# API Instances

## SyncCbmc

## `class SyncCbmc(CbmcBase)`

PARAMETERS:

- None

### `get_post(params)` ⇒ \[[Post](#post)]

Get a post from 麥塊匿名發文平台 with the given parameters.

| Param | Type | Description |
| :---: | :---: | --- |
| post_id | [int](https://docs.python.org/3/library/functions.html#int) | The post ID of the post you want to get. |

#### **Example**

```py
api.get_post(post_id=1)
```

### `get_posts(params)` ⇒ \[[List](https://docs.python.org/3/library/typing.html#typing.List)\[[Post](#post)]]

Get a list of posts from 麥塊匿名發文平台 with the given parameters.

| Param | Type | Default | Description |
| :---: | :---: | :---: | --- |
| limit | [int](https://docs.python.org/3/library/functions.html#int) | 10 | The number of the posts you want to get. (Max: 300) |

#### **Example**

```py
api.get_posts(limit=10)
```

### `get_status(params)` ⇒ \[[dict](https://docs.python.org/3/library/stdtypes.html#dict)]

Get the status of a post on 麥塊匿名發文平台.  
This method is NOT implemented yet.

| Param | Type | Description |
| :---: | :---: | --- |
| code | str | The code of the post you want to get the status. |

#### **Example**

```py
api.get_status(code="123456")
```

---

## AsyncCbmc

## `class AsyncCbmc(CbmcBase)`

PARAMETERS:

- None

### `await get_post(params)` ⇒ \[[Post](#post)]

Get a post from 麥塊匿名發文平台 with the given parameters.

| Param | Type | Description |
| :---: | :---: | --- |
| post_id | [int](https://docs.python.org/3/library/functions.html#int) | The post ID of the post you want to get. |

#### **Example**

```py
await api.get_post(post_id=1)
```

### `await get_posts(params)` ⇒ \[[List](https://docs.python.org/3/library/typing.html#typing.List)\[[Post](#post)]]

Get a list of posts from 麥塊匿名發文平台 with the given parameters.

| Param | Type | Default | Description |
| :---: | :---: | :---: | --- |
| limit | [int](https://docs.python.org/3/library/functions.html#int) | 10 | The number of the posts you want to get. (Max: 300) |

#### **Example**

```py
await api.get_posts(limit=10)
```

### `await get_status(params)` ⇒ \[[dict](https://docs.python.org/3/library/stdtypes.html#dict)]

Get the status of a post on 麥塊匿名發文平台.
This method is NOT implemented yet.

| Param | Type | Description |
| :---: | :---: | --- |
| code | str | The code of the post you want to get the status. |

#### **Example**

```py
await api.get_status(code="123456")
```

---

# Post Object

## Post

## `class Post(data)`

PARAMETERS:

- data: \[[dict](https://docs.python.org/3/library/stdtypes.html#dict)]

ATTRIBUTES:

- post_id: \[[int](https://docs.python.org/3/library/functions.html#int)] - The post ID of the post.
- platform_id: \[[int](https://docs.python.org/3/library/functions.html#int)] - The platform ID of the post.
- type: \[[str](https://docs.python.org/3/library/stdtypes.html#str)] - The post type of the post.
- content: \[[str](https://docs.python.org/3/library/stdtypes.html#str)] - The content of the post.
- photo: \[[str](https://docs.python.org/3/library/stdtypes.html#str) | None] - The photo url of the post or None if there is no photo.
- admin_post: \[[bool](https://docs.python.org/3/library/stdtypes.html#truth-value-testing)] - Whether the post is an admin post.
- approve_timestamp: \[[int](https://docs.python.org/3/library/functions.html#int)] - The timestamp of when the post was approved.
- approve_time: \[[datetime.datetime](https://docs.python.org/3/library/datetime.html#datetime-objects)] - The time of when the post was approved.
- approve_user: \[[str](https://docs.python.org/3/library/stdtypes.html#str)] - The user who approved the post.
- fbid: \[[str](https://docs.python.org/3/library/stdtypes.html#str)] - The Facebook ID of the post.

### `to_dict()` ⇒ \[[dict](https://docs.python.org/3/library/stdtypes.html#dict)]

Convert the post object to a dictionary.

#### **Example**

```py
post.to_dict()
```
