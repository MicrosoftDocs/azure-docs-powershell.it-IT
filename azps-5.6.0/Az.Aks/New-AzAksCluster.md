---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: 806c3a17dcfc470e01801548013d0d8c6ea58ae4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008158"
---
# <span data-ttu-id="e94b8-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="e94b8-101">New-AzAksCluster</span></span>

## <span data-ttu-id="e94b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e94b8-102">SYNOPSIS</span></span>
<span data-ttu-id="e94b8-103">Creare un nuovo cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="e94b8-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e94b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e94b8-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
 [-NodeScaleSetEvictionPolicy <String>] [-AddOnNameToBeEnabled <String[]>] [-WorkspaceResourceId <String>]
 [-SubnetName <String>] [-AcrNameToAttach <String>] [-EnableRbac] [-WindowsProfileAdminUserName <String>]
 [-WindowsProfileAdminUserPassword <SecureString>] [-NetworkPlugin <String>] [-LoadBalancerSku <String>]
 [-ResourceGroupName] <String> [-Name] <String> [[-ServicePrincipalIdAndSecret] <PSCredential>]
 [-Location <String>] [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>]
 [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e94b8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e94b8-105">DESCRIPTION</span></span>

<span data-ttu-id="e94b8-106">Creare un nuovo cluster del servizio Azure Kubernetes (AKS).</span><span class="sxs-lookup"><span data-stu-id="e94b8-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="e94b8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e94b8-107">EXAMPLES</span></span>

### <span data-ttu-id="e94b8-108">Nuovo AKS con parametri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="e94b8-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="e94b8-109">Creare il contenitore di Windows Server in un AKS.</span><span class="sxs-lookup"><span data-stu-id="e94b8-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="e94b8-110">Per creare il contenitore di Windows Server in un AKS, è necessario specificare almeno quattro parametri seguenti quando si creano gli AKS e il valore per e deve essere `NetworkPlugin` `NodeVmSetType` e `azure` `VirtualMachineScaleSets` rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="e94b8-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword *** -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="e94b8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e94b8-111">PARAMETERS</span></span>

### <span data-ttu-id="e94b8-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="e94b8-112">-AcrNameToAttach</span></span>
<span data-ttu-id="e94b8-113">Assegnare il ruolo di "acrpull" dell'ACR specificato all'entità servizio AKS, ad esempio myacr</span><span class="sxs-lookup"><span data-stu-id="e94b8-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="e94b8-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="e94b8-115">Nomi dei componenti aggiuntivi da abilitato durante la creazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="e94b8-115">Add-on names to be enabled when cluster is created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e94b8-116">-AsJob</span></span>
<span data-ttu-id="e94b8-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e94b8-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e94b8-118">-DefaultProfile</span></span>
<span data-ttu-id="e94b8-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e94b8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="e94b8-120">-DnsNamePrefix</span></span>
<span data-ttu-id="e94b8-121">Prefisso del nome DNS per il cluster.</span><span class="sxs-lookup"><span data-stu-id="e94b8-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="e94b8-122">La lunghezza deve essere <= 9 se gli utenti prevede di aggiungere il contenitore di finestre.</span><span class="sxs-lookup"><span data-stu-id="e94b8-122">The length must be <= 9 if users plan to add windows container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="e94b8-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="e94b8-124">Se abilitare o meno la scalabilità automatica</span><span class="sxs-lookup"><span data-stu-id="e94b8-124">Whether to enable auto-scaler</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="e94b8-125">-EnableRbac</span></span>
<span data-ttu-id="e94b8-126">Se abilitare Kubernetes Role-Based Access</span><span class="sxs-lookup"><span data-stu-id="e94b8-126">Whether to enable Kubernetes Role-Based Access</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-127">-Force</span><span class="sxs-lookup"><span data-stu-id="e94b8-127">-Force</span></span>
<span data-ttu-id="e94b8-128">Creare un cluster anche se esiste già</span><span class="sxs-lookup"><span data-stu-id="e94b8-128">Create cluster even if it already exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="e94b8-129">-GenerateSshKey</span></span>
<span data-ttu-id="e94b8-130">Genera il file di chiave SSH in {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="e94b8-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="e94b8-131">-KubernetesVersion</span></span>
<span data-ttu-id="e94b8-132">La versione di Kubernetes da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="e94b8-132">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="e94b8-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="e94b8-134">Nome utente per le Macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="e94b8-134">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AdminUserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="e94b8-135">-LoadBalancerSku</span></span>
<span data-ttu-id="e94b8-136">SKU di bilanciamento del carico per il cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="e94b8-136">The load balancer sku for the managed cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-137">-Location</span><span class="sxs-lookup"><span data-stu-id="e94b8-137">-Location</span></span>
<span data-ttu-id="e94b8-138">Posizione di Azure per il cluster.</span><span class="sxs-lookup"><span data-stu-id="e94b8-138">Azure location for the cluster.</span></span>
<span data-ttu-id="e94b8-139">Per impostazione predefinita, viene specificata la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e94b8-139">Defaults to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-140">-Name</span><span class="sxs-lookup"><span data-stu-id="e94b8-140">-Name</span></span>
<span data-ttu-id="e94b8-141">Nome cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e94b8-141">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="e94b8-142">-NetworkPlugin</span></span>
<span data-ttu-id="e94b8-143">Plug-in di rete usato per la creazione della rete Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e94b8-143">Network plugin used for building Kubernetes network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: azure
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="e94b8-144">-NodeCount</span></span>
<span data-ttu-id="e94b8-145">Il numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="e94b8-145">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="e94b8-146">-NodeMaxCount</span></span>
<span data-ttu-id="e94b8-147">Numero massimo di nodi per il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="e94b8-147">Maximum number of nodes for auto-scaling</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="e94b8-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="e94b8-149">Numero massimo di pod che possono essere eseguiti nel nodo.</span><span class="sxs-lookup"><span data-stu-id="e94b8-149">Maximum number of pods that can run on node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="e94b8-150">-NodeMinCount</span></span>
<span data-ttu-id="e94b8-151">Numero minimo di nodi per il ridimensionamento automatico.</span><span class="sxs-lookup"><span data-stu-id="e94b8-151">Minimum number of nodes for auto-scaling.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="e94b8-152">-NodeName</span></span>
<span data-ttu-id="e94b8-153">Nome univoco del profilo del pool di agenti nel contesto della sottoscrizione e del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e94b8-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="e94b8-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="e94b8-155">Dimensioni in GB del disco del sistema operativo per ogni nodo nel pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="e94b8-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="e94b8-156">Minimo 30 GB.</span><span class="sxs-lookup"><span data-stu-id="e94b8-156">Minimum 30 GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="e94b8-157">-NodePoolMode</span></span>
<span data-ttu-id="e94b8-158">NodePoolMode rappresenta la modalità di un pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="e94b8-158">NodePoolMode represents mode of an node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="e94b8-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="e94b8-160">ScaleSetEvictionPolicy da usare per specificare i criteri di spostazione per il set di scalabilità delle macchine virtuali con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="e94b8-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="e94b8-161">L'impostazione predefinita è Elimina.</span><span class="sxs-lookup"><span data-stu-id="e94b8-161">Default to Delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="e94b8-162">-NodeSetPriority</span></span>
<span data-ttu-id="e94b8-163">ScaleSetPriority da usare per specificare la priorità del set di scalabilità delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="e94b8-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="e94b8-164">L'impostazione predefinita è normale.</span><span class="sxs-lookup"><span data-stu-id="e94b8-164">Default to regular.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="e94b8-165">-NodeVmSetType</span></span>
<span data-ttu-id="e94b8-166">AgentPoolType rappresenta i tipi di un pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="e94b8-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="e94b8-167">I valori possibili includono: 'VirtualMachineScaleSets', 'AvailabilitySet'</span><span class="sxs-lookup"><span data-stu-id="e94b8-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: VirtualMachineScaleSets
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="e94b8-168">-NodeVmSize</span></span>
<span data-ttu-id="e94b8-169">Dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e94b8-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="e94b8-170">Il valore predefinito è Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="e94b8-170">Default value is Standard_D2_v2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="e94b8-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="e94b8-172">SubnetID VNet specifica l'identificatore di subnet della VNet.</span><span class="sxs-lookup"><span data-stu-id="e94b8-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e94b8-173">-ResourceGroupName</span></span>
<span data-ttu-id="e94b8-174">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e94b8-174">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="e94b8-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="e94b8-176">ID client e segreto client associati all'applicazione AAD o all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="e94b8-176">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="e94b8-177">-SshKeyValue</span></span>
<span data-ttu-id="e94b8-178">Valore del file di chiave SSH o percorso del file di chiave.</span><span class="sxs-lookup"><span data-stu-id="e94b8-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="e94b8-179">L'impostazione predefinita è {HOME}/.ssh/id_rsa.pub.</span><span class="sxs-lookup"><span data-stu-id="e94b8-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e94b8-180">-SubnetName</span></span>
<span data-ttu-id="e94b8-181">Nome subnet del componente aggiuntivo VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="e94b8-181">Subnet name of VirtualNode addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="e94b8-182">-Tag</span></span>
<span data-ttu-id="e94b8-183">Tag da applicare alla risorsa</span><span class="sxs-lookup"><span data-stu-id="e94b8-183">Tags to be applied to the resource</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="e94b8-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="e94b8-185">Nome utente dell'amministratore da usare per le macchine virtuali di Windows.</span><span class="sxs-lookup"><span data-stu-id="e94b8-185">The administrator username to use for Windows VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="e94b8-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="e94b8-187">La password dell'amministratore da usare per le macchine virtuali Windows deve contenere almeno 12 caratteri minuscoli, ad esempio uno e un `[a-z]` `[A-Z]` carattere `[!@#$%^&*()]` speciale.</span><span class="sxs-lookup"><span data-stu-id="e94b8-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&*()]`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="e94b8-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="e94b8-189">ID risorsa dell'area di lavoro del componente aggiuntivo Monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="e94b8-189">Resource Id of the workspace of Monitoring addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e94b8-190">-Confirm</span></span>
<span data-ttu-id="e94b8-191">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e94b8-191">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e94b8-192">-WhatIf</span></span>
<span data-ttu-id="e94b8-193">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e94b8-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e94b8-194">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e94b8-194">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94b8-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e94b8-195">CommonParameters</span></span>
<span data-ttu-id="e94b8-196">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e94b8-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e94b8-197">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e94b8-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e94b8-198">INPUT</span><span class="sxs-lookup"><span data-stu-id="e94b8-198">INPUTS</span></span>

### <span data-ttu-id="e94b8-199">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e94b8-199">None</span></span>

## <span data-ttu-id="e94b8-200">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e94b8-200">OUTPUTS</span></span>

### <span data-ttu-id="e94b8-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="e94b8-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="e94b8-202">NOTE</span><span class="sxs-lookup"><span data-stu-id="e94b8-202">NOTES</span></span>

## <span data-ttu-id="e94b8-203">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e94b8-203">RELATED LINKS</span></span>
