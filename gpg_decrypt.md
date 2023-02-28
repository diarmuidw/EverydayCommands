### Decrypt file with passphrase

First install python-gnugpg

https://pypi.org/project/python-gnupg/

pip install python-gnupg



```
import gnupg

encryptedfilename = 'filename.asc'
decryptedfilename = 'filename.txt'

gpg = gnupg.GPG()
with open("/home/ubuntu/%s"%encryptedfilename, 'rb') as f:
    status = gpg.decrypt_file(f, passphrase='cleverpassphrase', output='/home/ubuntu/%s'%decryptedfilename)

print 'ok: ', status.ok
print 'status: ', status.status
print 'stderr: ', status.stderr
```
