---
path: /docs/common-errors
title: Common Errors
---

# Errors you might encounter while setting up the project

## Redis connection error

```bash
ArgumentError: invalid uri scheme
```

This is an error thrown from the Redis connector. You might not have set up the Redis environment variables properly. Please refer to the dependencies section to install redis-server and [Configure Redis URL](https://www.chatwoot.com/docs/environment-variables) in the environment-variables section.

## pg gem Installation error

If you see the following error while bundle installation, provide the Postgres path as pg\_config.

```text
Gem::Ext::BuildError: ERROR: Failed to build gem native extension.

An error occurred while installing pg (1.2.3), and Bundler cannot
continue.
Make sure that `gem install pg -v '1.2.3' --source 'https://rubygems.org/'`
succeeds before bundling.

checking for pg_config... no
No pg_config... trying anyway. If building fails, please try again with
 --with-pg-config=/path/to/pg_config
```

To fix this, try executing

```text
gem install pg -v '1.2.3' --source 'https://rubygems.org/' -- --with-pg-config=path-to-postgres-installation/12/bin/pg_config
```

