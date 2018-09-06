# securityonion-ecrimelabs
Implementation of information from MISP through the eCrimeLabs API and into SecurityOnion

Prerequisites:

Security Onion (installed,configured)
eCrimeLabs Broker API access and API Key
Download and Configure (on Master or Standalone)

Clone the repo:
git clone https://github.com/eCrimeLabs/securityonion-ecrimelabs
Run the setup script:
sudo securityonion-ecrimelabs/setup-ecrimelabs
Update rules (if desired):
sudo rule-update
Confirm rules in place:
grep -i misp /etc/nsm/rules/downloaded.rules
Confirm Bro Intel in place:
cat /opt/bro/share/bro/intel/ecrimelabs-intel.dat

A cron job will run every 2 hours to download new NIDS rules and Intel.


------

The setup will allways pull the incident feed,
