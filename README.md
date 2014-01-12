A simple utility for smartly purging backup directories. 

Read more here: http://www.johnandcailin.com/blog/john/smartly-purge-your-old-backup-files-linux

```
Usage: purgeFiles [OPTION]...
 -h, --help                          Print this help message
 -a, --ages=age1,age2                Desired ages to keep (by default, in days)
 -c, --command=command               Command used to remove file/dir (ex. s3qlrm)
 -d, --directory=dir                 Target directory
 -p, --pattern=pattern               File pattern to match
 -f, --force                         Force deletion (no simulation mode)

e.g. purgeFiles --ages=1,1w,1m,2m,6m,2y --directory=/tmp --pattern="*.txt"
This would purge /tmp and try to keep files ending in .txt of the following ages:
- 1 day
- 1 week
- 1 month
- 2 months
- 6 months
- and 2 years old

Note: this would only do a simulation run. Specify --force to actually delete the files. 

Author: John Quinn, http://johnandcailin.com/john
```
