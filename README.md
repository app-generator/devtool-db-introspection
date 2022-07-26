# Database Introspection Tool

`Open-Source` **[developers tool](https://appseed.us/developer-tools/)** that provides simple helpers for legacy databases introspection. Crafted on top of `Python` and [Peewee](http://docs.peewee-orm.com/en/latest/).

- 👉 Free [support](https://appseed.us/support/) via Email and [Discord](https://discord.gg/fZC6hup)
- 👉 More [Developer Tools](https://appseed.us/developer-tools/) - provided by AppSeed

<br />

> Features

- `Peewee` DB Reflection
- Supported DB:
  - SQLite, MySql, PostgreSQL
- DbWrapper Class:
  - `print_all_models()` - returns all tables
  - `print_db_model` - print table definition
  - `dump_tables()` - Dump SQL definitions (all tables) 
  - `dump_tables_data()` - Dump database content (all tables)


> [Support](https://appseed.us/support) via **Github** (issues tracker) and [Discord](https://discord.gg/fZC6hup).
 
<br />

![DB Migration Tool - Open-Source Developer Tool provided by AppSeed.](https://user-images.githubusercontent.com/51070104/153570755-dde19fba-03ca-4eed-a156-6a8efb1ef949.png)

<br />

## ✨ Quick Start

> Clone Sources (this repo)

```bash
$ git clone https://github.com/app-generator/devtool-db.git
$ cd devtool-db
```

<br />

> Install Modules using a Virtual Environment

```bash
$ virtualenv env
$ source env/bin/activate
$ pip install -r requirements.txt
```

Or for **Windows-based Systems**

```bash
$ virtualenv env
$ .\env\Scripts\activate
$
$ # Install modules - SQLite Database
$ pip3 install -r requirements.txt
```

<br />

> Launch the Python console

```bash
$ python
>>> 
>>> from util import *                                  # import helpers      
>>>                    
>>> db_sqlite = DbWrapper()                             # invoke the Base Class  
>>> db_sqlite.driver = COMMON.DB_SQLITE                 # set driver
>>> db_sqlite.db_name = 'samples/api-django.sqlite3'    # set db name
>>> db_sqlite.connect()                                 # connect 
True 
>>> db_sqlite.load_models()                             # load DB SChema 
True
>>> db_sqlite.dump_tables()                             # Dump tables definitions 
True
>>> db_sqlite.dump_tables_data()                        # Dump data
 > Dump data for [api_user_user]
 > Dump data for [api_authentication_activesession]
 > Dump data for [auth_group]
 > Dump data for [api_user_user_groups]
 > Dump data for [django_content_type]
 > Dump data for [auth_permission]
 > Dump data for [api_user_user_user_permissions]
 > Dump data for [auth_group_permissions]
 > Dump data for [django_admin_log]
 > Dump data for [django_migrations]
 > Dump data for [django_session]
True
>>> db_sqlite.reset()                                     # reset the Class data  
>>>
```

<br />

At this point, the tables and data are saved in the [output](https://github.com/app-generator/devtool-db/tree/main/output) directory.

```bash
$ cd output ; ls 
$ SQLITE.sql
$ SQLITE_api_user_user.sql
$ SQLITE_auth_permission.sql
$ SQLITE_django_content_type.sql
$ SQLITE_django_migrations.sql
```

<br />

--- 
Database Introspection Tool - Provided by **AppSeed** [App Generator](https://appseed.us/app-generator).
