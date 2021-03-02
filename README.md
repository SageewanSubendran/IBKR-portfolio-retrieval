# IBKR-portfolio-retrieval
Allowing Users To Retrieve IBKR Portfolio Data

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------
IBKR's Portfolio Retrieval Demo App (https://interactivebrokers.github.io/cpwebapi/)
Download and unzip the CP WebAPI gateway from the website: https://www.interactivebrokers.com/en/index.php?f=5041

1) Navigate to the directory where the gateway has been unzipped in a command prompt.

2) Launch the gateway with the command "bin\run.bat root\conf.yaml" (on Windows) or "bin/run.sh root/conf.yaml" (on Mac/Unix).

3) To authenticate the gateway session with your account, go to https://localhost:5000/

4) The port number is 5000 by default and set in the root/conf.yaml configuration file.
Authenticate with your username/password and second factor device (for production accounts).

**Note**: you can login to paper accounts by using the paper account-specific username/password combination. Every paper account has its own username.
The paper account username can be found in Client Portal at: Settings -> Account Settings -> Paper Trading Account -> Configure
You can also reset your paper trading account password there if necessary.

You should receive the message "Client login succeeds" after successful authentication. The tab can then be closed.

It is expected that gateway will require restart and reauthentication at least daily.
If left inactive, the gateway session will automatically timeout for security reasons within a few minutes and all endpoints will return 401: Access Denied errors.
An active session can be extended by pinging the /portal/sso/validate endpoint are regular time intervals, such as once per minute.
