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
   close the SELinux
4.   centos nginx 502 `connect() failed (111: Connection refused) while connecting to upstream`   
   restart pm2 process
