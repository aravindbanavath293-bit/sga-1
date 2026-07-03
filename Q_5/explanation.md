# Explanation for Question 5

1. lsblk — This listed the storage devices visible in the environment, including disks and partitions.
2. mount | head -5 — This showed the mounted filesystems and confirmed which storage paths were active.
3. df -h — This reported disk space usage and available capacity for each mounted filesystem.
4. df -i — This reported inode usage to assess whether the system was running out of file entries.

The storage assessment showed sufficient free space and low inode usage, indicating that the current environment is healthy for normal operations. Recommended practices include monitoring usage trends and cleaning temporary or obsolete data regularly.
