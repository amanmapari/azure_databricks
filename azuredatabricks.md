##### https://www.youtube.com/watch?v=TScSdIJ-_Oo

#### MOUNTING VIDEO:
##### https://www.youtube.com/watch?v=8YL8T0kw75M

- Template

```bash
# dbutils.fs.mount(source = 'wasbs://containername@sa1aman.blob.core.windows.net/'
# extra_configs = {'fs.azure.account.key.storage_account_name.blob.core.windows.net':'Access_key_name'})
```
- Template used
```bash
dbutils.fs.mount(source = 'wasbs://all-data@sa1aman.blob.core.windows.net/',
                 mount_point = '/mnt/blobstorage',
                 extra_configs = {'fs.azure.account.key.sa1aman.blob.core.windows.net':'Bdt8FxU6VT8iHwZKMyJlwOHPO4YlPmH+nQlfBoRq+Sa9LH8w5hOQASM1RtP07AQCH7IXs4/0+Rar+AStXpKlSg=='})
```

- List down all tha content that is mounted inside the container
```bash
dbutils.fs.ls('/mnt/blobstorage')
```
- Copy all the data from one folder to another within the same container
```bash
dbutils.fs.cp('/mnt/blobstorage/raw_data/dvdrental/2024/01/03/.', '/mnt/blobstorage/cleaned_data/', recurse=True)
```