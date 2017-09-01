sa-sql-server
=============

[![Build Status](https://travis-ci.org/softasap/sa-sql-server.svg?branch=master)](https://travis-ci.org/softasap/sa-sql-server)


 This role installs SQL Server 2017 RC2 (or more recent) on Ubuntu 16.04.
 Then you can connect with sqlcmd to create your first database and run queries.


 Prerequisites

 You must have a Ubuntu machine with at least 3.25 GB of memory. Additional MS requirements
 might be checked here:  https://docs.microsoft.com/en-us/sql/linux/sql-server-linux-setup#system


Simple

```YAML
  roles:
    - {
        role: "sa-sql-server",
        # Password for the SA user (required)
        mssql_sa_password: "YourStrong1Passw0rd",

        # Product ID of the version of SQL server you're installing
        # Must be evaluation, developer, express, web, standard, enterprise, or your 25 digit product key
        # Defaults to developer
        mssql_pid: developer
      }
```

Advanced:


```YAML
  roles:
  - {
      role: "sa-sql-server",
      # Password for the SA user (required)
      mssql_sa_password: "YourStrong1Passw0rd",

      # Product ID of the version of SQL server you're installing
      # Must be evaluation, developer, express, web, standard, enterprise, or your 25 digit product key
      # Defaults to developer
      mssql_pid: developer,

      # Install SQL Server Agent (recommended)
      option_sql_install_agent: true,

      # Install SQL Server Full Text Search (optional)
      option_sql_install_fulltext: false,

      # Create an additional user with sysadmin privileges (optional)
      option_sql_install_user: true,
      sql_install_user: user,
      sql_install_user_password: "YourStrong1Passw0rd"
    }
```


Usage with ansible galaxy workflow
----------------------------------

If you installed the sa-sql-server  role using the command


`
   ansible-galaxy install softasap.sa-sql-server
`

the role will be available in the folder library/sa-sql-server

Please adjust the path accordingly.

```YAML

     - {
         role: "softasap.sa-sql-server"
       }

```



Copyright and license
---------------------

Code licensed under the [BSD 3 clause] (https://opensource.org/licenses/BSD-3-Clause) or the [MIT License] (http://opensource.org/licenses/MIT).

Subscribe for roles updates at [FB] (https://www.facebook.com/SoftAsap/)

Join Gitter channel at [Gitter] (https://gitter.im/softasap/)
