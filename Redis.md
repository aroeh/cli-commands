# Redis CLI Documentation
[Redis Commands](https://redis.io/commands)


# Info

See stats and information for the current redis instance

`redis-cli info`

```
redis-cli info
```

# Flushall

Removes all stored keys from all databases

`redis-cli flushall`

```
redis-cli flushall
```

# Keys

Get keys that match a provided pattern

> Not recommended for use in PROD.  This command is only recommended for debugging scenarios

`redis-cli keys <pattern>`

```
redis-cli keys *name*
```

# Scan

Scans available keys using a cursor

> The scan must be run in iterations.  The first iteration should start with a 0 and will output the cursor to use the next iteration

`redis-cli scan <cursor>`

```
redis-cli scan 0
```

# Get

Retrieves the value of the provided key

`redis-cli get <key>`

```
redis-cli get mykey
```

# Set

Adds a new key value pair to the database

`redis-cli set <key> <value> [options]`

```
redis-cli set mykey "Hello World!"
```

# Delete

Removes the specified key or keys and their values from the database

> To remove a single key

`redis-cli del <key>`

```
redis-cli del mykey
```

> To remove multiple keys pass in the key values as an array separated by a space

`redis-cli del [key]`

```
redis-cli del key1 key2
```

# Copy

Copies the value of one key to another key

`redis-cli copy <sourcekey> <outputkey>`

```
redis-cli copy mykey newkey
```