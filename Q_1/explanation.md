# Explanation for Question 1

1. whoami — This command confirmed the active Linux username for the current session.
2. groups — This listed the groups that the current account belongs to, which helps verify access privileges.
3. echo "$SHELL" — This checked the default shell in use so the environment could be validated correctly.
4. pwd — This showed the present working directory and confirmed the starting location of the lab.
5. ls -ls — This displayed the files and folders available in the current directory and helped verify the workspace structure.
6. curl -s --max-time 10 https://youtube.com > /dev/null && echo "Network: youtube.com reachable" — This tested outbound network access and confirmed that the environment could reach the internet.

These observations show that the Linux environment is active, the user account is correctly configured, and external network access is available.
