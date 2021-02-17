---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191478"
---
# <span data-ttu-id="c8d72-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="c8d72-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="c8d72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8d72-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d72-103">cluster di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c8d72-103">update cluster</span></span>

## <span data-ttu-id="c8d72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8d72-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8d72-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c8d72-105">DESCRIPTION</span></span>
<span data-ttu-id="c8d72-106">cluster di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c8d72-106">update cluster</span></span>

## <span data-ttu-id="c8d72-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8d72-107">EXAMPLES</span></span>

### <span data-ttu-id="c8d72-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c8d72-108">Example 1</span></span>
```powershell
Update-AzOperationalInsightsCluster -ResourceGroupName azps-test-group -ClusterName yabo-cluster10 -Location eastus -SkuName CapacityReservation -SkuCapacity 1200 -KeyVaultUri {uri} -KeyName {key-name} -KeyVersion {version}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Updating
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="c8d72-109">Aggiornare il cluster con proprietà chiave del vault e SKU</span><span class="sxs-lookup"><span data-stu-id="c8d72-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="c8d72-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8d72-110">PARAMETERS</span></span>

### <span data-ttu-id="c8d72-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8d72-111">-AsJob</span></span>
<span data-ttu-id="c8d72-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c8d72-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8d72-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c8d72-113">-ClusterName</span></span>
<span data-ttu-id="c8d72-114">Nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="c8d72-114">The cluster name.</span></span>

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

### <span data-ttu-id="c8d72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d72-115">-DefaultProfile</span></span>
<span data-ttu-id="c8d72-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8d72-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8d72-117">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c8d72-117">-KeyName</span></span>
<span data-ttu-id="c8d72-118">Nome chiave</span><span class="sxs-lookup"><span data-stu-id="c8d72-118">Key Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d72-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="c8d72-119">-KeyVaultUri</span></span>
<span data-ttu-id="c8d72-120">Uri vault chiave, "Protezione eliminazione" ed "Eliminazione reverscita" devono essere abilitati per questa chiave</span><span class="sxs-lookup"><span data-stu-id="c8d72-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d72-121">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="c8d72-121">-KeyVersion</span></span>
<span data-ttu-id="c8d72-122">Versione chiave</span><span class="sxs-lookup"><span data-stu-id="c8d72-122">Key Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d72-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8d72-123">-ResourceGroupName</span></span>
<span data-ttu-id="c8d72-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c8d72-124">The resource group name.</span></span>

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

### <span data-ttu-id="c8d72-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c8d72-125">-SkuCapacity</span></span>
<span data-ttu-id="c8d72-126">Capacità SKU</span><span class="sxs-lookup"><span data-stu-id="c8d72-126">Sku Capacity</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d72-127">-SKUName</span><span class="sxs-lookup"><span data-stu-id="c8d72-127">-SkuName</span></span>
<span data-ttu-id="c8d72-128">Nome SKU, ora può essere solo "CapacityReservation"</span><span class="sxs-lookup"><span data-stu-id="c8d72-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="c8d72-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="c8d72-129">-Tags</span></span>
<span data-ttu-id="c8d72-130">Tag del cluster</span><span class="sxs-lookup"><span data-stu-id="c8d72-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="c8d72-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8d72-131">-Confirm</span></span>
<span data-ttu-id="c8d72-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8d72-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8d72-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8d72-133">-WhatIf</span></span>
<span data-ttu-id="c8d72-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8d72-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8d72-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8d72-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8d72-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d72-136">CommonParameters</span></span>
<span data-ttu-id="c8d72-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8d72-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d72-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c8d72-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d72-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="c8d72-139">INPUTS</span></span>

### <span data-ttu-id="c8d72-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c8d72-140">System.String</span></span>

## <span data-ttu-id="c8d72-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8d72-141">OUTPUTS</span></span>

### <span data-ttu-id="c8d72-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="c8d72-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="c8d72-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="c8d72-143">NOTES</span></span>

## <span data-ttu-id="c8d72-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8d72-144">RELATED LINKS</span></span>
