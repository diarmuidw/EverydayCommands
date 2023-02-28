###FTP TLS simple example

```
from ftplib import FTP_TLS

FTP_TLS.port = 21 # just for force it to 21 

ftp = FTP_TLS(host='HOST',user='USR',passwd='PASSWORD') 
print("after ftp")

ftp.prot_p() #It won't work without this


filename = 'downloadedfile.txt'

handle = open('/home/ubuntu/%s'%filename, 'wb')
ftp.retrbinary('RETR %s' % filename, handle.write)
handle.close()
ftp.quit()

```
