# flowinfo
Couchapp for viewing flow table info in couchdb 

# Install/config steps
* `mkdir <source directory>`
* `cd <source directory>`
* `git clone https://github.com/harshad91/flowinfo.git`
* `virtualenv venv`
  * `virtualenv` can be installed using `sudo pip install virtualenv`
* `pip install couchapp`
  * Installs all the `counchapp` dependencies
* `cd flowinfo`
* Edit the `.couchapprc` file
  * Couchapp uses a db (same as flows db) to host files too. This info should be provided in couchapprc file.
  * Change line no. 3 of the file to use your couchdb user/pwd combination instead of root:admin (highlighted below)
    * {"db":"http://`root:admin`@localhost:5984/flowinfodb"}
* `couchapp push . http://<username>:<password>@localhost:5984/flowinfodb/`
  * Replace `<username>` and `<password>` with your couchdb credentials
* Site can now be accessed at <http://localhost:5984/flowinfodb/_design/flow-info/index.html>
