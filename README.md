# BugEveryday

1. Centos chrome black screen    
  run `google-chrome --no-sandbox`    
  or fix SELinux bug    
  ```
  grep chrome /var/log/audit/audit.log | audit2allow -M mypol
  
  semodule -i mypol.pp
  ```
2.   ng-bootstrap `Unexpected token <`   
fix bug:  https://github.com/valor-software/ng2-bootstrap/issues/50#issuecomment-165448962
3.   centos nginx 502  `connect() to 127.0.0.1:3000 failed (13: Permission denied) while connecting to upstream`   
   close the SELinux   https://github.com/cuitianze/BugEveryday/issues/1
4.   centos nginx 502 `connect() failed (111: Connection refused) while connecting to upstream`   
   restart pm2 process
5. centos connect vpn    
    http://www.apelearn.com/bbs/thread-6740-1-1.html
6. The ANDROID_HOME environment variable is not set or it points to a non-existent directory. You will not be able to perform any build-related operations for Android.     
   Solution:   
    edit your .bashrc from home folder  
    and add this line down there   
```
export ANDROID_HOME=~/android-sdk-linux   
PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools
```
