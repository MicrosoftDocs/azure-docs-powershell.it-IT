---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 56c99a1e3cf21f38544e97ee84ba10efb51bc983
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020133"
---
# <span data-ttu-id="0db0e-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="0db0e-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="0db0e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0db0e-102">SYNOPSIS</span></span>
<span data-ttu-id="0db0e-103">Aggiorna il valore di velocità effettiva di una tabella CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0db0e-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="0db0e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0db0e-104">SYNTAX</span></span>

### <span data-ttu-id="0db0e-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0db0e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0db0e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0db0e-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -Throughput <Int32> -ParentObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0db0e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0db0e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -Throughput <Int32> -InputObject <PSTableGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0db0e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0db0e-108">EXAMPLES</span></span>

### <span data-ttu-id="0db0e-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0db0e-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="0db0e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0db0e-110">PARAMETERS</span></span>

### <span data-ttu-id="0db0e-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0db0e-111">-AccountName</span></span>
<span data-ttu-id="0db0e-112">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0db0e-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0db0e-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0db0e-113">-Confirm</span></span>
<span data-ttu-id="0db0e-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0db0e-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0db0e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db0e-115">-DefaultProfile</span></span>
<span data-ttu-id="0db0e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0db0e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0db0e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0db0e-117">-InputObject</span></span>
<span data-ttu-id="0db0e-118">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0db0e-118">CosmosDB Account object</span></span>

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

### <span data-ttu-id="0db0e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0db0e-119">-Name</span></span>
<span data-ttu-id="0db0e-120">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="0db0e-120">Name of the Table.</span></span>

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

### <span data-ttu-id="0db0e-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0db0e-121">-ParentObject</span></span>
<span data-ttu-id="0db0e-122">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0db0e-122">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0db0e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db0e-123">-ResourceGroupName</span></span>
<span data-ttu-id="0db0e-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0db0e-124">Name of resource group.</span></span>

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

### <span data-ttu-id="0db0e-125">-Throughput</span><span class="sxs-lookup"><span data-stu-id="0db0e-125">-Throughput</span></span>
<span data-ttu-id="0db0e-126">La velocità effettiva della tabella (RU/s).</span><span class="sxs-lookup"><span data-stu-id="0db0e-126">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="0db0e-127">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="0db0e-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db0e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0db0e-128">-WhatIf</span></span>
<span data-ttu-id="0db0e-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0db0e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0db0e-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0db0e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0db0e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db0e-131">CommonParameters</span></span>
<span data-ttu-id="0db0e-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db0e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db0e-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0db0e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db0e-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0db0e-134">INPUTS</span></span>

### <span data-ttu-id="0db0e-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="0db0e-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="0db0e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0db0e-136">OUTPUTS</span></span>

### <span data-ttu-id="0db0e-137">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0db0e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0db0e-138">Note</span><span class="sxs-lookup"><span data-stu-id="0db0e-138">NOTES</span></span>

## <span data-ttu-id="0db0e-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0db0e-139">RELATED LINKS</span></span>
