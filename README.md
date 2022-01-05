# Vash-Green-Schools
Vash Green Schools Homepage

Landing Page 

Project Summary & Pictures


Links: 

  Podcast "Same Storm, Different Boats" (to-be-developed)
  
  Blog (to-be-developed)
  
  Speeches (Vash & Friends) (to-be-collected)
  
  Vash Social Media (to-be-developed)
  
  Project Management Tool / Nextcloud (see below)


Key Goals for the project landing page:
Outreach, Advocacy,

----------------
Project Management Tool Public Access (cloud.vashgreenschools.org) (background docs here)
  

Key Goals of the Cloud Backend:
- Enable Project Management, in particular on-boarding of other activists & controls by Vash
- Allow full transparency by photo & video documentation of the project activities (ideally directly on a map).
- Transparent financial accounts.
- Record keeping of contacts to schools to allow for "1-year-later" follow ups.

=> Workflow for adding more activists & schools must become super simple and straight forward on the backend, as there are a total of 25'000 schools in Uganda and most of them need solar & stove. 


Installation guide for Nextcloud on AWS:
create instance (min 8 GB RAM and 4 CPUs)
Firewall Settings (open 443 / https)
Set: Static IP
Connect via SSH
Username: ubuntu
Key: public key login follow for putty.
https://lightsail.aws.amazon.com/ls/docs/en_us/articles/lightsail-how-to-set-up-putty-to-connect-using-ssh

once inside:

sudo apt update
sudo apt upgrade
y

sudo snap install nextcloud

sudo nextcloud.manual-install USERNAME PASSWORD
sudo nextcloud.occ config:system:set trusted_domains 1 --value=cloud.vashgreenschools.org
#Replace -- IP Adress with the IP address you want to use to access the cloud
#sudo nextcloud.occ config:system:set trusted_domains 2 --IP Adress

sudo nextcloud.enable-https lets-encrypt
