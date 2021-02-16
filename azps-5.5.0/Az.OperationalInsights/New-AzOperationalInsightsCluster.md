---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: 078140a16a84089e5672fe160999d7db8577f7fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186783"
---
# <span data-ttu-id="76c97-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="76c97-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="76c97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76c97-102">SYNOPSIS</span></span>
<span data-ttu-id="76c97-103">Creare un cluster</span><span class="sxs-lookup"><span data-stu-id="76c97-103">Create cluster</span></span>

## <span data-ttu-id="76c97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76c97-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76c97-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="76c97-105">DESCRIPTION</span></span>

<span data-ttu-id="76c97-106">Creare un cluster</span><span class="sxs-lookup"><span data-stu-id="76c97-106">Create cluster</span></span>

## <span data-ttu-id="76c97-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76c97-107">EXAMPLES</span></span>

### <span data-ttu-id="76c97-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="76c97-108">Example 1</span></span>
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

<span data-ttu-id="76c97-109">Creare un cluster</span><span class="sxs-lookup"><span data-stu-id="76c97-109">Create cluster</span></span>

## <span data-ttu-id="76c97-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76c97-110">PARAMETERS</span></span>

### <span data-ttu-id="76c97-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76c97-111">-AsJob</span></span>
<span data-ttu-id="76c97-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="76c97-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76c97-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="76c97-113">-ClusterName</span></span>
<span data-ttu-id="76c97-114">Nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="76c97-114">The cluster name.</span></span>

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

### <span data-ttu-id="76c97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c97-115">-DefaultProfile</span></span>
<span data-ttu-id="76c97-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76c97-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76c97-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="76c97-117">-IdentityType</span></span>
<span data-ttu-id="76c97-118">il tipo di identità, il valore può essere 'SystemAssigned', 'None'.</span><span class="sxs-lookup"><span data-stu-id="76c97-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

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

### <span data-ttu-id="76c97-119">-Location</span><span class="sxs-lookup"><span data-stu-id="76c97-119">-Location</span></span>
<span data-ttu-id="76c97-120">Area geografica in cui verrà distribuito il cluster.</span><span class="sxs-lookup"><span data-stu-id="76c97-120">The geographic region that the cluster will be deployed.</span></span>

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

### <span data-ttu-id="76c97-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c97-121">-ResourceGroupName</span></span>
<span data-ttu-id="76c97-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="76c97-122">The resource group name.</span></span>

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

### <span data-ttu-id="76c97-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="76c97-123">-SkuCapacity</span></span>
<span data-ttu-id="76c97-124">Capacità SKU, il valore deve essere multiplo di 100 e nell'intervallo 1000-2000.</span><span class="sxs-lookup"><span data-stu-id="76c97-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

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

### <span data-ttu-id="76c97-125">-SKUName</span><span class="sxs-lookup"><span data-stu-id="76c97-125">-SkuName</span></span>
<span data-ttu-id="76c97-126">Nome SKU, ora può essere solo "CapacityReservation"</span><span class="sxs-lookup"><span data-stu-id="76c97-126">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="76c97-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="76c97-127">-Tags</span></span>
<span data-ttu-id="76c97-128">Tag del cluster</span><span class="sxs-lookup"><span data-stu-id="76c97-128">Tags of the cluster</span></span>

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

### <span data-ttu-id="76c97-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76c97-129">-Confirm</span></span>
<span data-ttu-id="76c97-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76c97-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76c97-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76c97-131">-WhatIf</span></span>
<span data-ttu-id="76c97-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76c97-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76c97-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76c97-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76c97-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c97-134">CommonParameters</span></span>
<span data-ttu-id="76c97-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76c97-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c97-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="76c97-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c97-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="76c97-137">INPUTS</span></span>

### <span data-ttu-id="76c97-138">System.String</span><span class="sxs-lookup"><span data-stu-id="76c97-138">System.String</span></span>

## <span data-ttu-id="76c97-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76c97-139">OUTPUTS</span></span>

### <span data-ttu-id="76c97-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="76c97-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="76c97-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="76c97-141">NOTES</span></span>

## <span data-ttu-id="76c97-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76c97-142">RELATED LINKS</span></span>
