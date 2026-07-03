# Explanation for Question 3

1. ln original.txt hardlink.txt — This created a hard link that pointed to the same inode as the original file.
2. ln -s original.txt symlink.txt — This created a symbolic link that stored the path to the target file rather than the inode.
3. ls -li — This displayed inode numbers and showed that the hard link shared the same inode while the symbolic link had a different one.
4. stat ... — This collected metadata such as inode, links, and file type for each entry.
5. rm original.txt — This removed the original file and demonstrated the difference between hard and symbolic links.

The experiment showed that hard links are direct references to the same inode, while symbolic links depend on a path and break if the target is deleted.
