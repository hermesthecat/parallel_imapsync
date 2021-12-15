Parallel Imapsync
=========
Run imapsync parallely for multiple mailboxes


### Pre-requisites
* Python 2.x
* make

### Run Instructions

* Add a CSV file containing data in following format on each line:
```
<remote_imap_host>,<remote_imap_port>,<remote_username>,<remote_password>,<local_imap_host>,<local_imap_port>,<local_username>,<local_password>
```

* From command line run:
```
./gen_imapsync_makefile <your_data_file>.csv
```
* You should get a generated `Makefile` in the current directory.
* Run `make -jn` where n is the number of parallel imapsync processes you want to run.
