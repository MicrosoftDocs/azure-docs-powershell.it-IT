---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199839"
---
# <span data-ttu-id="27c99-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="27c99-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="27c99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27c99-102">SYNOPSIS</span></span>
<span data-ttu-id="27c99-103">Creare un nuovo pool di nodi nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="27c99-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="27c99-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27c99-104">SYNTAX</span></span>

### <span data-ttu-id="27c99-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="27c99-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27c99-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27c99-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27c99-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="27c99-107">DESCRIPTION</span></span>
<span data-ttu-id="27c99-108">Creare un nuovo pool di nodi nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="27c99-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="27c99-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27c99-109">EXAMPLES</span></span>

### <span data-ttu-id="27c99-110">Creare un pool di nodi con parametri predefiniti</span><span class="sxs-lookup"><span data-stu-id="27c99-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="27c99-111">Creare un contenitore di Windows Server in un AKS</span><span class="sxs-lookup"><span data-stu-id="27c99-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="27c99-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27c99-112">PARAMETERS</span></span>

### <span data-ttu-id="27c99-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="27c99-113">-ClusterName</span></span>
<span data-ttu-id="27c99-114">Nome della risorsa cluster gestita.</span><span class="sxs-lookup"><span data-stu-id="27c99-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="27c99-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="27c99-115">-ClusterObject</span></span>
<span data-ttu-id="27c99-116">Specificare l'oggetto cluster in cui creare il pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="27c99-116">Specify cluster object in which to create node pool.</span></span>

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

### <span data-ttu-id="27c99-117">-Count</span><span class="sxs-lookup"><span data-stu-id="27c99-117">-Count</span></span>
<span data-ttu-id="27c99-118">Il numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="27c99-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="27c99-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27c99-119">-DefaultProfile</span></span>
<span data-ttu-id="27c99-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27c99-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27c99-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="27c99-121">-EnableAutoScaling</span></span>
<span data-ttu-id="27c99-122">Se abilitare o meno la scalabilità automatica</span><span class="sxs-lookup"><span data-stu-id="27c99-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="27c99-123">-Force</span><span class="sxs-lookup"><span data-stu-id="27c99-123">-Force</span></span>
<span data-ttu-id="27c99-124">Creare un pool di nodi anche se esiste già</span><span class="sxs-lookup"><span data-stu-id="27c99-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="27c99-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="27c99-125">-KubernetesVersion</span></span>
<span data-ttu-id="27c99-126">La versione di Kubernetes da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="27c99-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="27c99-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="27c99-127">-MaxCount</span></span>
<span data-ttu-id="27c99-128">Numero massimo di nodi per il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="27c99-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="27c99-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="27c99-129">-MaxPodCount</span></span>
<span data-ttu-id="27c99-130">Numero massimo di pod che possono essere eseguiti nel nodo.</span><span class="sxs-lookup"><span data-stu-id="27c99-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="27c99-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="27c99-131">-MinCount</span></span>
<span data-ttu-id="27c99-132">Numero minimo di nodi per il ridimensionamento automatico.</span><span class="sxs-lookup"><span data-stu-id="27c99-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="27c99-133">-Name</span><span class="sxs-lookup"><span data-stu-id="27c99-133">-Name</span></span>
<span data-ttu-id="27c99-134">Nome del pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="27c99-134">The name of the node pool.</span></span>

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

### <span data-ttu-id="27c99-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="27c99-135">-OsDiskSize</span></span>
<span data-ttu-id="27c99-136">Il numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="27c99-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="27c99-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="27c99-137">-OsType</span></span>
<span data-ttu-id="27c99-138">OsType da usare per specificare il tipo di carattere os.</span><span class="sxs-lookup"><span data-stu-id="27c99-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="27c99-139">Scegli tra Linux e Windows.</span><span class="sxs-lookup"><span data-stu-id="27c99-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="27c99-140">Per impostazione predefinita, Linux.</span><span class="sxs-lookup"><span data-stu-id="27c99-140">Default to Linux.</span></span>

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

### <span data-ttu-id="27c99-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27c99-141">-ResourceGroupName</span></span>
<span data-ttu-id="27c99-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="27c99-142">The name of the resource group.</span></span>

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

### <span data-ttu-id="27c99-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="27c99-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="27c99-144">ScaleSetEvictionPolicy da usare per specificare i criteri di spostazione per il set di scalabilità delle macchine virtuali con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="27c99-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="27c99-145">L'impostazione predefinita è Elimina.</span><span class="sxs-lookup"><span data-stu-id="27c99-145">Default to Delete.</span></span>

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

### <span data-ttu-id="27c99-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="27c99-146">-ScaleSetPriority</span></span>
<span data-ttu-id="27c99-147">ScaleSetPriority da usare per specificare la priorità del set di scalabilità delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="27c99-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="27c99-148">L'impostazione predefinita è normale.</span><span class="sxs-lookup"><span data-stu-id="27c99-148">Default to regular.</span></span>

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

### <span data-ttu-id="27c99-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="27c99-149">-VmSetType</span></span>
<span data-ttu-id="27c99-150">Rappresenta i tipi di un pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="27c99-150">Represents types of an node pool.</span></span>
<span data-ttu-id="27c99-151">I valori possibili includono: 'VirtualMachineScaleSets', 'AvailabilitySet'</span><span class="sxs-lookup"><span data-stu-id="27c99-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="27c99-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="27c99-152">-VmSize</span></span>
<span data-ttu-id="27c99-153">Dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="27c99-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="27c99-154">Il valore predefinito è Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="27c99-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="27c99-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="27c99-155">-VnetSubnetID</span></span>
<span data-ttu-id="27c99-156">SubnetID VNet specifica l'identificatore di subnet della VNet.</span><span class="sxs-lookup"><span data-stu-id="27c99-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="27c99-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27c99-157">-Confirm</span></span>
<span data-ttu-id="27c99-158">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27c99-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27c99-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27c99-159">-WhatIf</span></span>
<span data-ttu-id="27c99-160">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27c99-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27c99-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27c99-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27c99-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c99-162">CommonParameters</span></span>
<span data-ttu-id="27c99-163">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27c99-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c99-164">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="27c99-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c99-165">INPUT</span><span class="sxs-lookup"><span data-stu-id="27c99-165">INPUTS</span></span>

### <span data-ttu-id="27c99-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="27c99-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="27c99-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27c99-167">OUTPUTS</span></span>

### <span data-ttu-id="27c99-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="27c99-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="27c99-169">NOTE</span><span class="sxs-lookup"><span data-stu-id="27c99-169">NOTES</span></span>

## <span data-ttu-id="27c99-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27c99-170">RELATED LINKS</span></span>
