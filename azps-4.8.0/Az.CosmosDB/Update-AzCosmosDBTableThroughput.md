---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 24e73409dbb28c99b7b678963dc53a4d38584f85
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94193029"
---
# <span data-ttu-id="ddd74-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="ddd74-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="ddd74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ddd74-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd74-103">Aggiorna il valore di velocità effettiva di una tabella CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ddd74-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="ddd74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddd74-104">SYNTAX</span></span>

### <span data-ttu-id="ddd74-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ddd74-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddd74-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddd74-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddd74-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddd74-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -InputObject <PSTableGetResults> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddd74-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddd74-108">DESCRIPTION</span></span>
<span data-ttu-id="ddd74-109">Aggiorna il valore di velocità effettiva di una tabella CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ddd74-109">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="ddd74-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddd74-110">EXAMPLES</span></span>

### <span data-ttu-id="ddd74-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ddd74-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="ddd74-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ddd74-112">PARAMETERS</span></span>

### <span data-ttu-id="ddd74-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ddd74-113">-AccountName</span></span>
<span data-ttu-id="ddd74-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="ddd74-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ddd74-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="ddd74-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ddd74-116">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="ddd74-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="ddd74-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ddd74-117">-Confirm</span></span>
<span data-ttu-id="ddd74-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddd74-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd74-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd74-119">-DefaultProfile</span></span>
<span data-ttu-id="ddd74-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd74-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddd74-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddd74-121">-InputObject</span></span>
<span data-ttu-id="ddd74-122">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ddd74-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ddd74-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ddd74-123">-Name</span></span>
<span data-ttu-id="ddd74-124">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="ddd74-124">Name of the Table.</span></span>

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

### <span data-ttu-id="ddd74-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ddd74-125">-ParentObject</span></span>
<span data-ttu-id="ddd74-126">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ddd74-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ddd74-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd74-127">-ResourceGroupName</span></span>
<span data-ttu-id="ddd74-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ddd74-128">Name of resource group.</span></span>

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

### <span data-ttu-id="ddd74-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="ddd74-129">-Throughput</span></span>
<span data-ttu-id="ddd74-130">La velocità effettiva della tabella (RU/s).</span><span class="sxs-lookup"><span data-stu-id="ddd74-130">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="ddd74-131">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="ddd74-131">Default value is 400.</span></span>

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

### <span data-ttu-id="ddd74-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd74-132">-WhatIf</span></span>
<span data-ttu-id="ddd74-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddd74-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd74-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddd74-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd74-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd74-135">CommonParameters</span></span>
<span data-ttu-id="ddd74-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddd74-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd74-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddd74-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd74-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ddd74-138">INPUTS</span></span>

### <span data-ttu-id="ddd74-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="ddd74-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="ddd74-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddd74-140">OUTPUTS</span></span>

### <span data-ttu-id="ddd74-141">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ddd74-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ddd74-142">Note</span><span class="sxs-lookup"><span data-stu-id="ddd74-142">NOTES</span></span>

## <span data-ttu-id="ddd74-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddd74-143">RELATED LINKS</span></span>
