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
        role: "sa-sql-server"
      }
```

Advanced:


```YAML
  roles:
  - {
      role: "sa-sql-server"
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
