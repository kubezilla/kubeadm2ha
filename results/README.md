```
 sansible-playbook -i my-cluster.inventory cluster-setup.yaml

PLAY [Prepare Nodes] **************************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
ok: [md-kubernetes-minion-4]
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-2]

TASK [prepare-nodes : Make sure some needed software is installed via package manager] ********************************************************
ok: [md-kubernetes-master-3] => (item=perl)
ok: [md-kubernetes-master-2] => (item=perl)
ok: [md-kubernetes-minion-4] => (item=perl)
ok: [md-kubernetes-master-1] => (item=perl)
ok: [md-kubernetes-master-3] => (item=kubelet)
ok: [md-kubernetes-master-2] => (item=kubelet)
ok: [md-kubernetes-minion-4] => (item=kubelet)
ok: [md-kubernetes-master-3] => (item=kubectl)
ok: [md-kubernetes-master-2] => (item=kubectl)
ok: [md-kubernetes-minion-4] => (item=kubectl)
ok: [md-kubernetes-master-3] => (item=kubeadm)
ok: [md-kubernetes-master-2] => (item=kubeadm)
ok: [md-kubernetes-minion-4] => (item=kubeadm)
ok: [md-kubernetes-master-3] => (item=kubernetes-cni)
ok: [md-kubernetes-master-2] => (item=kubernetes-cni)
ok: [md-kubernetes-minion-4] => (item=kubernetes-cni)
changed: [md-kubernetes-master-1] => (item=kubelet)
ok: [md-kubernetes-master-1] => (item=kubectl)
changed: [md-kubernetes-master-1] => (item=kubeadm)
ok: [md-kubernetes-master-1] => (item=kubernetes-cni)

TASK [prepare-nodes : Enable kubelet] *********************************************************************************************************
ok: [md-kubernetes-master-3]
changed: [md-kubernetes-master-1]
ok: [md-kubernetes-minion-4]
ok: [md-kubernetes-master-2]

TASK [prepare-nodes : Create setup directory] *************************************************************************************************
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-minion-4]
ok: [md-kubernetes-master-1]

PLAY [Kube-VIP] *******************************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-master-2]

TASK [Create configuration directory /etc/kube-vip] *******************************************************************************************
skipping: [md-kubernetes-master-1]
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]

TASK [kube-vip : Create manifests directory for static pods /etc/kubernetes/manifests] ********************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [kube-vip : Create service configuration file] *******************************************************************************************
skipping: [md-kubernetes-master-1]
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]

TASK [kube-vip : Create manifest for static pod] **********************************************************************************************
skipping: [md-kubernetes-master-1]
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]

PLAY [Keepalived] *****************************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-2]

TASK [keepalived : Create configuration directory] ********************************************************************************************
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-3]

TASK [keepalived : Copy check script] *********************************************************************************************************
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-3]

TASK [keepalived : Generate configuraton file] ************************************************************************************************
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-master-1]

TASK [keepalived : Copying override script to primary master in order to have a VIP before at least one APIServer is up] **********************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
ok: [md-kubernetes-master-1]

TASK [keepalived : Generate static pod configuraton file directory] ***************************************************************************
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-master-2]

TASK [keepalived : Generate static pod configuraton file] *************************************************************************************
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-3]

PLAY [NGINX] **********************************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-1]

TASK [nginx : Create configuration directory] *************************************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-1]
skipping: [md-kubernetes-master-3]

TASK [nginx : Generate service configuraton file] *********************************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-1]
skipping: [md-kubernetes-master-3]

TASK [nginx : Generate static pod configuraton file directory] ********************************************************************************
skipping: [md-kubernetes-master-1]
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]

TASK [nginx : Generate static pod configuraton file] ******************************************************************************************
skipping: [md-kubernetes-master-1]
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]

PLAY [HAProxy] ********************************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-3]

TASK [haproxy : Create configuration directory] ***********************************************************************************************
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-3]

TASK [haproxy : Generate service configuraton file] *******************************************************************************************
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-1]

TASK [haproxy : Generate static pod configuraton file directory] ******************************************************************************
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-1]

TASK [haproxy : Generate static pod configuraton file] ****************************************************************************************
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-3]

PLAY [Deploy external etcd] *******************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-1]

TASK [external-etcd : Install preliminary kubelet configuration for systemd] ******************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Activate and restart kubelet] *******************************************************************************************
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-2]
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
skipping: [md-kubernetes-master-1]
skipping: [md-kubernetes-master-3]

TASK [external-etcd : Create temporary cert directories on primary etcd node] *****************************************************************
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-2)
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-3)
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-1)
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-2)
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-3)
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-1)
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-2)
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-3)
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-1)

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
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Unarchive certificates on localhost...] *********************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Copy certs to all etcd nodes] *******************************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Copy kubeadmcfg.yaml to all etcd nodes] *********************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Create etcd manifests on all etcd nodes] ********************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Archive certs for master nodes on primary etcd node] ********************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
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
changed: [md-kubernetes-master-1]

TASK [primary-master : Run 'kubeadm init' (external etcd only)] *******************************************************************************
skipping: [md-kubernetes-master-1]

TASK [primary-master : Run 'kubeadm init' (stacked etcd only)] ********************************************************************************
fatal: [md-kubernetes-master-1]: FAILED! => {"changed": true, "cmd": "kubeadm init --control-plane-endpoint '165.22.210.124:8443' --upload-certs --kubernetes-version 'v1.18.4' 2>&1 | tee /tmp/kubeadm-init.out; exit ${PIPESTATUS[0]}", "delta": "0:01:00.737494", "end": "2020-06-26 12:06:14.408586", "msg": "non-zero return code", "rc": 2, "start": "2020-06-26 12:05:13.671092", "stderr": "/bin/sh: 1: Bad substitution", "stderr_lines": ["/bin/sh: 1: Bad substitution"], "stdout": "W0626 12:05:13.729984   10341 configset.go:202] WARNING: kubeadm cannot validate component configs for API groups [kubelet.config.k8s.io kubeproxy.config.k8s.io]\n[init] Using Kubernetes version: v1.18.4\n[preflight] Running pre-flight checks\n\t[WARNING IsDockerSystemdCheck]: detected \"cgroupfs\" as the Docker cgroup driver. The recommended driver is \"systemd\". Please follow the guide at https://kubernetes.io/docs/setup/cri/\n[preflight] Pulling images required for setting up a Kubernetes cluster\n[preflight] This might take a minute or two, depending on the speed of your internet connection\n[preflight] You can also perform this action in beforehand using 'kubeadm config images pull'\n[kubelet-start] Writing kubelet environment file with flags to file \"/var/lib/kubelet/kubeadm-flags.env\"\n[kubelet-start] Writing kubelet configuration to file \"/var/lib/kubelet/config.yaml\"\n[kubelet-start] Starting the kubelet\n[certs] Using certificateDir folder \"/etc/kubernetes/pki\"\n[certs] Generating \"ca\" certificate and key\n[certs] Generating \"apiserver\" certificate and key\n[certs] apiserver serving cert is signed for DNS names [ha-proxy kubernetes kubernetes.default kubernetes.default.svc kubernetes.default.svc.cluster.local] and IPs [10.96.0.1 165.22.210.124 165.22.210.124]\n[certs] Generating \"apiserver-kubelet-client\" certificate and key\n[certs] Generating \"front-proxy-ca\" certificate and key\n[certs] Generating \"front-proxy-client\" certificate and key\n[certs] Generating \"etcd/ca\" certificate and key\n[certs] Generating \"etcd/server\" certificate and key\n[certs] etcd/server serving cert is signed for DNS names [ha-proxy localhost] and IPs [165.22.210.124 127.0.0.1 ::1]\n[certs] Generating \"etcd/peer\" certificate and key\n[certs] etcd/peer serving cert is signed for DNS names [ha-proxy localhost] and IPs [165.22.210.124 127.0.0.1 ::1]\n[certs] Generating \"etcd/healthcheck-client\" certificate and key\n[certs] Generating \"apiserver-etcd-client\" certificate and key\n[certs] Generating \"sa\" key and public key\n[kubeconfig] Using kubeconfig folder \"/etc/kubernetes\"\n[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address\n[kubeconfig] Writing \"admin.conf\" kubeconfig file\n[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address\n[kubeconfig] Writing \"kubelet.conf\" kubeconfig file\n[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address\n[kubeconfig] Writing \"controller-manager.conf\" kubeconfig file\n[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address\n[kubeconfig] Writing \"scheduler.conf\" kubeconfig file\n[control-plane] Using manifest folder \"/etc/kubernetes/manifests\"\n[control-plane] Creating static Pod manifest for \"kube-apiserver\"\n[control-plane] Creating static Pod manifest for \"kube-controller-manager\"\nW0626 12:05:51.621090   10341 manifests.go:225] the default kube-apiserver authorization-mode is \"Node,RBAC\"; using \"Node,RBAC\"\n[control-plane] Creating static Pod manifest for \"kube-scheduler\"\nW0626 12:05:51.622472   10341 manifests.go:225] the default kube-apiserver authorization-mode is \"Node,RBAC\"; using \"Node,RBAC\"\n[etcd] Creating static Pod manifest for local etcd in \"/etc/kubernetes/manifests\"\n[wait-control-plane] Waiting for the kubelet to boot up the control plane as static Pods from directory \"/etc/kubernetes/manifests\". This can take up to 4m0s\n[apiclient] All control plane components are healthy after 17.541692 seconds\n[upload-config] Storing the configuration used in ConfigMap \"kubeadm-config\" in the \"kube-system\" Namespace\n[kubelet] Creating a ConfigMap \"kubelet-config-1.18\" in namespace kube-system with the configuration for the kubelets in the cluster\n[upload-certs] Storing the certificates in Secret \"kubeadm-certs\" in the \"kube-system\" Namespace\n[upload-certs] Using certificate key:\n97a68fc6aacd6862a99cea47915a4b9fd7f8d57e89d8714549ec93055547ab7b\n[mark-control-plane] Marking the node ha-proxy as control-plane by adding the label \"node-role.kubernetes.io/master=''\"\n[mark-control-plane] Marking the node ha-proxy as control-plane by adding the taints [node-role.kubernetes.io/master:NoSchedule]\n[bootstrap-token] Using token: lruhss.ozhyjfm5fwmrujfo\n[bootstrap-token] Configuring bootstrap tokens, cluster-info ConfigMap, RBAC Roles\n[bootstrap-token] configured RBAC rules to allow Node Bootstrap tokens to get nodes\n[bootstrap-token] configured RBAC rules to allow Node Bootstrap tokens to post CSRs in order for nodes to get long term certificate credentials\n[bootstrap-token] configured RBAC rules to allow the csrapprover controller automatically approve CSRs from a Node Bootstrap Token\n[bootstrap-token] configured RBAC rules to allow certificate rotation for all node client certificates in the cluster\n[bootstrap-token] Creating the \"cluster-info\" ConfigMap in the \"kube-public\" namespace\n[kubelet-finalize] Updating \"/etc/kubernetes/kubelet.conf\" to point to a rotatable kubelet client certificate and key\n[addons] Applied essential addon: CoreDNS\n[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address\n[addons] Applied essential addon: kube-proxy\n\nYour Kubernetes control-plane has initialized successfully!\n\nTo start using your cluster, you need to run the following as a regular user:\n\n  mkdir -p $HOME/.kube\n  sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config\n  sudo chown $(id -u):$(id -g) $HOME/.kube/config\n\nYou should now deploy a pod network to the cluster.\nRun \"kubectl apply -f [podnetwork].yaml\" with one of the options listed at:\n  https://kubernetes.io/docs/concepts/cluster-administration/addons/\n\nYou can now join any number of the control-plane node running the following command on each as root:\n\n  kubeadm join 165.22.210.124:8443 --token lruhss.ozhyjfm5fwmrujfo \\\n    --discovery-token-ca-cert-hash sha256:92f0ae5162b82484e7b27741e71473ede268ff7794d9d23710a6a3955dfc7605 \\\n    --control-plane --certificate-key 97a68fc6aacd6862a99cea47915a4b9fd7f8d57e89d8714549ec93055547ab7b\n\nPlease note that the certificate-key gives access to cluster sensitive data, keep it secret!\nAs a safeguard, uploaded-certs will be deleted in two hours; If necessary, you can use\n\"kubeadm init phase upload-certs --upload-certs\" to reload certs afterward.\n\nThen you can join any number of worker nodes by running the following on each as root:\n\nkubeadm join 165.22.210.124:8443 --token lruhss.ozhyjfm5fwmrujfo \\\n    --discovery-token-ca-cert-hash sha256:92f0ae5162b82484e7b27741e71473ede268ff7794d9d23710a6a3955dfc7605 ", "stdout_lines": ["W0626 12:05:13.729984   10341 configset.go:202] WARNING: kubeadm cannot validate component configs for API groups [kubelet.config.k8s.io kubeproxy.config.k8s.io]", "[init] Using Kubernetes version: v1.18.4", "[preflight] Running pre-flight checks", "\t[WARNING IsDockerSystemdCheck]: detected \"cgroupfs\" as the Docker cgroup driver. The recommended driver is \"systemd\". Please follow the guide at https://kubernetes.io/docs/setup/cri/", "[preflight] Pulling images required for setting up a Kubernetes cluster", "[preflight] This might take a minute or two, depending on the speed of your internet connection", "[preflight] You can also perform this action in beforehand using 'kubeadm config images pull'", "[kubelet-start] Writing kubelet environment file with flags to file \"/var/lib/kubelet/kubeadm-flags.env\"", "[kubelet-start] Writing kubelet configuration to file \"/var/lib/kubelet/config.yaml\"", "[kubelet-start] Starting the kubelet", "[certs] Using certificateDir folder \"/etc/kubernetes/pki\"", "[certs] Generating \"ca\" certificate and key", "[certs] Generating \"apiserver\" certificate and key", "[certs] apiserver serving cert is signed for DNS names [ha-proxy kubernetes kubernetes.default kubernetes.default.svc kubernetes.default.svc.cluster.local] and IPs [10.96.0.1 165.22.210.124 165.22.210.124]", "[certs] Generating \"apiserver-kubelet-client\" certificate and key", "[certs] Generating \"front-proxy-ca\" certificate and key", "[certs] Generating \"front-proxy-client\" certificate and key", "[certs] Generating \"etcd/ca\" certificate and key", "[certs] Generating \"etcd/server\" certificate and key", "[certs] etcd/server serving cert is signed for DNS names [ha-proxy localhost] and IPs [165.22.210.124 127.0.0.1 ::1]", "[certs] Generating \"etcd/peer\" certificate and key", "[certs] etcd/peer serving cert is signed for DNS names [ha-proxy localhost] and IPs [165.22.210.124 127.0.0.1 ::1]", "[certs] Generating \"etcd/healthcheck-client\" certificate and key", "[certs] Generating \"apiserver-etcd-client\" certificate and key", "[certs] Generating \"sa\" key and public key", "[kubeconfig] Using kubeconfig folder \"/etc/kubernetes\"", "[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address", "[kubeconfig] Writing \"admin.conf\" kubeconfig file", "[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address", "[kubeconfig] Writing \"kubelet.conf\" kubeconfig file", "[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address", "[kubeconfig] Writing \"controller-manager.conf\" kubeconfig file", "[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address", "[kubeconfig] Writing \"scheduler.conf\" kubeconfig file", "[control-plane] Using manifest folder \"/etc/kubernetes/manifests\"", "[control-plane] Creating static Pod manifest for \"kube-apiserver\"", "[control-plane] Creating static Pod manifest for \"kube-controller-manager\"", "W0626 12:05:51.621090   10341 manifests.go:225] the default kube-apiserver authorization-mode is \"Node,RBAC\"; using \"Node,RBAC\"", "[control-plane] Creating static Pod manifest for \"kube-scheduler\"", "W0626 12:05:51.622472   10341 manifests.go:225] the default kube-apiserver authorization-mode is \"Node,RBAC\"; using \"Node,RBAC\"", "[etcd] Creating static Pod manifest for local etcd in \"/etc/kubernetes/manifests\"", "[wait-control-plane] Waiting for the kubelet to boot up the control plane as static Pods from directory \"/etc/kubernetes/manifests\". This can take up to 4m0s", "[apiclient] All control plane components are healthy after 17.541692 seconds", "[upload-config] Storing the configuration used in ConfigMap \"kubeadm-config\" in the \"kube-system\" Namespace", "[kubelet] Creating a ConfigMap \"kubelet-config-1.18\" in namespace kube-system with the configuration for the kubelets in the cluster", "[upload-certs] Storing the certificates in Secret \"kubeadm-certs\" in the \"kube-system\" Namespace", "[upload-certs] Using certificate key:", "97a68fc6aacd6862a99cea47915a4b9fd7f8d57e89d8714549ec93055547ab7b", "[mark-control-plane] Marking the node ha-proxy as control-plane by adding the label \"node-role.kubernetes.io/master=''\"", "[mark-control-plane] Marking the node ha-proxy as control-plane by adding the taints [node-role.kubernetes.io/master:NoSchedule]", "[bootstrap-token] Using token: lruhss.ozhyjfm5fwmrujfo", "[bootstrap-token] Configuring bootstrap tokens, cluster-info ConfigMap, RBAC Roles", "[bootstrap-token] configured RBAC rules to allow Node Bootstrap tokens to get nodes", "[bootstrap-token] configured RBAC rules to allow Node Bootstrap tokens to post CSRs in order for nodes to get long term certificate credentials", "[bootstrap-token] configured RBAC rules to allow the csrapprover controller automatically approve CSRs from a Node Bootstrap Token", "[bootstrap-token] configured RBAC rules to allow certificate rotation for all node client certificates in the cluster", "[bootstrap-token] Creating the \"cluster-info\" ConfigMap in the \"kube-public\" namespace", "[kubelet-finalize] Updating \"/etc/kubernetes/kubelet.conf\" to point to a rotatable kubelet client certificate and key", "[addons] Applied essential addon: CoreDNS", "[endpoint] WARNING: port specified in controlPlaneEndpoint overrides bindPort in the controlplane address", "[addons] Applied essential addon: kube-proxy", "", "Your Kubernetes control-plane has initialized successfully!", "", "To start using your cluster, you need to run the following as a regular user:", "", "  mkdir -p $HOME/.kube", "  sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config", "  sudo chown $(id -u):$(id -g) $HOME/.kube/config", "", "You should now deploy a pod network to the cluster.", "Run \"kubectl apply -f [podnetwork].yaml\" with one of the options listed at:", "  https://kubernetes.io/docs/concepts/cluster-administration/addons/", "", "You can now join any number of the control-plane node running the following command on each as root:", "", "  kubeadm join 165.22.210.124:8443 --token lruhss.ozhyjfm5fwmrujfo \\", "    --discovery-token-ca-cert-hash sha256:92f0ae5162b82484e7b27741e71473ede268ff7794d9d23710a6a3955dfc7605 \\", "    --control-plane --certificate-key 97a68fc6aacd6862a99cea47915a4b9fd7f8d57e89d8714549ec93055547ab7b", "", "Please note that the certificate-key gives access to cluster sensitive data, keep it secret!", "As a safeguard, uploaded-certs will be deleted in two hours; If necessary, you can use", "\"kubeadm init phase upload-certs --upload-certs\" to reload certs afterward.", "", "Then you can join any number of worker nodes by running the following on each as root:", "", "kubeadm join 165.22.210.124:8443 --token lruhss.ozhyjfm5fwmrujfo \\", "    --discovery-token-ca-cert-hash sha256:92f0ae5162b82484e7b27741e71473ede268ff7794d9d23710a6a3955dfc7605 "]}

NO MORE HOSTS LEFT ****************************************************************************************************************************

PLAY RECAP ************************************************************************************************************************************
md-kubernetes-master-1     : ok=21   changed=3    unreachable=0    failed=1    skipped=31   rescued=0    ignored=0
md-kubernetes-master-2     : ok=17   changed=0    unreachable=0    failed=0    skipped=30   rescued=0    ignored=0
md-kubernetes-master-3     : ok=17   changed=0    unreachable=0    failed=0    skipped=30   rescued=0    ignored=0
md-kubernetes-minion-4     : ok=3    changed=0    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

```
