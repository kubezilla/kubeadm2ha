```
TASK [nginx : Generate service configuraton file] *********************************************************************************************
skipping: [md-kubernetes-master-1]
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]

TASK [nginx : Generate static pod configuraton file directory] ********************************************************************************
skipping: [md-kubernetes-master-1]
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]

TASK [nginx : Generate static pod configuraton file] ******************************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-1]
skipping: [md-kubernetes-master-3]

PLAY [HAProxy] ********************************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-3]

TASK [haproxy : Create configuration directory] ***********************************************************************************************
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-3]

TASK [haproxy : Generate service configuraton file] *******************************************************************************************
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-3]

TASK [haproxy : Generate static pod configuraton file directory] ******************************************************************************
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-3]

TASK [haproxy : Generate static pod configuraton file] ****************************************************************************************
changed: [md-kubernetes-master-1]
changed: [md-kubernetes-master-2]
changed: [md-kubernetes-master-3]

PLAY [Deploy external etcd] *******************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-3]

TASK [external-etcd : Install preliminary kubelet configuration for systemd] ******************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Activate and restart kubelet] *******************************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Clean up /etc/kubernetes/manifests/etcd.yaml from previous installations] ***********************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Clean up /var/lib/etcd/member from previous installations] **************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Clean up /etc/kubernetes/pki from previous installations] ***************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Clean up /tmp/etcd from previous installations on primary etcd node] ****************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Create temporary cert directories on primary etcd node] *****************************************************************
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-2)
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-2)
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-2)
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-3)
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-3)
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-3)
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-1)
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-1)
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-1)

TASK [external-etcd : Generate kubeadmcfg.yaml on primary etcd node] **************************************************************************
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-2)
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-3)
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-1)
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-2)
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-3)
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-1)
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-2)
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-3)
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-1)

TASK [external-etcd : Create etcd CA] *********************************************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Create script for creating all certs for all etcd nodes primary etcd node] **********************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Run script for creating all certs for all etcd nodes primary etcd node] *************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Archive certificate files on primary etcd node] *************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Fetch certificate files from primary etcd node] *************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-1]
skipping: [md-kubernetes-master-3]

TASK [external-etcd : Unarchive certificates on localhost...] *********************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Copy certs to all etcd nodes] *******************************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Copy kubeadmcfg.yaml to all etcd nodes] *********************************************************************************
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Create etcd manifests on all etcd nodes] ********************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Archive certs for master nodes on primary etcd node] ********************************************************************
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Fetch master certs from primary etcd node] ******************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Check etcd cluster health on primary etcd node] *************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

PLAY [Set up primary master] ******************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
ok: [md-kubernetes-master-1]

TASK [primary-master : Generate 'kubeadm' configuration file (external etcd only)] ************************************************************
skipping: [md-kubernetes-master-1]

TASK [primary-master : Remove /etc/systemd/system/kubelet.service.d/20-etcd-service-manager.conf on primary master (external etcd only)] ******
skipping: [md-kubernetes-master-1]

TASK [primary-master : Stop kubelet on primary master] ****************************************************************************************
ok: [md-kubernetes-master-1]

TASK [primary-master : Run 'kubeadm init' (external etcd only)] *******************************************************************************
skipping: [md-kubernetes-master-1]

TASK [primary-master : Run 'kubeadm init' (stacked etcd only)] ********************************************************************************
fatal: [md-kubernetes-master-1]: FAILED! => {"changed": true, "cmd": "kubeadm init --control-plane-endpoint '165.22.210.124:8443' --upload-certs --kubernetes-version 'v1.18.4' 2>&1 | tee /tmp/kubeadm-init.out; exit ${PIPESTATUS[0]}", "delta": "0:00:30.544012", "end": "2020-06-26 12:24:38.153231", "msg": "non-zero return code", "rc": 2, "start": "2020-06-26 12:24:07.609219", "stderr": "/bin/sh: 1: Bad substitution", "stderr_lines": ["/bin/sh: 1: Bad substitution"], "stdout": "W0626 12:24:07.856649    2555 configset.go:202] WARNING: kubeadm cannot validate component configs for API groups [kubelet.config.k8s.io kubeproxy.config.k8s.io]\n[init] Using Kubernetes version: v1.18.4\n[preflight] Running pre-flight checks\n\t[WARNING IsDockerSystemdCheck]: detected \"cgroupfs\" as the Docker cgroup driver. The recommended driver is \"systemd\". Please follow the guide at https://kubernetes.io/docs/setup/cri/\n[preflight] Pulling images required for setting up a Kubernetes cluster\n[preflight] This might take a minute or two, depending on the speed of your internet connection\n[preflight] You can also perform this action in beforehand using 'kubeadm config images pull'\n[kubelet-start] Writing kubelet environment file with flags to file \"/var/lib/kubelet/kubeadm-flags.env\"\n[kubelet-start] Writing kubelet configuration to file \"/var/lib/kubelet/config.yaml\"\n[kubelet-start] Starting the kubelet\n[certs] Using certificateDir folder \"/etc/kubernetes/pki\"\n[certs] Generating \"ca\" certificate and key\n[certs] Generating \"apiserver\" certificate and key\n[certs] apiserver serving cert is signed for DNS names [ha-proxy kubernetes kubernetes.default kubernetes.default.svc kubernetes.default.svc.cluster.local] and IPs [10.96.0.1 165.22.210.124 165.22.210.124]\n[certs] Generating \"apiserver-kubelet-client\" certificate and key\n[certs] Generating \"front-proxy-ca\" certificate and key\n[certs] Generating \"front-proxy-client\" certificate and key\n[certs] Generating \"etcd/ca\" certificate and key\n[certs] Generating \"etcd/server\" certificate and key\n[certs] etcd/server serving cert is signed for DNS names [ha-proxy localhost] and IPs [165.22.210.124 127.0.0.1 ::1]\n[certs] Generating \"etcd/peer\" certificate and key\n[certs] etcd/peer serving cert is signed for DNS names [ha-proxy localhost] and IPs [165.22.210.124 127.0.0.1 ::1]\n[certs] Generating \"etcd/healthcheck-client\" certificate and key\n[certs] Generating \"apiserver-etcd-client\" certificate and key\n[certs] Generating \"sa\" key and public key\n[kubeconfig] Using kubeconfig folder \"/etc/kubernetes\"\n[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address\n[kubeconfig] Writing \"admin.conf\" kubeconfig file\n[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address\n[kubeconfig] Writing \"kubelet.conf\" kubeconfig file\n[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address\n[kubeconfig] Writing \"controller-manager.conf\" kubeconfig file\n[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address\n[kubeconfig] Writing \"scheduler.conf\" kubeconfig file\n[control-plane] Using manifest folder \"/etc/kubernetes/manifests\"\n[control-plane] Creating static Pod manifest for \"kube-apiserver\"\n[control-plane] Creating static Pod manifest for \"kube-controller-manager\"\nW0626 12:24:13.824174    2555 manifests.go:225] the default kube-apiserver authorization-mode is \"Node,RBAC\"; using \"Node,RBAC\"\n[control-plane] Creating static Pod manifest for \"kube-scheduler\"\nW0626 12:24:13.825428    2555 manifests.go:225] the default kube-apiserver authorization-mode is \"Node,RBAC\"; using \"Node,RBAC\"\n[etcd] Creating static Pod manifest for local etcd in \"/etc/kubernetes/manifests\"\n[wait-control-plane] Waiting for the kubelet to boot up the control plane as static Pods from directory \"/etc/kubernetes/manifests\". This can take up to 4m0s\n[apiclient] All control plane components are healthy after 20.046758 seconds\n[upload-config] Storing the configuration used in ConfigMap \"kubeadm-config\" in the \"kube-system\" Namespace\n[kubelet] Creating a ConfigMap \"kubelet-config-1.18\" in namespace kube-system with the configuration for the kubelets in the cluster\n[upload-certs] Storing the certificates in Secret \"kubeadm-certs\" in the \"kube-system\" Namespace\n[upload-certs] Using certificate key:\n18a7584876002e49e1f42c351582c0a455d061db25376170068731d9aa210f58\n[mark-control-plane] Marking the node ha-proxy as control-plane by adding the label \"node-role.kubernetes.io/master=''\"\n[mark-control-plane] Marking the node ha-proxy as control-plane by adding the taints [node-role.kubernetes.io/master:NoSchedule]\n[bootstrap-token] Using token: xgrbom.0ibjo2i6hxabazxi\n[bootstrap-token] Configuring bootstrap tokens, cluster-info ConfigMap, RBAC Roles\n[bootstrap-token] configured RBAC rules to allow Node Bootstrap tokens to get nodes\n[bootstrap-token] configured RBAC rules to allow Node Bootstrap tokens to post CSRs in order for nodes to get long term certificate credentials\n[bootstrap-token] configured RBAC rules to allow the csrapprover controller automatically approve CSRs from a Node Bootstrap Token\n[bootstrap-token] configured RBAC rules to allow certificate rotation for all node client certificates in the cluster\n[bootstrap-token] Creating the \"cluster-info\" ConfigMap in the \"kube-public\" namespace\n[kubelet-finalize] Updating \"/etc/kubernetes/kubelet.conf\" to point to a rotatable kubelet client certificate and key\n[addons] Applied essential addon: CoreDNS\n[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address\n[addons] Applied essential addon: kube-proxy\n\nYour Kubernetes control-plane has initialized successfully!\n\nTo start using your cluster, you need to run the following as a regular user:\n\n  mkdir -p $HOME/.kube\n  sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config\n  sudo chown $(id -u):$(id -g) $HOME/.kube/config\n\nYou should now deploy a pod network to the cluster.\nRun \"kubectl apply -f [podnetwork].yaml\" with one of the options listed at:\n  https://kubernetes.io/docs/concepts/cluster-administration/addons/\n\nYou can now join any number of the control-plane node running the following command on each as root:\n\n  kubeadm join 165.22.210.124:8443 --token xgrbom.0ibjo2i6hxabazxi \\\n    --discovery-token-ca-cert-hash sha256:bde7f33168b6c7f0338c742883f5bd8bd8953f92ebf06aa5e7a20be0322195c1 \\\n    --control-plane --certificate-key 18a7584876002e49e1f42c351582c0a455d061db25376170068731d9aa210f58\n\nPlease note that the certificate-key gives access to cluster sensitive data, keep it secret!\nAs a safeguard, uploaded-certs will be deleted in two hours; If necessary, you can use\n\"kubeadm init phase upload-certs --upload-certs\" to reload certs afterward.\n\nThen you can join any number of worker nodes by running the following on each as root:\n\nkubeadm join 165.22.210.124:8443 --token xgrbom.0ibjo2i6hxabazxi \\\n    --discovery-token-ca-cert-hash sha256:bde7f33168b6c7f0338c742883f5bd8bd8953f92ebf06aa5e7a20be0322195c1 ", "stdout_lines": ["W0626 12:24:07.856649    2555 configset.go:202] WARNING: kubeadm cannot validate component configs for API groups [kubelet.config.k8s.io kubeproxy.config.k8s.io]", "[init] Using Kubernetes version: v1.18.4", "[preflight] Running pre-flight checks", "\t[WARNING IsDockerSystemdCheck]: detected \"cgroupfs\" as the Docker cgroup driver. The recommended driver is \"systemd\". Please follow the guide at https://kubernetes.io/docs/setup/cri/", "[preflight] Pulling images required for setting up a Kubernetes cluster", "[preflight] This might take a minute or two, depending on the speed of your internet connection", "[preflight] You can also perform this action in beforehand using 'kubeadm config images pull'", "[kubelet-start] Writing kubelet environment file with flags to file \"/var/lib/kubelet/kubeadm-flags.env\"", "[kubelet-start] Writing kubelet configuration to file \"/var/lib/kubelet/config.yaml\"", "[kubelet-start] Starting the kubelet", "[certs] Using certificateDir folder \"/etc/kubernetes/pki\"", "[certs] Generating \"ca\" certificate and key", "[certs] Generating \"apiserver\" certificate and key", "[certs] apiserver serving cert is signed for DNS names [ha-proxy kubernetes kubernetes.default kubernetes.default.svc kubernetes.default.svc.cluster.local] and IPs [10.96.0.1 165.22.210.124 165.22.210.124]", "[certs] Generating \"apiserver-kubelet-client\" certificate and key", "[certs] Generating \"front-proxy-ca\" certificate and key", "[certs] Generating \"front-proxy-client\" certificate and key", "[certs] Generating \"etcd/ca\" certificate and key", "[certs] Generating \"etcd/server\" certificate and key", "[certs] etcd/server serving cert is signed for DNS names [ha-proxy localhost] and IPs [165.22.210.124 127.0.0.1 ::1]", "[certs] Generating \"etcd/peer\" certificate and key", "[certs] etcd/peer serving cert is signed for DNS names [ha-proxy localhost] and IPs [165.22.210.124 127.0.0.1 ::1]", "[certs] Generating \"etcd/healthcheck-client\" certificate and key", "[certs] Generating \"apiserver-etcd-client\" certificate and key", "[certs] Generating \"sa\" key and public key", "[kubeconfig] Using kubeconfig folder \"/etc/kubernetes\"", "[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address", "[kubeconfig] Writing \"admin.conf\" kubeconfig file", "[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address", "[kubeconfig] Writing \"kubelet.conf\" kubeconfig file", "[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address", "[kubeconfig] Writing \"controller-manager.conf\" kubeconfig file", "[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address", "[kubeconfig] Writing \"scheduler.conf\" kubeconfig file", "[control-plane] Using manifest folder \"/etc/kubernetes/manifests\"", "[control-plane] Creating static Pod manifest for \"kube-apiserver\"", "[control-plane] Creating static Pod manifest for \"kube-controller-manager\"", "W0626 12:24:13.824174    2555 manifests.go:225] the default kube-apiserver authorization-mode is \"Node,RBAC\"; using \"Node,RBAC\"", "[control-plane] Creating static Pod manifest for \"kube-scheduler\"", "W0626 12:24:13.825428    2555 manifests.go:225] the default kube-apiserver authorization-mode is \"Node,RBAC\"; using \"Node,RBAC\"", "[etcd] Creating static Pod manifest for local etcd in \"/etc/kubernetes/manifests\"", "[wait-control-plane] Waiting for the kubelet to boot up the control plane as static Pods from directory \"/etc/kubernetes/manifests\". This can take up to 4m0s", "[apiclient] All control plane components are healthy after 20.046758 seconds", "[upload-config] Storing the configuration used in ConfigMap \"kubeadm-config\" in the \"kube-system\" Namespace", "[kubelet] Creating a ConfigMap \"kubelet-config-1.18\" in namespace kube-system with the configuration for the kubelets in the cluster", "[upload-certs] Storing the certificates in Secret \"kubeadm-certs\" in the \"kube-system\" Namespace", "[upload-certs] Using certificate key:", "18a7584876002e49e1f42c351582c0a455d061db25376170068731d9aa210f58", "[mark-control-plane] Marking the node ha-proxy as control-plane by adding the label \"node-role.kubernetes.io/master=''\"", "[mark-control-plane] Marking the node ha-proxy as control-plane by adding the taints [node-role.kubernetes.io/master:NoSchedule]", "[bootstrap-token] Using token: xgrbom.0ibjo2i6hxabazxi", "[bootstrap-token] Configuring bootstrap tokens, cluster-info ConfigMap, RBAC Roles", "[bootstrap-token] configured RBAC rules to allow Node Bootstrap tokens to get nodes", "[bootstrap-token] configured RBAC rules to allow Node Bootstrap tokens to post CSRs in order for nodes to get long term certificate credentials", "[bootstrap-token] configured RBAC rules to allow the csrapprover controller automatically approve CSRs from a Node Bootstrap Token", "[bootstrap-token] configured RBAC rules to allow certificate rotation for all node client certificates in the cluster", "[bootstrap-token] Creating the \"cluster-info\" ConfigMap in the \"kube-public\" namespace", "[kubelet-finalize] Updating \"/etc/kubernetes/kubelet.conf\" to point to a rotatable kubelet client certificate and key", "[addons] Applied essential addon: CoreDNS", "[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address", "[addons] Applied essential addon: kube-proxy", "", "Your Kubernetes control-plane has initialized successfully!", "", "To start using your cluster, you need to run the following as a regular user:", "", "  mkdir -p $HOME/.kube", "  sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config", "  sudo chown $(id -u):$(id -g) $HOME/.kube/config", "", "You should now deploy a pod network to the cluster.", "Run \"kubectl apply -f [podnetwork].yaml\" with one of the options listed at:", "  https://kubernetes.io/docs/concepts/cluster-administration/addons/", "", "You can now join any number of the control-plane node running the following command on each as root:", "", "  kubeadm join 165.22.210.124:8443 --token xgrbom.0ibjo2i6hxabazxi \\", "    --discovery-token-ca-cert-hash sha256:bde7f33168b6c7f0338c742883f5bd8bd8953f92ebf06aa5e7a20be0322195c1 \\", "    --control-plane --certificate-key 18a7584876002e49e1f42c351582c0a455d061db25376170068731d9aa210f58", "", "Please note that the certificate-key gives access to cluster sensitive data, keep it secret!", "As a safeguard, uploaded-certs will be deleted in two hours; If necessary, you can use", "\"kubeadm init phase upload-certs --upload-certs\" to reload certs afterward.", "", "Then you can join any number of worker nodes by running the following on each as root:", "", "kubeadm join 165.22.210.124:8443 --token xgrbom.0ibjo2i6hxabazxi \\", "    --discovery-token-ca-cert-hash sha256:bde7f33168b6c7f0338c742883f5bd8bd8953f92ebf06aa5e7a20be0322195c1 "]}

NO MORE HOSTS LEFT ****************************************************************************************************************************

PLAY RECAP ************************************************************************************************************************************
md-kubernetes-master-1     : ok=21   changed=4    unreachable=0    failed=1    skipped=31   rescued=0    ignored=0
md-kubernetes-master-2     : ok=17   changed=4    unreachable=0    failed=0    skipped=30   rescued=0    ignored=0
md-kubernetes-master-3     : ok=17   changed=4    unreachable=0    failed=0    skipped=30   rescued=0    ignored=0
md-kubernetes-minion-4     : ok=3    changed=1    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

[Captains-Bay]🚩 >
[Captains-Bay]🚩 >
[Captains-Bay]🚩 >
[Captains-Bay]🚩 >  ls
TODO				cluster-upgrade.yaml		images.lst			templates
cluster-dashboard.yaml		efk-stack.yaml			local-access.yaml		uninstall-dashboard.yaml
cluster-images.yaml		etcd-operator.yaml		my-cluster.inventory		uninstall-efk-stack.yaml
cluster-setup.yaml		files				prometheus-operator.yaml	xxx.yaml
cluster-uninstall.yaml		group_vars			roles
[Captains-Bay]🚩 >  vi my-cluster.inventory
[Captains-Bay]🚩 >  vansible-playbook -vv -i my-cluster.inventory cluster-setup.yaml
ansible-playbook 2.9.10
  config file = None
  configured module search path = ['/Users/ajeetraina/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/local/Cellar/ansible/2.9.10/libexec/lib/python3.8/site-packages/ansible
  executable location = /usr/local/bin/ansible-playbook
  python version = 3.8.3 (default, May 27 2020, 20:53:50) [Clang 10.0.0 (clang-1000.11.45.5)]
No config file found; using defaults
statically imported: /Users/ajeetraina/kubeadm2ha/ansible/roles/network-plugin/tasks/weavenet.yaml
statically imported: /Users/ajeetraina/kubeadm2ha/ansible/roles/network-plugin/tasks/flannel.yaml
statically imported: /Users/ajeetraina/kubeadm2ha/ansible/roles/network-plugin/tasks/calico.yaml

PLAYBOOK: cluster-setup.yaml ******************************************************************************************************************
13 plays in cluster-setup.yaml

PLAY [Prepare Nodes] **************************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/cluster-setup.yaml:5
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-minion-4]
ok: [md-kubernetes-master-1]
META: ran handlers

TASK [prepare-nodes : Make sure some needed software is installed via package manager] ********************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/prepare-nodes/tasks/main.yaml:6
ok: [md-kubernetes-master-2] => (item=perl) => {"ansible_loop_var": "item", "cache_update_time": 1593164949, "cache_updated": false, "changed": false, "item": "perl"}
ok: [md-kubernetes-master-3] => (item=perl) => {"ansible_loop_var": "item", "cache_update_time": 1593165097, "cache_updated": false, "changed": false, "item": "perl"}
ok: [md-kubernetes-minion-4] => (item=perl) => {"ansible_loop_var": "item", "cache_update_time": 1593169962, "cache_updated": false, "changed": false, "item": "perl"}
ok: [md-kubernetes-master-1] => (item=perl) => {"ansible_loop_var": "item", "cache_update_time": 1593170357, "cache_updated": false, "changed": false, "item": "perl"}
ok: [md-kubernetes-master-2] => (item=kubelet) => {"ansible_loop_var": "item", "cache_update_time": 1593164949, "cache_updated": false, "changed": false, "item": "kubelet"}
ok: [md-kubernetes-master-3] => (item=kubelet) => {"ansible_loop_var": "item", "cache_update_time": 1593165097, "cache_updated": false, "changed": false, "item": "kubelet"}
ok: [md-kubernetes-minion-4] => (item=kubelet) => {"ansible_loop_var": "item", "cache_update_time": 1593169962, "cache_updated": false, "changed": false, "item": "kubelet"}
ok: [md-kubernetes-master-1] => (item=kubelet) => {"ansible_loop_var": "item", "cache_update_time": 1593170357, "cache_updated": false, "changed": false, "item": "kubelet"}
ok: [md-kubernetes-master-2] => (item=kubectl) => {"ansible_loop_var": "item", "cache_update_time": 1593164949, "cache_updated": false, "changed": false, "item": "kubectl"}
ok: [md-kubernetes-master-3] => (item=kubectl) => {"ansible_loop_var": "item", "cache_update_time": 1593165097, "cache_updated": false, "changed": false, "item": "kubectl"}
ok: [md-kubernetes-minion-4] => (item=kubectl) => {"ansible_loop_var": "item", "cache_update_time": 1593169962, "cache_updated": false, "changed": false, "item": "kubectl"}
ok: [md-kubernetes-master-1] => (item=kubectl) => {"ansible_loop_var": "item", "cache_update_time": 1593170357, "cache_updated": false, "changed": false, "item": "kubectl"}
ok: [md-kubernetes-master-2] => (item=kubeadm) => {"ansible_loop_var": "item", "cache_update_time": 1593164949, "cache_updated": false, "changed": false, "item": "kubeadm"}
ok: [md-kubernetes-master-3] => (item=kubeadm) => {"ansible_loop_var": "item", "cache_update_time": 1593165097, "cache_updated": false, "changed": false, "item": "kubeadm"}
ok: [md-kubernetes-minion-4] => (item=kubeadm) => {"ansible_loop_var": "item", "cache_update_time": 1593169962, "cache_updated": false, "changed": false, "item": "kubeadm"}
ok: [md-kubernetes-master-1] => (item=kubeadm) => {"ansible_loop_var": "item", "cache_update_time": 1593170357, "cache_updated": false, "changed": false, "item": "kubeadm"}
ok: [md-kubernetes-master-2] => (item=kubernetes-cni) => {"ansible_loop_var": "item", "cache_update_time": 1593164949, "cache_updated": false, "changed": false, "item": "kubernetes-cni"}
ok: [md-kubernetes-master-3] => (item=kubernetes-cni) => {"ansible_loop_var": "item", "cache_update_time": 1593165097, "cache_updated": false, "changed": false, "item": "kubernetes-cni"}
ok: [md-kubernetes-minion-4] => (item=kubernetes-cni) => {"ansible_loop_var": "item", "cache_update_time": 1593169962, "cache_updated": false, "changed": false, "item": "kubernetes-cni"}
ok: [md-kubernetes-master-1] => (item=kubernetes-cni) => {"ansible_loop_var": "item", "cache_update_time": 1593170357, "cache_updated": false, "changed": false, "item": "kubernetes-cni"}

TASK [prepare-nodes : Enable kubelet] *********************************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/prepare-nodes/tasks/main.yaml:15
ok: [md-kubernetes-minion-4] => {"changed": false, "enabled": true, "name": "kubelet", "status": {"ActiveEnterTimestampMonotonic": "0", "ActiveExitTimestampMonotonic": "0", "ActiveState": "inactive", "After": "system.slice systemd-journald.socket network-online.target sysinit.target basic.target", "AllowIsolate": "no", "AmbientCapabilities": "", "AssertResult": "no", "AssertTimestampMonotonic": "0", "Before": "shutdown.target multi-user.target", "BlockIOAccounting": "no", "BlockIOWeight": "[not set]", "CPUAccounting": "no", "CPUQuotaPerSecUSec": "infinity", "CPUSchedulingPolicy": "0", "CPUSchedulingPriority": "0", "CPUSchedulingResetOnFork": "no", "CPUShares": "[not set]", "CPUUsageNSec": "[not set]", "CPUWeight": "[not set]", "CacheDirectoryMode": "0755", "CanIsolate": "no", "CanReload": "no", "CanStart": "yes", "CanStop": "yes", "CapabilityBoundingSet": "cap_chown cap_dac_override cap_dac_read_search cap_fowner cap_fsetid cap_kill cap_setgid cap_setuid cap_setpcap cap_linux_immutable cap_net_bind_service cap_net_broadcast cap_net_admin cap_net_raw cap_ipc_lock cap_ipc_owner cap_sys_module cap_sys_rawio cap_sys_chroot cap_sys_ptrace cap_sys_pacct cap_sys_admin cap_sys_boot cap_sys_nice cap_sys_resource cap_sys_time cap_sys_tty_config cap_mknod cap_lease cap_audit_write cap_audit_control cap_setfcap cap_mac_override cap_mac_admin cap_syslog cap_wake_alarm cap_block_suspend", "CollectMode": "inactive", "ConditionResult": "no", "ConditionTimestampMonotonic": "0", "ConfigurationDirectoryMode": "0755", "Conflicts": "shutdown.target", "ControlPID": "0", "DefaultDependencies": "yes", "Delegate": "no", "Description": "kubelet: The Kubernetes Node Agent", "DevicePolicy": "auto", "Documentation": "https://kubernetes.io/docs/home/", "DropInPaths": "/etc/systemd/system/kubelet.service.d/10-kubeadm.conf", "DynamicUser": "no", "Environment": "[unprintable] KUBELET_CONFIG_ARGS=--config=/var/lib/kubelet/config.yaml", "EnvironmentFile": "/etc/default/kubelet (ignore_errors=yes)", "ExecMainCode": "0", "ExecMainExitTimestampMonotonic": "0", "ExecMainPID": "0", "ExecMainStartTimestampMonotonic": "0", "ExecMainStatus": "0", "ExecStart": "{ path=/usr/bin/kubelet ; argv[]=/usr/bin/kubelet $KUBELET_KUBECONFIG_ARGS $KUBELET_CONFIG_ARGS $KUBELET_KUBEADM_ARGS $KUBELET_EXTRA_ARGS ; ignore_errors=no ; start_time=[n/a] ; stop_time=[n/a] ; pid=0 ; code=(null) ; status=0/0 }", "FailureAction": "none", "FileDescriptorStoreMax": "0", "FragmentPath": "/lib/systemd/system/kubelet.service", "GID": "[not set]", "GuessMainPID": "yes", "IOAccounting": "no", "IOSchedulingClass": "0", "IOSchedulingPriority": "0", "IOWeight": "[not set]", "IPAccounting": "no", "IPEgressBytes": "18446744073709551615", "IPEgressPackets": "18446744073709551615", "IPIngressBytes": "18446744073709551615", "IPIngressPackets": "18446744073709551615", "Id": "kubelet.service", "IgnoreOnIsolate": "no", "IgnoreSIGPIPE": "yes", "InactiveEnterTimestampMonotonic": "0", "InactiveExitTimestampMonotonic": "0", "JobRunningTimeoutUSec": "infinity", "JobTimeoutAction": "none", "JobTimeoutUSec": "infinity", "KeyringMode": "private", "KillMode": "control-group", "KillSignal": "15", "LimitAS": "infinity", "LimitASSoft": "infinity", "LimitCORE": "infinity", "LimitCORESoft": "0", "LimitCPU": "infinity", "LimitCPUSoft": "infinity", "LimitDATA": "infinity", "LimitDATASoft": "infinity", "LimitFSIZE": "infinity", "LimitFSIZESoft": "infinity", "LimitLOCKS": "infinity", "LimitLOCKSSoft": "infinity", "LimitMEMLOCK": "16777216", "LimitMEMLOCKSoft": "16777216", "LimitMSGQUEUE": "819200", "LimitMSGQUEUESoft": "819200", "LimitNICE": "0", "LimitNICESoft": "0", "LimitNOFILE": "4096", "LimitNOFILESoft": "1024", "LimitNPROC": "64057", "LimitNPROCSoft": "64057", "LimitRSS": "infinity", "LimitRSSSoft": "infinity", "LimitRTPRIO": "0", "LimitRTPRIOSoft": "0", "LimitRTTIME": "infinity", "LimitRTTIMESoft": "infinity", "LimitSIGPENDING": "64057", "LimitSIGPENDINGSoft": "64057", "LimitSTACK": "infinity", "LimitSTACKSoft": "8388608", "LoadState": "loaded", "LockPersonality": "no", "LogLevelMax": "-1", "LogsDirectoryMode": "0755", "MainPID": "0", "MemoryAccounting": "no", "MemoryCurrent": "[not set]", "MemoryDenyWriteExecute": "no", "MemoryHigh": "infinity", "MemoryLimit": "infinity", "MemoryLow": "0", "MemoryMax": "infinity", "MemorySwapMax": "infinity", "MountAPIVFS": "no", "MountFlags": "", "NFileDescriptorStore": "0", "NRestarts": "0", "Names": "kubelet.service", "NeedDaemonReload": "no", "Nice": "0", "NoNewPrivileges": "no", "NonBlocking": "no", "NotifyAccess": "none", "OOMScoreAdjust": "0", "OnFailureJobMode": "replace", "PermissionsStartOnly": "no", "Perpetual": "no", "PrivateDevices": "no", "PrivateNetwork": "no", "PrivateTmp": "no", "PrivateUsers": "no", "ProtectControlGroups": "no", "ProtectHome": "no", "ProtectKernelModules": "no", "ProtectKernelTunables": "no", "ProtectSystem": "no", "RefuseManualStart": "no", "RefuseManualStop": "no", "RemainAfterExit": "no", "RemoveIPC": "no", "Requires": "system.slice sysinit.target", "Restart": "always", "RestartUSec": "10s", "RestrictNamespaces": "no", "RestrictRealtime": "no", "RestrictSUIDSGID": "no", "Result": "success", "RootDirectoryStartOnly": "no", "RuntimeDirectoryMode": "0755", "RuntimeDirectoryPreserve": "no", "RuntimeMaxUSec": "infinity", "SameProcessGroup": "no", "SecureBits": "0", "SendSIGHUP": "no", "SendSIGKILL": "yes", "Slice": "system.slice", "StandardError": "inherit", "StandardInput": "null", "StandardInputData": "", "StandardOutput": "journal", "StartLimitAction": "none", "StartLimitBurst": "5", "StartLimitIntervalUSec": "0", "StartupBlockIOWeight": "[not set]", "StartupCPUShares": "[not set]", "StartupCPUWeight": "[not set]", "StartupIOWeight": "[not set]", "StateChangeTimestampMonotonic": "0", "StateDirectoryMode": "0755", "StatusErrno": "0", "StopWhenUnneeded": "no", "SubState": "dead", "SuccessAction": "none", "SyslogFacility": "3", "SyslogLevel": "6", "SyslogLevelPrefix": "yes", "SyslogPriority": "30", "SystemCallErrorNumber": "0", "TTYReset": "no", "TTYVHangup": "no", "TTYVTDisallocate": "no", "TasksAccounting": "yes", "TasksCurrent": "[not set]", "TasksMax": "4915", "TimeoutStartUSec": "1min 30s", "TimeoutStopUSec": "1min 30s", "TimerSlackNSec": "50000", "Transient": "no", "Type": "simple", "UID": "[not set]", "UMask": "0022", "UnitFilePreset": "enabled", "UnitFileState": "enabled", "UtmpMode": "init", "WantedBy": "multi-user.target", "Wants": "network-online.target", "WatchdogTimestampMonotonic": "0", "WatchdogUSec": "0"}}
ok: [md-kubernetes-master-3] => {"changed": false, "enabled": true, "name": "kubelet", "status": {"ActiveEnterTimestampMonotonic": "0", "ActiveExitTimestampMonotonic": "0", "ActiveState": "inactive", "After": "basic.target network-online.target system.slice systemd-journald.socket sysinit.target", "AllowIsolate": "no", "AmbientCapabilities": "", "AssertResult": "no", "AssertTimestampMonotonic": "0", "Before": "multi-user.target shutdown.target", "BlockIOAccounting": "no", "BlockIOWeight": "[not set]", "CPUAccounting": "no", "CPUQuotaPerSecUSec": "infinity", "CPUSchedulingPolicy": "0", "CPUSchedulingPriority": "0", "CPUSchedulingResetOnFork": "no", "CPUShares": "[not set]", "CPUUsageNSec": "[not set]", "CPUWeight": "[not set]", "CacheDirectoryMode": "0755", "CanIsolate": "no", "CanReload": "no", "CanStart": "yes", "CanStop": "yes", "CapabilityBoundingSet": "cap_chown cap_dac_override cap_dac_read_search cap_fowner cap_fsetid cap_kill cap_setgid cap_setuid cap_setpcap cap_linux_immutable cap_net_bind_service cap_net_broadcast cap_net_admin cap_net_raw cap_ipc_lock cap_ipc_owner cap_sys_module cap_sys_rawio cap_sys_chroot cap_sys_ptrace cap_sys_pacct cap_sys_admin cap_sys_boot cap_sys_nice cap_sys_resource cap_sys_time cap_sys_tty_config cap_mknod cap_lease cap_audit_write cap_audit_control cap_setfcap cap_mac_override cap_mac_admin cap_syslog cap_wake_alarm cap_block_suspend", "CollectMode": "inactive", "ConditionResult": "no", "ConditionTimestampMonotonic": "0", "ConfigurationDirectoryMode": "0755", "Conflicts": "shutdown.target", "ControlPID": "0", "DefaultDependencies": "yes", "Delegate": "no", "Description": "kubelet: The Kubernetes Node Agent", "DevicePolicy": "auto", "Documentation": "https://kubernetes.io/docs/home/", "DropInPaths": "/etc/systemd/system/kubelet.service.d/10-kubeadm.conf", "DynamicUser": "no", "Environment": "[unprintable] KUBELET_CONFIG_ARGS=--config=/var/lib/kubelet/config.yaml", "EnvironmentFile": "/etc/default/kubelet (ignore_errors=yes)", "ExecMainCode": "0", "ExecMainExitTimestampMonotonic": "0", "ExecMainPID": "0", "ExecMainStartTimestampMonotonic": "0", "ExecMainStatus": "0", "ExecStart": "{ path=/usr/bin/kubelet ; argv[]=/usr/bin/kubelet $KUBELET_KUBECONFIG_ARGS $KUBELET_CONFIG_ARGS $KUBELET_KUBEADM_ARGS $KUBELET_EXTRA_ARGS ; ignore_errors=no ; start_time=[n/a] ; stop_time=[n/a] ; pid=0 ; code=(null) ; status=0/0 }", "FailureAction": "none", "FileDescriptorStoreMax": "0", "FragmentPath": "/lib/systemd/system/kubelet.service", "GID": "[not set]", "GuessMainPID": "yes", "IOAccounting": "no", "IOSchedulingClass": "0", "IOSchedulingPriority": "0", "IOWeight": "[not set]", "IPAccounting": "no", "IPEgressBytes": "18446744073709551615", "IPEgressPackets": "18446744073709551615", "IPIngressBytes": "18446744073709551615", "IPIngressPackets": "18446744073709551615", "Id": "kubelet.service", "IgnoreOnIsolate": "no", "IgnoreSIGPIPE": "yes", "InactiveEnterTimestampMonotonic": "0", "InactiveExitTimestampMonotonic": "0", "JobRunningTimeoutUSec": "infinity", "JobTimeoutAction": "none", "JobTimeoutUSec": "infinity", "KeyringMode": "private", "KillMode": "control-group", "KillSignal": "15", "LimitAS": "infinity", "LimitASSoft": "infinity", "LimitCORE": "infinity", "LimitCORESoft": "0", "LimitCPU": "infinity", "LimitCPUSoft": "infinity", "LimitDATA": "infinity", "LimitDATASoft": "infinity", "LimitFSIZE": "infinity", "LimitFSIZESoft": "infinity", "LimitLOCKS": "infinity", "LimitLOCKSSoft": "infinity", "LimitMEMLOCK": "16777216", "LimitMEMLOCKSoft": "16777216", "LimitMSGQUEUE": "819200", "LimitMSGQUEUESoft": "819200", "LimitNICE": "0", "LimitNICESoft": "0", "LimitNOFILE": "4096", "LimitNOFILESoft": "1024", "LimitNPROC": "64057", "LimitNPROCSoft": "64057", "LimitRSS": "infinity", "LimitRSSSoft": "infinity", "LimitRTPRIO": "0", "LimitRTPRIOSoft": "0", "LimitRTTIME": "infinity", "LimitRTTIMESoft": "infinity", "LimitSIGPENDING": "64057", "LimitSIGPENDINGSoft": "64057", "LimitSTACK": "infinity", "LimitSTACKSoft": "8388608", "LoadState": "loaded", "LockPersonality": "no", "LogLevelMax": "-1", "LogsDirectoryMode": "0755", "MainPID": "0", "MemoryAccounting": "no", "MemoryCurrent": "[not set]", "MemoryDenyWriteExecute": "no", "MemoryHigh": "infinity", "MemoryLimit": "infinity", "MemoryLow": "0", "MemoryMax": "infinity", "MemorySwapMax": "infinity", "MountAPIVFS": "no", "MountFlags": "", "NFileDescriptorStore": "0", "NRestarts": "0", "Names": "kubelet.service", "NeedDaemonReload": "no", "Nice": "0", "NoNewPrivileges": "no", "NonBlocking": "no", "NotifyAccess": "none", "OOMScoreAdjust": "0", "OnFailureJobMode": "replace", "PermissionsStartOnly": "no", "Perpetual": "no", "PrivateDevices": "no", "PrivateNetwork": "no", "PrivateTmp": "no", "PrivateUsers": "no", "ProtectControlGroups": "no", "ProtectHome": "no", "ProtectKernelModules": "no", "ProtectKernelTunables": "no", "ProtectSystem": "no", "RefuseManualStart": "no", "RefuseManualStop": "no", "RemainAfterExit": "no", "RemoveIPC": "no", "Requires": "sysinit.target system.slice", "Restart": "always", "RestartUSec": "10s", "RestrictNamespaces": "no", "RestrictRealtime": "no", "RestrictSUIDSGID": "no", "Result": "success", "RootDirectoryStartOnly": "no", "RuntimeDirectoryMode": "0755", "RuntimeDirectoryPreserve": "no", "RuntimeMaxUSec": "infinity", "SameProcessGroup": "no", "SecureBits": "0", "SendSIGHUP": "no", "SendSIGKILL": "yes", "Slice": "system.slice", "StandardError": "inherit", "StandardInput": "null", "StandardInputData": "", "StandardOutput": "journal", "StartLimitAction": "none", "StartLimitBurst": "5", "StartLimitIntervalUSec": "0", "StartupBlockIOWeight": "[not set]", "StartupCPUShares": "[not set]", "StartupCPUWeight": "[not set]", "StartupIOWeight": "[not set]", "StateChangeTimestampMonotonic": "0", "StateDirectoryMode": "0755", "StatusErrno": "0", "StopWhenUnneeded": "no", "SubState": "dead", "SuccessAction": "none", "SyslogFacility": "3", "SyslogLevel": "6", "SyslogLevelPrefix": "yes", "SyslogPriority": "30", "SystemCallErrorNumber": "0", "TTYReset": "no", "TTYVHangup": "no", "TTYVTDisallocate": "no", "TasksAccounting": "yes", "TasksCurrent": "[not set]", "TasksMax": "4915", "TimeoutStartUSec": "1min 30s", "TimeoutStopUSec": "1min 30s", "TimerSlackNSec": "50000", "Transient": "no", "Type": "simple", "UID": "[not set]", "UMask": "0022", "UnitFilePreset": "enabled", "UnitFileState": "enabled", "UtmpMode": "init", "WantedBy": "multi-user.target", "Wants": "network-online.target", "WatchdogTimestampMonotonic": "0", "WatchdogUSec": "0"}}
ok: [md-kubernetes-master-1] => {"changed": false, "enabled": true, "name": "kubelet", "status": {"ActiveEnterTimestamp": "Fri 2020-06-26 12:24:37 UTC", "ActiveEnterTimestampMonotonic": "220443494", "ActiveExitTimestamp": "Fri 2020-06-26 12:24:37 UTC", "ActiveExitTimestampMonotonic": "220380694", "ActiveState": "active", "After": "basic.target sysinit.target network-online.target system.slice systemd-journald.socket", "AllowIsolate": "no", "AmbientCapabilities": "", "AssertResult": "yes", "AssertTimestamp": "Fri 2020-06-26 12:24:37 UTC", "AssertTimestampMonotonic": "220441909", "Before": "shutdown.target multi-user.target", "BlockIOAccounting": "no", "BlockIOWeight": "[not set]", "CPUAccounting": "no", "CPUQuotaPerSecUSec": "infinity", "CPUSchedulingPolicy": "0", "CPUSchedulingPriority": "0", "CPUSchedulingResetOnFork": "no", "CPUShares": "[not set]", "CPUUsageNSec": "[not set]", "CPUWeight": "[not set]", "CacheDirectoryMode": "0755", "CanIsolate": "no", "CanReload": "no", "CanStart": "yes", "CanStop": "yes", "CapabilityBoundingSet": "cap_chown cap_dac_override cap_dac_read_search cap_fowner cap_fsetid cap_kill cap_setgid cap_setuid cap_setpcap cap_linux_immutable cap_net_bind_service cap_net_broadcast cap_net_admin cap_net_raw cap_ipc_lock cap_ipc_owner cap_sys_module cap_sys_rawio cap_sys_chroot cap_sys_ptrace cap_sys_pacct cap_sys_admin cap_sys_boot cap_sys_nice cap_sys_resource cap_sys_time cap_sys_tty_config cap_mknod cap_lease cap_audit_write cap_audit_control cap_setfcap cap_mac_override cap_mac_admin cap_syslog cap_wake_alarm cap_block_suspend", "CollectMode": "inactive", "ConditionResult": "yes", "ConditionTimestamp": "Fri 2020-06-26 12:24:37 UTC", "ConditionTimestampMonotonic": "220441908", "ConfigurationDirectoryMode": "0755", "Conflicts": "shutdown.target", "ControlGroup": "/system.slice/kubelet.service", "ControlPID": "0", "DefaultDependencies": "yes", "Delegate": "no", "Description": "kubelet: The Kubernetes Node Agent", "DevicePolicy": "auto", "Documentation": "https://kubernetes.io/docs/home/", "DropInPaths": "/etc/systemd/system/kubelet.service.d/10-kubeadm.conf", "DynamicUser": "no", "Environment": "[unprintable] KUBELET_CONFIG_ARGS=--config=/var/lib/kubelet/config.yaml", "EnvironmentFile": "/etc/default/kubelet (ignore_errors=yes)", "ExecMainCode": "0", "ExecMainExitTimestampMonotonic": "0", "ExecMainPID": "4776", "ExecMainStartTimestamp": "Fri 2020-06-26 12:24:37 UTC", "ExecMainStartTimestampMonotonic": "220443437", "ExecMainStatus": "0", "ExecStart": "{ path=/usr/bin/kubelet ; argv[]=/usr/bin/kubelet $KUBELET_KUBECONFIG_ARGS $KUBELET_CONFIG_ARGS $KUBELET_KUBEADM_ARGS $KUBELET_EXTRA_ARGS ; ignore_errors=no ; start_time=[Fri 2020-06-26 12:24:37 UTC] ; stop_time=[n/a] ; pid=4776 ; code=(null) ; status=0/0 }", "FailureAction": "none", "FileDescriptorStoreMax": "0", "FragmentPath": "/lib/systemd/system/kubelet.service", "GID": "[not set]", "GuessMainPID": "yes", "IOAccounting": "no", "IOSchedulingClass": "0", "IOSchedulingPriority": "0", "IOWeight": "[not set]", "IPAccounting": "no", "IPEgressBytes": "18446744073709551615", "IPEgressPackets": "18446744073709551615", "IPIngressBytes": "18446744073709551615", "IPIngressPackets": "18446744073709551615", "Id": "kubelet.service", "IgnoreOnIsolate": "no", "IgnoreSIGPIPE": "yes", "InactiveEnterTimestamp": "Fri 2020-06-26 12:24:37 UTC", "InactiveEnterTimestampMonotonic": "220440700", "InactiveExitTimestamp": "Fri 2020-06-26 12:24:37 UTC", "InactiveExitTimestampMonotonic": "220443494", "InvocationID": "22bb23f117934b4cae5080e2fb1fe97f", "JobRunningTimeoutUSec": "infinity", "JobTimeoutAction": "none", "JobTimeoutUSec": "infinity", "KeyringMode": "private", "KillMode": "control-group", "KillSignal": "15", "LimitAS": "infinity", "LimitASSoft": "infinity", "LimitCORE": "infinity", "LimitCORESoft": "0", "LimitCPU": "infinity", "LimitCPUSoft": "infinity", "LimitDATA": "infinity", "LimitDATASoft": "infinity", "LimitFSIZE": "infinity", "LimitFSIZESoft": "infinity", "LimitLOCKS": "infinity", "LimitLOCKSSoft": "infinity", "LimitMEMLOCK": "16777216", "LimitMEMLOCKSoft": "16777216", "LimitMSGQUEUE": "819200", "LimitMSGQUEUESoft": "819200", "LimitNICE": "0", "LimitNICESoft": "0", "LimitNOFILE": "4096", "LimitNOFILESoft": "1024", "LimitNPROC": "15676", "LimitNPROCSoft": "15676", "LimitRSS": "infinity", "LimitRSSSoft": "infinity", "LimitRTPRIO": "0", "LimitRTPRIOSoft": "0", "LimitRTTIME": "infinity", "LimitRTTIMESoft": "infinity", "LimitSIGPENDING": "15676", "LimitSIGPENDINGSoft": "15676", "LimitSTACK": "infinity", "LimitSTACKSoft": "8388608", "LoadState": "loaded", "LockPersonality": "no", "LogLevelMax": "-1", "LogsDirectoryMode": "0755", "MainPID": "4776", "MemoryAccounting": "no", "MemoryCurrent": "[not set]", "MemoryDenyWriteExecute": "no", "MemoryHigh": "infinity", "MemoryLimit": "infinity", "MemoryLow": "0", "MemoryMax": "infinity", "MemorySwapMax": "infinity", "MountAPIVFS": "no", "MountFlags": "", "NFileDescriptorStore": "0", "NRestarts": "0", "Names": "kubelet.service", "NeedDaemonReload": "no", "Nice": "0", "NoNewPrivileges": "no", "NonBlocking": "no", "NotifyAccess": "none", "OOMScoreAdjust": "0", "OnFailureJobMode": "replace", "PermissionsStartOnly": "no", "Perpetual": "no", "PrivateDevices": "no", "PrivateNetwork": "no", "PrivateTmp": "no", "PrivateUsers": "no", "ProtectControlGroups": "no", "ProtectHome": "no", "ProtectKernelModules": "no", "ProtectKernelTunables": "no", "ProtectSystem": "no", "RefuseManualStart": "no", "RefuseManualStop": "no", "RemainAfterExit": "no", "RemoveIPC": "no", "Requires": "system.slice sysinit.target", "Restart": "always", "RestartUSec": "10s", "RestrictNamespaces": "no", "RestrictRealtime": "no", "RestrictSUIDSGID": "no", "Result": "success", "RootDirectoryStartOnly": "no", "RuntimeDirectoryMode": "0755", "RuntimeDirectoryPreserve": "no", "RuntimeMaxUSec": "infinity", "SameProcessGroup": "no", "SecureBits": "0", "SendSIGHUP": "no", "SendSIGKILL": "yes", "Slice": "system.slice", "StandardError": "inherit", "StandardInput": "null", "StandardInputData": "", "StandardOutput": "journal", "StartLimitAction": "none", "StartLimitBurst": "5", "StartLimitIntervalUSec": "0", "StartupBlockIOWeight": "[not set]", "StartupCPUShares": "[not set]", "StartupCPUWeight": "[not set]", "StartupIOWeight": "[not set]", "StateChangeTimestamp": "Fri 2020-06-26 12:24:37 UTC", "StateChangeTimestampMonotonic": "220443494", "StateDirectoryMode": "0755", "StatusErrno": "0", "StopWhenUnneeded": "no", "SubState": "running", "SuccessAction": "none", "SyslogFacility": "3", "SyslogLevel": "6", "SyslogLevelPrefix": "yes", "SyslogPriority": "30", "SystemCallErrorNumber": "0", "TTYReset": "no", "TTYVHangup": "no", "TTYVTDisallocate": "no", "TasksAccounting": "yes", "TasksCurrent": "16", "TasksMax": "4702", "TimeoutStartUSec": "1min 30s", "TimeoutStopUSec": "1min 30s", "TimerSlackNSec": "50000", "Transient": "no", "Type": "simple", "UID": "[not set]", "UMask": "0022", "UnitFilePreset": "enabled", "UnitFileState": "enabled", "UtmpMode": "init", "WantedBy": "multi-user.target", "Wants": "network-online.target", "WatchdogTimestamp": "Fri 2020-06-26 12:24:37 UTC", "WatchdogTimestampMonotonic": "220443493", "WatchdogUSec": "0"}}
ok: [md-kubernetes-master-2] => {"changed": false, "enabled": true, "name": "kubelet", "status": {"ActiveEnterTimestampMonotonic": "0", "ActiveExitTimestampMonotonic": "0", "ActiveState": "inactive", "After": "system.slice network-online.target sysinit.target systemd-journald.socket basic.target", "AllowIsolate": "no", "AmbientCapabilities": "", "AssertResult": "no", "AssertTimestampMonotonic": "0", "Before": "multi-user.target shutdown.target", "BlockIOAccounting": "no", "BlockIOWeight": "[not set]", "CPUAccounting": "no", "CPUQuotaPerSecUSec": "infinity", "CPUSchedulingPolicy": "0", "CPUSchedulingPriority": "0", "CPUSchedulingResetOnFork": "no", "CPUShares": "[not set]", "CPUUsageNSec": "[not set]", "CPUWeight": "[not set]", "CacheDirectoryMode": "0755", "CanIsolate": "no", "CanReload": "no", "CanStart": "yes", "CanStop": "yes", "CapabilityBoundingSet": "cap_chown cap_dac_override cap_dac_read_search cap_fowner cap_fsetid cap_kill cap_setgid cap_setuid cap_setpcap cap_linux_immutable cap_net_bind_service cap_net_broadcast cap_net_admin cap_net_raw cap_ipc_lock cap_ipc_owner cap_sys_module cap_sys_rawio cap_sys_chroot cap_sys_ptrace cap_sys_pacct cap_sys_admin cap_sys_boot cap_sys_nice cap_sys_resource cap_sys_time cap_sys_tty_config cap_mknod cap_lease cap_audit_write cap_audit_control cap_setfcap cap_mac_override cap_mac_admin cap_syslog cap_wake_alarm cap_block_suspend", "CollectMode": "inactive", "ConditionResult": "no", "ConditionTimestampMonotonic": "0", "ConfigurationDirectoryMode": "0755", "Conflicts": "shutdown.target", "ControlPID": "0", "DefaultDependencies": "yes", "Delegate": "no", "Description": "kubelet: The Kubernetes Node Agent", "DevicePolicy": "auto", "Documentation": "https://kubernetes.io/docs/home/", "DropInPaths": "/etc/systemd/system/kubelet.service.d/10-kubeadm.conf", "DynamicUser": "no", "Environment": "[unprintable] KUBELET_CONFIG_ARGS=--config=/var/lib/kubelet/config.yaml", "EnvironmentFile": "/etc/default/kubelet (ignore_errors=yes)", "ExecMainCode": "0", "ExecMainExitTimestampMonotonic": "0", "ExecMainPID": "0", "ExecMainStartTimestampMonotonic": "0", "ExecMainStatus": "0", "ExecStart": "{ path=/usr/bin/kubelet ; argv[]=/usr/bin/kubelet $KUBELET_KUBECONFIG_ARGS $KUBELET_CONFIG_ARGS $KUBELET_KUBEADM_ARGS $KUBELET_EXTRA_ARGS ; ignore_errors=no ; start_time=[n/a] ; stop_time=[n/a] ; pid=0 ; code=(null) ; status=0/0 }", "FailureAction": "none", "FileDescriptorStoreMax": "0", "FragmentPath": "/lib/systemd/system/kubelet.service", "GID": "[not set]", "GuessMainPID": "yes", "IOAccounting": "no", "IOSchedulingClass": "0", "IOSchedulingPriority": "0", "IOWeight": "[not set]", "IPAccounting": "no", "IPEgressBytes": "18446744073709551615", "IPEgressPackets": "18446744073709551615", "IPIngressBytes": "18446744073709551615", "IPIngressPackets": "18446744073709551615", "Id": "kubelet.service", "IgnoreOnIsolate": "no", "IgnoreSIGPIPE": "yes", "InactiveEnterTimestampMonotonic": "0", "InactiveExitTimestampMonotonic": "0", "JobRunningTimeoutUSec": "infinity", "JobTimeoutAction": "none", "JobTimeoutUSec": "infinity", "KeyringMode": "private", "KillMode": "control-group", "KillSignal": "15", "LimitAS": "infinity", "LimitASSoft": "infinity", "LimitCORE": "infinity", "LimitCORESoft": "0", "LimitCPU": "infinity", "LimitCPUSoft": "infinity", "LimitDATA": "infinity", "LimitDATASoft": "infinity", "LimitFSIZE": "infinity", "LimitFSIZESoft": "infinity", "LimitLOCKS": "infinity", "LimitLOCKSSoft": "infinity", "LimitMEMLOCK": "16777216", "LimitMEMLOCKSoft": "16777216", "LimitMSGQUEUE": "819200", "LimitMSGQUEUESoft": "819200", "LimitNICE": "0", "LimitNICESoft": "0", "LimitNOFILE": "4096", "LimitNOFILESoft": "1024", "LimitNPROC": "64057", "LimitNPROCSoft": "64057", "LimitRSS": "infinity", "LimitRSSSoft": "infinity", "LimitRTPRIO": "0", "LimitRTPRIOSoft": "0", "LimitRTTIME": "infinity", "LimitRTTIMESoft": "infinity", "LimitSIGPENDING": "64057", "LimitSIGPENDINGSoft": "64057", "LimitSTACK": "infinity", "LimitSTACKSoft": "8388608", "LoadState": "loaded", "LockPersonality": "no", "LogLevelMax": "-1", "LogsDirectoryMode": "0755", "MainPID": "0", "MemoryAccounting": "no", "MemoryCurrent": "[not set]", "MemoryDenyWriteExecute": "no", "MemoryHigh": "infinity", "MemoryLimit": "infinity", "MemoryLow": "0", "MemoryMax": "infinity", "MemorySwapMax": "infinity", "MountAPIVFS": "no", "MountFlags": "", "NFileDescriptorStore": "0", "NRestarts": "0", "Names": "kubelet.service", "NeedDaemonReload": "no", "Nice": "0", "NoNewPrivileges": "no", "NonBlocking": "no", "NotifyAccess": "none", "OOMScoreAdjust": "0", "OnFailureJobMode": "replace", "PermissionsStartOnly": "no", "Perpetual": "no", "PrivateDevices": "no", "PrivateNetwork": "no", "PrivateTmp": "no", "PrivateUsers": "no", "ProtectControlGroups": "no", "ProtectHome": "no", "ProtectKernelModules": "no", "ProtectKernelTunables": "no", "ProtectSystem": "no", "RefuseManualStart": "no", "RefuseManualStop": "no", "RemainAfterExit": "no", "RemoveIPC": "no", "Requires": "system.slice sysinit.target", "Restart": "always", "RestartUSec": "10s", "RestrictNamespaces": "no", "RestrictRealtime": "no", "RestrictSUIDSGID": "no", "Result": "success", "RootDirectoryStartOnly": "no", "RuntimeDirectoryMode": "0755", "RuntimeDirectoryPreserve": "no", "RuntimeMaxUSec": "infinity", "SameProcessGroup": "no", "SecureBits": "0", "SendSIGHUP": "no", "SendSIGKILL": "yes", "Slice": "system.slice", "StandardError": "inherit", "StandardInput": "null", "StandardInputData": "", "StandardOutput": "journal", "StartLimitAction": "none", "StartLimitBurst": "5", "StartLimitIntervalUSec": "0", "StartupBlockIOWeight": "[not set]", "StartupCPUShares": "[not set]", "StartupCPUWeight": "[not set]", "StartupIOWeight": "[not set]", "StateChangeTimestampMonotonic": "0", "StateDirectoryMode": "0755", "StatusErrno": "0", "StopWhenUnneeded": "no", "SubState": "dead", "SuccessAction": "none", "SyslogFacility": "3", "SyslogLevel": "6", "SyslogLevelPrefix": "yes", "SyslogPriority": "30", "SystemCallErrorNumber": "0", "TTYReset": "no", "TTYVHangup": "no", "TTYVTDisallocate": "no", "TasksAccounting": "yes", "TasksCurrent": "[not set]", "TasksMax": "4915", "TimeoutStartUSec": "1min 30s", "TimeoutStopUSec": "1min 30s", "TimerSlackNSec": "50000", "Transient": "no", "Type": "simple", "UID": "[not set]", "UMask": "0022", "UnitFilePreset": "enabled", "UnitFileState": "enabled", "UtmpMode": "init", "WantedBy": "multi-user.target", "Wants": "network-online.target", "WatchdogTimestampMonotonic": "0", "WatchdogUSec": "0"}}

TASK [prepare-nodes : Create setup directory] *************************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/prepare-nodes/tasks/main.yaml:18
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-minion-4] => {"changed": false, "skip_reason": "Conditional result was False"}
ok: [md-kubernetes-master-1] => {"changed": false, "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/root/setup", "size": 4096, "state": "directory", "uid": 0}
META: ran handlers
META: ran handlers

PLAY [Kube-VIP] *******************************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/cluster-setup.yaml:15
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-master-2]
META: ran handlers

TASK [Create configuration directory /etc/kube-vip] *******************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/kube-vip/tasks/main.yaml:6
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [kube-vip : Create manifests directory for static pods /etc/kubernetes/manifests] ********************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/kube-vip/tasks/main.yaml:9
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [kube-vip : Create service configuration file] *******************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/kube-vip/tasks/main.yaml:12
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [kube-vip : Create manifest for static pod] **********************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/kube-vip/tasks/main.yaml:15
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
META: ran handlers
META: ran handlers

PLAY [Keepalived] *****************************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/cluster-setup.yaml:25
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-1]
META: ran handlers

TASK [keepalived : Create configuration directory] ********************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/keepalived/tasks/main.yaml:5
ok: [md-kubernetes-master-1] => {"changed": false, "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/etc/keepalived", "size": 4096, "state": "directory", "uid": 0}
ok: [md-kubernetes-master-2] => {"changed": false, "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/etc/keepalived", "size": 4096, "state": "directory", "uid": 0}
ok: [md-kubernetes-master-3] => {"changed": false, "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/etc/keepalived", "size": 4096, "state": "directory", "uid": 0}

TASK [keepalived : Copy check script] *********************************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/keepalived/tasks/main.yaml:8
ok: [md-kubernetes-master-3] => {"changed": false, "checksum": "bc514558b5fa4df244ee06c950393d0d3c29ee30", "dest": "/etc/keepalived/check_apiserver.sh", "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/etc/keepalived/check_apiserver.sh", "size": 526, "state": "file", "uid": 0}
ok: [md-kubernetes-master-2] => {"changed": false, "checksum": "bc514558b5fa4df244ee06c950393d0d3c29ee30", "dest": "/etc/keepalived/check_apiserver.sh", "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/etc/keepalived/check_apiserver.sh", "size": 526, "state": "file", "uid": 0}
ok: [md-kubernetes-master-1] => {"changed": false, "checksum": "bc514558b5fa4df244ee06c950393d0d3c29ee30", "dest": "/etc/keepalived/check_apiserver.sh", "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/etc/keepalived/check_apiserver.sh", "size": 526, "state": "file", "uid": 0}

TASK [keepalived : Generate configuraton file] ************************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/keepalived/tasks/main.yaml:11
ok: [md-kubernetes-master-2] => {"changed": false, "checksum": "38471f047c239231caacfb65097f91855c84b0e1", "dest": "/etc/keepalived/keepalived.conf", "gid": 0, "group": "root", "mode": "0644", "owner": "root", "path": "/etc/keepalived/keepalived.conf", "size": 500, "state": "file", "uid": 0}
ok: [md-kubernetes-master-3] => {"changed": false, "checksum": "38471f047c239231caacfb65097f91855c84b0e1", "dest": "/etc/keepalived/keepalived.conf", "gid": 0, "group": "root", "mode": "0644", "owner": "root", "path": "/etc/keepalived/keepalived.conf", "size": 500, "state": "file", "uid": 0}
ok: [md-kubernetes-master-1] => {"changed": false, "checksum": "1cd29755fa84bd2a05e423009807da536b1b01ed", "dest": "/etc/keepalived/keepalived.conf", "gid": 0, "group": "root", "mode": "0644", "owner": "root", "path": "/etc/keepalived/keepalived.conf", "size": 500, "state": "file", "uid": 0}

TASK [keepalived : Copying override script to primary master in order to have a VIP before at least one APIServer is up] **********************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/keepalived/tasks/main.yaml:14
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}
ok: [md-kubernetes-master-1] => {"changed": false, "checksum": "cdba55b02314b489d2a99382ae511860f6971df2", "dest": "/etc/keepalived/check_override.sh", "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/etc/keepalived/check_override.sh", "size": 18, "state": "file", "uid": 0}

TASK [keepalived : Generate static pod configuraton file directory] ***************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/keepalived/tasks/main.yaml:18
ok: [md-kubernetes-master-1] => {"changed": false, "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/etc/kubernetes/manifests", "size": 4096, "state": "directory", "uid": 0}
ok: [md-kubernetes-master-2] => {"changed": false, "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/etc/kubernetes/manifests", "size": 4096, "state": "directory", "uid": 0}
ok: [md-kubernetes-master-3] => {"changed": false, "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/etc/kubernetes/manifests", "size": 4096, "state": "directory", "uid": 0}

TASK [keepalived : Generate static pod configuraton file] *************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/keepalived/tasks/main.yaml:21
ok: [md-kubernetes-master-1] => {"changed": false, "checksum": "b3a593c4c97fa8422895fe2cf1d26f0dfd7ee235", "dest": "/etc/kubernetes/manifests/keepalived.yaml", "gid": 0, "group": "root", "mode": "0644", "owner": "root", "path": "/etc/kubernetes/manifests/keepalived.yaml", "size": 679, "state": "file", "uid": 0}
ok: [md-kubernetes-master-2] => {"changed": false, "checksum": "b3a593c4c97fa8422895fe2cf1d26f0dfd7ee235", "dest": "/etc/kubernetes/manifests/keepalived.yaml", "gid": 0, "group": "root", "mode": "0644", "owner": "root", "path": "/etc/kubernetes/manifests/keepalived.yaml", "size": 679, "state": "file", "uid": 0}
ok: [md-kubernetes-master-3] => {"changed": false, "checksum": "b3a593c4c97fa8422895fe2cf1d26f0dfd7ee235", "dest": "/etc/kubernetes/manifests/keepalived.yaml", "gid": 0, "group": "root", "mode": "0644", "owner": "root", "path": "/etc/kubernetes/manifests/keepalived.yaml", "size": 679, "state": "file", "uid": 0}
META: ran handlers
META: ran handlers

PLAY [NGINX] **********************************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/cluster-setup.yaml:35
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-2]
META: ran handlers

TASK [nginx : Create configuration directory] *************************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/nginx/tasks/main.yaml:5
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [nginx : Generate service configuraton file] *********************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/nginx/tasks/main.yaml:8
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [nginx : Generate static pod configuraton file directory] ********************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/nginx/tasks/main.yaml:11
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [nginx : Generate static pod configuraton file] ******************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/nginx/tasks/main.yaml:14
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}
META: ran handlers
META: ran handlers

PLAY [HAProxy] ********************************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/cluster-setup.yaml:45
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-2]
META: ran handlers

TASK [haproxy : Create configuration directory] ***********************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/haproxy/tasks/main.yaml:5
ok: [md-kubernetes-master-3] => {"changed": false, "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/etc/haproxy", "size": 4096, "state": "directory", "uid": 0}
ok: [md-kubernetes-master-1] => {"changed": false, "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/etc/haproxy", "size": 4096, "state": "directory", "uid": 0}
ok: [md-kubernetes-master-2] => {"changed": false, "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/etc/haproxy", "size": 4096, "state": "directory", "uid": 0}

TASK [haproxy : Generate service configuraton file] *******************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/haproxy/tasks/main.yaml:8
ok: [md-kubernetes-master-3] => {"changed": false, "checksum": "64cc2f2565031e5c4340c427b2086be39a380f8a", "dest": "/etc/haproxy/haproxy.cfg", "gid": 0, "group": "root", "mode": "0644", "owner": "root", "path": "/etc/haproxy/haproxy.cfg", "size": 1813, "state": "file", "uid": 0}
ok: [md-kubernetes-master-1] => {"changed": false, "checksum": "64cc2f2565031e5c4340c427b2086be39a380f8a", "dest": "/etc/haproxy/haproxy.cfg", "gid": 0, "group": "root", "mode": "0644", "owner": "root", "path": "/etc/haproxy/haproxy.cfg", "size": 1813, "state": "file", "uid": 0}
ok: [md-kubernetes-master-2] => {"changed": false, "checksum": "64cc2f2565031e5c4340c427b2086be39a380f8a", "dest": "/etc/haproxy/haproxy.cfg", "gid": 0, "group": "root", "mode": "0644", "owner": "root", "path": "/etc/haproxy/haproxy.cfg", "size": 1813, "state": "file", "uid": 0}

TASK [haproxy : Generate static pod configuraton file directory] ******************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/haproxy/tasks/main.yaml:11
ok: [md-kubernetes-master-1] => {"changed": false, "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/etc/kubernetes/manifests", "size": 4096, "state": "directory", "uid": 0}
ok: [md-kubernetes-master-2] => {"changed": false, "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/etc/kubernetes/manifests", "size": 4096, "state": "directory", "uid": 0}
ok: [md-kubernetes-master-3] => {"changed": false, "gid": 0, "group": "root", "mode": "0755", "owner": "root", "path": "/etc/kubernetes/manifests", "size": 4096, "state": "directory", "uid": 0}

TASK [haproxy : Generate static pod configuraton file] ****************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/haproxy/tasks/main.yaml:14
ok: [md-kubernetes-master-3] => {"changed": false, "checksum": "801099c35b5b1f3c177e5cffd3af2c05327efce6", "dest": "/etc/kubernetes/manifests/haproxy.yaml", "gid": 0, "group": "root", "mode": "0644", "owner": "root", "path": "/etc/kubernetes/manifests/haproxy.yaml", "size": 549, "state": "file", "uid": 0}
ok: [md-kubernetes-master-1] => {"changed": false, "checksum": "801099c35b5b1f3c177e5cffd3af2c05327efce6", "dest": "/etc/kubernetes/manifests/haproxy.yaml", "gid": 0, "group": "root", "mode": "0644", "owner": "root", "path": "/etc/kubernetes/manifests/haproxy.yaml", "size": 549, "state": "file", "uid": 0}
ok: [md-kubernetes-master-2] => {"changed": false, "checksum": "801099c35b5b1f3c177e5cffd3af2c05327efce6", "dest": "/etc/kubernetes/manifests/haproxy.yaml", "gid": 0, "group": "root", "mode": "0644", "owner": "root", "path": "/etc/kubernetes/manifests/haproxy.yaml", "size": 549, "state": "file", "uid": 0}
META: ran handlers
META: ran handlers

PLAY [Deploy external etcd] *******************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/cluster-setup.yaml:55
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-3]
META: ran handlers

TASK [external-etcd : Install preliminary kubelet configuration for systemd] ******************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:5
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Activate and restart kubelet] *******************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:8
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Clean up /etc/kubernetes/manifests/etcd.yaml from previous installations] ***********************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:11
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Clean up /var/lib/etcd/member from previous installations] **************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:14
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Clean up /etc/kubernetes/pki from previous installations] ***************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:17
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Clean up /tmp/etcd from previous installations on primary etcd node] ****************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:20
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Create temporary cert directories on primary etcd node] *****************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:24
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-1)  => {"ansible_loop_var": "item", "changed": false, "item": "md-kubernetes-master-1", "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-2)  => {"ansible_loop_var": "item", "changed": false, "item": "md-kubernetes-master-2", "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-1)  => {"ansible_loop_var": "item", "changed": false, "item": "md-kubernetes-master-1", "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-3)  => {"ansible_loop_var": "item", "changed": false, "item": "md-kubernetes-master-3", "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-2)  => {"ansible_loop_var": "item", "changed": false, "item": "md-kubernetes-master-2", "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-3)  => {"ansible_loop_var": "item", "changed": false, "item": "md-kubernetes-master-3", "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-1)  => {"ansible_loop_var": "item", "changed": false, "item": "md-kubernetes-master-1", "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-2)  => {"ansible_loop_var": "item", "changed": false, "item": "md-kubernetes-master-2", "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-3)  => {"ansible_loop_var": "item", "changed": false, "item": "md-kubernetes-master-3", "skip_reason": "Conditional result was False"}

TASK [external-etcd : Generate kubeadmcfg.yaml on primary etcd node] **************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:29
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-1)  => {"ansible_loop_var": "etcdnode", "changed": false, "etcdnode": "md-kubernetes-master-1", "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-2)  => {"ansible_loop_var": "etcdnode", "changed": false, "etcdnode": "md-kubernetes-master-2", "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-3)  => {"ansible_loop_var": "etcdnode", "changed": false, "etcdnode": "md-kubernetes-master-3", "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-1)  => {"ansible_loop_var": "etcdnode", "changed": false, "etcdnode": "md-kubernetes-master-1", "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-2)  => {"ansible_loop_var": "etcdnode", "changed": false, "etcdnode": "md-kubernetes-master-2", "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-3)  => {"ansible_loop_var": "etcdnode", "changed": false, "etcdnode": "md-kubernetes-master-3", "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-1)  => {"ansible_loop_var": "etcdnode", "changed": false, "etcdnode": "md-kubernetes-master-1", "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-2)  => {"ansible_loop_var": "etcdnode", "changed": false, "etcdnode": "md-kubernetes-master-2", "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-3)  => {"ansible_loop_var": "etcdnode", "changed": false, "etcdnode": "md-kubernetes-master-3", "skip_reason": "Conditional result was False"}

TASK [external-etcd : Create etcd CA] *********************************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:36
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Create script for creating all certs for all etcd nodes primary etcd node] **********************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:40
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Run script for creating all certs for all etcd nodes primary etcd node] *************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:44
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Archive certificate files on primary etcd node] *************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:48
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Fetch certificate files from primary etcd node] *************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:52
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Unarchive certificates on localhost...] *********************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:56
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Copy certs to all etcd nodes] *******************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:60
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Copy kubeadmcfg.yaml to all etcd nodes] *********************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:63
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Create etcd manifests on all etcd nodes] ********************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:66
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Archive certs for master nodes on primary etcd node] ********************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:69
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Fetch master certs from primary etcd node] ******************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:73
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [external-etcd : Check etcd cluster health on primary etcd node] *************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/external-etcd/tasks/main.yaml:77
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-2] => {"changed": false, "skip_reason": "Conditional result was False"}
skipping: [md-kubernetes-master-3] => {"changed": false, "skip_reason": "Conditional result was False"}
META: ran handlers
META: ran handlers

PLAY [Set up primary master] ******************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/cluster-setup.yaml:65
ok: [md-kubernetes-master-1]
META: ran handlers

TASK [primary-master : Generate 'kubeadm' configuration file (external etcd only)] ************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/primary-master/tasks/main.yaml:6
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [primary-master : Remove /etc/systemd/system/kubelet.service.d/20-etcd-service-manager.conf on primary master (external etcd only)] ******
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/primary-master/tasks/main.yaml:10
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [primary-master : Stop kubelet on primary master] ****************************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/primary-master/tasks/main.yaml:14
changed: [md-kubernetes-master-1] => {"changed": true, "name": "kubelet", "state": "stopped", "status": {"ActiveEnterTimestamp": "Fri 2020-06-26 12:24:37 UTC", "ActiveEnterTimestampMonotonic": "220443494", "ActiveExitTimestamp": "Fri 2020-06-26 12:24:37 UTC", "ActiveExitTimestampMonotonic": "220380694", "ActiveState": "active", "After": "basic.target sysinit.target network-online.target system.slice systemd-journald.socket", "AllowIsolate": "no", "AmbientCapabilities": "", "AssertResult": "yes", "AssertTimestamp": "Fri 2020-06-26 12:24:37 UTC", "AssertTimestampMonotonic": "220441909", "Before": "shutdown.target multi-user.target", "BlockIOAccounting": "no", "BlockIOWeight": "[not set]", "CPUAccounting": "no", "CPUQuotaPerSecUSec": "infinity", "CPUSchedulingPolicy": "0", "CPUSchedulingPriority": "0", "CPUSchedulingResetOnFork": "no", "CPUShares": "[not set]", "CPUUsageNSec": "[not set]", "CPUWeight": "[not set]", "CacheDirectoryMode": "0755", "CanIsolate": "no", "CanReload": "no", "CanStart": "yes", "CanStop": "yes", "CapabilityBoundingSet": "cap_chown cap_dac_override cap_dac_read_search cap_fowner cap_fsetid cap_kill cap_setgid cap_setuid cap_setpcap cap_linux_immutable cap_net_bind_service cap_net_broadcast cap_net_admin cap_net_raw cap_ipc_lock cap_ipc_owner cap_sys_module cap_sys_rawio cap_sys_chroot cap_sys_ptrace cap_sys_pacct cap_sys_admin cap_sys_boot cap_sys_nice cap_sys_resource cap_sys_time cap_sys_tty_config cap_mknod cap_lease cap_audit_write cap_audit_control cap_setfcap cap_mac_override cap_mac_admin cap_syslog cap_wake_alarm cap_block_suspend", "CollectMode": "inactive", "ConditionResult": "yes", "ConditionTimestamp": "Fri 2020-06-26 12:24:37 UTC", "ConditionTimestampMonotonic": "220441908", "ConfigurationDirectoryMode": "0755", "Conflicts": "shutdown.target", "ControlGroup": "/system.slice/kubelet.service", "ControlPID": "0", "DefaultDependencies": "yes", "Delegate": "no", "Description": "kubelet: The Kubernetes Node Agent", "DevicePolicy": "auto", "Documentation": "https://kubernetes.io/docs/home/", "DropInPaths": "/etc/systemd/system/kubelet.service.d/10-kubeadm.conf", "DynamicUser": "no", "Environment": "[unprintable] KUBELET_CONFIG_ARGS=--config=/var/lib/kubelet/config.yaml", "EnvironmentFile": "/etc/default/kubelet (ignore_errors=yes)", "ExecMainCode": "0", "ExecMainExitTimestampMonotonic": "0", "ExecMainPID": "4776", "ExecMainStartTimestamp": "Fri 2020-06-26 12:24:37 UTC", "ExecMainStartTimestampMonotonic": "220443437", "ExecMainStatus": "0", "ExecStart": "{ path=/usr/bin/kubelet ; argv[]=/usr/bin/kubelet $KUBELET_KUBECONFIG_ARGS $KUBELET_CONFIG_ARGS $KUBELET_KUBEADM_ARGS $KUBELET_EXTRA_ARGS ; ignore_errors=no ; start_time=[Fri 2020-06-26 12:24:37 UTC] ; stop_time=[n/a] ; pid=4776 ; code=(null) ; status=0/0 }", "FailureAction": "none", "FileDescriptorStoreMax": "0", "FragmentPath": "/lib/systemd/system/kubelet.service", "GID": "[not set]", "GuessMainPID": "yes", "IOAccounting": "no", "IOSchedulingClass": "0", "IOSchedulingPriority": "0", "IOWeight": "[not set]", "IPAccounting": "no", "IPEgressBytes": "18446744073709551615", "IPEgressPackets": "18446744073709551615", "IPIngressBytes": "18446744073709551615", "IPIngressPackets": "18446744073709551615", "Id": "kubelet.service", "IgnoreOnIsolate": "no", "IgnoreSIGPIPE": "yes", "InactiveEnterTimestamp": "Fri 2020-06-26 12:24:37 UTC", "InactiveEnterTimestampMonotonic": "220440700", "InactiveExitTimestamp": "Fri 2020-06-26 12:24:37 UTC", "InactiveExitTimestampMonotonic": "220443494", "InvocationID": "22bb23f117934b4cae5080e2fb1fe97f", "JobRunningTimeoutUSec": "infinity", "JobTimeoutAction": "none", "JobTimeoutUSec": "infinity", "KeyringMode": "private", "KillMode": "control-group", "KillSignal": "15", "LimitAS": "infinity", "LimitASSoft": "infinity", "LimitCORE": "infinity", "LimitCORESoft": "0", "LimitCPU": "infinity", "LimitCPUSoft": "infinity", "LimitDATA": "infinity", "LimitDATASoft": "infinity", "LimitFSIZE": "infinity", "LimitFSIZESoft": "infinity", "LimitLOCKS": "infinity", "LimitLOCKSSoft": "infinity", "LimitMEMLOCK": "16777216", "LimitMEMLOCKSoft": "16777216", "LimitMSGQUEUE": "819200", "LimitMSGQUEUESoft": "819200", "LimitNICE": "0", "LimitNICESoft": "0", "LimitNOFILE": "4096", "LimitNOFILESoft": "1024", "LimitNPROC": "15676", "LimitNPROCSoft": "15676", "LimitRSS": "infinity", "LimitRSSSoft": "infinity", "LimitRTPRIO": "0", "LimitRTPRIOSoft": "0", "LimitRTTIME": "infinity", "LimitRTTIMESoft": "infinity", "LimitSIGPENDING": "15676", "LimitSIGPENDINGSoft": "15676", "LimitSTACK": "infinity", "LimitSTACKSoft": "8388608", "LoadState": "loaded", "LockPersonality": "no", "LogLevelMax": "-1", "LogsDirectoryMode": "0755", "MainPID": "4776", "MemoryAccounting": "no", "MemoryCurrent": "[not set]", "MemoryDenyWriteExecute": "no", "MemoryHigh": "infinity", "MemoryLimit": "infinity", "MemoryLow": "0", "MemoryMax": "infinity", "MemorySwapMax": "infinity", "MountAPIVFS": "no", "MountFlags": "", "NFileDescriptorStore": "0", "NRestarts": "0", "Names": "kubelet.service", "NeedDaemonReload": "no", "Nice": "0", "NoNewPrivileges": "no", "NonBlocking": "no", "NotifyAccess": "none", "OOMScoreAdjust": "0", "OnFailureJobMode": "replace", "PermissionsStartOnly": "no", "Perpetual": "no", "PrivateDevices": "no", "PrivateNetwork": "no", "PrivateTmp": "no", "PrivateUsers": "no", "ProtectControlGroups": "no", "ProtectHome": "no", "ProtectKernelModules": "no", "ProtectKernelTunables": "no", "ProtectSystem": "no", "RefuseManualStart": "no", "RefuseManualStop": "no", "RemainAfterExit": "no", "RemoveIPC": "no", "Requires": "system.slice sysinit.target", "Restart": "always", "RestartUSec": "10s", "RestrictNamespaces": "no", "RestrictRealtime": "no", "RestrictSUIDSGID": "no", "Result": "success", "RootDirectoryStartOnly": "no", "RuntimeDirectoryMode": "0755", "RuntimeDirectoryPreserve": "no", "RuntimeMaxUSec": "infinity", "SameProcessGroup": "no", "SecureBits": "0", "SendSIGHUP": "no", "SendSIGKILL": "yes", "Slice": "system.slice", "StandardError": "inherit", "StandardInput": "null", "StandardInputData": "", "StandardOutput": "journal", "StartLimitAction": "none", "StartLimitBurst": "5", "StartLimitIntervalUSec": "0", "StartupBlockIOWeight": "[not set]", "StartupCPUShares": "[not set]", "StartupCPUWeight": "[not set]", "StartupIOWeight": "[not set]", "StateChangeTimestamp": "Fri 2020-06-26 12:24:37 UTC", "StateChangeTimestampMonotonic": "220443494", "StateDirectoryMode": "0755", "StatusErrno": "0", "StopWhenUnneeded": "no", "SubState": "running", "SuccessAction": "none", "SyslogFacility": "3", "SyslogLevel": "6", "SyslogLevelPrefix": "yes", "SyslogPriority": "30", "SystemCallErrorNumber": "0", "TTYReset": "no", "TTYVHangup": "no", "TTYVTDisallocate": "no", "TasksAccounting": "yes", "TasksCurrent": "17", "TasksMax": "4702", "TimeoutStartUSec": "1min 30s", "TimeoutStopUSec": "1min 30s", "TimerSlackNSec": "50000", "Transient": "no", "Type": "simple", "UID": "[not set]", "UMask": "0022", "UnitFilePreset": "enabled", "UnitFileState": "enabled", "UtmpMode": "init", "WantedBy": "multi-user.target", "Wants": "network-online.target", "WatchdogTimestamp": "Fri 2020-06-26 12:24:37 UTC", "WatchdogTimestampMonotonic": "220443493", "WatchdogUSec": "0"}}

TASK [primary-master : Run 'kubeadm init' (external etcd only)] *******************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/primary-master/tasks/main.yaml:17
skipping: [md-kubernetes-master-1] => {"changed": false, "skip_reason": "Conditional result was False"}

TASK [primary-master : Run 'kubeadm init' (stacked etcd only)] ********************************************************************************
task path: /Users/ajeetraina/kubeadm2ha/ansible/roles/primary-master/tasks/main.yaml:21
fatal: [md-kubernetes-master-1]: FAILED! => {"changed": true, "cmd": "kubeadm init --control-plane-endpoint '165.22.210.124:8443' --upload-certs --kubernetes-version 'v1.18.4' 2>&1 | tee /tmp/kubeadm-init.out; exit ${PIPESTATUS[0]}", "delta": "0:00:00.575141", "end": "2020-06-26 12:44:12.021006", "msg": "non-zero return code", "rc": 2, "start": "2020-06-26 12:44:11.445865", "stderr": "/bin/sh: 1: Bad substitution", "stderr_lines": ["/bin/sh: 1: Bad substitution"], "stdout": "W0626 12:44:11.496576   12272 configset.go:202] WARNING: kubeadm cannot validate component configs for API groups [kubelet.config.k8s.io kubeproxy.config.k8s.io]\n[init] Using Kubernetes version: v1.18.4\n[preflight] Running pre-flight checks\n\t[WARNING IsDockerSystemdCheck]: detected \"cgroupfs\" as the Docker cgroup driver. The recommended driver is \"systemd\". Please follow the guide at https://kubernetes.io/docs/setup/cri/\nerror execution phase preflight: [preflight] Some fatal errors occurred:\n\t[ERROR Port-6443]: Port 6443 is in use\n\t[ERROR Port-10259]: Port 10259 is in use\n\t[ERROR Port-10257]: Port 10257 is in use\n\t[ERROR FileAvailable--etc-kubernetes-manifests-kube-apiserver.yaml]: /etc/kubernetes/manifests/kube-apiserver.yaml already exists\n\t[ERROR FileAvailable--etc-kubernetes-manifests-kube-controller-manager.yaml]: /etc/kubernetes/manifests/kube-controller-manager.yaml already exists\n\t[ERROR FileAvailable--etc-kubernetes-manifests-kube-scheduler.yaml]: /etc/kubernetes/manifests/kube-scheduler.yaml already exists\n\t[ERROR FileAvailable--etc-kubernetes-manifests-etcd.yaml]: /etc/kubernetes/manifests/etcd.yaml already exists\n\t[ERROR Port-2379]: Port 2379 is in use\n\t[ERROR Port-2380]: Port 2380 is in use\n\t[ERROR DirAvailable--var-lib-etcd]: /var/lib/etcd is not empty\n[preflight] If you know what you are doing, you can make a check non-fatal with `--ignore-preflight-errors=...`\nTo see the stack trace of this error execute with --v=5 or higher", "stdout_lines": ["W0626 12:44:11.496576   12272 configset.go:202] WARNING: kubeadm cannot validate component configs for API groups [kubelet.config.k8s.io kubeproxy.config.k8s.io]", "[init] Using Kubernetes version: v1.18.4", "[preflight] Running pre-flight checks", "\t[WARNING IsDockerSystemdCheck]: detected \"cgroupfs\" as the Docker cgroup driver. The recommended driver is \"systemd\". Please follow the guide at https://kubernetes.io/docs/setup/cri/", "error execution phase preflight: [preflight] Some fatal errors occurred:", "\t[ERROR Port-6443]: Port 6443 is in use", "\t[ERROR Port-10259]: Port 10259 is in use", "\t[ERROR Port-10257]: Port 10257 is in use", "\t[ERROR FileAvailable--etc-kubernetes-manifests-kube-apiserver.yaml]: /etc/kubernetes/manifests/kube-apiserver.yaml already exists", "\t[ERROR FileAvailable--etc-kubernetes-manifests-kube-controller-manager.yaml]: /etc/kubernetes/manifests/kube-controller-manager.yaml already exists", "\t[ERROR FileAvailable--etc-kubernetes-manifests-kube-scheduler.yaml]: /etc/kubernetes/manifests/kube-scheduler.yaml already exists", "\t[ERROR FileAvailable--etc-kubernetes-manifests-etcd.yaml]: /etc/kubernetes/manifests/etcd.yaml already exists", "\t[ERROR Port-2379]: Port 2379 is in use", "\t[ERROR Port-2380]: Port 2380 is in use", "\t[ERROR DirAvailable--var-lib-etcd]: /var/lib/etcd is not empty", "[preflight] If you know what you are doing, you can make a check non-fatal with `--ignore-preflight-errors=...`", "To see the stack trace of this error execute with --v=5 or higher"]}

NO MORE HOSTS LEFT ****************************************************************************************************************************

PLAY RECAP ************************************************************************************************************************************
md-kubernetes-master-1     : ok=21   changed=1    unreachable=0    failed=1    skipped=31   rescued=0    ignored=0
md-kubernetes-master-2     : ok=17   changed=0    unreachable=0    failed=0    skipped=30   rescued=0    ignored=0
md-kubernetes-master-3     : ok=17   changed=0    unreachable=0    failed=0    skipped=30   rescued=0    ignored=0
md-kubernetes-minion-4     : ok=3    changed=0    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

[Captains-Bay]🚩 >
```
