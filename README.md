**_Ubuntu Terminal Proxy Setup_**

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

**Update Proxy Configuration System-wide:**

1. Open the terminal.

2. Enter the command:

<!---->

    sudo vim /etc/environment

3. Add the following lines to the file:

<!---->

    http_proxy="http://username:password@10.10.10.10:3128/"
    https_proxy="http://username:password@10.10.10.10:3128/"

4. Replace "username" and "password" with your actual proxy credentials.

5. Save the changes and exit the text editor.

![](https://lh7-us.googleusercontent.com/docsz/AD_4nXcFW68Vy8vgUAgdwtmVfECu7-xXvFt0DG1s56fKtE2sF-nrtogQuFYUjJOL8twmUKn2SeHWDeNJqCDMK9i-j_UXpUssCk4YMsL1pktowJEQ04YujN-tCVqV3g8mRRfMU5eiUm3RSYaM_TKlKXXWtukVtb0o?key=-Fvzt4dE_You1HlFh6EC6Q)

**Update Proxy Settings using apt.conf:**

1. Open a terminal.

2. Enter the command:

<!---->

    sudo vim /etc/apt/apt.conf

3. Add the following lines to the file:

<!---->

    Acquire::http::Proxy "http://username:password@10.10.10.10:3128/";
    Acquire::https::Proxy "http://username:password@10.10.10.10:3128/"

4. Replace "username" and "password" with your actual proxy credentials.

5. Save the changes and exit the text editor.

6. After updating the apt configuration, retry the command:

```
sudo apt update
```



**Verify Network Connection:**

1. Ensure that your system has a working internet connection.

2. Check for any network issues that may prevent communication with the proxy server.
