# prerequisites

## [kubectl](https://kubernetes.io/docs/tasks/tools/)

– A command line tool for working with Kubernetes clusters. For more information,

## [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli/)

– A command line tool for working with AZURE services, including AKS. For more information, see Installing, updating, and uninstalling the AZURE CLI
https://learn.microsoft.com/en-us/cli/azure/install-azure-cli#install in the AZURE Command Line Interface User Guide.

## Connect to cluster using kubectl

### [Azure CLI](#tab/azure-cli)

1. Configure `kubectl` to connect to your Kubernetes cluster using the [`az aks get-credentials`][az aks get-credentials] command. The following example gets credentials for the AKS cluster named _myAKSCluster_ in _myResourceGroup_.

   ```azurecli-interactive
   az aks get-credentials --resource-group myResourceGroup --name myAKSCluster
   ```

2. Verify connection to your cluster using the [`kubectl get nodes`][kubectl-get] command, which returns a list of cluster nodes.

   ```azurecli-interactive
   kubectl get nodes
   ```

   The following example output shows a list of the cluster nodes:

   ```output
   NAME                                STATUS   ROLES   AGE   VERSION
   aks-nodepool1-19366578-vmss000002   Ready    agent   47h   v1.25.6
   aks-nodepool1-19366578-vmss000003   Ready    agent   47h   v1.25.6
   ```

### [Azure PowerShell](#tab/azure-powershell)

1. Configure `kubectl` to connect to your Kubernetes cluster using the [`Import-AzAksCredential`][import-azakscredential] cmdlet. The following example gets credentials for the AKS cluster named _myAKSCluster_ in _myResourceGroup_.

   ```azurepowershell-interactive
   Import-AzAksCredential -ResourceGroupName myResourceGroup -Name myAKSCluster
   ```

2. Verify connection to your cluster using the [`kubectl get nodes`][kubectl-get] command, which returns a list of cluster nodes.

   ```azurepowershell-interactive
   kubectl get nodes
   ```

   The following example output shows a list of the cluster nodes:

   ```output
   NAME                                STATUS   ROLES   AGE   VERSION
   aks-nodepool1-19366578-vmss000002   Ready    agent   47h   v1.25.6
   aks-nodepool1-19366578-vmss000003   Ready    agent   47h   v1.25.6
   ```
