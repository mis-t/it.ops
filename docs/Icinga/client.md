# Install Icinga Agent

## Windows

1. Download the [Icinga2 Agent](https://packages.icinga.com/windows/). **NOTE:** Download the 64bit msi file.
1. Setup the Agent by double click on the msi file, then follow the setup wizard. Check the ***Run Icing 2 setup wizard*** before **Finish** the installation.
1. From the Master node, run
   ```bash
     icinga2 pki ticket --cn domain.uccs.edu
   ```
1. Copy the generated hash to the *Icinga Windows Agent Setup Wizard* where it says **CSR Signing Ticket**.
1. Add the master instance with the master node's information. Keep the default port number.
1. Add the global zone name. Windows OS is under ZoneName ***windows*** and Linux OS is under ***linux***.
1. Check the radio button of TCP Listener and checkbox of Accept commands from master/satellite instance(s) and Accept config updates from master/satellite instance(s).
1. continue until the setup is complete.
