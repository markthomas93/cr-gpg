This is a quick run though of the files in this folder
and a basic setup.

## Folders : 

chromeExtension : This is the chrome extension , you need to pack
it wil chrome to distribute it or you can load it as is.

gmailGPG : This is the gpg plugin and is what interacts with the
the gpg bin installed on your machine. To compile this you need to
grab the FireBreath project from [here](http://www.firebreath.org/display/documentation/Download).
Place this folder in the projects folders and run the prep command
for your system.

## Using the extension :

Encrypting a message : 
The extension is hopefully easy enough to use , open up a gmail
window(mail.thinkst.com) to begin. To encrypt a new message use
the compose button as normal , but you will notice that there is
a encrypt link next to the Rich Formatting link.

Clicking the button will encrypt the message that you are typing
with the public key for the current recepients. If they are not
found in your local pc keyring a error message will be displayed.

If no recepients or message is enterd a error message will be
displayed.

Decrypting a message :
Start of by clicking a email thread , this will show all mails
in that thread. Below each mail in the a Decrypt message link
will be shown.

Clicking the link will prompt you for your passphrase with
which to decrypt the message, a error will be show if no
valid gpg data can be found or if the passphrase is incorrect.

## Other considerations :

Note : If at any time a decrypt or encrypt link is not visible
please mouse over the actual composing form or your message thread
(when reading old mails).

Note : There is some flakyness with the multiple user encryption
especially if the user does not exist in your keyring.

Note : The default paths are requirements in the extension are
        tempPath = /tmp/
        gpgPath = /opt/local/bin/

       If your paths are different you can change them from the
       options menu for the chrome extension.

Final Note : All the dev was done on a mac and I was unable to
get libgpgme to build and include into a app directly , if you
can provide me with direct info please feel free to message me.
