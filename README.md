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
