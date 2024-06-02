# Recommended iLO settings

- **Set up hostname**

  Set up hostname for iLO:
  
  1. Go to _Network_ → _iLO Dedicated Network Port_ → _General_.
  2. Set a hostname and click _Submit_.

- **Set up NTP**

  Set up close NTP servers:
  
  1. Go to _Network_ → _iLO Dedicated Network Port_ → SNTP.
  2. Uncheck _Use DHCPv4 Supplied Time Settings_ and _Use DHCPv6 Supplied Time Settings_.
  3. Input addresses of two close NTP servers, select timezone and click _Submit_.
