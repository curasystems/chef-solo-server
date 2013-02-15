# When the cookbooks are changed use this command
tar zcvf smartos_cookbooks.tar.gz -C c:/Development/ops/smartos_cookbooks cookbooks

# Initial Bootstrap Command for a new Node (Adjust IP of course to server URL)
curl -s http://192.168.3.114:8080/smartos/bootstrap-smartos.sh | bash

# Force update of zone chef configuration
/opt/chef/bin/chef-solo -c /var/chef/solo.rb

