# 3PAR Nagios check script v0.3
Last update 2014/08/13 Marcel Stangenberger

For installation instructions, follow the HPe 3PAR plugin for Nagios installation guide and install all required software.
Then download this script and copy to your Nagios plugins directory with executable rights

Please make sure the CONNECTCOMMAND variable matches with your environment.

## Changelist
2014/08/13
 - adjust check_pd so it works with InFormOS 3.1.2MU3
 - adjust check_port_fc so it works with InFormOS 3.1.2MU3 and does not whine about free ports

## 3PAR Nagios check script v0.2
Last update 2010/05/14 fredl@3par.com
Last update 2011/03/03 ddu@antemeta.fr

This script is provided "as is" without warranty of any kind and 3PAR specifically disclaims all implied warranties of merchantability, 
non-infringement and fitness for a particular purpose. In no event shall 3PAR have any liability arising out of or related to 
customer's 'use of the script including lost data, lost profits, or any direct or indirect, incidental, special, or 
consequential damages arising there from.
In addition, 3PAR reserves the right not to perform fixes or updates to this script


 Usage : check_3par InServ Username Command

 Supported commands 
       check_pd :      Check status of physical disks
                       Degraded ->             Warning
                       Failed ->               Critical

       check_node :    Check status of controller nodes
                       Degraded ->             Warning
                       Failed ->               Critical

       check_ld :      Check status of logical disks
                       Degraded ->             Warning
                       Failed ->               Critical

       check_vv :      Check status of virtual volumes
                       Degraded ->             Warning
                       Failed ->               Critical

       check_port_fc : Check status of virtual volumes
                       loss_sync ->            Warning
                       config_wait ->          Warning
                       login_wait ->           Warning
                       non_participate ->      Warning
                       error ->                Critical

       check_cap_ssd : Check used SSD capacity
                       >= $PCWARNINGSSD ->      Warning
                       >= $PCCRITICALSSD ->     Critical

       check_cap_fc :  Check used FC capacity
                       >= $PCWARNINGFC ->      Warning
                       >= $PCCRITICALFC ->     Critical

       check_cap_nl : Check used NL capacity 
                       >= $PCWARNINGNL ->      Warning
                       >= $PCCRITICALNL ->     Critical

       check_ps : Check Power Supply Node and Cage
                       Degraded ->             Warning
                       Failed ->               Critical
