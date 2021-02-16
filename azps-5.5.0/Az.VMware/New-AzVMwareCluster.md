---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
ms.openlocfilehash: d654b2fa012a793ce48dff2cc5bfb9ade4f99d34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182543"
---
# <span data-ttu-id="27401-101">New-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="27401-101">New-AzVMwareCluster</span></span>

## <span data-ttu-id="27401-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27401-102">SYNOPSIS</span></span>
<span data-ttu-id="27401-103">Creare o aggiornare un cluster in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="27401-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="27401-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27401-104">SYNTAX</span></span>

```
New-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -SkuName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="27401-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="27401-105">DESCRIPTION</span></span>
<span data-ttu-id="27401-106">Creare o aggiornare un cluster in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="27401-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="27401-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27401-107">EXAMPLES</span></span>

### <span data-ttu-id="27401-108">Esempio 1: Creare un cluster</span><span class="sxs-lookup"><span data-stu-id="27401-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="27401-109">Creare un cluster</span><span class="sxs-lookup"><span data-stu-id="27401-109">Create cluster</span></span>

## <span data-ttu-id="27401-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27401-110">PARAMETERS</span></span>

### <span data-ttu-id="27401-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27401-111">-AsJob</span></span>
<span data-ttu-id="27401-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="27401-112">Run the command as a job</span></span>

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

### <span data-ttu-id="27401-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="27401-113">-ClusterSize</span></span>
<span data-ttu-id="27401-114">Le dimensioni del cluster</span><span class="sxs-lookup"><span data-stu-id="27401-114">The cluster size</span></span>

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

### <span data-ttu-id="27401-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27401-115">-DefaultProfile</span></span>
<span data-ttu-id="27401-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27401-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27401-117">-Name</span><span class="sxs-lookup"><span data-stu-id="27401-117">-Name</span></span>
<span data-ttu-id="27401-118">Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="27401-118">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27401-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="27401-119">-NoWait</span></span>
<span data-ttu-id="27401-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="27401-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="27401-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="27401-121">-PrivateCloudName</span></span>
<span data-ttu-id="27401-122">Nome del cloud privato.</span><span class="sxs-lookup"><span data-stu-id="27401-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="27401-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27401-123">-ResourceGroupName</span></span>
<span data-ttu-id="27401-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="27401-124">The name of the resource group.</span></span>
<span data-ttu-id="27401-125">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="27401-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="27401-126">-SKUName</span><span class="sxs-lookup"><span data-stu-id="27401-126">-SkuName</span></span>
<span data-ttu-id="27401-127">Nome dello SKU.</span><span class="sxs-lookup"><span data-stu-id="27401-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="27401-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27401-128">-SubscriptionId</span></span>
<span data-ttu-id="27401-129">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="27401-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27401-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27401-130">-Confirm</span></span>
<span data-ttu-id="27401-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27401-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27401-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27401-132">-WhatIf</span></span>
<span data-ttu-id="27401-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27401-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27401-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27401-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27401-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27401-135">CommonParameters</span></span>
<span data-ttu-id="27401-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27401-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27401-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="27401-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27401-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="27401-138">INPUTS</span></span>

## <span data-ttu-id="27401-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27401-139">OUTPUTS</span></span>

### <span data-ttu-id="27401-140">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="27401-140">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="27401-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="27401-141">NOTES</span></span>

<span data-ttu-id="27401-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="27401-142">ALIASES</span></span>

## <span data-ttu-id="27401-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27401-143">RELATED LINKS</span></span>

