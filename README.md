# SecurityOnion-eCrimeLabs
Implementation of information from MISP through the eCrimeLabs API and into SecurityOnion

**Prerequisites:**

- Security Onion (installed,configured)
- eCrimeLabs Broker API access and API Key
- Download and Configure (on Master or Standalone)

**Clone the repo:**
```
git clone https://github.com/eCrimeLabs/securityonion-ecrimelabs
```

**Run the setup script:**
```
sudo bash securityonion-ecrimelabs/setup-ecrimelabs
```

**Update rules (if desired):**
```
/usr/sbin/download-ecrimelabs
sudo rule-update
```

**Confirm rules in place:**
```
cat /etc/nsm/rules/alert.ecrimelabs.rules
cat /etc/nsm/rules/incident.ecrimelabs.rules
```

**Confirm Bro Intel in place:**
```
cat /opt/bro/share/bro/intel/ecrimelabs-intel.dat
```

A cron job will run every 2 hours to download new NIDS rules and Intel.

------

Remember to modify **ecrimelabscfg**

The setup will allways pull the incident feed, and here from it is up to the individual
implementation on what other feeds will be extracted.
