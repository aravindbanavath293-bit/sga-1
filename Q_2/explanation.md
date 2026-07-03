# Explanation for Question 2

1. mkdir -p secure_workspace/{docs,src,logs} — This created the secure workspace structure needed for the project.
2. touch ... — This created the required project files inside the new directories.
3. ls -ld ... — This verified the directory structure and initial permissions.
4. chmod 750 secure_workspace — This restricted the top-level workspace so only the owner could access it fully, while group members had limited access.
5. chmod 750 ... — This applied the same controlled access to the docs, src, and logs directories.
6. chmod 640 ... — This limited access to the files so that only the owner could write and the group could read.
7. ls -ld ... — This confirmed the permissions after the changes were applied.
8. ls -l ... — This displayed the final file-level permissions and ownership details.
9. umask — This revealed the default mask that governs new file and directory permissions.

These permissions protect project data by limiting access to the owner and, where appropriate, the group, while reducing exposure to other users.
