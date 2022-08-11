# cdb-scripts-sw
This repository serves to faster create inventory into the database (CDB).
Please, after changes in excel files, update information in [sharepoint](https://cnpemcamp.sharepoint.com/sites/sei) (Access permission only authorized account).

# Information

##### The API works for Windows Subsystem Linux or an actual Linux system

##### Before install the API, check if you have Python2.7 and the setuptools library installed
```
sudo apt-get install python
sudo apt-get install pip
sudo pip install setuptools
```

## CDB Python API Installation

##### 1- Clone CDB repository

It's possible to clone it in any directory. It won't affect the API functions, but it is recommended to install it in directory used to keep repositories in your computer
```
git clone https://github.com/AdvancedPhotonSource/ComponentDB.git
```

##### 2- Install the API setup

The Python API is in the CDB files. It will be installed with the following command:
```
cd ComponentDB/src/python/
sudo python setup.py install
```

##### 3- Check if the API is working
To chek the API operation, use the following command:
```
cd ComponentDB/bin/
./cdb-get-item --service-url=https://your.host.name:port/cdb --id=item id
```

This command will find the item with the given id in the CDB database and print his values. In the code bellow the terminal shows one item with the id=50. It has to be like this:
```
id=50 name=MOE item_identifier1=1.0 item_identifier2=Optoelectric Module
```

If the answers was like this, your API is installed and ready to use!
