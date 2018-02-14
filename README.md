sa-vpn-pptp-client
==================

[![Build Status](https://travis-ci.org/softasap/sa-java.svg?branch=master)](https://travis-ci.org/softasap/sa-java)

Helper repo for smarthome

Allows to inject control unit to smarthome local network via PPP to receive broadcasts from hardware units.

Troubleshouting
```shell
killall pppd

pppd call VPNprofile
```

Usage example:

```YAML

roles:
   - {
       role: "sa-vpn-pptp-client",
       pptp_user: "{{target_pptp_user}}",
       pptp_password: "{{target_pptp_password}}",
       pptp_server: "{{target_pptp_server}}",
       pptp_profile: "{{target_pptp_profile}}",
       pptp_remote_network: "{{target_pptp_remote_network}}",
       pptp_remote_network_mask: "{{target_pptp_remote_network_mask}}",
     }
```

Usage with ansible galaxy workflow
----------------------------------

If you installed the sa-vpn-pptp-client  role using the command


`
   ansible-galaxy install softasap.sa-vpn-pptp-client
`

the role will be available in the folder library/sa-vpn-pptp-client

Please adjust the path accordingly.

```YAML

     - {
         role: "softasap.sa-vpn-pptp-client"
       }

```




Copyright and license
---------------------

Code is dual licensed under the [BSD 3 clause] (https://opensource.org/licenses/BSD-3-Clause) and the [MIT License] (http://opensource.org/licenses/MIT). Choose the one that suits you best.

Reach us:

Subscribe for roles updates at [FB] (https://www.facebook.com/SoftAsap/)

Join gitter discussion channel at [Gitter](https://gitter.im/softasap)

Discover other roles at  http://www.softasap.com/roles/registry_generated.html

visit our blog at http://www.softasap.com/blog/archive.html
