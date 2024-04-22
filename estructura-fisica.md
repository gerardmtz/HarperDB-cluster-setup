## Fisical structure and DB storage
HarperDB’s databases and data tables are stored in the `~/hdb` directory. 

**Note:** you can change the location of HarperDB’s data directory by updating the **rootPath** in the configuration file (which you specified during installation) to a new location. Then, edit the `hdb_boot_properties.file` to direct HarperDB to the new location by updating the `settings_path` variable.

It’s important to mention that HarperDB uses *LMDB (Lightning Memory-Mapped Database)*  as the underlying key-value store.

The data is **memory-mapped**, which allows for fast access to data without duplication. All write operations are fully serialized, making writes deadlock-free.