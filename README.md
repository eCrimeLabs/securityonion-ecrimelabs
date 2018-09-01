# securityonion-ecrimelabs
Implementation of informaiton from MISP through the eCrimeLabs API and into SecurityOnion

Prerequisites:

Security Onion (installed,configured)
MISP Instance and API Key
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
cat /opt/bro/share/bro/intel/misp-intel.dat
A cron job will run every morning at 6:01AM to download new NIDS rules and Intel.
