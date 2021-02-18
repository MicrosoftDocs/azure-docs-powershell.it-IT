---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: 41494f860eea0ad811e9066d1fa8a45032b2317d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204610"
---
# <span data-ttu-id="ebbc9-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="ebbc9-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="ebbc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebbc9-102">SYNOPSIS</span></span>
<span data-ttu-id="ebbc9-103">Crea una nuova tabellaDbDb.</span><span class="sxs-lookup"><span data-stu-id="ebbc9-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="ebbc9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ebbc9-104">SYNTAX</span></span>

### <span data-ttu-id="ebbc9-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ebbc9-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebbc9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebbc9-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ebbc9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ebbc9-107">DESCRIPTION</span></span>
<span data-ttu-id="ebbc9-108">Crea una nuova tabellaDbDb.</span><span class="sxs-lookup"><span data-stu-id="ebbc9-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="ebbc9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ebbc9-109">EXAMPLES</span></span>

### <span data-ttu-id="ebbc9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ebbc9-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="ebbc9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebbc9-111">PARAMETERS</span></span>

### <span data-ttu-id="ebbc9-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ebbc9-112">-AccountName</span></span>
<span data-ttu-id="ebbc9-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="ebbc9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ebbc9-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="ebbc9-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ebbc9-115">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="ebbc9-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="ebbc9-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebbc9-116">-Confirm</span></span>
<span data-ttu-id="ebbc9-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebbc9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebbc9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebbc9-118">-DefaultProfile</span></span>
<span data-ttu-id="ebbc9-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ebbc9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebbc9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ebbc9-120">-Name</span></span>
<span data-ttu-id="ebbc9-121">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="ebbc9-121">Name of the Table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc9-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ebbc9-122">-ParentObject</span></span>
<span data-ttu-id="ebbc9-123">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="ebbc9-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ebbc9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebbc9-124">-ResourceGroupName</span></span>
<span data-ttu-id="ebbc9-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ebbc9-125">Name of resource group.</span></span>

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

### <span data-ttu-id="ebbc9-126">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="ebbc9-126">-Throughput</span></span>
<span data-ttu-id="ebbc9-127">Velocità effettiva della tabella (RU).</span><span class="sxs-lookup"><span data-stu-id="ebbc9-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="ebbc9-128">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="ebbc9-128">Default value is 400.</span></span>

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

### <span data-ttu-id="ebbc9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebbc9-129">-WhatIf</span></span>
<span data-ttu-id="ebbc9-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ebbc9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebbc9-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ebbc9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebbc9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebbc9-132">CommonParameters</span></span>
<span data-ttu-id="ebbc9-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebbc9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebbc9-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ebbc9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebbc9-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="ebbc9-135">INPUTS</span></span>

### <span data-ttu-id="ebbc9-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="ebbc9-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="ebbc9-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ebbc9-137">OUTPUTS</span></span>

### <span data-ttu-id="ebbc9-138">Microsoft.Azure.Commands.EnterpriseDb.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="ebbc9-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="ebbc9-139">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="ebbc9-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="ebbc9-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="ebbc9-140">NOTES</span></span>

## <span data-ttu-id="ebbc9-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ebbc9-141">RELATED LINKS</span></span>
