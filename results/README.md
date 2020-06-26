```
ansible-playbook -i my-cluster.inventory cluster-setup.yaml

PLAY [Prepare Nodes] **************************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-minion-4]

TASK [prepare-nodes : Make sure some needed software is installed via package manager] ********************************************************
ok: [md-kubernetes-master-3] => (item=perl)
ok: [md-kubernetes-master-2] => (item=perl)
ok: [md-kubernetes-master-1] => (item=perl)
ok: [md-kubernetes-minion-4] => (item=perl)
ok: [md-kubernetes-master-3] => (item=kubelet)
ok: [md-kubernetes-master-2] => (item=kubelet)
ok: [md-kubernetes-master-1] => (item=kubelet)
ok: [md-kubernetes-minion-4] => (item=kubelet)
ok: [md-kubernetes-master-3] => (item=kubectl)
ok: [md-kubernetes-master-2] => (item=kubectl)
ok: [md-kubernetes-master-1] => (item=kubectl)
ok: [md-kubernetes-minion-4] => (item=kubectl)
ok: [md-kubernetes-master-3] => (item=kubeadm)
ok: [md-kubernetes-master-2] => (item=kubeadm)
ok: [md-kubernetes-minion-4] => (item=kubeadm)
ok: [md-kubernetes-master-1] => (item=kubeadm)
ok: [md-kubernetes-master-2] => (item=kubernetes-cni)
ok: [md-kubernetes-master-3] => (item=kubernetes-cni)
ok: [md-kubernetes-master-1] => (item=kubernetes-cni)
ok: [md-kubernetes-minion-4] => (item=kubernetes-cni)

TASK [prepare-nodes : Enable kubelet] *********************************************************************************************************
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-minion-4]
ok: [md-kubernetes-master-2]

TASK [prepare-nodes : Create setup directory] *************************************************************************************************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-minion-4]
changed: [md-kubernetes-master-1]

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
skipping: [md-kubernetes-master-1]
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]

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
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-3]

TASK [keepalived : Create configuration directory] ********************************************************************************************
changed: [md-kubernetes-master-2]
changed: [md-kubernetes-master-1]
changed: [md-kubernetes-master-3]

TASK [keepalived : Copy check script] *********************************************************************************************************
changed: [md-kubernetes-master-1]
changed: [md-kubernetes-master-2]
changed: [md-kubernetes-master-3]

TASK [keepalived : Generate configuraton file] ************************************************************************************************
changed: [md-kubernetes-master-2]
changed: [md-kubernetes-master-3]
changed: [md-kubernetes-master-1]

TASK [keepalived : Copying override script to primary master in order to have a VIP before at least one APIServer is up] **********************
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]
changed: [md-kubernetes-master-1]

TASK [keepalived : Generate static pod configuraton file directory] ***************************************************************************
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-3]

TASK [keepalived : Generate static pod configuraton file] *************************************************************************************
changed: [md-kubernetes-master-1]
changed: [md-kubernetes-master-3]
changed: [md-kubernetes-master-2]

PLAY [NGINX] **********************************************************************************************************************************

TASK [Gathering Facts] ************************************************************************************************************************
ok: [md-kubernetes-master-1]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-3]

TASK [nginx : Create configuration directory] *************************************************************************************************
skipping: [md-kubernetes-master-1]
skipping: [md-kubernetes-master-2]
skipping: [md-kubernetes-master-3]

TASK [nginx : Generate service configuraton file] *********************************************************************************************
skipping: [md-kubernetes-master-1]
skipping: [md-kubernetes-master-2]
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
ok: [md-kubernetes-master-3]
ok: [md-kubernetes-master-2]
ok: [md-kubernetes-master-1]

TASK [haproxy : Create configuration directory] ***********************************************************************************************
ok: [md-kubernetes-master-1]
changed: [md-kubernetes-master-2]
changed: [md-kubernetes-master-3]

TASK [haproxy : Generate service configuraton file] *******************************************************************************************
changed: [md-kubernetes-master-1]
changed: [md-kubernetes-master-2]
changed: [md-kubernetes-master-3]

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
skipping: [md-kubernetes-master-3]
skipping: [md-kubernetes-master-1]

TASK [external-etcd : Create temporary cert directories on primary etcd node] *****************************************************************
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-2)
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-3)
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-2)
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-1)
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-3)
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-1)
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-2)
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-3)
skipping: [md-kubernetes-master-1] => (item=md-kubernetes-master-1)

TASK [external-etcd : Generate kubeadmcfg.yaml on primary etcd node] **************************************************************************
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-2)
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-3)
skipping: [md-kubernetes-master-3] => (item=md-kubernetes-master-2)
skipping: [md-kubernetes-master-2] => (item=md-kubernetes-master-1)
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
fatal: [md-kubernetes-master-1]: FAILED! => {"changed": true, "cmd": "kubeadm init --control-plane-endpoint '165.22.210.124:8443' --upload-certs --kubernetes-version 'v1.18.4-01' 2>&1 | tee /tmp/kubeadm-init.out; exit ${PIPESTATUS[0]}", "delta": "0:00:00.054245", "end": "2020-06-26 10:46:17.677561", "msg": "non-zero return code", "rc": 2, "start": "2020-06-26 10:46:17.623316", "stderr": "/bin/sh: 1: Bad substitution", "stderr_lines": ["/bin/sh: 1: Bad substitution"], "stdout": "couldn't parse Kubernetes version \"v1.18.4-01\": illegal zero-prefixed version component \"01\" in \"v1.18.4-01\"\nTo see the stack trace of this error execute with --v=5 or higher", "stdout_lines": ["couldn't parse Kubernetes version \"v1.18.4-01\": illegal zero-prefixed version component \"01\" in \"v1.18.4-01\"", "To see the stack trace of this error execute with --v=5 or higher"]}

NO MORE HOSTS LEFT ****************************************************************************************************************************

PLAY RECAP ************************************************************************************************************************************
md-kubernetes-master-1     : ok=21   changed=9    unreachable=0    failed=1    skipped=31   rescued=0    ignored=0
md-kubernetes-master-2     : ok=17   changed=7    unreachable=0    failed=0    skipped=30   rescued=0    ignored=0
md-kubernetes-master-3     : ok=17   changed=7    unreachable=0    failed=0    skipped=30   rescued=0    ignored=0
md-kubernetes-minion-4     : ok=3    changed=0    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

```
