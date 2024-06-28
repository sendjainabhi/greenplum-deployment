# Greenplum FAQ and Important points 

* Q - How can I get Greenplum added to our list of entitlements in the support portal? 
   * A - Open the support ticket on [broadcom portal](https://broadcomcms-software.wolkenservicedesk.com/web-form). Or you can try calling the **Phone: +1 800 225-5224, Option 1 (Global Contact Numbers)**

* Q - What is the memory recommendation per segment ? 
   * A - We need 4GB to 8GB of memory per segment or more. More depending on how much data is managed per segment or used on queries. Usually very hard to anticipate, therefore the ballpark recommendations. Minimum 4GB per segment if memory does not fail.

* Q - How much MTU(maximum transmission unit) should I set for Greenplum.
    * A - Greenplum recommends MTU 9000. If it's not possible you can go with 1500.

* Q - What mechanism do you recommend we use to backup the Greenplum environment?
   * A - Greenplum has a backup tool called `gpbackup` which is the usual way people do backups. We have a new tool that does `PITR` type backups called `GPDR`, which is also an option.`gpbackup` can be granular and you can restore only one table if needed. It's more common to lose one table than to lose the entire system.

* Q - Where can I get the Greenplum TPS-DS performance test ?
   * A - You can get the Greenplum TPS-DS performance test in [TPC-DS](https://github.com/greenplum-db/TPC-DS) git repo.

* **GM command center** - If you are installing GPCC on cloud - ensure you open port 28080 for gpcc web and 5432 for postures db in cloud security groups.

* **Greenplum backup and restore** - [Greenplum backup and restore installation instructions]( https://docs.vmware.com/en/VMware-Greenplum-Backup-and-Restore/1.30/greenplum-backup-and-restore/backup-restore-install.html) for version 1.3.0.