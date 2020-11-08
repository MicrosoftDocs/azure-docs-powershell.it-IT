---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200574"
---
# <span data-ttu-id="57025-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="57025-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="57025-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57025-102">SYNOPSIS</span></span>
<span data-ttu-id="57025-103">Creare un nuovo pool di nodi nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="57025-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="57025-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57025-104">SYNTAX</span></span>

### <span data-ttu-id="57025-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="57025-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57025-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57025-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57025-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57025-107">DESCRIPTION</span></span>
<span data-ttu-id="57025-108">Creare un nuovo pool di nodi nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="57025-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="57025-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57025-109">EXAMPLES</span></span>

### <span data-ttu-id="57025-110">Creare un pool di nodi con parametri predefiniti</span><span class="sxs-lookup"><span data-stu-id="57025-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="57025-111">Creare un contenitore di Windows Server in un AKS</span><span class="sxs-lookup"><span data-stu-id="57025-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="57025-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57025-112">PARAMETERS</span></span>

### <span data-ttu-id="57025-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="57025-113">-ClusterName</span></span>
<span data-ttu-id="57025-114">Nome della risorsa del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="57025-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57025-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="57025-115">-ClusterObject</span></span>
<span data-ttu-id="57025-116">Specificare l'oggetto cluster in cui creare il pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="57025-116">Specify cluster object in which to create node pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57025-117">-Conteggio</span><span class="sxs-lookup"><span data-stu-id="57025-117">-Count</span></span>
<span data-ttu-id="57025-118">Numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="57025-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="57025-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57025-119">-DefaultProfile</span></span>
<span data-ttu-id="57025-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57025-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57025-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="57025-121">-EnableAutoScaling</span></span>
<span data-ttu-id="57025-122">Se abilitare il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="57025-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="57025-123">-Force</span><span class="sxs-lookup"><span data-stu-id="57025-123">-Force</span></span>
<span data-ttu-id="57025-124">Creare un pool di nodi anche se esiste già</span><span class="sxs-lookup"><span data-stu-id="57025-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="57025-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="57025-125">-KubernetesVersion</span></span>
<span data-ttu-id="57025-126">La versione di Kubernetes da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="57025-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="57025-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="57025-127">-MaxCount</span></span>
<span data-ttu-id="57025-128">Numero massimo di nodi per il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="57025-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="57025-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="57025-129">-MaxPodCount</span></span>
<span data-ttu-id="57025-130">Numero massimo di pod che possono essere eseguiti nel nodo.</span><span class="sxs-lookup"><span data-stu-id="57025-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="57025-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="57025-131">-MinCount</span></span>
<span data-ttu-id="57025-132">Numero minimo di nodi per il ridimensionamento automatico.</span><span class="sxs-lookup"><span data-stu-id="57025-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="57025-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="57025-133">-Name</span></span>
<span data-ttu-id="57025-134">Nome del pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="57025-134">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57025-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="57025-135">-OsDiskSize</span></span>
<span data-ttu-id="57025-136">Numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="57025-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="57025-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="57025-137">-OsType</span></span>
<span data-ttu-id="57025-138">OsType da usare per specificare il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="57025-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="57025-139">Scegliere tra Linux e Windows.</span><span class="sxs-lookup"><span data-stu-id="57025-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="57025-140">Impostazione predefinita per Linux.</span><span class="sxs-lookup"><span data-stu-id="57025-140">Default to Linux.</span></span>

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

### <span data-ttu-id="57025-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57025-141">-ResourceGroupName</span></span>
<span data-ttu-id="57025-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="57025-142">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57025-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="57025-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="57025-144">ScaleSetEvictionPolicy da usare per specificare i criteri di eliminazione per il set di scale della macchina virtuale con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="57025-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="57025-145">Impostazione predefinita per l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="57025-145">Default to Delete.</span></span>

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

### <span data-ttu-id="57025-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="57025-146">-ScaleSetPriority</span></span>
<span data-ttu-id="57025-147">ScaleSetPriority da usare per specificare la priorità impostata per la scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="57025-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="57025-148">Impostazione predefinita su normale.</span><span class="sxs-lookup"><span data-stu-id="57025-148">Default to regular.</span></span>

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

### <span data-ttu-id="57025-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="57025-149">-VmSetType</span></span>
<span data-ttu-id="57025-150">Rappresenta i tipi di un pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="57025-150">Represents types of an node pool.</span></span>
<span data-ttu-id="57025-151">I valori possibili includono: "VirtualMachineScaleSets", "AvailabilitySet"</span><span class="sxs-lookup"><span data-stu-id="57025-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="57025-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="57025-152">-VmSize</span></span>
<span data-ttu-id="57025-153">Le dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="57025-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="57025-154">Il valore predefinito è Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="57025-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="57025-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="57025-155">-VnetSubnetID</span></span>
<span data-ttu-id="57025-156">VNet SubnetID specifica l'identificatore di subnet di VNet.</span><span class="sxs-lookup"><span data-stu-id="57025-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="57025-157">-Confermare</span><span class="sxs-lookup"><span data-stu-id="57025-157">-Confirm</span></span>
<span data-ttu-id="57025-158">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57025-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57025-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57025-159">-WhatIf</span></span>
<span data-ttu-id="57025-160">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57025-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57025-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57025-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57025-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57025-162">CommonParameters</span></span>
<span data-ttu-id="57025-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57025-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57025-164">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57025-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57025-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57025-165">INPUTS</span></span>

### <span data-ttu-id="57025-166">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="57025-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="57025-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57025-167">OUTPUTS</span></span>

### <span data-ttu-id="57025-168">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="57025-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="57025-169">Note</span><span class="sxs-lookup"><span data-stu-id="57025-169">NOTES</span></span>

## <span data-ttu-id="57025-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57025-170">RELATED LINKS</span></span>