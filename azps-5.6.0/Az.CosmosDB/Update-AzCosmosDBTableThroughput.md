---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 78cae2438b941e479d1f1ab26fbf2275bcff7b3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996839"
---
# <span data-ttu-id="46f68-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="46f68-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="46f68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46f68-102">SYNOPSIS</span></span>
<span data-ttu-id="46f68-103">Aggiorna il valore di velocità effettiva di una tabella AMMORT.</span><span class="sxs-lookup"><span data-stu-id="46f68-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="46f68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46f68-104">SYNTAX</span></span>

### <span data-ttu-id="46f68-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="46f68-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46f68-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46f68-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46f68-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46f68-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -InputObject <PSTableGetResults> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46f68-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="46f68-108">DESCRIPTION</span></span>
<span data-ttu-id="46f68-109">Aggiorna il valore di velocità effettiva di una tabella AMMORT.</span><span class="sxs-lookup"><span data-stu-id="46f68-109">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="46f68-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46f68-110">EXAMPLES</span></span>

### <span data-ttu-id="46f68-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="46f68-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="46f68-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46f68-112">PARAMETERS</span></span>

### <span data-ttu-id="46f68-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="46f68-113">-AccountName</span></span>
<span data-ttu-id="46f68-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="46f68-114">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f68-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="46f68-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="46f68-116">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="46f68-116">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f68-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46f68-117">-Confirm</span></span>
<span data-ttu-id="46f68-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46f68-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46f68-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f68-119">-DefaultProfile</span></span>
<span data-ttu-id="46f68-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46f68-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46f68-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46f68-121">-InputObject</span></span>
<span data-ttu-id="46f68-122">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="46f68-122">CosmosDB Account object</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46f68-123">-Name</span><span class="sxs-lookup"><span data-stu-id="46f68-123">-Name</span></span>
<span data-ttu-id="46f68-124">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="46f68-124">Name of the Table.</span></span>

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

### <span data-ttu-id="46f68-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="46f68-125">-ParentObject</span></span>
<span data-ttu-id="46f68-126">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="46f68-126">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46f68-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46f68-127">-ResourceGroupName</span></span>
<span data-ttu-id="46f68-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="46f68-128">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f68-129">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="46f68-129">-Throughput</span></span>
<span data-ttu-id="46f68-130">Velocità effettiva della tabella (RU).</span><span class="sxs-lookup"><span data-stu-id="46f68-130">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="46f68-131">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="46f68-131">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f68-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46f68-132">-WhatIf</span></span>
<span data-ttu-id="46f68-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46f68-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46f68-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46f68-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46f68-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f68-135">CommonParameters</span></span>
<span data-ttu-id="46f68-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46f68-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f68-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="46f68-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f68-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="46f68-138">INPUTS</span></span>

### <span data-ttu-id="46f68-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="46f68-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="46f68-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46f68-140">OUTPUTS</span></span>

### <span data-ttu-id="46f68-141">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="46f68-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="46f68-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="46f68-142">NOTES</span></span>

## <span data-ttu-id="46f68-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46f68-143">RELATED LINKS</span></span>
