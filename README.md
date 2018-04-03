# OPNsense Suricata Application Detection

## Welcome to the OPNsense IDS/IPS Application Detection rules!

If you are searching for an easy way to block specific applications like Youtube or Netflix this is the right resource for you.

We have categorized the rules in seven categories:

```
file-transfer (file sharing in general)
media-streaming (streaming, like youtube or shoutcast)
social-networking (facebook, google+)
messaging (ICQ, whatsapp)
mail (gmail, yahoo mail, mail.ru)
uncategorized (Zynga, Amazon, etc. Please add your favorites)
```

To add more applications to the ruleset please fork this repository and only edit the .lst files.
The content of the files (e.g. messaging.lst) look like this:

```
ICQ_WebClient messaging icq.com
```

There is first the name of the application (if more words extend with underscore),
then the category which must always be the same for each file, and then the URL to block.

If one application uses more than one URL like DropBox, you can add as many lines as you
want but be sure to leave the name always the same!

Order is most important for editing .lst files. Always append new rules at the end,
a sorting is not possible since our rule generator counts the rules always one up. 
This would mix up your existing configuration. 

Feel free to add new applications and rules to our ruleset!


