---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188644"
---
# <span data-ttu-id="1607f-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="1607f-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="1607f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1607f-102">SYNOPSIS</span></span>
<span data-ttu-id="1607f-103">Creare un nuovo pool di nodi nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="1607f-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="1607f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1607f-104">SYNTAX</span></span>

### <span data-ttu-id="1607f-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="1607f-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1607f-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1607f-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1607f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1607f-107">DESCRIPTION</span></span>
<span data-ttu-id="1607f-108">Creare un nuovo pool di nodi nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="1607f-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="1607f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1607f-109">EXAMPLES</span></span>

### <span data-ttu-id="1607f-110">Creare un pool di nodi con parametri predefiniti</span><span class="sxs-lookup"><span data-stu-id="1607f-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="1607f-111">Creare un contenitore di Windows Server in un AKS</span><span class="sxs-lookup"><span data-stu-id="1607f-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="1607f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1607f-112">PARAMETERS</span></span>

### <span data-ttu-id="1607f-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="1607f-113">-ClusterName</span></span>
<span data-ttu-id="1607f-114">Nome della risorsa del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="1607f-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="1607f-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="1607f-115">-ClusterObject</span></span>
<span data-ttu-id="1607f-116">Specificare l'oggetto cluster in cui creare il pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="1607f-116">Specify cluster object in which to create node pool.</span></span>

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

### <span data-ttu-id="1607f-117">-Conteggio</span><span class="sxs-lookup"><span data-stu-id="1607f-117">-Count</span></span>
<span data-ttu-id="1607f-118">Numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="1607f-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="1607f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1607f-119">-DefaultProfile</span></span>
<span data-ttu-id="1607f-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1607f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1607f-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="1607f-121">-EnableAutoScaling</span></span>
<span data-ttu-id="1607f-122">Se abilitare il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="1607f-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="1607f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1607f-123">-Force</span></span>
<span data-ttu-id="1607f-124">Creare un pool di nodi anche se esiste già</span><span class="sxs-lookup"><span data-stu-id="1607f-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="1607f-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="1607f-125">-KubernetesVersion</span></span>
<span data-ttu-id="1607f-126">La versione di Kubernetes da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="1607f-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="1607f-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1607f-127">-MaxCount</span></span>
<span data-ttu-id="1607f-128">Numero massimo di nodi per il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="1607f-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="1607f-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="1607f-129">-MaxPodCount</span></span>
<span data-ttu-id="1607f-130">Numero massimo di pod che possono essere eseguiti nel nodo.</span><span class="sxs-lookup"><span data-stu-id="1607f-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="1607f-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="1607f-131">-MinCount</span></span>
<span data-ttu-id="1607f-132">Numero minimo di nodi per il ridimensionamento automatico.</span><span class="sxs-lookup"><span data-stu-id="1607f-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="1607f-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="1607f-133">-Name</span></span>
<span data-ttu-id="1607f-134">Nome del pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="1607f-134">The name of the node pool.</span></span>

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

### <span data-ttu-id="1607f-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="1607f-135">-OsDiskSize</span></span>
<span data-ttu-id="1607f-136">Numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="1607f-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="1607f-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="1607f-137">-OsType</span></span>
<span data-ttu-id="1607f-138">OsType da usare per specificare il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1607f-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="1607f-139">Scegliere tra Linux e Windows.</span><span class="sxs-lookup"><span data-stu-id="1607f-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="1607f-140">Impostazione predefinita per Linux.</span><span class="sxs-lookup"><span data-stu-id="1607f-140">Default to Linux.</span></span>

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

### <span data-ttu-id="1607f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1607f-141">-ResourceGroupName</span></span>
<span data-ttu-id="1607f-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1607f-142">The name of the resource group.</span></span>

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

### <span data-ttu-id="1607f-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="1607f-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="1607f-144">ScaleSetEvictionPolicy da usare per specificare i criteri di eliminazione per il set di scale della macchina virtuale con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="1607f-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="1607f-145">Impostazione predefinita per l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="1607f-145">Default to Delete.</span></span>

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

### <span data-ttu-id="1607f-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="1607f-146">-ScaleSetPriority</span></span>
<span data-ttu-id="1607f-147">ScaleSetPriority da usare per specificare la priorità impostata per la scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1607f-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="1607f-148">Impostazione predefinita su normale.</span><span class="sxs-lookup"><span data-stu-id="1607f-148">Default to regular.</span></span>

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

### <span data-ttu-id="1607f-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="1607f-149">-VmSetType</span></span>
<span data-ttu-id="1607f-150">Rappresenta i tipi di un pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="1607f-150">Represents types of an node pool.</span></span>
<span data-ttu-id="1607f-151">I valori possibili includono: "VirtualMachineScaleSets", "AvailabilitySet"</span><span class="sxs-lookup"><span data-stu-id="1607f-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="1607f-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="1607f-152">-VmSize</span></span>
<span data-ttu-id="1607f-153">Le dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1607f-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="1607f-154">Il valore predefinito è Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="1607f-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="1607f-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="1607f-155">-VnetSubnetID</span></span>
<span data-ttu-id="1607f-156">VNet SubnetID specifica l'identificatore di subnet di VNet.</span><span class="sxs-lookup"><span data-stu-id="1607f-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="1607f-157">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1607f-157">-Confirm</span></span>
<span data-ttu-id="1607f-158">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1607f-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1607f-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1607f-159">-WhatIf</span></span>
<span data-ttu-id="1607f-160">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1607f-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1607f-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1607f-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1607f-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1607f-162">CommonParameters</span></span>
<span data-ttu-id="1607f-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1607f-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1607f-164">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1607f-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1607f-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1607f-165">INPUTS</span></span>

### <span data-ttu-id="1607f-166">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="1607f-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="1607f-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1607f-167">OUTPUTS</span></span>

### <span data-ttu-id="1607f-168">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="1607f-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="1607f-169">Note</span><span class="sxs-lookup"><span data-stu-id="1607f-169">NOTES</span></span>

## <span data-ttu-id="1607f-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1607f-170">RELATED LINKS</span></span>
