This is the result of running `./airship-in-a-bottle.sh > thefilewhereitsredirected` on a fresh [ubuntu 16.04](http://releases.ubuntu.com/16.04/) install with updates


```
Welcome to Airship in a Bottle

 /--------------------\
|                      \
|        |---|          \----
|        | x |                \
|        |---|                 |
|          |                  /
|     \____|____/       /----
|                      /
 \--------------------/


A prototype example of deploying the Airship suite on a single VM.


This example will run through:
 - Setup
 - Genesis of Airship (Kubernetes)
 - Basic deployment of Openstack (including Nova, Neutron, and Horizon using Openstack Helm)
 - VM creation automation using Heat

The expected runtime of this script is greater than 1 hour


The minimum recommended size of the Ubuntu 16.04 VM is 4 vCPUs, 20GB of RAM with 32GB disk space.
Let's collect some information about your VM to get started.
Updating /etc/hosts with: 10.0.0.38 airsHiP
10.0.0.38 airsHiP
Not changing DNS servers, /etc/resolv.conf already updated.

Starting Airship deployment...
1 package can be upgraded. Run 'apt list --upgradable' to see it.
Reading package lists...
Building dependency tree...
Reading state information...
nmap is already the newest version (7.01-2ubuntu2).
nfs-common is already the newest version (1:1.2.8-9ubuntu12.2).
jq is already the newest version (1.5+dfsg-1ubuntu0.1).
The following package was automatically installed and is no longer required:
  snapd-login-service
Use 'sudo apt autoremove' to remove it.
Suggested packages:
  aufs-tools btrfs-tools debootstrap docker-doc rinse zfs-fuse | zfsutils
Recommended packages:
  cgroupfs-mount | cgroup-lite pigz ubuntu-fan
The following packages will be REMOVED:
  docker-ce
The following NEW packages will be installed:
  docker.io
0 upgraded, 1 newly installed, 1 to remove and 0 not upgraded.
Need to get 30,4 MB of archives.
After this operation, 65,8 MB of additional disk space will be used.
Get:1 http://be.archive.ubuntu.com/ubuntu xenial-updates/universe amd64 docker.io amd64 18.09.5-0ubuntu1~16.04.2 [30,4 MB]
Preconfiguring packages ...
Fetched 30,4 MB in 16s (1.879 kB/s)
(Reading database ... 
(Reading database ... 5%
(Reading database ... 10%
(Reading database ... 15%
(Reading database ... 20%
(Reading database ... 25%
(Reading database ... 30%
(Reading database ... 35%
(Reading database ... 40%
(Reading database ... 45%
(Reading database ... 50%
(Reading database ... 55%
(Reading database ... 60%
(Reading database ... 65%
(Reading database ... 70%
(Reading database ... 75%
(Reading database ... 80%
(Reading database ... 85%
(Reading database ... 90%
(Reading database ... 95%
(Reading database ... 100%
(Reading database ... 216836 files and directories currently installed.)
Removing docker-ce (17.03.3~ce-0~ubuntu-xenial) ...
Processing triggers for man-db (2.7.5-1) ...
Selecting previously unselected package docker.io.
(Reading database ... 
(Reading database ... 5%
(Reading database ... 10%
(Reading database ... 15%
(Reading database ... 20%
(Reading database ... 25%
(Reading database ... 30%
(Reading database ... 35%
(Reading database ... 40%
(Reading database ... 45%
(Reading database ... 50%
(Reading database ... 55%
(Reading database ... 60%
(Reading database ... 65%
(Reading database ... 70%
(Reading database ... 75%
(Reading database ... 80%
(Reading database ... 85%
(Reading database ... 90%
(Reading database ... 95%
(Reading database ... 100%
(Reading database ... 216634 files and directories currently installed.)
Preparing to unpack .../docker.io_18.09.5-0ubuntu1~16.04.2_amd64.deb ...
Unpacking docker.io (18.09.5-0ubuntu1~16.04.2) ...
Processing triggers for ureadahead (0.100.0-19.1) ...
ureadahead will be reprofiled on next reboot
Processing triggers for systemd (229-4ubuntu21.21) ...
Processing triggers for man-db (2.7.5-1) ...
Setting up docker.io (18.09.5-0ubuntu1~16.04.2) ...
Installing new version of config file /etc/init.d/docker ...
Installing new version of config file /etc/init/docker.conf ...
Processing triggers for ureadahead (0.100.0-19.1) ...
Processing triggers for systemd (229-4ubuntu21.21) ...
This is a good time to grab a coffee :)
~/deploy ~/deploy/treasuremap/tools/deployment/aiab
~/deploy/treasuremap/tools/deployment/aiab
=== Generating updated certificates ===
~/deploy ~/deploy/treasuremap/tools/deployment/aiab
~/deploy/treasuremap/tools/deployment/aiab
~/deploy ~/deploy/treasuremap/tools/deployment/aiab
~/deploy/treasuremap/tools/deployment/aiab
~/deploy ~/deploy/treasuremap/tools/deployment/aiab
~/deploy/treasuremap/tools/deployment/aiab
usr/local/bin/debug-report.sh
usr/local/bin/kubectl
usr/local/bin/promenade-teardown
etc/resolv.conf
etc/hosts
etc/docker/daemon.json
etc/promenade/haproxy/haproxy.cfg
etc/kubernetes/kubeconfig
etc/kubernetes/admin/kubeconfig.yaml
etc/kubernetes/admin/pki/cluster-ca.pem
etc/kubernetes/admin/pki/admin-key.pem
etc/kubernetes/admin/pki/admin.pem
etc/kubernetes/manifests/haproxy.yaml
etc/kubernetes/pki/kubelet-key.pem
etc/kubernetes/pki/kubelet-client-ca.pem
etc/kubernetes/pki/kubelet.pem
etc/kubernetes/pki/cluster-ca.pem
etc/systemd/system/kubelet.service
etc/systemd/system/docker.service.d/http-proxy.conf
etc/apt/sources.list.d/promenade-sources.list
usr/local/bin/helm
usr/local/bin/armada
etc/kubernetes/manifests/kubernetes-apiserver.yaml
etc/kubernetes/manifests/auxiliary-kubernetes-etcd.yaml
etc/kubernetes/manifests/bootstrap-armada.yaml
etc/kubernetes/manifests/kubernetes-controller-manager.yaml
etc/kubernetes/manifests/kubernetes-etcd.yaml
etc/kubernetes/manifests/kubernetes-scheduler.yaml
etc/genesis/etcd/pki/peer-ca.pem
etc/genesis/etcd/pki/etcd-peer-key.pem
etc/genesis/etcd/pki/client-ca.pem
etc/genesis/etcd/pki/etcd-client.pem
etc/genesis/etcd/pki/etcd-peer.pem
etc/genesis/etcd/pki/etcd-client-key.pem
etc/genesis/scheduler/kubeconfig.yaml
etc/genesis/scheduler/pki/cluster-ca.pem
etc/genesis/scheduler/pki/scheduler-key.pem
etc/genesis/scheduler/pki/scheduler.pem
etc/genesis/controller-manager/kubeconfig.yaml
etc/genesis/controller-manager/pki/service-account.key
etc/genesis/controller-manager/pki/controller-manager.pem
etc/genesis/controller-manager/pki/cluster-ca.pem
etc/genesis/controller-manager/pki/controller-manager-key.pem
etc/genesis/apiserver/pki/apiserver.pem
etc/genesis/apiserver/pki/kubelet-client.pem
etc/genesis/apiserver/pki/service-account.pub
etc/genesis/apiserver/pki/etcd-client-ca.pem
etc/genesis/apiserver/pki/apiserver-key.pem
etc/genesis/apiserver/pki/kubelet-client-ca.pem
etc/genesis/apiserver/pki/cluster-ca.pem
etc/genesis/apiserver/pki/etcd-client.pem
etc/genesis/apiserver/pki/etcd-client-key.pem
etc/genesis/apiserver/pki/kubelet-client-key.pem
etc/genesis/armada/assets/manifest.yaml
etc/genesis/armada/auth/config
etc/genesis/armada/auth/pki/armada-key.pem
etc/genesis/armada/auth/pki/cluster-ca.pem
etc/genesis/armada/auth/pki/armada.pem
etc/genesis/armada-cli/auth/config
etc/genesis/armada-cli/auth/pki/armada-key.pem
etc/genesis/armada-cli/auth/pki/cluster-ca.pem
etc/genesis/armada-cli/auth/pki/armada.pem
opt/kubernetes/bin/kubelet
etc/logrotate.d/json-logrotate
var/lib/kubelet/.dockercfg
var/lib/prom.done
var/lib/anchor/calico-etcd-bootstrap
etc/genesis/armada/assets/charts/.gitignore
etc/genesis/armada/assets/charts/haproxy/requirements.yaml
etc/genesis/armada/assets/charts/haproxy/Chart.yaml
etc/genesis/armada/assets/charts/haproxy/values.yaml
etc/genesis/armada/assets/charts/haproxy/templates/configmap-bin.yaml
etc/genesis/armada/assets/charts/haproxy/templates/rbac.yaml
etc/genesis/armada/assets/charts/haproxy/templates/configmap-etc.yaml
etc/genesis/armada/assets/charts/haproxy/templates/daemonset.yaml
etc/genesis/armada/assets/charts/haproxy/templates/tests/test-haproxy-health.yaml
etc/genesis/armada/assets/charts/haproxy/templates/etc/_haproxy.yaml.tpl
etc/genesis/armada/assets/charts/haproxy/templates/bin/_pre_stop.tpl
etc/genesis/armada/assets/charts/haproxy/templates/bin/_anchor.tpl
etc/genesis/armada/assets/charts/coredns/requirements.yaml
etc/genesis/armada/assets/charts/coredns/Chart.yaml
etc/genesis/armada/assets/charts/coredns/values.yaml
etc/genesis/armada/assets/charts/coredns/templates/service.yaml
etc/genesis/armada/assets/charts/coredns/templates/configmap-bin.yaml
etc/genesis/armada/assets/charts/coredns/templates/rbac.yaml
etc/genesis/armada/assets/charts/coredns/templates/configmap-etc.yaml
etc/genesis/armada/assets/charts/coredns/templates/pod-test.yaml
etc/genesis/armada/assets/charts/coredns/templates/deployment.yaml
etc/genesis/armada/assets/charts/coredns/templates/bin/_probe.sh.tpl
etc/genesis/armada/assets/charts/promenade/requirements.yaml
etc/genesis/armada/assets/charts/promenade/Chart.yaml
etc/genesis/armada/assets/charts/promenade/values.yaml
etc/genesis/armada/assets/charts/promenade/templates/configmap-bin.yaml
etc/genesis/armada/assets/charts/promenade/templates/secret-keystone-env.yaml
etc/genesis/armada/assets/charts/promenade/templates/rbac.yaml
etc/genesis/armada/assets/charts/promenade/templates/job-ks-service.yaml
etc/genesis/armada/assets/charts/promenade/templates/configmap-etc.yaml
etc/genesis/armada/assets/charts/promenade/templates/deployment-api.yaml
etc/genesis/armada/assets/charts/promenade/templates/job-ks-endpoints.yaml
etc/genesis/armada/assets/charts/promenade/templates/job-ks-user.yaml
etc/genesis/armada/assets/charts/promenade/templates/service-api.yaml
etc/genesis/armada/assets/charts/promenade/templates/tests/test-promenade-api.yaml
etc/genesis/armada/assets/charts/proxy/requirements.yaml
etc/genesis/armada/assets/charts/proxy/Chart.yaml
etc/genesis/armada/assets/charts/proxy/values.yaml
etc/genesis/armada/assets/charts/proxy/templates/configmap-bin.yaml
etc/genesis/armada/assets/charts/proxy/templates/rbac.yaml
etc/genesis/armada/assets/charts/proxy/templates/daemonset.yaml
etc/genesis/armada/assets/charts/proxy/templates/bin/_liveness-probe.sh.tpl
etc/genesis/armada/assets/charts/proxy/templates/bin/_readiness-probe.sh.tpl
etc/genesis/armada/assets/charts/etcd/requirements.yaml
etc/genesis/armada/assets/charts/etcd/Chart.yaml
etc/genesis/armada/assets/charts/etcd/values.yaml
etc/genesis/armada/assets/charts/etcd/templates/service.yaml
etc/genesis/armada/assets/charts/etcd/templates/configmap-bin.yaml
etc/genesis/armada/assets/charts/etcd/templates/daemonset-anchor.yaml
etc/genesis/armada/assets/charts/etcd/templates/secret-keys.yaml
etc/genesis/armada/assets/charts/etcd/templates/configmap-etc.yaml
etc/genesis/armada/assets/charts/etcd/templates/cron-job-etcd-backup.yaml
etc/genesis/armada/assets/charts/etcd/templates/configmap-certs.yaml
etc/genesis/armada/assets/charts/etcd/templates/tests/test-etcd-health.yaml
etc/genesis/armada/assets/charts/etcd/templates/etc/_kubernetes-etcd.yaml.tpl
etc/genesis/armada/assets/charts/etcd/templates/bin/_readiness.tpl
etc/genesis/armada/assets/charts/etcd/templates/bin/_etcdbackup.tpl
etc/genesis/armada/assets/charts/etcd/templates/bin/_pre_stop.tpl
etc/genesis/armada/assets/charts/etcd/templates/bin/_etcdctl_anchor.tpl
etc/genesis/armada/assets/charts/apiserver-webhook/requirements.yaml
etc/genesis/armada/assets/charts/apiserver-webhook/Chart.yaml
etc/genesis/armada/assets/charts/apiserver-webhook/values.yaml
etc/genesis/armada/assets/charts/apiserver-webhook/templates/service.yaml
etc/genesis/armada/assets/charts/apiserver-webhook/templates/configmap-bin.yaml
etc/genesis/armada/assets/charts/apiserver-webhook/templates/secret-tls.yaml
etc/genesis/armada/assets/charts/apiserver-webhook/templates/secret-keystone.yaml
etc/genesis/armada/assets/charts/apiserver-webhook/templates/ingress-api.yaml
etc/genesis/armada/assets/charts/apiserver-webhook/templates/service-ingress-api.yaml
etc/genesis/armada/assets/charts/apiserver-webhook/templates/configmap-etc.yaml
etc/genesis/armada/assets/charts/apiserver-webhook/templates/job-ks-user.yaml
etc/genesis/armada/assets/charts/apiserver-webhook/templates/deployment.yaml
etc/genesis/armada/assets/charts/apiserver-webhook/templates/etc/_webhook.kubeconfig.tpl
etc/genesis/armada/assets/charts/apiserver-webhook/templates/bin/_webhook_start.sh.tpl
etc/genesis/armada/assets/charts/scheduler/requirements.yaml
etc/genesis/armada/assets/charts/scheduler/Chart.yaml
etc/genesis/armada/assets/charts/scheduler/values.yaml
etc/genesis/armada/assets/charts/scheduler/templates/configmap-bin.yaml
etc/genesis/armada/assets/charts/scheduler/templates/sched-anchor.yaml
etc/genesis/armada/assets/charts/scheduler/templates/configmap-etc.yaml
etc/genesis/armada/assets/charts/scheduler/templates/secret.yaml
etc/genesis/armada/assets/charts/scheduler/templates/etc/_kubernetes-scheduler.yaml.tpl
etc/genesis/armada/assets/charts/scheduler/templates/etc/_kubeconfig.yaml.tpl
etc/genesis/armada/assets/charts/scheduler/templates/bin/_pre_stop.tpl
etc/genesis/armada/assets/charts/scheduler/templates/bin/_anchor.tpl
etc/genesis/armada/assets/charts/controller_manager/requirements.yaml
etc/genesis/armada/assets/charts/controller_manager/Chart.yaml
etc/genesis/armada/assets/charts/controller_manager/values.yaml
etc/genesis/armada/assets/charts/controller_manager/templates/configmap-bin.yaml
etc/genesis/armada/assets/charts/controller_manager/templates/configmap-etc.yaml
etc/genesis/armada/assets/charts/controller_manager/templates/secret.yaml
etc/genesis/armada/assets/charts/controller_manager/templates/daemonset.yaml
etc/genesis/armada/assets/charts/controller_manager/templates/etc/_kubernetes-controller-manager.yaml.tpl
etc/genesis/armada/assets/charts/controller_manager/templates/etc/_kubeconfig.yaml.tpl
etc/genesis/armada/assets/charts/controller_manager/templates/bin/_pre_stop.tpl
etc/genesis/armada/assets/charts/controller_manager/templates/bin/_anchor.tpl
etc/genesis/armada/assets/charts/apiserver/requirements.yaml
etc/genesis/armada/assets/charts/apiserver/Chart.yaml
etc/genesis/armada/assets/charts/apiserver/values.yaml
etc/genesis/armada/assets/charts/apiserver/templates/service.yaml
etc/genesis/armada/assets/charts/apiserver/templates/configmap-bin.yaml
etc/genesis/armada/assets/charts/apiserver/templates/rbac.yaml
etc/genesis/armada/assets/charts/apiserver/templates/ingress-api.yaml
etc/genesis/armada/assets/charts/apiserver/templates/configmap-etc.yaml
etc/genesis/armada/assets/charts/apiserver/templates/service-apiserver-ingress.yaml
etc/genesis/armada/assets/charts/apiserver/templates/secret-ingress-tls.yaml
etc/genesis/armada/assets/charts/apiserver/templates/secret-apiserver.yaml
etc/genesis/armada/assets/charts/apiserver/templates/configmap-certs.yaml
etc/genesis/armada/assets/charts/apiserver/templates/daemonset.yaml
etc/genesis/armada/assets/charts/apiserver/templates/etc/_kubernetes-apiserver.yaml.tpl
etc/genesis/armada/assets/charts/apiserver/templates/etc/_kubeconfig.yaml.tpl
etc/genesis/armada/assets/charts/apiserver/templates/bin/_pre_stop.tpl
etc/genesis/armada/assets/charts/apiserver/templates/bin/_anchor.tpl
OK
Hit:1 https://download.docker.com/linux/ubuntu xenial InRelease
Hit:2 http://be.archive.ubuntu.com/ubuntu xenial InRelease
Hit:3 http://be.archive.ubuntu.com/ubuntu xenial-updates InRelease
Get:4 http://security.ubuntu.com/ubuntu xenial-security InRelease [109 kB]
Hit:5 http://be.archive.ubuntu.com/ubuntu xenial-backports InRelease
Fetched 109 kB in 2s (39,8 kB/s)
Reading package lists...
Reading package lists...
Building dependency tree...
Reading state information...
socat is already the newest version (1.7.3.1-1).
ceph-common is already the newest version (10.2.11-0ubuntu0.16.04.2).
The following packages were automatically installed and are no longer required:
  containerd runc snapd-login-service
Use 'sudo apt autoremove' to remove them.
Recommended packages:
  aufs-tools cgroupfs-mount | cgroup-lite
The following packages will be REMOVED:
  docker.io
The following NEW packages will be installed:
  docker-ce
0 upgraded, 1 newly installed, 1 to remove and 0 not upgraded.
Need to get 0 B/19,4 MB of archives.
After this operation, 65,8 MB disk space will be freed.
(Reading database ... 
(Reading database ... 5%
(Reading database ... 10%
(Reading database ... 15%
(Reading database ... 20%
(Reading database ... 25%
(Reading database ... 30%
(Reading database ... 35%
(Reading database ... 40%
(Reading database ... 45%
(Reading database ... 50%
(Reading database ... 55%
(Reading database ... 60%
(Reading database ... 65%
(Reading database ... 70%
(Reading database ... 75%
(Reading database ... 80%
(Reading database ... 85%
(Reading database ... 90%
(Reading database ... 95%
(Reading database ... 100%
(Reading database ... 216832 files and directories currently installed.)
Removing docker.io (18.09.5-0ubuntu1~16.04.2) ...
'/usr/share/docker.io/contrib/nuke-graph-directory.sh' -> '/var/lib/docker/nuke-graph-directory.sh'
Processing triggers for man-db (2.7.5-1) ...
Selecting previously unselected package docker-ce.
(Reading database ... 
(Reading database ... 5%
(Reading database ... 10%
(Reading database ... 15%
(Reading database ... 20%
(Reading database ... 25%
(Reading database ... 30%
(Reading database ... 35%
(Reading database ... 40%
(Reading database ... 45%
(Reading database ... 50%
(Reading database ... 55%
(Reading database ... 60%
(Reading database ... 65%
(Reading database ... 70%
(Reading database ... 75%
(Reading database ... 80%
(Reading database ... 85%
(Reading database ... 90%
(Reading database ... 95%
(Reading database ... 100%
(Reading database ... 216634 files and directories currently installed.)
Preparing to unpack .../docker-ce_17.03.3~ce-0~ubuntu-xenial_amd64.deb ...
Unpacking docker-ce (17.03.3~ce-0~ubuntu-xenial) ...
Processing triggers for man-db (2.7.5-1) ...
Processing triggers for ureadahead (0.100.0-19.1) ...
Processing triggers for systemd (229-4ubuntu21.21) ...
Setting up docker-ce (17.03.3~ce-0~ubuntu-xenial) ...
Installing new version of config file /etc/init.d/docker ...
Installing new version of config file /etc/init/docker.conf ...
Processing triggers for ureadahead (0.100.0-19.1) ...
Processing triggers for systemd (229-4ubuntu21.21) ...
Unable to connect to the server: EOF
Unable to connect to the server: EOF
E0627 11:11:38.937690       1 round_trippers.go:169] CancelRequest not implemented
Unable to connect to the server: EOF
E0627 11:12:09.786160       1 round_trippers.go:169] CancelRequest not implemented
E0627 11:12:14.786265       1 round_trippers.go:169] CancelRequest not implemented
Unable to connect to the server: EOF
Unable to connect to the server: EOF
E0627 11:13:00.644338       1 round_trippers.go:169] CancelRequest not implemented
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
E0627 11:14:00.361682       1 round_trippers.go:169] CancelRequest not implemented
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
E0627 11:15:49.854784       1 round_trippers.go:169] CancelRequest not implemented
E0627 11:15:54.855251       1 round_trippers.go:169] CancelRequest not implemented
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
E0627 11:18:59.978078       1 round_trippers.go:169] CancelRequest not implemented
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
E0627 11:24:28.953286       1 round_trippers.go:169] CancelRequest not implemented
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
E0627 11:29:56.925320       1 round_trippers.go:169] CancelRequest not implemented
E0627 11:30:01.925818       1 round_trippers.go:169] CancelRequest not implemented
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
E0627 11:35:29.486960       1 round_trippers.go:169] CancelRequest not implemented
E0627 11:35:34.487189       1 round_trippers.go:169] CancelRequest not implemented
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
E0627 11:40:48.696488       1 round_trippers.go:169] CancelRequest not implemented
E0627 11:40:53.697047       1 round_trippers.go:169] CancelRequest not implemented
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
E0627 11:51:51.538056       1 round_trippers.go:169] CancelRequest not implemented
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
E0627 12:02:48.126509       1 round_trippers.go:169] CancelRequest not implemented
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
E0627 12:08:02.261706       1 round_trippers.go:169] CancelRequest not implemented
E0627 12:08:07.261956       1 round_trippers.go:169] CancelRequest not implemented
E0627 12:08:12.262121       1 round_trippers.go:169] CancelRequest not implemented
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Unable to connect to the server: EOF
Containers: 24
 Running: 10
 Paused: 0
 Stopped: 14
Images: 8
Server Version: 17.03.3-ce
Storage Driver: overlay2
 Backing Filesystem: extfs
 Supports d_type: true
 Native Overlay Diff: true
Logging Driver: json-file
Cgroup Driver: cgroupfs
Plugins: 
 Volume: local
 Network: bridge host macvlan null overlay
Swarm: inactive
Runtimes: runc
Default Runtime: runc
Init Binary: docker-init
containerd version: 6c463891b1ad274d505ae3bb738e530d1df2b3c7
runc version: 54296cf40ad8143b62dbcaa1d90e520a2136ddfe
init version: 949e6fa
Security Options:
 apparmor
 seccomp
  Profile: default
Kernel Version: 4.15.0-52-generic
Operating System: Ubuntu 16.04.6 LTS
OSType: linux
Architecture: x86_64
CPUs: 8
Total Memory: 15.62 GiB
Name: airsHiP
ID: TJHR:YKUW:EX2Y:L2GU:3FCM:SOLK:FHPJ:UQMS:QVLN:XVYJ:S5SW:ERFF
Docker Root Dir: /var/lib/docker
Debug Mode (client): false
Debug Mode (server): false
Registry: https://index.docker.io/v1/
Experimental: false
Insecure Registries:
 127.0.0.0/8
Live Restore Enabled: true

CONTAINER ID        IMAGE                                      COMMAND                  CREATED             STATUS                           PORTS               NAMES
e4d33eb2aaff        30deddf83908                               "/apiserver --serv..."   2 minutes ago       Exited (1) 2 minutes ago                             k8s_kubectl-apiserver_bootstrap-armada-airship_kube-system_77e267bf6417c36e4309c651e338866a_22
4239161927b2        cb5aea7d0466                               "/tiller -logtostd..."   2 minutes ago       Exited (1) 2 minutes ago                             k8s_tiller_bootstrap-armada-airship_kube-system_77e267bf6417c36e4309c651e338866a_23
fadb7017dedc        e21fb69683f3                               "/usr/local/bin/etcd"    2 minutes ago       Exited (1) 2 minutes ago                             k8s_etcd-auxiliary-1_auxiliary-etcd-airship_kube-system_3c8223a65caffe3d69e99bfb925d15b7_22
32d73e5e8e8f        e21fb69683f3                               "/usr/local/bin/etcd"    2 minutes ago       Exited (1) 2 minutes ago                             k8s_etcd-auxiliary-0_auxiliary-etcd-airship_kube-system_3c8223a65caffe3d69e99bfb925d15b7_22
bbc5dd0c2ba8        30deddf83908                               "./hyperkube sched..."   3 minutes ago       Exited (1) 3 minutes ago                             k8s_kube-scheduler_kubernetes-scheduler-airship_kube-system_a06ed6a86d9149264fb85e438a7d5794_22
00cc810259bc        30deddf83908                               "/apiserver --serv..."   3 minutes ago       Exited (255) 2 minutes ago                           k8s_kube-apiserver_kubernetes-apiserver-airship_kube-system_f6490f4a9f1c3cbd0c9dcbfba0f11ab2_22
9e7285a7544a        30deddf83908                               "kube-controller-m..."   3 minutes ago       Exited (1) 3 minutes ago                             k8s_kube-controller-manager_kubernetes-controller-manager-airship_kube-system_7ee2a7f01e5063f236bcc13daccaeaf2_22
76a0ca81e37e        30deddf83908                               "/bin/sh -c 'set -..."   59 minutes ago      Up 59 minutes                                        k8s_monitor_bootstrap-armada-airship_kube-system_77e267bf6417c36e4309c651e338866a_4
1acc6c691481        e21fb69683f3                               "/bin/sh -c 'set -..."   59 minutes ago      Up 59 minutes                                        k8s_monitor_auxiliary-etcd-airship_kube-system_3c8223a65caffe3d69e99bfb925d15b7_4
8e36fa89cd58        291681d2405b                               "/bin/bash -c 'set..."   59 minutes ago      Up 59 minutes                                        k8s_armada_bootstrap-armada-airship_kube-system_77e267bf6417c36e4309c651e338866a_4
112975ef7444        3163c3bb9b0d                               "/bin/sh -c 'set -..."   59 minutes ago      Up 59 minutes                                        k8s_haproxy_haproxy-airship_kube-system_f29c4e58bbe06649af627575484caa9b_4
0f534978a4ab        gcr.io/google-containers/pause-amd64:3.1   "/pause"                 About an hour ago   Up About an hour                                     k8s_POD_kubernetes-apiserver-airship_kube-system_f6490f4a9f1c3cbd0c9dcbfba0f11ab2_3
cfc0d0ead2d0        gcr.io/google-containers/pause-amd64:3.1   "/pause"                 About an hour ago   Up About an hour                                     k8s_POD_kubernetes-scheduler-airship_kube-system_a06ed6a86d9149264fb85e438a7d5794_4
b83ac91c47d1        gcr.io/google-containers/pause-amd64:3.1   "/pause"                 About an hour ago   Up About an hour                                     k8s_POD_kubernetes-controller-manager-airship_kube-system_7ee2a7f01e5063f236bcc13daccaeaf2_4
410ff549dc77        gcr.io/google-containers/pause-amd64:3.1   "/pause"                 About an hour ago   Up About an hour                                     k8s_POD_haproxy-airship_kube-system_f29c4e58bbe06649af627575484caa9b_4
36d18ead1bbf        gcr.io/google-containers/pause-amd64:3.1   "/pause"                 About an hour ago   Up About an hour                                     k8s_POD_auxiliary-etcd-airship_kube-system_3c8223a65caffe3d69e99bfb925d15b7_4
a0d9f8ff1115        gcr.io/google-containers/pause-amd64:3.1   "/pause"                 About an hour ago   Up About an hour                                     k8s_POD_bootstrap-armada-airship_kube-system_77e267bf6417c36e4309c651e338866a_4
203b9b18c9f9        30deddf83908                               "/bin/sh -c 'set -..."   About an hour ago   Exited (255) About an hour ago                       k8s_monitor_bootstrap-armada-airship_kube-system_77e267bf6417c36e4309c651e338866a_3
ebaf5702dd6b        e21fb69683f3                               "/bin/sh -c 'set -..."   About an hour ago   Exited (255) About an hour ago                       k8s_monitor_auxiliary-etcd-airship_kube-system_3c8223a65caffe3d69e99bfb925d15b7_3
551133d85fb7        291681d2405b                               "/bin/bash -c 'set..."   About an hour ago   Exited (255) About an hour ago                       k8s_armada_bootstrap-armada-airship_kube-system_77e267bf6417c36e4309c651e338866a_3
b35d081c782f        3163c3bb9b0d                               "/bin/sh -c 'set -..."   About an hour ago   Exited (255) About an hour ago                       k8s_haproxy_haproxy-airship_kube-system_f29c4e58bbe06649af627575484caa9b_3
1de9a695cced        gcr.io/google-containers/pause-amd64:3.1   "/pause"                 About an hour ago   Exited (255) About an hour ago                       k8s_POD_bootstrap-armada-airship_kube-system_77e267bf6417c36e4309c651e338866a_3
626fbed71c4e        gcr.io/google-containers/pause-amd64:3.1   "/pause"                 About an hour ago   Exited (255) About an hour ago                       k8s_POD_haproxy-airship_kube-system_f29c4e58bbe06649af627575484caa9b_3
44dba7fbacdc        gcr.io/google-containers/pause-amd64:3.1   "/pause"                 About an hour ago   Exited (255) About an hour ago                       k8s_POD_auxiliary-etcd-airship_kube-system_3c8223a65caffe3d69e99bfb925d15b7_3
[
    {
        "Id": "e4d33eb2aaff9228409322c00bbcce76bb8722338c6a06567debb0ec00490b6f",
        "Created": "2019-06-27T12:08:28.303598854Z",
        "Path": "/apiserver",
        "Args": [
            "--service-cluster-ip-range=10.96.0.0/16",
            "--service-node-port-range=30000-32767",
            "--authorization-mode=Node,RBAC",
            "--admission-control=NamespaceLifecycle,LimitRanger,ServiceAccount,PersistentVolumeLabel,DefaultStorageClass,ResourceQuota,DefaultTolerationSeconds",
            "--endpoint-reconciler-type=lease",
            "--feature-gates=PodShareProcessNamespace=true",
            "--advertise-address=10.0.0.38",
            "--allow-privileged=true",
            "--anonymous-auth=false",
            "--bind-address=0.0.0.0",
            "--client-ca-file=/etc/kubernetes/apiserver/pki/cluster-ca.pem",
            "--etcd-cafile=/etc/kubernetes/apiserver/pki/etcd-client-ca.pem",
            "--etcd-certfile=/etc/kubernetes/apiserver/pki/etcd-client.pem",
            "--etcd-keyfile=/etc/kubernetes/apiserver/pki/etcd-client-key.pem",
            "--kubelet-certificate-authority=/etc/kubernetes/apiserver/pki/kubelet-client-ca.pem",
            "--kubelet-client-certificate=/etc/kubernetes/apiserver/pki/kubelet-client.pem",
            "--kubelet-client-key=/etc/kubernetes/apiserver/pki/kubelet-client-key.pem",
            "--kubelet-preferred-address-types=InternalIP,ExternalIP,Hostname",
            "--service-account-key-file=/etc/kubernetes/apiserver/pki/service-account.pub",
            "--tls-cert-file=/etc/kubernetes/apiserver/pki/apiserver.pem",
            "--tls-private-key-file=/etc/kubernetes/apiserver/pki/apiserver-key.pem",
            "--etcd-servers=https://localhost:12379",
            "--insecure-port=8080",
            "--secure-port=6444"
        ],
        "State": {
            "Status": "exited",
            "Running": false,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 0,
            "ExitCode": 1,
            "Error": "",
            "StartedAt": "2019-06-27T12:08:28.563588825Z",
            "FinishedAt": "2019-06-27T12:08:28.770411531Z"
        },
        "Image": "sha256:30deddf83908b7fe79cb5219acfdb3091660bd95ef17292f45cf967400d46822",
        "ResolvConfPath": "/var/lib/docker/containers/a0d9f8ff11159a0dc91afeff318ec00c88f6be4e01ccfd42180b0d79f0bc3440/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/a0d9f8ff11159a0dc91afeff318ec00c88f6be4e01ccfd42180b0d79f0bc3440/hostname",
        "HostsPath": "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/etc-hosts",
        "LogPath": "/var/lib/docker/containers/e4d33eb2aaff9228409322c00bbcce76bb8722338c6a06567debb0ec00490b6f/e4d33eb2aaff9228409322c00bbcce76bb8722338c6a06567debb0ec00490b6f-json.log",
        "Name": "/k8s_kubectl-apiserver_bootstrap-armada-airship_kube-system_77e267bf6417c36e4309c651e338866a_22",
        "RestartCount": 0,
        "Driver": "overlay2",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": [
                "/etc/genesis/armada/auth:/etc/kubernetes/admin",
                "/etc/genesis/apiserver:/etc/kubernetes/apiserver:ro",
                "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/etc-hosts:/etc/hosts",
                "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/containers/kubectl-apiserver/fdb4fa0a:/dev/termination-log"
            ],
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "container:a0d9f8ff11159a0dc91afeff318ec00c88f6be4e01ccfd42180b0d79f0bc3440",
            "PortBindings": null,
            "RestartPolicy": {
                "Name": "",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Dns": null,
            "DnsOptions": null,
            "DnsSearch": null,
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "container:a0d9f8ff11159a0dc91afeff318ec00c88f6be4e01ccfd42180b0d79f0bc3440",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 1000,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": [
                "seccomp=unconfined"
            ],
            "UTSMode": "host",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 2,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "/kubepods/besteffort/pod77e267bf6417c36e4309c651e338866a",
            "BlkioWeight": 0,
            "BlkioWeightDevice": null,
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DiskQuota": 0,
            "KernelMemory": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": -1,
            "OomKillDisable": false,
            "PidsLimit": 0,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0
        },
        "GraphDriver": {
            "Name": "overlay2",
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/40d98d8331eb01cfd1639558dda4b57ad12faeb880cbe9bd0132e575db0238a3-init/diff:/var/lib/docker/overlay2/a5374904306836793b0d850cdfb306785d11c06a1d60e3c5980e93bcf664095d/diff:/var/lib/docker/overlay2/49a5452849fabbdd61e06c5c53747da6977ee866bf949c98de8247e0ddf80dca/diff:/var/lib/docker/overlay2/f005f15b2c4651b69b97d6348d6a114ad873ac6290dfd9fb40376e32081c1885/diff:/var/lib/docker/overlay2/943ec4b40a064feacecda875355d7fa82bc903a8825cb6651bc49bcaec6ea6f6/diff:/var/lib/docker/overlay2/d328e069711ef3f0cc4f9bcc68b754d4577574103a0edecf5c640bcda1fa6e85/diff:/var/lib/docker/overlay2/7e2ae6faeb631a2993c0d0ba39268b7992cda176dec3800c14158de18fb56baf/diff:/var/lib/docker/overlay2/f0a7b1ac68ac69eafbccfc97d28599d91373ea50ffc114a523789a44c6e54aef/diff:/var/lib/docker/overlay2/3f24acc4f94a325dab5e176a5e40785f9f14b13293d1ccd6b071ad729adb0021/diff",
                "MergedDir": "/var/lib/docker/overlay2/40d98d8331eb01cfd1639558dda4b57ad12faeb880cbe9bd0132e575db0238a3/merged",
                "UpperDir": "/var/lib/docker/overlay2/40d98d8331eb01cfd1639558dda4b57ad12faeb880cbe9bd0132e575db0238a3/diff",
                "WorkDir": "/var/lib/docker/overlay2/40d98d8331eb01cfd1639558dda4b57ad12faeb880cbe9bd0132e575db0238a3/work"
            }
        },
        "Mounts": [
            {
                "Type": "bind",
                "Source": "/etc/genesis/armada/auth",
                "Destination": "/etc/kubernetes/admin",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/etc/genesis/apiserver",
                "Destination": "/etc/kubernetes/apiserver",
                "Mode": "ro",
                "RW": false,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/etc-hosts",
                "Destination": "/etc/hosts",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/containers/kubectl-apiserver/fdb4fa0a",
                "Destination": "/dev/termination-log",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            }
        ],
        "Config": {
            "Hostname": "airsHiP",
            "Domainname": "",
            "User": "0",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "KUBECONFIG=/etc/kubernetes/admin/config",
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": null,
            "Healthcheck": {
                "Test": [
                    "NONE"
                ]
            },
            "Image": "sha256:30deddf83908b7fe79cb5219acfdb3091660bd95ef17292f45cf967400d46822",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": [
                "/apiserver",
                "--service-cluster-ip-range=10.96.0.0/16",
                "--service-node-port-range=30000-32767",
                "--authorization-mode=Node,RBAC",
                "--admission-control=NamespaceLifecycle,LimitRanger,ServiceAccount,PersistentVolumeLabel,DefaultStorageClass,ResourceQuota,DefaultTolerationSeconds",
                "--endpoint-reconciler-type=lease",
                "--feature-gates=PodShareProcessNamespace=true",
                "--advertise-address=10.0.0.38",
                "--allow-privileged=true",
                "--anonymous-auth=false",
                "--bind-address=0.0.0.0",
                "--client-ca-file=/etc/kubernetes/apiserver/pki/cluster-ca.pem",
                "--etcd-cafile=/etc/kubernetes/apiserver/pki/etcd-client-ca.pem",
                "--etcd-certfile=/etc/kubernetes/apiserver/pki/etcd-client.pem",
                "--etcd-keyfile=/etc/kubernetes/apiserver/pki/etcd-client-key.pem",
                "--kubelet-certificate-authority=/etc/kubernetes/apiserver/pki/kubelet-client-ca.pem",
                "--kubelet-client-certificate=/etc/kubernetes/apiserver/pki/kubelet-client.pem",
                "--kubelet-client-key=/etc/kubernetes/apiserver/pki/kubelet-client-key.pem",
                "--kubelet-preferred-address-types=InternalIP,ExternalIP,Hostname",
                "--service-account-key-file=/etc/kubernetes/apiserver/pki/service-account.pub",
                "--tls-cert-file=/etc/kubernetes/apiserver/pki/apiserver.pem",
                "--tls-private-key-file=/etc/kubernetes/apiserver/pki/apiserver-key.pem",
                "--etcd-servers=https://localhost:12379",
                "--insecure-port=8080",
                "--secure-port=6444"
            ],
            "OnBuild": null,
            "Labels": {
                "annotation.io.kubernetes.container.hash": "28c32011",
                "annotation.io.kubernetes.container.restartCount": "22",
                "annotation.io.kubernetes.container.terminationMessagePath": "/dev/termination-log",
                "annotation.io.kubernetes.container.terminationMessagePolicy": "File",
                "annotation.io.kubernetes.pod.terminationGracePeriod": "30",
                "io.kubernetes.container.logpath": "/var/log/pods/77e267bf6417c36e4309c651e338866a/kubectl-apiserver/22.log",
                "io.kubernetes.container.name": "kubectl-apiserver",
                "io.kubernetes.docker.type": "container",
                "io.kubernetes.pod.name": "bootstrap-armada-airship",
                "io.kubernetes.pod.namespace": "kube-system",
                "io.kubernetes.pod.uid": "77e267bf6417c36e4309c651e338866a",
                "io.kubernetes.sandbox.id": "a0d9f8ff11159a0dc91afeff318ec00c88f6be4e01ccfd42180b0d79f0bc3440"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": null,
            "SandboxKey": "",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {}
        }
    }
]
[
    {
        "Id": "4239161927b2b82b777009aafdbadc68b3f2e86899e3b77f14cf55c0eb51bd21",
        "Created": "2019-06-27T12:08:28.038904298Z",
        "Path": "/tiller",
        "Args": [
            "-logtostderr",
            "-v",
            "5"
        ],
        "State": {
            "Status": "exited",
            "Running": false,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 0,
            "ExitCode": 1,
            "Error": "",
            "StartedAt": "2019-06-27T12:08:28.277397217Z",
            "FinishedAt": "2019-06-27T12:08:28.362481199Z"
        },
        "Image": "sha256:cb5aea7d04661c6f123223e784e9287397e38078ee05704762673633edcd9ec3",
        "ResolvConfPath": "/var/lib/docker/containers/a0d9f8ff11159a0dc91afeff318ec00c88f6be4e01ccfd42180b0d79f0bc3440/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/a0d9f8ff11159a0dc91afeff318ec00c88f6be4e01ccfd42180b0d79f0bc3440/hostname",
        "HostsPath": "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/etc-hosts",
        "LogPath": "/var/lib/docker/containers/4239161927b2b82b777009aafdbadc68b3f2e86899e3b77f14cf55c0eb51bd21/4239161927b2b82b777009aafdbadc68b3f2e86899e3b77f14cf55c0eb51bd21-json.log",
        "Name": "/k8s_tiller_bootstrap-armada-airship_kube-system_77e267bf6417c36e4309c651e338866a_23",
        "RestartCount": 0,
        "Driver": "overlay2",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": [
                "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/etc-hosts:/etc/hosts",
                "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/containers/tiller/6c3dbc4a:/dev/termination-log"
            ],
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "container:a0d9f8ff11159a0dc91afeff318ec00c88f6be4e01ccfd42180b0d79f0bc3440",
            "PortBindings": null,
            "RestartPolicy": {
                "Name": "",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Dns": null,
            "DnsOptions": null,
            "DnsSearch": null,
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "container:a0d9f8ff11159a0dc91afeff318ec00c88f6be4e01ccfd42180b0d79f0bc3440",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 1000,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": [
                "seccomp=unconfined"
            ],
            "UTSMode": "host",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 2,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "/kubepods/besteffort/pod77e267bf6417c36e4309c651e338866a",
            "BlkioWeight": 0,
            "BlkioWeightDevice": null,
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DiskQuota": 0,
            "KernelMemory": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": -1,
            "OomKillDisable": false,
            "PidsLimit": 0,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0
        },
        "GraphDriver": {
            "Name": "overlay2",
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/6f45ee50acefce5f3b9db21d3712b729a90f96e7fb990eae65716d67a475c531-init/diff:/var/lib/docker/overlay2/9b4c73fe630f471f2492ce435b2682cc7f4ab2b8b7dae94ba9d3d47bd92be79e/diff:/var/lib/docker/overlay2/6bc896083bde357ef05d5d980e65dd130a7d8abbb84dc8b1464cb26a8cc81914/diff:/var/lib/docker/overlay2/1cc6fe874d72adb784e234134a29a2532cb5b3fddc7b45629634db91fdc81103/diff:/var/lib/docker/overlay2/37075b46dc7e08820f1cdee739a1a4b4fb369d934afa43d8151e99800da7cc32/diff",
                "MergedDir": "/var/lib/docker/overlay2/6f45ee50acefce5f3b9db21d3712b729a90f96e7fb990eae65716d67a475c531/merged",
                "UpperDir": "/var/lib/docker/overlay2/6f45ee50acefce5f3b9db21d3712b729a90f96e7fb990eae65716d67a475c531/diff",
                "WorkDir": "/var/lib/docker/overlay2/6f45ee50acefce5f3b9db21d3712b729a90f96e7fb990eae65716d67a475c531/work"
            }
        },
        "Mounts": [
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/etc-hosts",
                "Destination": "/etc/hosts",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/containers/tiller/6c3dbc4a",
                "Destination": "/dev/termination-log",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            }
        ],
        "Config": {
            "Hostname": "airsHiP",
            "Domainname": "",
            "User": "65534",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "ExposedPorts": {
                "44134/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "TILLER_NAMESPACE=kube-system",
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                "HOME=/tmp"
            ],
            "Cmd": null,
            "Healthcheck": {
                "Test": [
                    "NONE"
                ]
            },
            "Image": "sha256:cb5aea7d04661c6f123223e784e9287397e38078ee05704762673633edcd9ec3",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": [
                "/tiller",
                "-logtostderr",
                "-v",
                "5"
            ],
            "OnBuild": null,
            "Labels": {
                "annotation.io.kubernetes.container.hash": "ce062074",
                "annotation.io.kubernetes.container.ports": "[{\"name\":\"tiller\",\"hostPort\":44134,\"containerPort\":44134,\"protocol\":\"TCP\"}]",
                "annotation.io.kubernetes.container.restartCount": "23",
                "annotation.io.kubernetes.container.terminationMessagePath": "/dev/termination-log",
                "annotation.io.kubernetes.container.terminationMessagePolicy": "File",
                "annotation.io.kubernetes.pod.terminationGracePeriod": "30",
                "io.kubernetes.container.logpath": "/var/log/pods/77e267bf6417c36e4309c651e338866a/tiller/23.log",
                "io.kubernetes.container.name": "tiller",
                "io.kubernetes.docker.type": "container",
                "io.kubernetes.pod.name": "bootstrap-armada-airship",
                "io.kubernetes.pod.namespace": "kube-system",
                "io.kubernetes.pod.uid": "77e267bf6417c36e4309c651e338866a",
                "io.kubernetes.sandbox.id": "a0d9f8ff11159a0dc91afeff318ec00c88f6be4e01ccfd42180b0d79f0bc3440"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": null,
            "SandboxKey": "",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {}
        }
    }
]
[
    {
        "Id": "fadb7017dedc2b39e8fd5070631c9b476498d7948d52d4444441828a93047221",
        "Created": "2019-06-27T12:08:25.258719717Z",
        "Path": "/usr/local/bin/etcd",
        "Args": [],
        "State": {
            "Status": "exited",
            "Running": false,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 0,
            "ExitCode": 1,
            "Error": "",
            "StartedAt": "2019-06-27T12:08:25.456154279Z",
            "FinishedAt": "2019-06-27T12:08:25.500794204Z"
        },
        "Image": "sha256:e21fb69683f3f754d40128ba1981244c3679fe92e5f692ee67a2b94f65564fb0",
        "ResolvConfPath": "/var/lib/docker/containers/36d18ead1bbf9f6c200f1d43641fdf4711be7f0dcca13842b29f3a3b396c4e23/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/36d18ead1bbf9f6c200f1d43641fdf4711be7f0dcca13842b29f3a3b396c4e23/hostname",
        "HostsPath": "/var/lib/kubelet/pods/3c8223a65caffe3d69e99bfb925d15b7/etc-hosts",
        "LogPath": "/var/lib/docker/containers/fadb7017dedc2b39e8fd5070631c9b476498d7948d52d4444441828a93047221/fadb7017dedc2b39e8fd5070631c9b476498d7948d52d4444441828a93047221-json.log",
        "Name": "/k8s_etcd-auxiliary-1_auxiliary-etcd-airship_kube-system_3c8223a65caffe3d69e99bfb925d15b7_22",
        "RestartCount": 0,
        "Driver": "overlay2",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": [
                "/var/lib/etcd/auxiliary-1:/var/lib/etcd",
                "/etc/genesis/etcd/pki:/etc/etcd/pki",
                "/var/lib/kubelet/pods/3c8223a65caffe3d69e99bfb925d15b7/etc-hosts:/etc/hosts",
                "/var/lib/kubelet/pods/3c8223a65caffe3d69e99bfb925d15b7/containers/etcd-auxiliary-1/5147de74:/dev/termination-log"
            ],
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "container:36d18ead1bbf9f6c200f1d43641fdf4711be7f0dcca13842b29f3a3b396c4e23",
            "PortBindings": null,
            "RestartPolicy": {
                "Name": "",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Dns": null,
            "DnsOptions": null,
            "DnsSearch": null,
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "container:36d18ead1bbf9f6c200f1d43641fdf4711be7f0dcca13842b29f3a3b396c4e23",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 1000,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": [
                "seccomp=unconfined"
            ],
            "UTSMode": "host",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 2,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "/kubepods/besteffort/pod3c8223a65caffe3d69e99bfb925d15b7",
            "BlkioWeight": 0,
            "BlkioWeightDevice": null,
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DiskQuota": 0,
            "KernelMemory": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": -1,
            "OomKillDisable": false,
            "PidsLimit": 0,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0
        },
        "GraphDriver": {
            "Name": "overlay2",
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/ae9cb6b39777f3e78ce2336f6fad82c595a3f6c47b02c33ae1d8c86cc9e8446e-init/diff:/var/lib/docker/overlay2/c86a911a63e34effabe3b54ed3faa3fcaa0d6f7db7477f5edc226def55e5908d/diff:/var/lib/docker/overlay2/1ff7b2f8bdc83db9a36e25b21c2a8bb73a9aaee9f6157814079086f406edee00/diff:/var/lib/docker/overlay2/a2b22b11d412599622d16742f7944e9bcd6a6b861e84d3441016a09111cc975c/diff:/var/lib/docker/overlay2/ff54e40c2b7dbb13ea6e6cac253af60a7c2816bc1d62ca178a7cb41cd140af36/diff:/var/lib/docker/overlay2/bc3ff432394da390da83bfbaa2c2a6e579e9f1184217ddd817571c9fa005f414/diff:/var/lib/docker/overlay2/50de7866c436185ee3b746b87e48b1e2e110ea00bcd6481a0ee970d2999ceac9/diff",
                "MergedDir": "/var/lib/docker/overlay2/ae9cb6b39777f3e78ce2336f6fad82c595a3f6c47b02c33ae1d8c86cc9e8446e/merged",
                "UpperDir": "/var/lib/docker/overlay2/ae9cb6b39777f3e78ce2336f6fad82c595a3f6c47b02c33ae1d8c86cc9e8446e/diff",
                "WorkDir": "/var/lib/docker/overlay2/ae9cb6b39777f3e78ce2336f6fad82c595a3f6c47b02c33ae1d8c86cc9e8446e/work"
            }
        },
        "Mounts": [
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/3c8223a65caffe3d69e99bfb925d15b7/etc-hosts",
                "Destination": "/etc/hosts",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/3c8223a65caffe3d69e99bfb925d15b7/containers/etcd-auxiliary-1/5147de74",
                "Destination": "/dev/termination-log",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/etcd/auxiliary-1",
                "Destination": "/var/lib/etcd",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/etc/genesis/etcd/pki",
                "Destination": "/etc/etcd/pki",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            }
        ],
        "Config": {
            "Hostname": "airsHiP",
            "Domainname": "",
            "User": "0",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "ExposedPorts": {
                "2379/tcp": {},
                "2380/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "ETCD_PEER_CLIENT_CERT_AUTH=true",
                "ETCD_TRUSTED_CA_FILE=/etc/etcd/pki/client-ca.pem",
                "ETCD_KEY_FILE=/etc/etcd/pki/etcd-client-key.pem",
                "ETCD_PEER_KEY_FILE=/etc/etcd/pki/etcd-peer-key.pem",
                "ETCD_INITIAL_ADVERTISE_PEER_URLS=https://10.0.0.38:22380",
                "ETCD_LISTEN_PEER_URLS=https://0.0.0.0:22380",
                "ETCDCTL_CACERT=/etc/etcd/pki/client-ca.pem",
                "ETCD_NAME=auxiliary-1",
                "ETCD_DATA_DIR=/var/lib/etcd",
                "ETCDCTL_API=3",
                "ETCDCTL_DIAL_TIMEOUT=3s",
                "POD_IP=10.0.0.38",
                "ETCD_CLIENT_CERT_AUTH=true",
                "ETCD_CERT_FILE=/etc/etcd/pki/etcd-client.pem",
                "ETCD_INITIAL_CLUSTER_TOKEN=promenade-kube-etcd-token",
                "ETCD_INITIAL_CLUSTER_STATE=new",
                "ETCDCTL_ENDPOINTS=https://10.0.0.38:22379,https://127.0.0.1:22379",
                "ETCDCTL_KEY=/etc/etcd/pki/etcd-client-key.pem",
                "ETCD_PEER_TRUSTED_CA_FILE=/etc/etcd/pki/peer-ca.pem",
                "ETCD_PEER_CERT_FILE=/etc/etcd/pki/etcd-peer.pem",
                "ETCD_ADVERTISE_CLIENT_URLS=https://10.0.0.38:22379",
                "ETCD_LISTEN_CLIENT_URLS=https://0.0.0.0:22379",
                "ETCD_INITIAL_CLUSTER=airsHiP=https://10.0.0.38:2380,auxiliary-0=https://10.0.0.38:12380,auxiliary-1=https://10.0.0.38:22380",
                "ETCDCTL_CERT=/etc/etcd/pki/etcd-client.pem",
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": [
                "/usr/local/bin/etcd"
            ],
            "Healthcheck": {
                "Test": [
                    "NONE"
                ]
            },
            "ArgsEscaped": true,
            "Image": "sha256:e21fb69683f3f754d40128ba1981244c3679fe92e5f692ee67a2b94f65564fb0",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": null,
            "OnBuild": null,
            "Labels": {
                "annotation.io.kubernetes.container.hash": "8efbc179",
                "annotation.io.kubernetes.container.ports": "[{\"name\":\"client\",\"hostPort\":22379,\"containerPort\":22379,\"protocol\":\"TCP\"},{\"name\":\"peer\",\"hostPort\":22380,\"containerPort\":22380,\"protocol\":\"TCP\"}]",
                "annotation.io.kubernetes.container.restartCount": "22",
                "annotation.io.kubernetes.container.terminationMessagePath": "/dev/termination-log",
                "annotation.io.kubernetes.container.terminationMessagePolicy": "File",
                "annotation.io.kubernetes.pod.terminationGracePeriod": "30",
                "io.kubernetes.container.logpath": "/var/log/pods/3c8223a65caffe3d69e99bfb925d15b7/etcd-auxiliary-1/22.log",
                "io.kubernetes.container.name": "etcd-auxiliary-1",
                "io.kubernetes.docker.type": "container",
                "io.kubernetes.pod.name": "auxiliary-etcd-airship",
                "io.kubernetes.pod.namespace": "kube-system",
                "io.kubernetes.pod.uid": "3c8223a65caffe3d69e99bfb925d15b7",
                "io.kubernetes.sandbox.id": "36d18ead1bbf9f6c200f1d43641fdf4711be7f0dcca13842b29f3a3b396c4e23"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": null,
            "SandboxKey": "",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {}
        }
    }
]
[
    {
        "Id": "32d73e5e8e8f113970395a3e23acab76c6fd4fd6f0c7c64f9a14adba034e910f",
        "Created": "2019-06-27T12:08:25.031455455Z",
        "Path": "/usr/local/bin/etcd",
        "Args": [],
        "State": {
            "Status": "exited",
            "Running": false,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 0,
            "ExitCode": 1,
            "Error": "",
            "StartedAt": "2019-06-27T12:08:25.241563374Z",
            "FinishedAt": "2019-06-27T12:08:25.296661926Z"
        },
        "Image": "sha256:e21fb69683f3f754d40128ba1981244c3679fe92e5f692ee67a2b94f65564fb0",
        "ResolvConfPath": "/var/lib/docker/containers/36d18ead1bbf9f6c200f1d43641fdf4711be7f0dcca13842b29f3a3b396c4e23/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/36d18ead1bbf9f6c200f1d43641fdf4711be7f0dcca13842b29f3a3b396c4e23/hostname",
        "HostsPath": "/var/lib/kubelet/pods/3c8223a65caffe3d69e99bfb925d15b7/etc-hosts",
        "LogPath": "/var/lib/docker/containers/32d73e5e8e8f113970395a3e23acab76c6fd4fd6f0c7c64f9a14adba034e910f/32d73e5e8e8f113970395a3e23acab76c6fd4fd6f0c7c64f9a14adba034e910f-json.log",
        "Name": "/k8s_etcd-auxiliary-0_auxiliary-etcd-airship_kube-system_3c8223a65caffe3d69e99bfb925d15b7_22",
        "RestartCount": 0,
        "Driver": "overlay2",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": [
                "/var/lib/etcd/auxiliary-0:/var/lib/etcd",
                "/etc/genesis/etcd/pki:/etc/etcd/pki",
                "/var/lib/kubelet/pods/3c8223a65caffe3d69e99bfb925d15b7/etc-hosts:/etc/hosts",
                "/var/lib/kubelet/pods/3c8223a65caffe3d69e99bfb925d15b7/containers/etcd-auxiliary-0/75b2d485:/dev/termination-log"
            ],
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "container:36d18ead1bbf9f6c200f1d43641fdf4711be7f0dcca13842b29f3a3b396c4e23",
            "PortBindings": null,
            "RestartPolicy": {
                "Name": "",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Dns": null,
            "DnsOptions": null,
            "DnsSearch": null,
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "container:36d18ead1bbf9f6c200f1d43641fdf4711be7f0dcca13842b29f3a3b396c4e23",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 1000,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": [
                "seccomp=unconfined"
            ],
            "UTSMode": "host",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 2,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "/kubepods/besteffort/pod3c8223a65caffe3d69e99bfb925d15b7",
            "BlkioWeight": 0,
            "BlkioWeightDevice": null,
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DiskQuota": 0,
            "KernelMemory": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": -1,
            "OomKillDisable": false,
            "PidsLimit": 0,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0
        },
        "GraphDriver": {
            "Name": "overlay2",
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/2a7b4a0159dd2b5b981a639007efe1aac70fbfa79fbd75f5ab51e769de758803-init/diff:/var/lib/docker/overlay2/c86a911a63e34effabe3b54ed3faa3fcaa0d6f7db7477f5edc226def55e5908d/diff:/var/lib/docker/overlay2/1ff7b2f8bdc83db9a36e25b21c2a8bb73a9aaee9f6157814079086f406edee00/diff:/var/lib/docker/overlay2/a2b22b11d412599622d16742f7944e9bcd6a6b861e84d3441016a09111cc975c/diff:/var/lib/docker/overlay2/ff54e40c2b7dbb13ea6e6cac253af60a7c2816bc1d62ca178a7cb41cd140af36/diff:/var/lib/docker/overlay2/bc3ff432394da390da83bfbaa2c2a6e579e9f1184217ddd817571c9fa005f414/diff:/var/lib/docker/overlay2/50de7866c436185ee3b746b87e48b1e2e110ea00bcd6481a0ee970d2999ceac9/diff",
                "MergedDir": "/var/lib/docker/overlay2/2a7b4a0159dd2b5b981a639007efe1aac70fbfa79fbd75f5ab51e769de758803/merged",
                "UpperDir": "/var/lib/docker/overlay2/2a7b4a0159dd2b5b981a639007efe1aac70fbfa79fbd75f5ab51e769de758803/diff",
                "WorkDir": "/var/lib/docker/overlay2/2a7b4a0159dd2b5b981a639007efe1aac70fbfa79fbd75f5ab51e769de758803/work"
            }
        },
        "Mounts": [
            {
                "Type": "bind",
                "Source": "/var/lib/etcd/auxiliary-0",
                "Destination": "/var/lib/etcd",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/etc/genesis/etcd/pki",
                "Destination": "/etc/etcd/pki",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/3c8223a65caffe3d69e99bfb925d15b7/etc-hosts",
                "Destination": "/etc/hosts",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/3c8223a65caffe3d69e99bfb925d15b7/containers/etcd-auxiliary-0/75b2d485",
                "Destination": "/dev/termination-log",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            }
        ],
        "Config": {
            "Hostname": "airsHiP",
            "Domainname": "",
            "User": "0",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "ExposedPorts": {
                "2379/tcp": {},
                "2380/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "ETCD_CLIENT_CERT_AUTH=true",
                "ETCD_PEER_CLIENT_CERT_AUTH=true",
                "ETCD_DATA_DIR=/var/lib/etcd",
                "ETCD_TRUSTED_CA_FILE=/etc/etcd/pki/client-ca.pem",
                "ETCD_KEY_FILE=/etc/etcd/pki/etcd-client-key.pem",
                "ETCD_ADVERTISE_CLIENT_URLS=https://10.0.0.38:12379",
                "ETCD_INITIAL_ADVERTISE_PEER_URLS=https://10.0.0.38:12380",
                "ETCD_LISTEN_CLIENT_URLS=https://0.0.0.0:12379",
                "ETCD_LISTEN_PEER_URLS=https://0.0.0.0:12380",
                "ETCD_INITIAL_CLUSTER=airsHiP=https://10.0.0.38:2380,auxiliary-0=https://10.0.0.38:12380,auxiliary-1=https://10.0.0.38:22380",
                "ETCDCTL_CERT=/etc/etcd/pki/etcd-client.pem",
                "ETCDCTL_KEY=/etc/etcd/pki/etcd-client-key.pem",
                "ETCD_NAME=auxiliary-0",
                "ETCD_PEER_TRUSTED_CA_FILE=/etc/etcd/pki/peer-ca.pem",
                "ETCD_INITIAL_CLUSTER_TOKEN=promenade-kube-etcd-token",
                "ETCDCTL_DIAL_TIMEOUT=3s",
                "ETCDCTL_ENDPOINTS=https://10.0.0.38:12379,https://127.0.0.1:12379",
                "ETCDCTL_CACERT=/etc/etcd/pki/client-ca.pem",
                "POD_IP=10.0.0.38",
                "ETCD_CERT_FILE=/etc/etcd/pki/etcd-client.pem",
                "ETCD_PEER_CERT_FILE=/etc/etcd/pki/etcd-peer.pem",
                "ETCD_PEER_KEY_FILE=/etc/etcd/pki/etcd-peer-key.pem",
                "ETCD_INITIAL_CLUSTER_STATE=new",
                "ETCDCTL_API=3",
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": [
                "/usr/local/bin/etcd"
            ],
            "Healthcheck": {
                "Test": [
                    "NONE"
                ]
            },
            "ArgsEscaped": true,
            "Image": "sha256:e21fb69683f3f754d40128ba1981244c3679fe92e5f692ee67a2b94f65564fb0",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": null,
            "OnBuild": null,
            "Labels": {
                "annotation.io.kubernetes.container.hash": "94e904dd",
                "annotation.io.kubernetes.container.ports": "[{\"name\":\"client\",\"hostPort\":12379,\"containerPort\":12379,\"protocol\":\"TCP\"},{\"name\":\"peer\",\"hostPort\":12380,\"containerPort\":12380,\"protocol\":\"TCP\"}]",
                "annotation.io.kubernetes.container.restartCount": "22",
                "annotation.io.kubernetes.container.terminationMessagePath": "/dev/termination-log",
                "annotation.io.kubernetes.container.terminationMessagePolicy": "File",
                "annotation.io.kubernetes.pod.terminationGracePeriod": "30",
                "io.kubernetes.container.logpath": "/var/log/pods/3c8223a65caffe3d69e99bfb925d15b7/etcd-auxiliary-0/22.log",
                "io.kubernetes.container.name": "etcd-auxiliary-0",
                "io.kubernetes.docker.type": "container",
                "io.kubernetes.pod.name": "auxiliary-etcd-airship",
                "io.kubernetes.pod.namespace": "kube-system",
                "io.kubernetes.pod.uid": "3c8223a65caffe3d69e99bfb925d15b7",
                "io.kubernetes.sandbox.id": "36d18ead1bbf9f6c200f1d43641fdf4711be7f0dcca13842b29f3a3b396c4e23"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": null,
            "SandboxKey": "",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {}
        }
    }
]
[
    {
        "Id": "bbc5dd0c2ba88b06c9b97048bae54e1ecbe206984d44bf7494b6c7102a92175d",
        "Created": "2019-06-27T12:07:57.037286061Z",
        "Path": "./hyperkube",
        "Args": [
            "scheduler",
            "--leader-elect=true",
            "--kubeconfig=/etc/kubernetes/scheduler/kubeconfig.yaml",
            "--feature-gates=TaintNodesByCondition=true",
            "--v=5"
        ],
        "State": {
            "Status": "exited",
            "Running": false,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 0,
            "ExitCode": 1,
            "Error": "",
            "StartedAt": "2019-06-27T12:07:57.243660424Z",
            "FinishedAt": "2019-06-27T12:07:57.444845777Z"
        },
        "Image": "sha256:30deddf83908b7fe79cb5219acfdb3091660bd95ef17292f45cf967400d46822",
        "ResolvConfPath": "/var/lib/docker/containers/cfc0d0ead2d08c04e38a160673b63d4b2a3602e91d18690fd3de34c37164b340/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/cfc0d0ead2d08c04e38a160673b63d4b2a3602e91d18690fd3de34c37164b340/hostname",
        "HostsPath": "/var/lib/kubelet/pods/a06ed6a86d9149264fb85e438a7d5794/etc-hosts",
        "LogPath": "/var/lib/docker/containers/bbc5dd0c2ba88b06c9b97048bae54e1ecbe206984d44bf7494b6c7102a92175d/bbc5dd0c2ba88b06c9b97048bae54e1ecbe206984d44bf7494b6c7102a92175d-json.log",
        "Name": "/k8s_kube-scheduler_kubernetes-scheduler-airship_kube-system_a06ed6a86d9149264fb85e438a7d5794_22",
        "RestartCount": 0,
        "Driver": "overlay2",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": [
                "/etc/genesis/scheduler:/etc/kubernetes/scheduler",
                "/var/lib/kubelet/pods/a06ed6a86d9149264fb85e438a7d5794/etc-hosts:/etc/hosts",
                "/var/lib/kubelet/pods/a06ed6a86d9149264fb85e438a7d5794/containers/kube-scheduler/d16cfa6d:/dev/termination-log"
            ],
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "container:cfc0d0ead2d08c04e38a160673b63d4b2a3602e91d18690fd3de34c37164b340",
            "PortBindings": null,
            "RestartPolicy": {
                "Name": "",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Dns": null,
            "DnsOptions": null,
            "DnsSearch": null,
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "container:cfc0d0ead2d08c04e38a160673b63d4b2a3602e91d18690fd3de34c37164b340",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 1000,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": [
                "seccomp=unconfined"
            ],
            "UTSMode": "host",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 2,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "/kubepods/besteffort/poda06ed6a86d9149264fb85e438a7d5794",
            "BlkioWeight": 0,
            "BlkioWeightDevice": null,
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DiskQuota": 0,
            "KernelMemory": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": -1,
            "OomKillDisable": false,
            "PidsLimit": 0,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0
        },
        "GraphDriver": {
            "Name": "overlay2",
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/df967bb21d99ae1f07a1230e166ff439b130056d9f1a6ece4e0210d777a870fa-init/diff:/var/lib/docker/overlay2/a5374904306836793b0d850cdfb306785d11c06a1d60e3c5980e93bcf664095d/diff:/var/lib/docker/overlay2/49a5452849fabbdd61e06c5c53747da6977ee866bf949c98de8247e0ddf80dca/diff:/var/lib/docker/overlay2/f005f15b2c4651b69b97d6348d6a114ad873ac6290dfd9fb40376e32081c1885/diff:/var/lib/docker/overlay2/943ec4b40a064feacecda875355d7fa82bc903a8825cb6651bc49bcaec6ea6f6/diff:/var/lib/docker/overlay2/d328e069711ef3f0cc4f9bcc68b754d4577574103a0edecf5c640bcda1fa6e85/diff:/var/lib/docker/overlay2/7e2ae6faeb631a2993c0d0ba39268b7992cda176dec3800c14158de18fb56baf/diff:/var/lib/docker/overlay2/f0a7b1ac68ac69eafbccfc97d28599d91373ea50ffc114a523789a44c6e54aef/diff:/var/lib/docker/overlay2/3f24acc4f94a325dab5e176a5e40785f9f14b13293d1ccd6b071ad729adb0021/diff",
                "MergedDir": "/var/lib/docker/overlay2/df967bb21d99ae1f07a1230e166ff439b130056d9f1a6ece4e0210d777a870fa/merged",
                "UpperDir": "/var/lib/docker/overlay2/df967bb21d99ae1f07a1230e166ff439b130056d9f1a6ece4e0210d777a870fa/diff",
                "WorkDir": "/var/lib/docker/overlay2/df967bb21d99ae1f07a1230e166ff439b130056d9f1a6ece4e0210d777a870fa/work"
            }
        },
        "Mounts": [
            {
                "Type": "bind",
                "Source": "/etc/genesis/scheduler",
                "Destination": "/etc/kubernetes/scheduler",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/a06ed6a86d9149264fb85e438a7d5794/etc-hosts",
                "Destination": "/etc/hosts",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/a06ed6a86d9149264fb85e438a7d5794/containers/kube-scheduler/d16cfa6d",
                "Destination": "/dev/termination-log",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            }
        ],
        "Config": {
            "Hostname": "airsHiP",
            "Domainname": "",
            "User": "0",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": null,
            "Healthcheck": {
                "Test": [
                    "NONE"
                ]
            },
            "Image": "sha256:30deddf83908b7fe79cb5219acfdb3091660bd95ef17292f45cf967400d46822",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": [
                "./hyperkube",
                "scheduler",
                "--leader-elect=true",
                "--kubeconfig=/etc/kubernetes/scheduler/kubeconfig.yaml",
                "--feature-gates=TaintNodesByCondition=true",
                "--v=5"
            ],
            "OnBuild": null,
            "Labels": {
                "annotation.io.kubernetes.container.hash": "550dcd0f",
                "annotation.io.kubernetes.container.restartCount": "22",
                "annotation.io.kubernetes.container.terminationMessagePath": "/dev/termination-log",
                "annotation.io.kubernetes.container.terminationMessagePolicy": "File",
                "annotation.io.kubernetes.pod.terminationGracePeriod": "30",
                "io.kubernetes.container.logpath": "/var/log/pods/a06ed6a86d9149264fb85e438a7d5794/kube-scheduler/22.log",
                "io.kubernetes.container.name": "kube-scheduler",
                "io.kubernetes.docker.type": "container",
                "io.kubernetes.pod.name": "kubernetes-scheduler-airship",
                "io.kubernetes.pod.namespace": "kube-system",
                "io.kubernetes.pod.uid": "a06ed6a86d9149264fb85e438a7d5794",
                "io.kubernetes.sandbox.id": "cfc0d0ead2d08c04e38a160673b63d4b2a3602e91d18690fd3de34c37164b340"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": null,
            "SandboxKey": "",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {}
        }
    }
]
[
    {
        "Id": "00cc810259bcd26eed49d105e657a041d0cdee1c692b2742d382ff3c249b6629",
        "Created": "2019-06-27T12:07:54.030819482Z",
        "Path": "/apiserver",
        "Args": [
            "--service-cluster-ip-range=10.96.0.0/16",
            "--service-node-port-range=30000-32767",
            "--authorization-mode=Node,RBAC",
            "--admission-control=NamespaceLifecycle,LimitRanger,ServiceAccount,PersistentVolumeLabel,DefaultStorageClass,ResourceQuota,DefaultTolerationSeconds",
            "--endpoint-reconciler-type=lease",
            "--feature-gates=PodShareProcessNamespace=true",
            "--advertise-address=10.0.0.38",
            "--allow-privileged=true",
            "--anonymous-auth=false",
            "--bind-address=0.0.0.0",
            "--client-ca-file=/etc/kubernetes/apiserver/pki/cluster-ca.pem",
            "--etcd-cafile=/etc/kubernetes/apiserver/pki/etcd-client-ca.pem",
            "--etcd-certfile=/etc/kubernetes/apiserver/pki/etcd-client.pem",
            "--etcd-keyfile=/etc/kubernetes/apiserver/pki/etcd-client-key.pem",
            "--kubelet-certificate-authority=/etc/kubernetes/apiserver/pki/kubelet-client-ca.pem",
            "--kubelet-client-certificate=/etc/kubernetes/apiserver/pki/kubelet-client.pem",
            "--kubelet-client-key=/etc/kubernetes/apiserver/pki/kubelet-client-key.pem",
            "--kubelet-preferred-address-types=InternalIP,ExternalIP,Hostname",
            "--service-account-key-file=/etc/kubernetes/apiserver/pki/service-account.pub",
            "--tls-cert-file=/etc/kubernetes/apiserver/pki/apiserver.pem",
            "--tls-private-key-file=/etc/kubernetes/apiserver/pki/apiserver-key.pem",
            "--etcd-servers=https://localhost:2379",
            "--insecure-port=0",
            "--secure-port=6443"
        ],
        "State": {
            "Status": "exited",
            "Running": false,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 0,
            "ExitCode": 255,
            "Error": "",
            "StartedAt": "2019-06-27T12:07:54.233122303Z",
            "FinishedAt": "2019-06-27T12:08:15.423389315Z"
        },
        "Image": "sha256:30deddf83908b7fe79cb5219acfdb3091660bd95ef17292f45cf967400d46822",
        "ResolvConfPath": "/var/lib/docker/containers/0f534978a4ab561c5e4234688c72f55d8484471b401e06205661222cda839277/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/0f534978a4ab561c5e4234688c72f55d8484471b401e06205661222cda839277/hostname",
        "HostsPath": "/var/lib/kubelet/pods/f6490f4a9f1c3cbd0c9dcbfba0f11ab2/etc-hosts",
        "LogPath": "/var/lib/docker/containers/00cc810259bcd26eed49d105e657a041d0cdee1c692b2742d382ff3c249b6629/00cc810259bcd26eed49d105e657a041d0cdee1c692b2742d382ff3c249b6629-json.log",
        "Name": "/k8s_kube-apiserver_kubernetes-apiserver-airship_kube-system_f6490f4a9f1c3cbd0c9dcbfba0f11ab2_22",
        "RestartCount": 0,
        "Driver": "overlay2",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": [
                "/etc/genesis/apiserver:/etc/kubernetes/apiserver:ro",
                "/var/lib/kubelet/pods/f6490f4a9f1c3cbd0c9dcbfba0f11ab2/etc-hosts:/etc/hosts",
                "/var/lib/kubelet/pods/f6490f4a9f1c3cbd0c9dcbfba0f11ab2/containers/kube-apiserver/18815d20:/dev/termination-log"
            ],
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "container:0f534978a4ab561c5e4234688c72f55d8484471b401e06205661222cda839277",
            "PortBindings": null,
            "RestartPolicy": {
                "Name": "",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Dns": null,
            "DnsOptions": null,
            "DnsSearch": null,
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "container:0f534978a4ab561c5e4234688c72f55d8484471b401e06205661222cda839277",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 1000,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": [
                "seccomp=unconfined"
            ],
            "UTSMode": "host",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 2,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "/kubepods/besteffort/podf6490f4a9f1c3cbd0c9dcbfba0f11ab2",
            "BlkioWeight": 0,
            "BlkioWeightDevice": null,
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DiskQuota": 0,
            "KernelMemory": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": -1,
            "OomKillDisable": false,
            "PidsLimit": 0,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0
        },
        "GraphDriver": {
            "Name": "overlay2",
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/a86acae8a6a20fb91565a16ad0b912351ead7e8c1d025a2ae18d37030bcf2e48-init/diff:/var/lib/docker/overlay2/a5374904306836793b0d850cdfb306785d11c06a1d60e3c5980e93bcf664095d/diff:/var/lib/docker/overlay2/49a5452849fabbdd61e06c5c53747da6977ee866bf949c98de8247e0ddf80dca/diff:/var/lib/docker/overlay2/f005f15b2c4651b69b97d6348d6a114ad873ac6290dfd9fb40376e32081c1885/diff:/var/lib/docker/overlay2/943ec4b40a064feacecda875355d7fa82bc903a8825cb6651bc49bcaec6ea6f6/diff:/var/lib/docker/overlay2/d328e069711ef3f0cc4f9bcc68b754d4577574103a0edecf5c640bcda1fa6e85/diff:/var/lib/docker/overlay2/7e2ae6faeb631a2993c0d0ba39268b7992cda176dec3800c14158de18fb56baf/diff:/var/lib/docker/overlay2/f0a7b1ac68ac69eafbccfc97d28599d91373ea50ffc114a523789a44c6e54aef/diff:/var/lib/docker/overlay2/3f24acc4f94a325dab5e176a5e40785f9f14b13293d1ccd6b071ad729adb0021/diff",
                "MergedDir": "/var/lib/docker/overlay2/a86acae8a6a20fb91565a16ad0b912351ead7e8c1d025a2ae18d37030bcf2e48/merged",
                "UpperDir": "/var/lib/docker/overlay2/a86acae8a6a20fb91565a16ad0b912351ead7e8c1d025a2ae18d37030bcf2e48/diff",
                "WorkDir": "/var/lib/docker/overlay2/a86acae8a6a20fb91565a16ad0b912351ead7e8c1d025a2ae18d37030bcf2e48/work"
            }
        },
        "Mounts": [
            {
                "Type": "bind",
                "Source": "/etc/genesis/apiserver",
                "Destination": "/etc/kubernetes/apiserver",
                "Mode": "ro",
                "RW": false,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/f6490f4a9f1c3cbd0c9dcbfba0f11ab2/etc-hosts",
                "Destination": "/etc/hosts",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/f6490f4a9f1c3cbd0c9dcbfba0f11ab2/containers/kube-apiserver/18815d20",
                "Destination": "/dev/termination-log",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            }
        ],
        "Config": {
            "Hostname": "airsHiP",
            "Domainname": "",
            "User": "0",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": null,
            "Healthcheck": {
                "Test": [
                    "NONE"
                ]
            },
            "Image": "sha256:30deddf83908b7fe79cb5219acfdb3091660bd95ef17292f45cf967400d46822",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": [
                "/apiserver",
                "--service-cluster-ip-range=10.96.0.0/16",
                "--service-node-port-range=30000-32767",
                "--authorization-mode=Node,RBAC",
                "--admission-control=NamespaceLifecycle,LimitRanger,ServiceAccount,PersistentVolumeLabel,DefaultStorageClass,ResourceQuota,DefaultTolerationSeconds",
                "--endpoint-reconciler-type=lease",
                "--feature-gates=PodShareProcessNamespace=true",
                "--advertise-address=10.0.0.38",
                "--allow-privileged=true",
                "--anonymous-auth=false",
                "--bind-address=0.0.0.0",
                "--client-ca-file=/etc/kubernetes/apiserver/pki/cluster-ca.pem",
                "--etcd-cafile=/etc/kubernetes/apiserver/pki/etcd-client-ca.pem",
                "--etcd-certfile=/etc/kubernetes/apiserver/pki/etcd-client.pem",
                "--etcd-keyfile=/etc/kubernetes/apiserver/pki/etcd-client-key.pem",
                "--kubelet-certificate-authority=/etc/kubernetes/apiserver/pki/kubelet-client-ca.pem",
                "--kubelet-client-certificate=/etc/kubernetes/apiserver/pki/kubelet-client.pem",
                "--kubelet-client-key=/etc/kubernetes/apiserver/pki/kubelet-client-key.pem",
                "--kubelet-preferred-address-types=InternalIP,ExternalIP,Hostname",
                "--service-account-key-file=/etc/kubernetes/apiserver/pki/service-account.pub",
                "--tls-cert-file=/etc/kubernetes/apiserver/pki/apiserver.pem",
                "--tls-private-key-file=/etc/kubernetes/apiserver/pki/apiserver-key.pem",
                "--etcd-servers=https://localhost:2379",
                "--insecure-port=0",
                "--secure-port=6443"
            ],
            "OnBuild": null,
            "Labels": {
                "annotation.io.kubernetes.container.hash": "bec31a12",
                "annotation.io.kubernetes.container.restartCount": "22",
                "annotation.io.kubernetes.container.terminationMessagePath": "/dev/termination-log",
                "annotation.io.kubernetes.container.terminationMessagePolicy": "File",
                "annotation.io.kubernetes.pod.terminationGracePeriod": "30",
                "io.kubernetes.container.logpath": "/var/log/pods/f6490f4a9f1c3cbd0c9dcbfba0f11ab2/kube-apiserver/22.log",
                "io.kubernetes.container.name": "kube-apiserver",
                "io.kubernetes.docker.type": "container",
                "io.kubernetes.pod.name": "kubernetes-apiserver-airship",
                "io.kubernetes.pod.namespace": "kube-system",
                "io.kubernetes.pod.uid": "f6490f4a9f1c3cbd0c9dcbfba0f11ab2",
                "io.kubernetes.sandbox.id": "0f534978a4ab561c5e4234688c72f55d8484471b401e06205661222cda839277"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": null,
            "SandboxKey": "",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {}
        }
    }
]
[
    {
        "Id": "9e7285a7544ae513527864da17c7d752dfb0dc407106b8385e6476e555a3284b",
        "Created": "2019-06-27T12:07:51.031453604Z",
        "Path": "kube-controller-manager",
        "Args": [
            "--allocate-node-cidrs=true",
            "--cluster-cidr=10.97.0.0/16",
            "--configure-cloud-routes=false",
            "--leader-elect=true",
            "--kubeconfig=/etc/kubernetes/controller-manager/kubeconfig.yaml",
            "--root-ca-file=/etc/kubernetes/controller-manager/pki/cluster-ca.pem",
            "--service-account-private-key-file=/etc/kubernetes/controller-manager/pki/service-account.key",
            "--service-cluster-ip-range=10.96.0.0/16",
            "--use-service-account-credentials=true",
            "--v=5"
        ],
        "State": {
            "Status": "exited",
            "Running": false,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 0,
            "ExitCode": 1,
            "Error": "",
            "StartedAt": "2019-06-27T12:07:51.239215184Z",
            "FinishedAt": "2019-06-27T12:07:51.439083626Z"
        },
        "Image": "sha256:30deddf83908b7fe79cb5219acfdb3091660bd95ef17292f45cf967400d46822",
        "ResolvConfPath": "/var/lib/docker/containers/b83ac91c47d1793ab5e3b3eef9dcd8036efdc82dd120ae781f9036160989d270/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/b83ac91c47d1793ab5e3b3eef9dcd8036efdc82dd120ae781f9036160989d270/hostname",
        "HostsPath": "/var/lib/kubelet/pods/7ee2a7f01e5063f236bcc13daccaeaf2/etc-hosts",
        "LogPath": "/var/lib/docker/containers/9e7285a7544ae513527864da17c7d752dfb0dc407106b8385e6476e555a3284b/9e7285a7544ae513527864da17c7d752dfb0dc407106b8385e6476e555a3284b-json.log",
        "Name": "/k8s_kube-controller-manager_kubernetes-controller-manager-airship_kube-system_7ee2a7f01e5063f236bcc13daccaeaf2_22",
        "RestartCount": 0,
        "Driver": "overlay2",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": [
                "/etc/genesis/controller-manager:/etc/kubernetes/controller-manager:ro",
                "/var/lib/kubelet/pods/7ee2a7f01e5063f236bcc13daccaeaf2/etc-hosts:/etc/hosts",
                "/var/lib/kubelet/pods/7ee2a7f01e5063f236bcc13daccaeaf2/containers/kube-controller-manager/e8c59f7a:/dev/termination-log"
            ],
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "container:b83ac91c47d1793ab5e3b3eef9dcd8036efdc82dd120ae781f9036160989d270",
            "PortBindings": null,
            "RestartPolicy": {
                "Name": "",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Dns": null,
            "DnsOptions": null,
            "DnsSearch": null,
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "container:b83ac91c47d1793ab5e3b3eef9dcd8036efdc82dd120ae781f9036160989d270",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 1000,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": [
                "seccomp=unconfined"
            ],
            "UTSMode": "host",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 2,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "/kubepods/besteffort/pod7ee2a7f01e5063f236bcc13daccaeaf2",
            "BlkioWeight": 0,
            "BlkioWeightDevice": null,
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DiskQuota": 0,
            "KernelMemory": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": -1,
            "OomKillDisable": false,
            "PidsLimit": 0,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0
        },
        "GraphDriver": {
            "Name": "overlay2",
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/7fd16a217b88fdb0d53345f39c9cd6cd48a4cad0b004d2cb2327180dc1f1cb23-init/diff:/var/lib/docker/overlay2/a5374904306836793b0d850cdfb306785d11c06a1d60e3c5980e93bcf664095d/diff:/var/lib/docker/overlay2/49a5452849fabbdd61e06c5c53747da6977ee866bf949c98de8247e0ddf80dca/diff:/var/lib/docker/overlay2/f005f15b2c4651b69b97d6348d6a114ad873ac6290dfd9fb40376e32081c1885/diff:/var/lib/docker/overlay2/943ec4b40a064feacecda875355d7fa82bc903a8825cb6651bc49bcaec6ea6f6/diff:/var/lib/docker/overlay2/d328e069711ef3f0cc4f9bcc68b754d4577574103a0edecf5c640bcda1fa6e85/diff:/var/lib/docker/overlay2/7e2ae6faeb631a2993c0d0ba39268b7992cda176dec3800c14158de18fb56baf/diff:/var/lib/docker/overlay2/f0a7b1ac68ac69eafbccfc97d28599d91373ea50ffc114a523789a44c6e54aef/diff:/var/lib/docker/overlay2/3f24acc4f94a325dab5e176a5e40785f9f14b13293d1ccd6b071ad729adb0021/diff",
                "MergedDir": "/var/lib/docker/overlay2/7fd16a217b88fdb0d53345f39c9cd6cd48a4cad0b004d2cb2327180dc1f1cb23/merged",
                "UpperDir": "/var/lib/docker/overlay2/7fd16a217b88fdb0d53345f39c9cd6cd48a4cad0b004d2cb2327180dc1f1cb23/diff",
                "WorkDir": "/var/lib/docker/overlay2/7fd16a217b88fdb0d53345f39c9cd6cd48a4cad0b004d2cb2327180dc1f1cb23/work"
            }
        },
        "Mounts": [
            {
                "Type": "bind",
                "Source": "/etc/genesis/controller-manager",
                "Destination": "/etc/kubernetes/controller-manager",
                "Mode": "ro",
                "RW": false,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/7ee2a7f01e5063f236bcc13daccaeaf2/etc-hosts",
                "Destination": "/etc/hosts",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/7ee2a7f01e5063f236bcc13daccaeaf2/containers/kube-controller-manager/e8c59f7a",
                "Destination": "/dev/termination-log",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            }
        ],
        "Config": {
            "Hostname": "airsHiP",
            "Domainname": "",
            "User": "0",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": null,
            "Healthcheck": {
                "Test": [
                    "NONE"
                ]
            },
            "Image": "sha256:30deddf83908b7fe79cb5219acfdb3091660bd95ef17292f45cf967400d46822",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": [
                "kube-controller-manager",
                "--allocate-node-cidrs=true",
                "--cluster-cidr=10.97.0.0/16",
                "--configure-cloud-routes=false",
                "--leader-elect=true",
                "--kubeconfig=/etc/kubernetes/controller-manager/kubeconfig.yaml",
                "--root-ca-file=/etc/kubernetes/controller-manager/pki/cluster-ca.pem",
                "--service-account-private-key-file=/etc/kubernetes/controller-manager/pki/service-account.key",
                "--service-cluster-ip-range=10.96.0.0/16",
                "--use-service-account-credentials=true",
                "--v=5"
            ],
            "OnBuild": null,
            "Labels": {
                "annotation.io.kubernetes.container.hash": "cee11e8c",
                "annotation.io.kubernetes.container.restartCount": "22",
                "annotation.io.kubernetes.container.terminationMessagePath": "/dev/termination-log",
                "annotation.io.kubernetes.container.terminationMessagePolicy": "File",
                "annotation.io.kubernetes.pod.terminationGracePeriod": "30",
                "io.kubernetes.container.logpath": "/var/log/pods/7ee2a7f01e5063f236bcc13daccaeaf2/kube-controller-manager/22.log",
                "io.kubernetes.container.name": "kube-controller-manager",
                "io.kubernetes.docker.type": "container",
                "io.kubernetes.pod.name": "kubernetes-controller-manager-airship",
                "io.kubernetes.pod.namespace": "kube-system",
                "io.kubernetes.pod.uid": "7ee2a7f01e5063f236bcc13daccaeaf2",
                "io.kubernetes.sandbox.id": "b83ac91c47d1793ab5e3b3eef9dcd8036efdc82dd120ae781f9036160989d270"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": null,
            "SandboxKey": "",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {}
        }
    }
]
[
    {
        "Id": "203b9b18c9f97e68d6686355e55ec2e787d68297cb3f92286e0b96fbef1586be",
        "Created": "2019-06-27T11:08:14.677054139Z",
        "Path": "/bin/sh",
        "Args": [
            "-c",
            "set -x\n\nwhile ! [ -e /ipc/armada-done ]; do\n  sleep 5\ndone\n\nrm -f /etc/kubernetes/manifests/bootstrap-armada.yaml\nsleep 10000"
        ],
        "State": {
            "Status": "exited",
            "Running": false,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 0,
            "ExitCode": 255,
            "Error": "",
            "StartedAt": "2019-06-27T11:08:15.2266166Z",
            "FinishedAt": "2019-06-27T11:10:52.999028891Z"
        },
        "Image": "sha256:30deddf83908b7fe79cb5219acfdb3091660bd95ef17292f45cf967400d46822",
        "ResolvConfPath": "/var/lib/docker/containers/1de9a695cced6d1bccecd4a5a80584450c4e252ca42b15ecf3b2391141185393/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/1de9a695cced6d1bccecd4a5a80584450c4e252ca42b15ecf3b2391141185393/hostname",
        "HostsPath": "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/etc-hosts",
        "LogPath": "/var/lib/docker/containers/203b9b18c9f97e68d6686355e55ec2e787d68297cb3f92286e0b96fbef1586be/203b9b18c9f97e68d6686355e55ec2e787d68297cb3f92286e0b96fbef1586be-json.log",
        "Name": "/k8s_monitor_bootstrap-armada-airship_kube-system_77e267bf6417c36e4309c651e338866a_3",
        "RestartCount": 0,
        "Driver": "overlay2",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "docker-default",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": [
                "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/volumes/kubernetes.io~empty-dir/ipc:/ipc",
                "/etc/kubernetes/manifests:/etc/kubernetes/manifests",
                "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/etc-hosts:/etc/hosts",
                "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/containers/monitor/0626ab4d:/dev/termination-log"
            ],
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "container:1de9a695cced6d1bccecd4a5a80584450c4e252ca42b15ecf3b2391141185393",
            "PortBindings": null,
            "RestartPolicy": {
                "Name": "",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "container:1de9a695cced6d1bccecd4a5a80584450c4e252ca42b15ecf3b2391141185393",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 1000,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": [
                "seccomp=unconfined"
            ],
            "UTSMode": "host",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 2,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "/kubepods/besteffort/pod77e267bf6417c36e4309c651e338866a",
            "BlkioWeight": 0,
            "BlkioWeightDevice": null,
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DiskQuota": 0,
            "KernelMemory": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": false,
            "PidsLimit": 0,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0
        },
        "GraphDriver": {
            "Name": "overlay2",
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/05a9d78725320334a37618666535b9cdef3de4312794eb0eb050e157cbc11d38-init/diff:/var/lib/docker/overlay2/a5374904306836793b0d850cdfb306785d11c06a1d60e3c5980e93bcf664095d/diff:/var/lib/docker/overlay2/49a5452849fabbdd61e06c5c53747da6977ee866bf949c98de8247e0ddf80dca/diff:/var/lib/docker/overlay2/f005f15b2c4651b69b97d6348d6a114ad873ac6290dfd9fb40376e32081c1885/diff:/var/lib/docker/overlay2/943ec4b40a064feacecda875355d7fa82bc903a8825cb6651bc49bcaec6ea6f6/diff:/var/lib/docker/overlay2/d328e069711ef3f0cc4f9bcc68b754d4577574103a0edecf5c640bcda1fa6e85/diff:/var/lib/docker/overlay2/7e2ae6faeb631a2993c0d0ba39268b7992cda176dec3800c14158de18fb56baf/diff:/var/lib/docker/overlay2/f0a7b1ac68ac69eafbccfc97d28599d91373ea50ffc114a523789a44c6e54aef/diff:/var/lib/docker/overlay2/3f24acc4f94a325dab5e176a5e40785f9f14b13293d1ccd6b071ad729adb0021/diff",
                "MergedDir": "/var/lib/docker/overlay2/05a9d78725320334a37618666535b9cdef3de4312794eb0eb050e157cbc11d38/merged",
                "UpperDir": "/var/lib/docker/overlay2/05a9d78725320334a37618666535b9cdef3de4312794eb0eb050e157cbc11d38/diff",
                "WorkDir": "/var/lib/docker/overlay2/05a9d78725320334a37618666535b9cdef3de4312794eb0eb050e157cbc11d38/work"
            }
        },
        "Mounts": [
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/containers/monitor/0626ab4d",
                "Destination": "/dev/termination-log",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/etc-hosts",
                "Destination": "/etc/hosts",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/etc/kubernetes/manifests",
                "Destination": "/etc/kubernetes/manifests",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/volumes/kubernetes.io~empty-dir/ipc",
                "Destination": "/ipc",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            }
        ],
        "Config": {
            "Hostname": "airsHiP",
            "Domainname": "",
            "User": "0",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": null,
            "Healthcheck": {
                "Test": [
                    "NONE"
                ]
            },
            "Image": "sha256:30deddf83908b7fe79cb5219acfdb3091660bd95ef17292f45cf967400d46822",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": [
                "/bin/sh",
                "-c",
                "set -x\n\nwhile ! [ -e /ipc/armada-done ]; do\n  sleep 5\ndone\n\nrm -f /etc/kubernetes/manifests/bootstrap-armada.yaml\nsleep 10000"
            ],
            "OnBuild": null,
            "Labels": {
                "annotation.io.kubernetes.container.hash": "f96f974b",
                "annotation.io.kubernetes.container.restartCount": "3",
                "annotation.io.kubernetes.container.terminationMessagePath": "/dev/termination-log",
                "annotation.io.kubernetes.container.terminationMessagePolicy": "File",
                "annotation.io.kubernetes.pod.terminationGracePeriod": "30",
                "io.kubernetes.container.logpath": "/var/log/pods/77e267bf6417c36e4309c651e338866a/monitor/3.log",
                "io.kubernetes.container.name": "monitor",
                "io.kubernetes.docker.type": "container",
                "io.kubernetes.pod.name": "bootstrap-armada-airship",
                "io.kubernetes.pod.namespace": "kube-system",
                "io.kubernetes.pod.uid": "77e267bf6417c36e4309c651e338866a",
                "io.kubernetes.sandbox.id": "1de9a695cced6d1bccecd4a5a80584450c4e252ca42b15ecf3b2391141185393"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": null,
            "SandboxKey": "",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {}
        }
    }
]
[
    {
        "Id": "ebaf5702dd6b365a534c5ae2d2dfbb3375b61d7377bf675497a7848ade4380d4",
        "Created": "2019-06-27T11:08:14.675383556Z",
        "Path": "/bin/sh",
        "Args": [
            "-c",
            "set -x\n\nfunction external_member_count() {\n    etcdctl member list \\\n        | grep '\\bstarted\\b' \\\n        | grep -Ev \"\\\\b(airsHiP|auxiliary-0|auxiliary-1)\\\\b\" \\\n        | wc -l\n}\n\nfunction remove_if_possible() {\n    MEMBER_NAME=$1\n    MEMBER_ID=$(etcdctl member list | grep \"${MEMBER_NAME}\" | awk -F ', ' '{ print $1 }')\n    if [ -n \"${MEMBER_ID}\" ]; then\n        etcdctl member remove $MEMBER_ID\n    fi\n}\n\n# NOTE(mark-burnett): If there are any non-genesis members, then we are ready to\n# remove the auxiliary members.  Otherwise, wait.\nwhile [ ! \"$(external_member_count)\" -gt 0 ]; do\n    sleep 10\ndone\n\n# NOTE(mark-burnett): Failures beyond this point are unexpected, but\n# should be recovered by restarting this container.\nset -e\n\nremove_if_possible auxiliary-0\nremove_if_possible auxiliary-1\n\nrm -rf \\\n    /var/lib/etcd/auxiliary-0 \\\n    /var/lib/etcd/auxiliary-1 \\\n    /manifests/auxiliary-kubernetes-etcd.yaml\n\nsleep 10000"
        ],
        "State": {
            "Status": "exited",
            "Running": false,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 0,
            "ExitCode": 255,
            "Error": "",
            "StartedAt": "2019-06-27T11:08:15.200762048Z",
            "FinishedAt": "2019-06-27T11:10:54.205708956Z"
        },
        "Image": "sha256:e21fb69683f3f754d40128ba1981244c3679fe92e5f692ee67a2b94f65564fb0",
        "ResolvConfPath": "/var/lib/docker/containers/44dba7fbacdc18f8f249ec2ac7fe231069a782070253649ad401cf7cd1876a0c/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/44dba7fbacdc18f8f249ec2ac7fe231069a782070253649ad401cf7cd1876a0c/hostname",
        "HostsPath": "/var/lib/kubelet/pods/3c8223a65caffe3d69e99bfb925d15b7/etc-hosts",
        "LogPath": "/var/lib/docker/containers/ebaf5702dd6b365a534c5ae2d2dfbb3375b61d7377bf675497a7848ade4380d4/ebaf5702dd6b365a534c5ae2d2dfbb3375b61d7377bf675497a7848ade4380d4-json.log",
        "Name": "/k8s_monitor_auxiliary-etcd-airship_kube-system_3c8223a65caffe3d69e99bfb925d15b7_3",
        "RestartCount": 0,
        "Driver": "overlay2",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "docker-default",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": [
                "/var/lib/etcd:/var/lib/etcd",
                "/etc/genesis/etcd/pki:/etc/etcd/pki",
                "/etc/kubernetes/manifests:/manifests",
                "/var/lib/kubelet/pods/3c8223a65caffe3d69e99bfb925d15b7/etc-hosts:/etc/hosts",
                "/var/lib/kubelet/pods/3c8223a65caffe3d69e99bfb925d15b7/containers/monitor/08ccc634:/dev/termination-log"
            ],
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "container:44dba7fbacdc18f8f249ec2ac7fe231069a782070253649ad401cf7cd1876a0c",
            "PortBindings": null,
            "RestartPolicy": {
                "Name": "",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "container:44dba7fbacdc18f8f249ec2ac7fe231069a782070253649ad401cf7cd1876a0c",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 1000,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": [
                "seccomp=unconfined"
            ],
            "UTSMode": "host",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 2,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "/kubepods/besteffort/pod3c8223a65caffe3d69e99bfb925d15b7",
            "BlkioWeight": 0,
            "BlkioWeightDevice": null,
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DiskQuota": 0,
            "KernelMemory": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": false,
            "PidsLimit": 0,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0
        },
        "GraphDriver": {
            "Name": "overlay2",
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/92c3ace624946adcd5f690a9d3b002a0b929c17347c0c219e24d7fadbce9b2ac-init/diff:/var/lib/docker/overlay2/c86a911a63e34effabe3b54ed3faa3fcaa0d6f7db7477f5edc226def55e5908d/diff:/var/lib/docker/overlay2/1ff7b2f8bdc83db9a36e25b21c2a8bb73a9aaee9f6157814079086f406edee00/diff:/var/lib/docker/overlay2/a2b22b11d412599622d16742f7944e9bcd6a6b861e84d3441016a09111cc975c/diff:/var/lib/docker/overlay2/ff54e40c2b7dbb13ea6e6cac253af60a7c2816bc1d62ca178a7cb41cd140af36/diff:/var/lib/docker/overlay2/bc3ff432394da390da83bfbaa2c2a6e579e9f1184217ddd817571c9fa005f414/diff:/var/lib/docker/overlay2/50de7866c436185ee3b746b87e48b1e2e110ea00bcd6481a0ee970d2999ceac9/diff",
                "MergedDir": "/var/lib/docker/overlay2/92c3ace624946adcd5f690a9d3b002a0b929c17347c0c219e24d7fadbce9b2ac/merged",
                "UpperDir": "/var/lib/docker/overlay2/92c3ace624946adcd5f690a9d3b002a0b929c17347c0c219e24d7fadbce9b2ac/diff",
                "WorkDir": "/var/lib/docker/overlay2/92c3ace624946adcd5f690a9d3b002a0b929c17347c0c219e24d7fadbce9b2ac/work"
            }
        },
        "Mounts": [
            {
                "Type": "bind",
                "Source": "/etc/genesis/etcd/pki",
                "Destination": "/etc/etcd/pki",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/3c8223a65caffe3d69e99bfb925d15b7/etc-hosts",
                "Destination": "/etc/hosts",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/etc/kubernetes/manifests",
                "Destination": "/manifests",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/etcd",
                "Destination": "/var/lib/etcd",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/3c8223a65caffe3d69e99bfb925d15b7/containers/monitor/08ccc634",
                "Destination": "/dev/termination-log",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            }
        ],
        "Config": {
            "Hostname": "airsHiP",
            "Domainname": "",
            "User": "0",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "ExposedPorts": {
                "2379/tcp": {},
                "2380/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "ETCDCTL_KEY=/etc/etcd/pki/etcd-client-key.pem",
                "ETCDCTL_API=3",
                "ETCDCTL_DIAL_TIMEOUT=3s",
                "ETCDCTL_ENDPOINTS=https://127.0.0.1:2379",
                "ETCDCTL_CACERT=/etc/etcd/pki/client-ca.pem",
                "ETCDCTL_CERT=/etc/etcd/pki/etcd-client.pem",
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": null,
            "Healthcheck": {
                "Test": [
                    "NONE"
                ]
            },
            "Image": "sha256:e21fb69683f3f754d40128ba1981244c3679fe92e5f692ee67a2b94f65564fb0",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": [
                "/bin/sh",
                "-c",
                "set -x\n\nfunction external_member_count() {\n    etcdctl member list \\\n        | grep '\\bstarted\\b' \\\n        | grep -Ev \"\\\\b(airsHiP|auxiliary-0|auxiliary-1)\\\\b\" \\\n        | wc -l\n}\n\nfunction remove_if_possible() {\n    MEMBER_NAME=$1\n    MEMBER_ID=$(etcdctl member list | grep \"${MEMBER_NAME}\" | awk -F ', ' '{ print $1 }')\n    if [ -n \"${MEMBER_ID}\" ]; then\n        etcdctl member remove $MEMBER_ID\n    fi\n}\n\n# NOTE(mark-burnett): If there are any non-genesis members, then we are ready to\n# remove the auxiliary members.  Otherwise, wait.\nwhile [ ! \"$(external_member_count)\" -gt 0 ]; do\n    sleep 10\ndone\n\n# NOTE(mark-burnett): Failures beyond this point are unexpected, but\n# should be recovered by restarting this container.\nset -e\n\nremove_if_possible auxiliary-0\nremove_if_possible auxiliary-1\n\nrm -rf \\\n    /var/lib/etcd/auxiliary-0 \\\n    /var/lib/etcd/auxiliary-1 \\\n    /manifests/auxiliary-kubernetes-etcd.yaml\n\nsleep 10000"
            ],
            "OnBuild": null,
            "Labels": {
                "annotation.io.kubernetes.container.hash": "88db40be",
                "annotation.io.kubernetes.container.restartCount": "3",
                "annotation.io.kubernetes.container.terminationMessagePath": "/dev/termination-log",
                "annotation.io.kubernetes.container.terminationMessagePolicy": "File",
                "annotation.io.kubernetes.pod.terminationGracePeriod": "30",
                "io.kubernetes.container.logpath": "/var/log/pods/3c8223a65caffe3d69e99bfb925d15b7/monitor/3.log",
                "io.kubernetes.container.name": "monitor",
                "io.kubernetes.docker.type": "container",
                "io.kubernetes.pod.name": "auxiliary-etcd-airship",
                "io.kubernetes.pod.namespace": "kube-system",
                "io.kubernetes.pod.uid": "3c8223a65caffe3d69e99bfb925d15b7",
                "io.kubernetes.sandbox.id": "44dba7fbacdc18f8f249ec2ac7fe231069a782070253649ad401cf7cd1876a0c"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": null,
            "SandboxKey": "",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {}
        }
    }
]
[
    {
        "Id": "551133d85fb77e07618d2c4d2e29565d4727dce7472bc3d3fec9923e326220f0",
        "Created": "2019-06-27T11:08:14.175646871Z",
        "Path": "/bin/bash",
        "Args": [
            "-c",
            "set -x\n\nwhile true; do\n    sleep 10\n    if armada \\\n            apply \\\n            --target-manifest cluster-bootstrap-aiab \\\n            --tiller-host 127.0.0.1 \\\n            /etc/genesis/armada/assets/manifest.yaml &>> \"${ARMADA_LOGFILE}\"; then\n        break\n    fi\ndone\ntouch /ipc/armada-done\nsleep 10000"
        ],
        "State": {
            "Status": "exited",
            "Running": false,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 0,
            "ExitCode": 255,
            "Error": "",
            "StartedAt": "2019-06-27T11:08:14.651584848Z",
            "FinishedAt": "2019-06-27T11:10:54.144480387Z"
        },
        "Image": "sha256:291681d2405b6196f2552070d38cc3db42bbb84363e3c04e5b7f15bdb6272ef3",
        "ResolvConfPath": "/var/lib/docker/containers/1de9a695cced6d1bccecd4a5a80584450c4e252ca42b15ecf3b2391141185393/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/1de9a695cced6d1bccecd4a5a80584450c4e252ca42b15ecf3b2391141185393/hostname",
        "HostsPath": "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/etc-hosts",
        "LogPath": "/var/lib/docker/containers/551133d85fb77e07618d2c4d2e29565d4727dce7472bc3d3fec9923e326220f0/551133d85fb77e07618d2c4d2e29565d4727dce7472bc3d3fec9923e326220f0-json.log",
        "Name": "/k8s_armada_bootstrap-armada-airship_kube-system_77e267bf6417c36e4309c651e338866a_3",
        "RestartCount": 0,
        "Driver": "overlay2",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "docker-default",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": [
                "/etc/genesis/armada/assets:/etc/genesis/armada/assets",
                "/etc/genesis/armada/auth:/root/.kube",
                "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/volumes/kubernetes.io~empty-dir/ipc:/ipc",
                "/var/log/armada:/tmp/log",
                "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/etc-hosts:/etc/hosts",
                "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/containers/armada/0ee87389:/dev/termination-log"
            ],
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "container:1de9a695cced6d1bccecd4a5a80584450c4e252ca42b15ecf3b2391141185393",
            "PortBindings": null,
            "RestartPolicy": {
                "Name": "",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "container:1de9a695cced6d1bccecd4a5a80584450c4e252ca42b15ecf3b2391141185393",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 1000,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": [
                "seccomp=unconfined"
            ],
            "UTSMode": "host",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 2,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "/kubepods/besteffort/pod77e267bf6417c36e4309c651e338866a",
            "BlkioWeight": 0,
            "BlkioWeightDevice": null,
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DiskQuota": 0,
            "KernelMemory": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": false,
            "PidsLimit": 0,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0
        },
        "GraphDriver": {
            "Name": "overlay2",
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/1cfe476af192534fda8c5350beef6f1a82da921911911248d38b857b4bc045d9-init/diff:/var/lib/docker/overlay2/6ad636a67227cf9bb74b85a6d8ace1253a1459a84e8513dc13e1611d2548123d/diff:/var/lib/docker/overlay2/d98f4215469b181eee8475a6ac5f172ac94c5e66d77b8b324b497197f63d61ab/diff:/var/lib/docker/overlay2/ea5010dc2517902de8ed0c3efecd67533fad95779d34ff1340e756a949d6e35a/diff:/var/lib/docker/overlay2/5d878f0ecaa5386425da0aa30a951d60c890c36a912285fdf3c20a8195ac28c7/diff:/var/lib/docker/overlay2/cdc1db96871d54129c1a7bdde56e0c3d565c298e130c0356f747242159d7a4ea/diff:/var/lib/docker/overlay2/cb8ea589f606693f76e6267edaf3294835c00177c20252e9333dfffb2664585d/diff:/var/lib/docker/overlay2/f52165732657821664158112dfb4903e3eef5066e53c5c7a938d5d09ccae3f3c/diff:/var/lib/docker/overlay2/6e7eb20f3b532ca972234a07a021b501dd3ac4b09a13be79945527539978c76c/diff:/var/lib/docker/overlay2/739a1c080aa1f7c0d26dfe98580ea2c194aa6d95b0559a5f7949a600c4efa2df/diff:/var/lib/docker/overlay2/caf3c6780b81fade3f6ef96ece9e839806e4e64f48953c4e8cd43fa8e18c0461/diff:/var/lib/docker/overlay2/a6c58e5b9e4cce91390e8390fad575e43ee42d77934c2bc02577dffbf00a39df/diff",
                "MergedDir": "/var/lib/docker/overlay2/1cfe476af192534fda8c5350beef6f1a82da921911911248d38b857b4bc045d9/merged",
                "UpperDir": "/var/lib/docker/overlay2/1cfe476af192534fda8c5350beef6f1a82da921911911248d38b857b4bc045d9/diff",
                "WorkDir": "/var/lib/docker/overlay2/1cfe476af192534fda8c5350beef6f1a82da921911911248d38b857b4bc045d9/work"
            }
        },
        "Mounts": [
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/containers/armada/0ee87389",
                "Destination": "/dev/termination-log",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/etc/genesis/armada/assets",
                "Destination": "/etc/genesis/armada/assets",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/etc-hosts",
                "Destination": "/etc/hosts",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/77e267bf6417c36e4309c651e338866a/volumes/kubernetes.io~empty-dir/ipc",
                "Destination": "/ipc",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/etc/genesis/armada/auth",
                "Destination": "/root/.kube",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/log/armada",
                "Destination": "/tmp/log",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            }
        ],
        "Config": {
            "Hostname": "airsHiP",
            "Domainname": "",
            "User": "0",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "ExposedPorts": {
                "8000/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "ARMADA_LOGFILE=/tmp/log/bootstrap-armada.log",
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                "DEBIAN_FRONTEND=noninteractive",
                "LANG=C.UTF-8",
                "LC_ALL=C.UTF-8",
                "PBR_VERSION=0.8.0"
            ],
            "Cmd": null,
            "Healthcheck": {
                "Test": [
                    "NONE"
                ]
            },
            "Image": "sha256:291681d2405b6196f2552070d38cc3db42bbb84363e3c04e5b7f15bdb6272ef3",
            "Volumes": null,
            "WorkingDir": "/armada",
            "Entrypoint": [
                "/bin/bash",
                "-c",
                "set -x\n\nwhile true; do\n    sleep 10\n    if armada \\\n            apply \\\n            --target-manifest cluster-bootstrap-aiab \\\n            --tiller-host 127.0.0.1 \\\n            /etc/genesis/armada/assets/manifest.yaml &>> \"${ARMADA_LOGFILE}\"; then\n        break\n    fi\ndone\ntouch /ipc/armada-done\nsleep 10000"
            ],
            "OnBuild": null,
            "Labels": {
                "annotation.io.kubernetes.container.hash": "99764e8f",
                "annotation.io.kubernetes.container.restartCount": "3",
                "annotation.io.kubernetes.container.terminationMessagePath": "/dev/termination-log",
                "annotation.io.kubernetes.container.terminationMessagePolicy": "File",
                "annotation.io.kubernetes.pod.terminationGracePeriod": "30",
                "io.kubernetes.container.logpath": "/var/log/pods/77e267bf6417c36e4309c651e338866a/armada/3.log",
                "io.kubernetes.container.name": "armada",
                "io.kubernetes.docker.type": "container",
                "io.kubernetes.pod.name": "bootstrap-armada-airship",
                "io.kubernetes.pod.namespace": "kube-system",
                "io.kubernetes.pod.uid": "77e267bf6417c36e4309c651e338866a",
                "io.kubernetes.sandbox.id": "1de9a695cced6d1bccecd4a5a80584450c4e252ca42b15ecf3b2391141185393",
                "org.airshipit.build": "community",
                "org.opencontainers.image.authors": "airship-discuss@lists.airshipit.org, irc://#airshipit@freenode",
                "org.opencontainers.image.created": "2019-06-05 21:34:56+00:00",
                "org.opencontainers.image.documentation": "https://airship-armada.readthedocs.org",
                "org.opencontainers.image.licenses": "Apache-2.0",
                "org.opencontainers.image.revision": "2f28fb5bf04a613d9d31e53ff310c98555f6d179",
                "org.opencontainers.image.source": "https://opendev.org/airship/armada",
                "org.opencontainers.image.title": "armada",
                "org.opencontainers.image.url": "https://airshipit.org",
                "org.opencontainers.image.vendor": "The Airship Authors"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": null,
            "SandboxKey": "",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {}
        }
    }
]
[
    {
        "Id": "b35d081c782fab8d517c1fd67db6d02b294b4b9180a63a6df71a0fbccc423133",
        "Created": "2019-06-27T11:08:13.582576539Z",
        "Path": "/bin/sh",
        "Args": [
            "-c",
            "set -eux\n\nwhile [ ! -s \"$HAPROXY_CONF\" ]; do\n    echo Waiting for \"HAPROXY_CONF\"\n    sleep 1\ndone\n\nhaproxy -f \"$HAPROXY_CONF\"\n"
        ],
        "State": {
            "Status": "exited",
            "Running": false,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 0,
            "ExitCode": 255,
            "Error": "",
            "StartedAt": "2019-06-27T11:08:14.133237976Z",
            "FinishedAt": "2019-06-27T11:10:53.702755648Z"
        },
        "Image": "sha256:3163c3bb9b0d83e77c9e2af4d3da19cb793e6f60ef6c95e7d359149f1fba1a8c",
        "ResolvConfPath": "/var/lib/docker/containers/626fbed71c4eb5f73ed7cb81c6da9ea0ba4c183ee4b0755ea4c97da8d8735850/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/626fbed71c4eb5f73ed7cb81c6da9ea0ba4c183ee4b0755ea4c97da8d8735850/hostname",
        "HostsPath": "/var/lib/kubelet/pods/f29c4e58bbe06649af627575484caa9b/etc-hosts",
        "LogPath": "/var/lib/docker/containers/b35d081c782fab8d517c1fd67db6d02b294b4b9180a63a6df71a0fbccc423133/b35d081c782fab8d517c1fd67db6d02b294b4b9180a63a6df71a0fbccc423133-json.log",
        "Name": "/k8s_haproxy_haproxy-airship_kube-system_f29c4e58bbe06649af627575484caa9b_3",
        "RestartCount": 0,
        "Driver": "overlay2",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "docker-default",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": [
                "/etc/promenade/haproxy:/usr/local/etc/haproxy:ro",
                "/var/lib/kubelet/pods/f29c4e58bbe06649af627575484caa9b/etc-hosts:/etc/hosts",
                "/var/lib/kubelet/pods/f29c4e58bbe06649af627575484caa9b/containers/haproxy/e504db6b:/dev/termination-log"
            ],
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "container:626fbed71c4eb5f73ed7cb81c6da9ea0ba4c183ee4b0755ea4c97da8d8735850",
            "PortBindings": null,
            "RestartPolicy": {
                "Name": "",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "container:626fbed71c4eb5f73ed7cb81c6da9ea0ba4c183ee4b0755ea4c97da8d8735850",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 1000,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": [
                "seccomp=unconfined"
            ],
            "UTSMode": "host",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 2,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "/kubepods/besteffort/podf29c4e58bbe06649af627575484caa9b",
            "BlkioWeight": 0,
            "BlkioWeightDevice": null,
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DiskQuota": 0,
            "KernelMemory": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": false,
            "PidsLimit": 0,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0
        },
        "GraphDriver": {
            "Name": "overlay2",
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/5ffcd37d33fca2bdd907bf0d1675ace5f0bdf25f34cf02d2e75b5203277bc103-init/diff:/var/lib/docker/overlay2/bb9b2546ecfb8d0cece4be2ad5e7e953934c85a2dddd0553807ded08ec090a34/diff:/var/lib/docker/overlay2/fff9f721dbe5776a0e5abffa1c1531fdb7492c1449a6589c9b663c0774f3ca2b/diff:/var/lib/docker/overlay2/54a1766d549dbbaf5439e844dead3de65532dbde73a04ad84addb7ff2e2e3232/diff",
                "MergedDir": "/var/lib/docker/overlay2/5ffcd37d33fca2bdd907bf0d1675ace5f0bdf25f34cf02d2e75b5203277bc103/merged",
                "UpperDir": "/var/lib/docker/overlay2/5ffcd37d33fca2bdd907bf0d1675ace5f0bdf25f34cf02d2e75b5203277bc103/diff",
                "WorkDir": "/var/lib/docker/overlay2/5ffcd37d33fca2bdd907bf0d1675ace5f0bdf25f34cf02d2e75b5203277bc103/work"
            }
        },
        "Mounts": [
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/f29c4e58bbe06649af627575484caa9b/containers/haproxy/e504db6b",
                "Destination": "/dev/termination-log",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/var/lib/kubelet/pods/f29c4e58bbe06649af627575484caa9b/etc-hosts",
                "Destination": "/etc/hosts",
                "Mode": "",
                "RW": true,
                "Propagation": "rprivate"
            },
            {
                "Type": "bind",
                "Source": "/etc/promenade/haproxy",
                "Destination": "/usr/local/etc/haproxy",
                "Mode": "ro",
                "RW": false,
                "Propagation": "rprivate"
            }
        ],
        "Config": {
            "Hostname": "airsHiP",
            "Domainname": "",
            "User": "0",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "HAPROXY_CONF=/usr/local/etc/haproxy/haproxy.cfg",
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                "HAPROXY_VERSION=1.8.19",
                "HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.19.tar.gz",
                "HAPROXY_SHA256=64f5fbfd4e09ffeaf26cb6667398ba780704a14e96e60000caa8bf69962ba734"
            ],
            "Cmd": null,
            "Healthcheck": {
                "Test": [
                    "NONE"
                ]
            },
            "Image": "sha256:3163c3bb9b0d83e77c9e2af4d3da19cb793e6f60ef6c95e7d359149f1fba1a8c",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": [
                "/bin/sh",
                "-c",
                "set -eux\n\nwhile [ ! -s \"$HAPROXY_CONF\" ]; do\n    echo Waiting for \"HAPROXY_CONF\"\n    sleep 1\ndone\n\nhaproxy -f \"$HAPROXY_CONF\"\n"
            ],
            "OnBuild": null,
            "Labels": {
                "annotation.io.kubernetes.container.hash": "d994eb1c",
                "annotation.io.kubernetes.container.restartCount": "3",
                "annotation.io.kubernetes.container.terminationMessagePath": "/dev/termination-log",
                "annotation.io.kubernetes.container.terminationMessagePolicy": "File",
                "annotation.io.kubernetes.pod.terminationGracePeriod": "30",
                "io.kubernetes.container.logpath": "/var/log/pods/f29c4e58bbe06649af627575484caa9b/haproxy/3.log",
                "io.kubernetes.container.name": "haproxy",
                "io.kubernetes.docker.type": "container",
                "io.kubernetes.pod.name": "haproxy-airship",
                "io.kubernetes.pod.namespace": "kube-system",
                "io.kubernetes.pod.uid": "f29c4e58bbe06649af627575484caa9b",
                "io.kubernetes.sandbox.id": "626fbed71c4eb5f73ed7cb81c6da9ea0ba4c183ee4b0755ea4c97da8d8735850"
            },
            "StopSignal": "SIGUSR1"
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": null,
            "SandboxKey": "",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {}
        }
    }
]
[
    {
        "Id": "1de9a695cced6d1bccecd4a5a80584450c4e252ca42b15ecf3b2391141185393",
        "Created": "2019-06-27T11:08:12.673620116Z",
        "Path": "/pause",
        "Args": [],
        "State": {
            "Status": "exited",
            "Running": false,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 0,
            "ExitCode": 255,
            "Error": "",
            "StartedAt": "2019-06-27T11:08:13.456748315Z",
            "FinishedAt": "2019-06-27T11:10:54.107556281Z"
        },
        "Image": "sha256:da86e6ba6ca197bf6bc5e9d900febd906b133eaa4750e6bed647b0fbe50ed43e",
        "ResolvConfPath": "/var/lib/docker/containers/1de9a695cced6d1bccecd4a5a80584450c4e252ca42b15ecf3b2391141185393/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/1de9a695cced6d1bccecd4a5a80584450c4e252ca42b15ecf3b2391141185393/hostname",
        "HostsPath": "/var/lib/docker/containers/1de9a695cced6d1bccecd4a5a80584450c4e252ca42b15ecf3b2391141185393/hosts",
        "LogPath": "/var/lib/docker/containers/1de9a695cced6d1bccecd4a5a80584450c4e252ca42b15ecf3b2391141185393/1de9a695cced6d1bccecd4a5a80584450c4e252ca42b15ecf3b2391141185393-json.log",
        "Name": "/k8s_POD_bootstrap-armada-airship_kube-system_77e267bf6417c36e4309c651e338866a_3",
        "RestartCount": 0,
        "Driver": "overlay2",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "docker-default",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "host",
            "PortBindings": {
                "44134/tcp": [
                    {
                        "HostIp": "",
                        "HostPort": "44134"
                    }
                ]
            },
            "RestartPolicy": {
                "Name": "",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "shareable",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": -998,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": [
                "seccomp=unconfined"
            ],
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 2,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "/kubepods/besteffort/pod77e267bf6417c36e4309c651e338866a",
            "BlkioWeight": 0,
            "BlkioWeightDevice": null,
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": null,
            "DiskQuota": 0,
            "KernelMemory": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": false,
            "PidsLimit": 0,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0
        },
        "GraphDriver": {
            "Name": "overlay2",
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/5b50960d69d7219958edb480c57e8f22476d268be031ed5094eb348cb75f9322-init/diff:/var/lib/docker/overlay2/2d1df0d666ec7840e61832b13de4bc9a08ba067676cba04ea653b3d1f536ca99/diff",
                "MergedDir": "/var/lib/docker/overlay2/5b50960d69d7219958edb480c57e8f22476d268be031ed5094eb348cb75f9322/merged",
                "UpperDir": "/var/lib/docker/overlay2/5b50960d69d7219958edb480c57e8f22476d268be031ed5094eb348cb75f9322/diff",
                "WorkDir": "/var/lib/docker/overlay2/5b50960d69d7219958edb480c57e8f22476d268be031ed5094eb348cb75f9322/work"
            }
        },
        "Mounts": [],
        "Config": {
            "Hostname": "airsHiP",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "ExposedPorts": {
                "44134/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": null,
            "Image": "gcr.io/google-containers/pause-amd64:3.1",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": [
                "/pause"
            ],
            "OnBuild": null,
            "Labels": {
                "annotation.kubernetes.io/config.hash": "77e267bf6417c36e4309c651e338866a",
                "annotation.kubernetes.io/config.seen": "2019-06-27T12:58:04.3147465+02:00",
                "annotation.kubernetes.io/config.source": "file",
                "application": "promenade",
                "component": "genesis-tiller",
                "io.kubernetes.container.name": "POD",
                "io.kubernetes.docker.type": "podsandbox",
                "io.kubernetes.pod.name": "bootstrap-armada-airship",
                "io.kubernetes.pod.namespace": "kube-system",
                "io.kubernetes.pod.uid": "77e267bf6417c36e4309c651e338866a"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "2bf9d96f1e575d544f4a4f8b9c7b9c00d52ee53f3e168290ad66ba897d488a4c",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": {},
            "SandboxKey": "/var/run/docker/netns/default",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {
                "host": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": null,
                    "NetworkID": "fb005355db919b8b3b3fca41a7a4de6e847f7f835f36433c22978fad8bf48052",
                    "EndpointID": "5d087ed7b5985cfc8c2c5cf89d104a297d4a906779766182fae518bee0e483fa",
                    "Gateway": "",
                    "IPAddress": "",
                    "IPPrefixLen": 0,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "MacAddress": ""
                }
            }
        }
    }
]
[
    {
        "Id": "626fbed71c4eb5f73ed7cb81c6da9ea0ba4c183ee4b0755ea4c97da8d8735850",
        "Created": "2019-06-27T11:08:12.621335405Z",
        "Path": "/pause",
        "Args": [],
        "State": {
            "Status": "exited",
            "Running": false,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 0,
            "ExitCode": 255,
            "Error": "",
            "StartedAt": "2019-06-27T11:08:13.45611303Z",
            "FinishedAt": "2019-06-27T11:10:54.077731935Z"
        },
        "Image": "sha256:da86e6ba6ca197bf6bc5e9d900febd906b133eaa4750e6bed647b0fbe50ed43e",
        "ResolvConfPath": "/var/lib/docker/containers/626fbed71c4eb5f73ed7cb81c6da9ea0ba4c183ee4b0755ea4c97da8d8735850/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/626fbed71c4eb5f73ed7cb81c6da9ea0ba4c183ee4b0755ea4c97da8d8735850/hostname",
        "HostsPath": "/var/lib/docker/containers/626fbed71c4eb5f73ed7cb81c6da9ea0ba4c183ee4b0755ea4c97da8d8735850/hosts",
        "LogPath": "/var/lib/docker/containers/626fbed71c4eb5f73ed7cb81c6da9ea0ba4c183ee4b0755ea4c97da8d8735850/626fbed71c4eb5f73ed7cb81c6da9ea0ba4c183ee4b0755ea4c97da8d8735850-json.log",
        "Name": "/k8s_POD_haproxy-airship_kube-system_f29c4e58bbe06649af627575484caa9b_3",
        "RestartCount": 0,
        "Driver": "overlay2",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "docker-default",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "host",
            "PortBindings": {},
            "RestartPolicy": {
                "Name": "",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "shareable",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": -998,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": [
                "seccomp=unconfined"
            ],
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 2,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "/kubepods/besteffort/podf29c4e58bbe06649af627575484caa9b",
            "BlkioWeight": 0,
            "BlkioWeightDevice": null,
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": null,
            "DiskQuota": 0,
            "KernelMemory": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": false,
            "PidsLimit": 0,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0
        },
        "GraphDriver": {
            "Name": "overlay2",
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/f2f46ca8861de6f972f1ec09201377b5e68e3e2acc657e6afb79a2059554b450-init/diff:/var/lib/docker/overlay2/2d1df0d666ec7840e61832b13de4bc9a08ba067676cba04ea653b3d1f536ca99/diff",
                "MergedDir": "/var/lib/docker/overlay2/f2f46ca8861de6f972f1ec09201377b5e68e3e2acc657e6afb79a2059554b450/merged",
                "UpperDir": "/var/lib/docker/overlay2/f2f46ca8861de6f972f1ec09201377b5e68e3e2acc657e6afb79a2059554b450/diff",
                "WorkDir": "/var/lib/docker/overlay2/f2f46ca8861de6f972f1ec09201377b5e68e3e2acc657e6afb79a2059554b450/work"
            }
        },
        "Mounts": [],
        "Config": {
            "Hostname": "airsHiP",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": null,
            "Image": "gcr.io/google-containers/pause-amd64:3.1",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": [
                "/pause"
            ],
            "OnBuild": null,
            "Labels": {
                "annotation.kubernetes.io/config.hash": "f29c4e58bbe06649af627575484caa9b",
                "annotation.kubernetes.io/config.seen": "2019-06-27T12:58:04.314748598+02:00",
                "annotation.kubernetes.io/config.source": "file",
                "annotation.scheduler.alpha.kubernetes.io/critical-pod": "",
                "io.kubernetes.container.name": "POD",
                "io.kubernetes.docker.type": "podsandbox",
                "io.kubernetes.pod.name": "haproxy-airship",
                "io.kubernetes.pod.namespace": "kube-system",
                "io.kubernetes.pod.uid": "f29c4e58bbe06649af627575484caa9b"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "a97a6bbe69a47280ab98f4abcb0411e99f1d39c99a8b24054bf361292b8aa5db",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": {},
            "SandboxKey": "/var/run/docker/netns/default",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {
                "host": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": null,
                    "NetworkID": "fb005355db919b8b3b3fca41a7a4de6e847f7f835f36433c22978fad8bf48052",
                    "EndpointID": "80140d50a56ecc35295369d03392244a5c289124477c323f6bc6c2fed716e57b",
                    "Gateway": "",
                    "IPAddress": "",
                    "IPPrefixLen": 0,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "MacAddress": ""
                }
            }
        }
    }
]
[
    {
        "Id": "44dba7fbacdc18f8f249ec2ac7fe231069a782070253649ad401cf7cd1876a0c",
        "Created": "2019-06-27T11:08:12.612419178Z",
        "Path": "/pause",
        "Args": [],
        "State": {
            "Status": "exited",
            "Running": false,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 0,
            "ExitCode": 255,
            "Error": "",
            "StartedAt": "2019-06-27T11:08:13.285180968Z",
            "FinishedAt": "2019-06-27T11:10:54.172271088Z"
        },
        "Image": "sha256:da86e6ba6ca197bf6bc5e9d900febd906b133eaa4750e6bed647b0fbe50ed43e",
        "ResolvConfPath": "/var/lib/docker/containers/44dba7fbacdc18f8f249ec2ac7fe231069a782070253649ad401cf7cd1876a0c/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/44dba7fbacdc18f8f249ec2ac7fe231069a782070253649ad401cf7cd1876a0c/hostname",
        "HostsPath": "/var/lib/docker/containers/44dba7fbacdc18f8f249ec2ac7fe231069a782070253649ad401cf7cd1876a0c/hosts",
        "LogPath": "/var/lib/docker/containers/44dba7fbacdc18f8f249ec2ac7fe231069a782070253649ad401cf7cd1876a0c/44dba7fbacdc18f8f249ec2ac7fe231069a782070253649ad401cf7cd1876a0c-json.log",
        "Name": "/k8s_POD_auxiliary-etcd-airship_kube-system_3c8223a65caffe3d69e99bfb925d15b7_3",
        "RestartCount": 0,
        "Driver": "overlay2",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "docker-default",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "host",
            "PortBindings": {
                "12379/tcp": [
                    {
                        "HostIp": "",
                        "HostPort": "12379"
                    }
                ],
                "12380/tcp": [
                    {
                        "HostIp": "",
                        "HostPort": "12380"
                    }
                ],
                "22379/tcp": [
                    {
                        "HostIp": "",
                        "HostPort": "22379"
                    }
                ],
                "22380/tcp": [
                    {
                        "HostIp": "",
                        "HostPort": "22380"
                    }
                ]
            },
            "RestartPolicy": {
                "Name": "",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "shareable",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": -998,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": [
                "seccomp=unconfined"
            ],
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 2,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "/kubepods/besteffort/pod3c8223a65caffe3d69e99bfb925d15b7",
            "BlkioWeight": 0,
            "BlkioWeightDevice": null,
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": null,
            "DiskQuota": 0,
            "KernelMemory": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": false,
            "PidsLimit": 0,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0
        },
        "GraphDriver": {
            "Name": "overlay2",
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/b67ecd626e1688a59ef4a5d88ac1600a88ada92f05dbdade56e8d2d1a4ac6770-init/diff:/var/lib/docker/overlay2/2d1df0d666ec7840e61832b13de4bc9a08ba067676cba04ea653b3d1f536ca99/diff",
                "MergedDir": "/var/lib/docker/overlay2/b67ecd626e1688a59ef4a5d88ac1600a88ada92f05dbdade56e8d2d1a4ac6770/merged",
                "UpperDir": "/var/lib/docker/overlay2/b67ecd626e1688a59ef4a5d88ac1600a88ada92f05dbdade56e8d2d1a4ac6770/diff",
                "WorkDir": "/var/lib/docker/overlay2/b67ecd626e1688a59ef4a5d88ac1600a88ada92f05dbdade56e8d2d1a4ac6770/work"
            }
        },
        "Mounts": [],
        "Config": {
            "Hostname": "airsHiP",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "ExposedPorts": {
                "12379/tcp": {},
                "12380/tcp": {},
                "22379/tcp": {},
                "22380/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": null,
            "Image": "gcr.io/google-containers/pause-amd64:3.1",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": [
                "/pause"
            ],
            "OnBuild": null,
            "Labels": {
                "annotation.kubernetes.io/config.hash": "3c8223a65caffe3d69e99bfb925d15b7",
                "annotation.kubernetes.io/config.seen": "2019-06-27T12:58:04.314731405+02:00",
                "annotation.kubernetes.io/config.source": "file",
                "application": "kubernetes",
                "component": "auxiliary-etcd",
                "io.kubernetes.container.name": "POD",
                "io.kubernetes.docker.type": "podsandbox",
                "io.kubernetes.pod.name": "auxiliary-etcd-airship",
                "io.kubernetes.pod.namespace": "kube-system",
                "io.kubernetes.pod.uid": "3c8223a65caffe3d69e99bfb925d15b7",
                "promenade": "genesis"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "c4590a14e06d94a0a52dac33d32c18ae88252369cdb3e31bc117e9d17b8a816a",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": {},
            "SandboxKey": "/var/run/docker/netns/default",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {
                "host": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": null,
                    "NetworkID": "fb005355db919b8b3b3fca41a7a4de6e847f7f835f36433c22978fad8bf48052",
                    "EndpointID": "396b896ea5d4ee4d0c9f10df53cdba9e62b6a287c5f0cef49c17a9a213bc1b19",
                    "Gateway": "",
                    "IPAddress": "",
                    "IPPrefixLen": 0,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "MacAddress": ""
                }
            }
        }
    }
]
Error when running genesis.
To remove files generated during this script's execution, delete /root/deploy/treasuremap/../.
This VM is disposable. Re-deployment in this same VM will lead to unpredictable results.
```
