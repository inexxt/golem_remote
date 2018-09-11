# golem_remote

MVP version of library for wrapping Python functions to run on golem.  

Work in progress. Working revision: `d364ef748aaa94271559f62d274376f559191f74` here and `379e140c726c59bf1b80e5e61304ec5f27be7bc5` in `golemfactory/golem@runf`.  

Install:
 - `git clone git@github.com:golemfactory/golem.git && git checkout runf`
 - `pip install git+https://github.com/inexxt/golem_remote.git` 
 - Set config options in `golem_remote/config.py`

Run:
 - Run requestor (for example: ```
   python golemapp.py --log-level INFO --datadir golem_data_r/ 
   --accept-terms --protocol_id 97 --password "k123@" 
   -p localhost:40103 -r localhost:61000```)
 - Run provider (for example ```
   python golemapp.py --log-level INFO --datadir golem_data_p 
   --accept-terms --protocol_id 97 --password "k123@" 
   -p localhost:40102 -r localhost:61001```)
 - Run redis on `localhost:6379`
 - Run your task on Golem (for example: `python iteration6_golem_remote_package.py`)

Testing:
 - Run `pytest` in the package directory
 - If the redis tests don't pass, ensure you don't have another redis instance running on `localhost:6379`
 