---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: f7a3479fb7fd70c47d5d4d3b80004cb25d9baa0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188653"
---
# <span data-ttu-id="90846-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="90846-101">New-AzAksCluster</span></span>

## <span data-ttu-id="90846-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90846-102">SYNOPSIS</span></span>
<span data-ttu-id="90846-103">Creare un nuovo cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="90846-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="90846-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90846-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeOsType <String>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
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

## <span data-ttu-id="90846-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90846-105">DESCRIPTION</span></span>

<span data-ttu-id="90846-106">Creare un nuovo cluster AKS (Azure Kubernetes Service).</span><span class="sxs-lookup"><span data-stu-id="90846-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="90846-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90846-107">EXAMPLES</span></span>

### <span data-ttu-id="90846-108">Nuovo AK con params predefiniti.</span><span class="sxs-lookup"><span data-stu-id="90846-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="90846-109">Creare un contenitore di Windows Server in un AKS.</span><span class="sxs-lookup"><span data-stu-id="90846-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="90846-110">Per creare un contenitore Windows Server in un AKS, devi specificare almeno quattro parametri seguenti durante la creazione di AKS e il valore per `NetworkPlugin` e `NodeVmSetType` deve essere `azure` e `VirtualMachineScaleSets` rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="90846-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword *** -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="90846-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90846-111">PARAMETERS</span></span>

### <span data-ttu-id="90846-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="90846-112">-AcrNameToAttach</span></span>
<span data-ttu-id="90846-113">Concedere il ruolo "acrpull" dell'ACR specificato all'entità servizio AKS, ad esempio myacr</span><span class="sxs-lookup"><span data-stu-id="90846-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="90846-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="90846-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="90846-115">Nomi dei componenti aggiuntivi da abilitare quando viene creato il cluster.</span><span class="sxs-lookup"><span data-stu-id="90846-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="90846-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90846-116">-AsJob</span></span>
<span data-ttu-id="90846-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="90846-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90846-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90846-118">-DefaultProfile</span></span>
<span data-ttu-id="90846-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="90846-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90846-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="90846-120">-DnsNamePrefix</span></span>
<span data-ttu-id="90846-121">Prefisso del nome DNS per il cluster.</span><span class="sxs-lookup"><span data-stu-id="90846-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="90846-122">La lunghezza deve essere <= 9 se gli utenti intendono aggiungere un contenitore Windows.</span><span class="sxs-lookup"><span data-stu-id="90846-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="90846-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="90846-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="90846-124">Se abilitare il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="90846-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="90846-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="90846-125">-EnableRbac</span></span>
<span data-ttu-id="90846-126">Se abilitare l'accesso a Kubernetes Role-Based</span><span class="sxs-lookup"><span data-stu-id="90846-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="90846-127">-Force</span><span class="sxs-lookup"><span data-stu-id="90846-127">-Force</span></span>
<span data-ttu-id="90846-128">Creare un cluster anche se esiste già</span><span class="sxs-lookup"><span data-stu-id="90846-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="90846-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="90846-129">-GenerateSshKey</span></span>
<span data-ttu-id="90846-130">Genera file di chiave SSH in {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="90846-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="90846-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="90846-131">-KubernetesVersion</span></span>
<span data-ttu-id="90846-132">La versione di Kubernetes da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="90846-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="90846-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="90846-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="90846-134">Nome utente per le macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="90846-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="90846-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="90846-135">-LoadBalancerSku</span></span>
<span data-ttu-id="90846-136">SKU di bilanciamento del carico per il cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="90846-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="90846-137">-Posizione</span><span class="sxs-lookup"><span data-stu-id="90846-137">-Location</span></span>
<span data-ttu-id="90846-138">Posizione di Azure per il cluster.</span><span class="sxs-lookup"><span data-stu-id="90846-138">Azure location for the cluster.</span></span>
<span data-ttu-id="90846-139">Il valore predefinito è la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="90846-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="90846-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="90846-140">-Name</span></span>
<span data-ttu-id="90846-141">Nome del cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="90846-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="90846-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="90846-142">-NetworkPlugin</span></span>
<span data-ttu-id="90846-143">Plug-in di rete usato per la creazione di rete Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="90846-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="90846-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="90846-144">-NodeCount</span></span>
<span data-ttu-id="90846-145">Numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="90846-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="90846-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="90846-146">-NodeMaxCount</span></span>
<span data-ttu-id="90846-147">Numero massimo di nodi per il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="90846-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="90846-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="90846-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="90846-149">Numero massimo di pod che possono essere eseguiti nel nodo.</span><span class="sxs-lookup"><span data-stu-id="90846-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="90846-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="90846-150">-NodeMinCount</span></span>
<span data-ttu-id="90846-151">Numero minimo di nodi per il ridimensionamento automatico.</span><span class="sxs-lookup"><span data-stu-id="90846-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="90846-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="90846-152">-NodeName</span></span>
<span data-ttu-id="90846-153">Nome univoco del profilo del pool di agenti nel contesto del gruppo sottoscrizioni e risorse.</span><span class="sxs-lookup"><span data-stu-id="90846-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="90846-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="90846-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="90846-155">Dimensioni in GB del disco del sistema operativo per ogni nodo nel pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="90846-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="90846-156">Minimo 30 GB.</span><span class="sxs-lookup"><span data-stu-id="90846-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="90846-157">-NodeOsType</span><span class="sxs-lookup"><span data-stu-id="90846-157">-NodeOsType</span></span>
<span data-ttu-id="90846-158">OsType da usare per specificare il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="90846-158">OsType to be used to specify os type.</span></span> <span data-ttu-id="90846-159">Scegliere tra Linux e Windows.</span><span class="sxs-lookup"><span data-stu-id="90846-159">Choose from Linux and Windows.</span></span> <span data-ttu-id="90846-160">Impostazione predefinita per Linux.</span><span class="sxs-lookup"><span data-stu-id="90846-160">Default to Linux.</span></span>

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

### <span data-ttu-id="90846-161">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="90846-161">-NodePoolMode</span></span>
<span data-ttu-id="90846-162">NodePoolMode rappresenta la modalità di un pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="90846-162">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="90846-163">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="90846-163">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="90846-164">ScaleSetEvictionPolicy da usare per specificare i criteri di eliminazione per il set di scale della macchina virtuale con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="90846-164">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="90846-165">Impostazione predefinita per l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="90846-165">Default to Delete.</span></span>

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

### <span data-ttu-id="90846-166">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="90846-166">-NodeSetPriority</span></span>
<span data-ttu-id="90846-167">ScaleSetPriority da usare per specificare la priorità impostata per la scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="90846-167">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="90846-168">Impostazione predefinita su normale.</span><span class="sxs-lookup"><span data-stu-id="90846-168">Default to regular.</span></span>

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

### <span data-ttu-id="90846-169">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="90846-169">-NodeVmSetType</span></span>
<span data-ttu-id="90846-170">AgentPoolType rappresenta i tipi di un pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="90846-170">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="90846-171">I valori possibili includono: "VirtualMachineScaleSets", "AvailabilitySet"</span><span class="sxs-lookup"><span data-stu-id="90846-171">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="90846-172">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="90846-172">-NodeVmSize</span></span>
<span data-ttu-id="90846-173">Le dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="90846-173">The size of the Virtual Machine.</span></span> <span data-ttu-id="90846-174">Il valore predefinito è Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="90846-174">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="90846-175">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="90846-175">-NodeVnetSubnetID</span></span>
<span data-ttu-id="90846-176">VNet SubnetID specifica l'identificatore di subnet di VNet.</span><span class="sxs-lookup"><span data-stu-id="90846-176">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="90846-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90846-177">-ResourceGroupName</span></span>
<span data-ttu-id="90846-178">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="90846-178">Resource Group Name.</span></span>

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

### <span data-ttu-id="90846-179">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="90846-179">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="90846-180">ID client e segreto client associato all'entità dell'applicazione/servizio AAD.</span><span class="sxs-lookup"><span data-stu-id="90846-180">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClientIdAndSecret

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90846-181">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="90846-181">-SshKeyValue</span></span>
<span data-ttu-id="90846-182">Valore del file di chiave SSH o percorso file chiave.</span><span class="sxs-lookup"><span data-stu-id="90846-182">SSH key file value or key file path.</span></span>
<span data-ttu-id="90846-183">Il valore predefinito è {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="90846-183">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="90846-184">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="90846-184">-SubnetName</span></span>
<span data-ttu-id="90846-185">Nome subnet di VirtualNode addon.</span><span class="sxs-lookup"><span data-stu-id="90846-185">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="90846-186">-Tag</span><span class="sxs-lookup"><span data-stu-id="90846-186">-Tag</span></span>
<span data-ttu-id="90846-187">Tag da applicare alla risorsa</span><span class="sxs-lookup"><span data-stu-id="90846-187">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="90846-188">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="90846-188">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="90846-189">Il nome utente dell'amministratore da usare per le VM di Windows.</span><span class="sxs-lookup"><span data-stu-id="90846-189">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="90846-190">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="90846-190">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="90846-191">La password di amministratore da usare per le VM di Windows, la cui lunghezza deve essere di almeno 12, che contiene almeno un carattere maiuscolo inferiore, vale a dire `[a-z]` uno `[A-Z]` e uno speciale `[!@#$%^&*()]` .</span><span class="sxs-lookup"><span data-stu-id="90846-191">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&*()]`.</span></span>

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

### <span data-ttu-id="90846-192">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="90846-192">-WorkspaceResourceId</span></span>
<span data-ttu-id="90846-193">ID risorsa dell'area di lavoro di monitoraggio addon.</span><span class="sxs-lookup"><span data-stu-id="90846-193">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="90846-194">-Confermare</span><span class="sxs-lookup"><span data-stu-id="90846-194">-Confirm</span></span>
<span data-ttu-id="90846-195">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90846-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90846-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90846-196">-WhatIf</span></span>
<span data-ttu-id="90846-197">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90846-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90846-198">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90846-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90846-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90846-199">CommonParameters</span></span>
<span data-ttu-id="90846-200">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90846-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90846-201">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90846-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90846-202">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90846-202">INPUTS</span></span>

### <span data-ttu-id="90846-203">Nessuno</span><span class="sxs-lookup"><span data-stu-id="90846-203">None</span></span>

## <span data-ttu-id="90846-204">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90846-204">OUTPUTS</span></span>

### <span data-ttu-id="90846-205">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="90846-205">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="90846-206">Note</span><span class="sxs-lookup"><span data-stu-id="90846-206">NOTES</span></span>

## <span data-ttu-id="90846-207">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90846-207">RELATED LINKS</span></span>
