Научится настраивать протокол OSPF в Linux-based системах.

## стенд

Из корня `ospf-hw`:

```bash
root@nfsc:~/ospf-hw# ansible-galaxy collection install -r ansible/requirements.yml
vagrant validate
vagrant up --provider=virtualbox
vagrant status
Starting galaxy collection install process
Nothing to do. All requested collections are already installed. If you want to reinstall them, consider using `--force`.
==> router1: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router1: This is very often used by the router and can cause the
==> router1: network to not work properly. If the network doesn't work
==> router1: properly, try changing this IP.
==> router1: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router1: This is very often used by the router and can cause the
==> router1: network to not work properly. If the network doesn't work
==> router1: properly, try changing this IP.
==> router1: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router1: This is very often used by the router and can cause the
==> router1: network to not work properly. If the network doesn't work
==> router1: properly, try changing this IP.
==> router2: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router2: This is very often used by the router and can cause the
==> router2: network to not work properly. If the network doesn't work
==> router2: properly, try changing this IP.
==> router3: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router3: This is very often used by the router and can cause the
==> router3: network to not work properly. If the network doesn't work
==> router3: properly, try changing this IP.
==> router3: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router3: This is very often used by the router and can cause the
==> router3: network to not work properly. If the network doesn't work
==> router3: properly, try changing this IP.
Vagrantfile validated successfully.
Bringing machine 'router1' up with 'virtualbox' provider...
Bringing machine 'router2' up with 'virtualbox' provider...
Bringing machine 'router3' up with 'virtualbox' provider...
==> router1: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router1: This is very often used by the router and can cause the
==> router1: network to not work properly. If the network doesn't work
==> router1: properly, try changing this IP.
==> router1: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router1: This is very often used by the router and can cause the
==> router1: network to not work properly. If the network doesn't work
==> router1: properly, try changing this IP.
==> router1: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router1: This is very often used by the router and can cause the
==> router1: network to not work properly. If the network doesn't work
==> router1: properly, try changing this IP.
==> router1: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router1: This is very often used by the router and can cause the
==> router1: network to not work properly. If the network doesn't work
==> router1: properly, try changing this IP.
==> router1: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router1: This is very often used by the router and can cause the
==> router1: network to not work properly. If the network doesn't work
==> router1: properly, try changing this IP.
==> router1: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router1: This is very often used by the router and can cause the
==> router1: network to not work properly. If the network doesn't work
==> router1: properly, try changing this IP.
==> router1: Checking if box 'generic/ubuntu2004' version '4.3.12' is up to date...
==> router1: Clearing any previously set forwarded ports...
==> router1: Fixed port collision for 22 => 2222. Now on port 2201.
==> router1: Clearing any previously set network interfaces...
==> router1: Preparing network interfaces based on configuration...
    router1: Adapter 1: nat
    router1: Adapter 2: intnet
    router1: Adapter 3: intnet
    router1: Adapter 4: intnet
    router1: Adapter 5: hostonly
==> router1: Forwarding ports...
    router1: 22 (guest) => 2201 (host) (adapter 1)
==> router1: Running 'pre-boot' VM customizations...
==> router1: Booting VM...
==> router1: Waiting for machine to boot. This may take a few minutes...
    router1: SSH address: 127.0.0.1:2201
    router1: SSH username: vagrant
    router1: SSH auth method: private key
    router1: Warning: Connection reset. Retrying...
    router1: Warning: Connection reset. Retrying...
    router1: Warning: Connection reset. Retrying...
    router1: Warning: Connection reset. Retrying...
    router1: Warning: Connection reset. Retrying...
    router1: Warning: Connection reset. Retrying...
==> router1: Machine booted and ready!
==> router1: Checking for guest additions in VM...
    router1: The guest additions on this VM do not match the installed version of
    router1: VirtualBox! In most cases this is fine, but in rare cases it can
    router1: prevent things such as shared folders from working properly. If you see
    router1: shared folder errors, please make sure the guest additions within the
    router1: virtual machine match the version of VirtualBox you have installed on
    router1: your host and reload your VM.
    router1:
    router1: Guest Additions Version: 6.1.38
    router1: VirtualBox Version: 7.0
==> router1: Setting hostname...
==> router1: Configuring and enabling network interfaces...
==> router1: Machine already provisioned. Run `vagrant provision` or use the `--provision`
==> router1: flag to force provisioning. Provisioners marked to run always will still run.
==> router2: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router2: This is very often used by the router and can cause the
==> router2: network to not work properly. If the network doesn't work
==> router2: properly, try changing this IP.
==> router2: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router2: This is very often used by the router and can cause the
==> router2: network to not work properly. If the network doesn't work
==> router2: properly, try changing this IP.
==> router2: Checking if box 'generic/ubuntu2004' version '4.3.12' is up to date...
==> router2: Clearing any previously set forwarded ports...
==> router2: Fixed port collision for 22 => 2222. Now on port 2202.
==> router2: Clearing any previously set network interfaces...
==> router2: Preparing network interfaces based on configuration...
    router2: Adapter 1: nat
    router2: Adapter 2: intnet
    router2: Adapter 3: intnet
    router2: Adapter 4: intnet
    router2: Adapter 5: hostonly
==> router2: Forwarding ports...
    router2: 22 (guest) => 2202 (host) (adapter 1)
==> router2: Running 'pre-boot' VM customizations...
==> router2: Booting VM...
==> router2: Waiting for machine to boot. This may take a few minutes...
    router2: SSH address: 127.0.0.1:2202
    router2: SSH username: vagrant
    router2: SSH auth method: private key
    router2: Warning: Connection reset. Retrying...
    router2: Warning: Connection reset. Retrying...
    router2: Warning: Connection reset. Retrying...
    router2: Warning: Connection reset. Retrying...
    router2: Warning: Connection reset. Retrying...
==> router2: Machine booted and ready!
==> router2: Checking for guest additions in VM...
    router2: The guest additions on this VM do not match the installed version of
    router2: VirtualBox! In most cases this is fine, but in rare cases it can
    router2: prevent things such as shared folders from working properly. If you see
    router2: shared folder errors, please make sure the guest additions within the
    router2: virtual machine match the version of VirtualBox you have installed on
    router2: your host and reload your VM.
    router2:
    router2: Guest Additions Version: 6.1.38
    router2: VirtualBox Version: 7.0
==> router2: Setting hostname...
==> router2: Configuring and enabling network interfaces...
==> router2: Machine already provisioned. Run `vagrant provision` or use the `--provision`
==> router2: flag to force provisioning. Provisioners marked to run always will still run.
==> router3: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router3: This is very often used by the router and can cause the
==> router3: network to not work properly. If the network doesn't work
==> router3: properly, try changing this IP.
==> router3: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router3: This is very often used by the router and can cause the
==> router3: network to not work properly. If the network doesn't work
==> router3: properly, try changing this IP.
==> router3: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router3: This is very often used by the router and can cause the
==> router3: network to not work properly. If the network doesn't work
==> router3: properly, try changing this IP.
==> router3: You assigned a static IP ending in ".1" or ":1" to this machine.
==> router3: This is very often used by the router and can cause the
==> router3: network to not work properly. If the network doesn't work
==> router3: properly, try changing this IP.
==> router3: Checking if box 'generic/ubuntu2004' version '4.3.12' is up to date...
==> router3: Clearing any previously set forwarded ports...
==> router3: Fixed port collision for 22 => 2222. Now on port 2203.
==> router3: Clearing any previously set network interfaces...
==> router3: Preparing network interfaces based on configuration...
    router3: Adapter 1: nat
    router3: Adapter 2: intnet
    router3: Adapter 3: intnet
    router3: Adapter 4: intnet
    router3: Adapter 5: hostonly
==> router3: Forwarding ports...
    router3: 22 (guest) => 2203 (host) (adapter 1)
==> router3: Running 'pre-boot' VM customizations...
==> router3: Booting VM...
==> router3: Waiting for machine to boot. This may take a few minutes...
    router3: SSH address: 127.0.0.1:2203
    router3: SSH username: vagrant
    router3: SSH auth method: private key
    router3: Warning: Connection reset. Retrying...
    router3: Warning: Connection reset. Retrying...
    router3: Warning: Connection reset. Retrying...
    router3: Warning: Connection reset. Retrying...
    router3: Warning: Connection reset. Retrying...
    router3: Warning: Connection reset. Retrying...
==> router3: Machine booted and ready!
==> router3: Checking for guest additions in VM...
    router3: The guest additions on this VM do not match the installed version of
    router3: VirtualBox! In most cases this is fine, but in rare cases it can
    router3: prevent things such as shared folders from working properly. If you see
    router3: shared folder errors, please make sure the guest additions within the
    router3: virtual machine match the version of VirtualBox you have installed on
    router3: your host and reload your VM.
    router3:
    router3: Guest Additions Version: 6.1.38
    router3: VirtualBox Version: 7.0
==> router3: Setting hostname...
==> router3: Configuring and enabling network interfaces...
==> router3: Machine already provisioned. Run `vagrant provision` or use the `--provision`
==> router3: flag to force provisioning. Provisioners marked to run always will still run.
Current machine states:

router1                   running (virtualbox)
router2                   running (virtualbox)
router3                   running (virtualbox)

This environment represents multiple VMs. The VMs are all listed
above with their current state. For more information about a specific
VM, run `vagrant status NAME`.
root@nfsc:~/ospf-hw#

```

##  Проверка соседство и маршруты OSPF

Из корня проекта:

```bash
root@nfsc:~/ospf-hw# for router in router1 router2 router3; do
  echo "=== $router ==="
  vagrant ssh "$router" -c 'sudo vtysh -c "show ip ospf neighbor" -c "show ip route ospf"'
done
=== router1 ===

Neighbor ID     Pri State           Up Time         Dead Time Address         Interface                        RXmtL RqstL DBsmL
3.3.3.3           1 Full/Backup     4m51s             37.198s 10.0.12.2       eth2:10.0.12.1                       0     0     0
2.2.2.2           1 Full/Backup     9m53s             38.488s 10.0.10.2       eth1:10.0.10.1                       0     0     0

Codes: K - kernel route, C - connected, L - local, S - static,
       R - RIP, O - OSPF, I - IS-IS, B - BGP, E - EIGRP, N - NHRP,
       T - Table, v - VNC, V - VNC-Direct, A - Babel, F - PBR,
       f - OpenFabric, t - Table-Direct,
       > - selected route, * - FIB route, q - queued, r - rejected, b - backup
       t - trapped, o - offload failure

IPv4 unicast VRF default:
O   0.0.0.0/0 [110/1] via 10.0.10.2, eth1, weight 1, 00:04:50
                      via 10.0.12.2, eth2, weight 1, 00:04:50
O>* 10.0.11.0/30 [110/20] via 10.0.10.2, eth1, weight 1, 00:04:51
  *                       via 10.0.12.2, eth2, weight 1, 00:04:51
O>* 192.168.20.0/24 [110/20] via 10.0.10.2, eth1, weight 1, 00:09:48
O>* 192.168.30.0/24 [110/20] via 10.0.12.2, eth2, weight 1, 00:04:51
=== router2 ===

Neighbor ID     Pri State           Up Time         Dead Time Address         Interface                        RXmtL RqstL DBsmL
3.3.3.3           1 Full/Backup     5m09s             32.682s 10.0.11.1       eth2:10.0.11.2                       0     0     0
1.1.1.1           1 Full/DR         10m06s            35.246s 10.0.10.1       eth1:10.0.10.2                       0     0     0

Codes: K - kernel route, C - connected, L - local, S - static,
       R - RIP, O - OSPF, I - IS-IS, B - BGP, E - EIGRP, N - NHRP,
       T - Table, v - VNC, V - VNC-Direct, A - Babel, F - PBR,
       f - OpenFabric, t - Table-Direct,
       > - selected route, * - FIB route, q - queued, r - rejected, b - backup
       t - trapped, o - offload failure

IPv4 unicast VRF default:
O   0.0.0.0/0 [110/1] via 10.0.10.1, eth1, weight 1, 00:05:03
                      via 10.0.11.1, eth2, weight 1, 00:05:03
O>* 10.0.12.0/30 [110/20] via 10.0.10.1, eth1, weight 1, 00:05:04
  *                       via 10.0.11.1, eth2, weight 1, 00:05:04
O>* 192.168.10.0/24 [110/20] via 10.0.10.1, eth1, weight 1, 00:10:01
O>* 192.168.30.0/24 [110/20] via 10.0.11.1, eth2, weight 1, 00:05:04
=== router3 ===

Neighbor ID     Pri State           Up Time         Dead Time Address         Interface                        RXmtL RqstL DBsmL
2.2.2.2           1 Full/DR         5m34s             38.668s 10.0.11.2       eth1:10.0.11.1                       0     0     0
1.1.1.1           1 Full/DR         5m29s             37.565s 10.0.12.1       eth2:10.0.12.2                       0     0     0

Codes: K - kernel route, C - connected, L - local, S - static,
       R - RIP, O - OSPF, I - IS-IS, B - BGP, E - EIGRP, N - NHRP,
       T - Table, v - VNC, V - VNC-Direct, A - Babel, F - PBR,
       f - OpenFabric, t - Table-Direct,
       > - selected route, * - FIB route, q - queued, r - rejected, b - backup
       t - trapped, o - offload failure

IPv4 unicast VRF default:
O   0.0.0.0/0 [110/1] via 10.0.11.2, eth1, weight 1, 00:05:24
                      via 10.0.12.1, eth2, weight 1, 00:05:24
O>* 10.0.10.0/30 [110/20] via 10.0.11.2, eth1, weight 1, 00:05:25
  *                       via 10.0.12.1, eth2, weight 1, 00:05:25
O>* 192.168.10.0/24 [110/20] via 10.0.12.1, eth2, weight 1, 00:05:25
O>* 192.168.20.0/24 [110/20] via 10.0.11.2, eth1, weight 1, 00:05:30
root@nfsc:~/ospf-hw#

```

##  Проверка асимметричный маршрут


```bash
root@nfsc:~/ospf-hw# grep -n 'ifname:' ansible/host_vars/router*.yml
sed -i -e 's/\benp0s8\b/eth1/g' -e 's/\benp0s9\b/eth2/g' ansible/host_vars/router*.yml

ANSIBLE_CONFIG=ansible/ansible.cfg ansible-playbook \
  -i ansible/hosts ansible/provision.yml -t setup_ospf \
  -e '{"symmetric_routing": false}'
ansible/host_vars/router1.yml:5:  - ifname: enp0s8
ansible/host_vars/router1.yml:13:  - ifname: enp0s9
ansible/host_vars/router1.yml:21:  - ifname: enp0s10
ansible/host_vars/router2.yml:5:  - ifname: enp0s8
ansible/host_vars/router2.yml:13:  - ifname: enp0s9
ansible/host_vars/router2.yml:21:  - ifname: enp0s10
ansible/host_vars/router3.yml:5:  - ifname: enp0s8
ansible/host_vars/router3.yml:13:  - ifname: enp0s9
ansible/host_vars/router3.yml:21:  - ifname: enp0s10

PLAY [OSPF lab (FRR)] *******************************************************************************************************************************************************************************************************

TASK [Gathering Facts] ******************************************************************************************************************************************************************************************************
ok: [router1]
ok: [router3]
ok: [router2]

TASK [frr_ospf : Сгенерировать /etc/frr/frr.conf по host_vars этого роутера] ************************************************************************************************************************************************
changed: [router1]
changed: [router3]
changed: [router2]

RUNNING HANDLER [frr_ospf : restart frr] ************************************************************************************************************************************************************************************
changed: [router1]
changed: [router3]
changed: [router2]

PLAY RECAP ******************************************************************************************************************************************************************************************************************
router1                    : ok=3    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
router2                    : ok=3    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
router3                    : ok=3    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

root@nfsc:~/ospf-hw# ANSIBLE_CONFIG=ansible/ansible.cfg ansible-playbook \
  -i ansible/hosts ansible/provision.yml -t setup_ospf \
  -e '{"symmetric_routing": false}'

PLAY [OSPF lab (FRR)] *******************************************************************************************************************************************************************************************************

TASK [Gathering Facts] ******************************************************************************************************************************************************************************************************
ok: [router1]
ok: [router3]
ok: [router2]

TASK [frr_ospf : Сгенерировать /etc/frr/frr.conf по host_vars этого роутера] ************************************************************************************************************************************************
ok: [router1]
ok: [router3]
ok: [router2]

PLAY RECAP ******************************************************************************************************************************************************************************************************************
router1                    : ok=2    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
router2                    : ok=2    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
router3                    : ok=2    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

root@nfsc:~/ospf-hw# vagrant ssh router1 -c 'ip route get 192.168.20.1 from 192.168.10.1'
192.168.20.1 from 192.168.10.1 via 10.0.12.2 dev eth2 uid 1000
    cache
root@nfsc:~/ospf-hw# vagrant ssh router2 -c 'ip route get 192.168.10.1 from 192.168.20.1'
192.168.10.1 from 192.168.20.1 via 10.0.10.1 dev eth1 uid 1000
    cache
root@nfsc:~/ospf-hw#
```

##  Проверка симметричный маршрут с дорогим линком

Команда задаёт стоимость `1000` на обоих концах прямого линка `router1–router2`.

```bash
root@nfsc:~/ospf-hw# ANSIBLE_CONFIG=ansible/ansible.cfg ansible-playbook \
  -i ansible/hosts ansible/provision.yml -t setup_ospf \
  -e '{"symmetric_routing": true}'

PLAY [OSPF lab (FRR)] *******************************************************************************************************************************************************************************************************

TASK [Gathering Facts] ******************************************************************************************************************************************************************************************************
ok: [router1]
ok: [router3]
ok: [router2]

TASK [frr_ospf : Сгенерировать /etc/frr/frr.conf по host_vars этого роутера] ************************************************************************************************************************************************
ok: [router1]
ok: [router3]
changed: [router2]

RUNNING HANDLER [frr_ospf : restart frr] ************************************************************************************************************************************************************************************
changed: [router2]

PLAY RECAP ******************************************************************************************************************************************************************************************************************
router1                    : ok=2    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
router2                    : ok=3    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
router3                    : ok=2    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

root@nfsc:~/ospf-hw# vagrant ssh router1 -c 'sudo vtysh -c "show ip ospf interface eth1"'
vagrant ssh router2 -c 'sudo vtysh -c "show ip ospf interface eth1"'

vagrant ssh router1 -c 'ip route get 192.168.20.1 from 192.168.10.1'
vagrant ssh router2 -c 'ip route get 192.168.10.1 from 192.168.20.1'
eth1 is up
  ifindex 3, MTU 1500 bytes, BW 0 Mbit <UP,LOWER_UP,BROADCAST,RUNNING,MULTICAST>
  Internet Address 10.0.10.1/30, Broadcast 10.0.10.3, Area 0.0.0.0
  MTU mismatch detection: disabled
  Router ID 1.1.1.1, Network Type BROADCAST, Cost: 1000
  Transmit Delay is 1 sec, State DR, Priority 1
  Designated Router (ID) 1.1.1.1 Interface Address 10.0.10.1/30
  Backup Designated Router (ID) 2.2.2.2, Interface Address 10.0.10.2
  Multicast group memberships: OSPFAllRouters OSPFDesignatedRouters
  Timer intervals configured, Hello 10s, Dead 30s, Wait 30s, Retransmit 5
    Hello due in 3.279s
  Neighbor Count is 1, Adjacent neighbor count is 1
  Graceful Restart hello delay: 10s
  LSA retransmissions: 7

eth1 is up
  ifindex 3, MTU 1500 bytes, BW 0 Mbit <UP,LOWER_UP,BROADCAST,RUNNING,MULTICAST>
  Internet Address 10.0.10.2/30, Broadcast 10.0.10.3, Area 0.0.0.0
  MTU mismatch detection: disabled
  Router ID 2.2.2.2, Network Type BROADCAST, Cost: 1000
  Transmit Delay is 1 sec, State Backup, Priority 1
  Designated Router (ID) 1.1.1.1 Interface Address 10.0.10.1/30
  Backup Designated Router (ID) 2.2.2.2, Interface Address 10.0.10.2
  Multicast group memberships: OSPFAllRouters OSPFDesignatedRouters
  Timer intervals configured, Hello 10s, Dead 30s, Wait 30s, Retransmit 5
    Hello due in 2.679s
  Neighbor Count is 1, Adjacent neighbor count is 1
  Graceful Restart hello delay: 10s
  LSA retransmissions: 3

192.168.20.1 from 192.168.10.1 via 10.0.12.2 dev eth2 uid 1000
    cache
192.168.10.1 from 192.168.20.1 via 10.0.11.1 dev eth2 uid 1000
    cache
root@nfsc:~/ospf-hw#

```
