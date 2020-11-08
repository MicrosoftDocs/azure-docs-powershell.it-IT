---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201033"
---
# <span data-ttu-id="ab2d0-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="ab2d0-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="ab2d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab2d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ab2d0-103">aggiornare il cluster</span><span class="sxs-lookup"><span data-stu-id="ab2d0-103">update cluster</span></span>

## <span data-ttu-id="ab2d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab2d0-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab2d0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab2d0-105">DESCRIPTION</span></span>
<span data-ttu-id="ab2d0-106">aggiornare il cluster</span><span class="sxs-lookup"><span data-stu-id="ab2d0-106">update cluster</span></span>

## <span data-ttu-id="ab2d0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab2d0-107">EXAMPLES</span></span>

### <span data-ttu-id="ab2d0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ab2d0-108">Example 1</span></span>
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

<span data-ttu-id="ab2d0-109">aggiornare il cluster con le proprietà Key Vault e SKU</span><span class="sxs-lookup"><span data-stu-id="ab2d0-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="ab2d0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab2d0-110">PARAMETERS</span></span>

### <span data-ttu-id="ab2d0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab2d0-111">-AsJob</span></span>
<span data-ttu-id="ab2d0-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ab2d0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab2d0-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ab2d0-113">-ClusterName</span></span>
<span data-ttu-id="ab2d0-114">Nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="ab2d0-114">The cluster name.</span></span>

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

### <span data-ttu-id="ab2d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab2d0-115">-DefaultProfile</span></span>
<span data-ttu-id="ab2d0-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab2d0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab2d0-117">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="ab2d0-117">-KeyName</span></span>
<span data-ttu-id="ab2d0-118">Nome chiave</span><span class="sxs-lookup"><span data-stu-id="ab2d0-118">Key Name</span></span>

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

### <span data-ttu-id="ab2d0-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="ab2d0-119">-KeyVaultUri</span></span>
<span data-ttu-id="ab2d0-120">L'URI della chiave, "Elimina protezione" e "eliminazione morbida" devono essere abilitati per il Vault</span><span class="sxs-lookup"><span data-stu-id="ab2d0-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

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

### <span data-ttu-id="ab2d0-121">-Versione</span><span class="sxs-lookup"><span data-stu-id="ab2d0-121">-KeyVersion</span></span>
<span data-ttu-id="ab2d0-122">Versione chiave</span><span class="sxs-lookup"><span data-stu-id="ab2d0-122">Key Version</span></span>

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

### <span data-ttu-id="ab2d0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab2d0-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab2d0-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ab2d0-124">The resource group name.</span></span>

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

### <span data-ttu-id="ab2d0-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ab2d0-125">-SkuCapacity</span></span>
<span data-ttu-id="ab2d0-126">Capacità SKU</span><span class="sxs-lookup"><span data-stu-id="ab2d0-126">Sku Capacity</span></span>

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

### <span data-ttu-id="ab2d0-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ab2d0-127">-SkuName</span></span>
<span data-ttu-id="ab2d0-128">Nome Usk, ora può essere solo ' CapacityReservation '</span><span class="sxs-lookup"><span data-stu-id="ab2d0-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="ab2d0-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="ab2d0-129">-Tags</span></span>
<span data-ttu-id="ab2d0-130">Tag del cluster</span><span class="sxs-lookup"><span data-stu-id="ab2d0-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="ab2d0-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ab2d0-131">-Confirm</span></span>
<span data-ttu-id="ab2d0-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab2d0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab2d0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab2d0-133">-WhatIf</span></span>
<span data-ttu-id="ab2d0-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab2d0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab2d0-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab2d0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab2d0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab2d0-136">CommonParameters</span></span>
<span data-ttu-id="ab2d0-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab2d0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab2d0-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab2d0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab2d0-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab2d0-139">INPUTS</span></span>

### <span data-ttu-id="ab2d0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ab2d0-140">System.String</span></span>

## <span data-ttu-id="ab2d0-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab2d0-141">OUTPUTS</span></span>

### <span data-ttu-id="ab2d0-142">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="ab2d0-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="ab2d0-143">Note</span><span class="sxs-lookup"><span data-stu-id="ab2d0-143">NOTES</span></span>

## <span data-ttu-id="ab2d0-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab2d0-144">RELATED LINKS</span></span>
