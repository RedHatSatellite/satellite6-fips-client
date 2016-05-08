# satellite6-fips-client
Provisioning Templates and Snippets Useful for Deploying FIPS-140 enabled Clients with Satellite 6. 
Setting Up a Red Hat Enterprise Linux system in FIPS mode is documented in the [Red Hat Knowledgebase](https://access.redhat.com/solutions/137833).
However most of the steps documented in that article are manual. The provisioning templates in this repo aim to make it possible to integrate 
those commands into Satellite 6's kickstart provisioning process

# Repository Contents

This repository contains the following templates:

Item | Details | Notes
-------- | -------- | ------------------------
Kickstart_Default_PXELinux_FIPS.erb| Updated PXELinux Template |
fips_packages.erb | packages to be installed for FIPS mode to work properly (e.g dracut-fips)
Satellite_Kickstart_Default_FIPS.erb | Kickstart template with modifications to call the **fips_packages** snippet
puppet.conf.erb | Updated puppet.conf with updated (SHA256) digest_algorithm
