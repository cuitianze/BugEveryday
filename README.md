# BugEveryday

1. Centos chrome black screen    
  run `google-chrome --no-sandbox`    
  or fix SELinux bug    
  ```
  grep chrome /var/log/audit/audit.log | audit2allow -M mypol
  
  semodule -i mypol.pp
  ```
