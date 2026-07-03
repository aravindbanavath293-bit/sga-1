# Explanation for Question 4

1. echo "sample log line" > app.log — This created a sample log file for the investigation.
2. lsof | head -n 20 — This listed open files and helped identify active file descriptors in use by processes.
3. exec 3<app.log — This opened app.log and assigned it to file descriptor 3.
4. lsof -p $$ — This confirmed the current shell process had app.log open.
5. ls -l /proc/$$/fd — This displayed the shell's current file descriptors and proved that descriptor 3 referred to the log file.
6. ls -l > stdout.txt — This redirected standard output to a file.
7. ls /not_a_real_path 2> stderr.txt — This redirected standard error to a file.
8. (ls -l && ls /not_a_real_path) > combined.txt 2>&1 — This combined stdout and stderr into a single file.
9. ulimit -a — This displayed the resource limits related to open files and process usage.

The investigation showed how Linux uses file descriptors to represent files, terminals, and devices, and how redirection manages input and output streams.
