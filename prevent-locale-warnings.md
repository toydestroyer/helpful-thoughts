To prevent warnings like this on SSH connection:

    perl: warning: Setting locale failed.
    perl: warning: Please check that your locale settings:
      LANGUAGE = (unset),
      LC_ALL = (unset),
      LC_CTYPE = "UTF-8",
      LANG = "en_US.UTF-8"
        are supported and installed on your system.
    perl: warning: Falling back to the standard locale ("C").
    locale: Cannot set LC_CTYPE to default locale: No such file or directory
    locale: Cannot set LC_ALL to default locale: No such file or directory

Comment this string in `/etc/ssh/sshd_config`

    AcceptEnv LANG LC_*
