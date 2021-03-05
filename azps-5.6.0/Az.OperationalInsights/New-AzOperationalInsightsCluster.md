---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: c34bb862d3928e6dbbaa55a9660c4868e38941b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011790"
---
# <span data-ttu-id="e3583-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="e3583-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="e3583-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3583-102">SYNOPSIS</span></span>
<span data-ttu-id="e3583-103">Creare un cluster</span><span class="sxs-lookup"><span data-stu-id="e3583-103">Create cluster</span></span>

## <span data-ttu-id="e3583-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3583-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3583-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3583-105">DESCRIPTION</span></span>

<span data-ttu-id="e3583-106">Creare un cluster</span><span class="sxs-lookup"><span data-stu-id="e3583-106">Create cluster</span></span>

## <span data-ttu-id="e3583-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3583-107">EXAMPLES</span></span>

### <span data-ttu-id="e3583-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e3583-108">Example 1</span></span>
```powershell
New-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name} -Location eastus -IdentityType SystemAssigned -SkuName CapacityReservation -SkuCapacity 1000

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : ProvisioningAccount
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="e3583-109">Creare un cluster</span><span class="sxs-lookup"><span data-stu-id="e3583-109">Create cluster</span></span>

## <span data-ttu-id="e3583-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3583-110">PARAMETERS</span></span>

### <span data-ttu-id="e3583-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3583-111">-AsJob</span></span>
<span data-ttu-id="e3583-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e3583-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3583-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e3583-113">-ClusterName</span></span>
<span data-ttu-id="e3583-114">Nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="e3583-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3583-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3583-115">-DefaultProfile</span></span>
<span data-ttu-id="e3583-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3583-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3583-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e3583-117">-IdentityType</span></span>
<span data-ttu-id="e3583-118">il tipo di identità, il valore può essere 'SystemAssigned', 'None'.</span><span class="sxs-lookup"><span data-stu-id="e3583-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3583-119">-Location</span><span class="sxs-lookup"><span data-stu-id="e3583-119">-Location</span></span>
<span data-ttu-id="e3583-120">Area geografica in cui verrà distribuito il cluster.</span><span class="sxs-lookup"><span data-stu-id="e3583-120">The geographic region that the cluster will be deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3583-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3583-121">-ResourceGroupName</span></span>
<span data-ttu-id="e3583-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3583-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3583-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e3583-123">-SkuCapacity</span></span>
<span data-ttu-id="e3583-124">Capacità SKU, il valore deve essere multiplo di 100 e nell'intervallo 1000-2000.</span><span class="sxs-lookup"><span data-stu-id="e3583-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3583-125">-SKUName</span><span class="sxs-lookup"><span data-stu-id="e3583-125">-SkuName</span></span>
<span data-ttu-id="e3583-126">Nome SKU, ora può essere solo "CapacityReservation"</span><span class="sxs-lookup"><span data-stu-id="e3583-126">Sku Name, now can be 'CapacityReservation' only</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CapacityReservation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3583-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3583-127">-Tags</span></span>
<span data-ttu-id="e3583-128">Tag del cluster</span><span class="sxs-lookup"><span data-stu-id="e3583-128">Tags of the cluster</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3583-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3583-129">-Confirm</span></span>
<span data-ttu-id="e3583-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3583-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3583-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3583-131">-WhatIf</span></span>
<span data-ttu-id="e3583-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3583-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3583-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3583-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3583-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3583-134">CommonParameters</span></span>
<span data-ttu-id="e3583-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3583-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3583-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3583-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3583-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3583-137">INPUTS</span></span>

### <span data-ttu-id="e3583-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e3583-138">System.String</span></span>

## <span data-ttu-id="e3583-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3583-139">OUTPUTS</span></span>

### <span data-ttu-id="e3583-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="e3583-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="e3583-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3583-141">NOTES</span></span>

## <span data-ttu-id="e3583-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3583-142">RELATED LINKS</span></span>
