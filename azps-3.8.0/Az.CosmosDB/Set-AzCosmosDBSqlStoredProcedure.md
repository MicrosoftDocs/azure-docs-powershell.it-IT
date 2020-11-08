---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 2914284849fa9a00e3cb2d0b1c96c1efd905e9e2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018509"
---
# <span data-ttu-id="516cc-101">Set-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="516cc-101">Set-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="516cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="516cc-102">SYNOPSIS</span></span>
<span data-ttu-id="516cc-103">Crea un nuovo oggetto o aggiorna un CosmosDB SQL StoredProcedure esistente.</span><span class="sxs-lookup"><span data-stu-id="516cc-103">Creates a new or updates an existing CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="516cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="516cc-104">SYNTAX</span></span>

### <span data-ttu-id="516cc-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="516cc-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="516cc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="516cc-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="516cc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="516cc-107">DESCRIPTION</span></span>
<span data-ttu-id="516cc-108">Il cmdlet **set-AzCosmosDBSqlStoredProcedure** crea un nuovo o aggiorna un CosmosDB SQL StoredProcedure esistente.</span><span class="sxs-lookup"><span data-stu-id="516cc-108">The **Set-AzCosmosDBSqlStoredProcedure** cmdlet creates a new or updates an existing CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="516cc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="516cc-109">EXAMPLES</span></span>

### <span data-ttu-id="516cc-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="516cc-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName} -Body {sampleBody}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
SqlStoredProcedureGetResultsId :
Body                           :
_rid                           :
_ts                            :
_etag                          :
```

## <span data-ttu-id="516cc-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="516cc-111">PARAMETERS</span></span>

### <span data-ttu-id="516cc-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="516cc-112">-AccountName</span></span>
<span data-ttu-id="516cc-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="516cc-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="516cc-114">-Body</span><span class="sxs-lookup"><span data-stu-id="516cc-114">-Body</span></span>
<span data-ttu-id="516cc-115">Corpo della stored procedure.</span><span class="sxs-lookup"><span data-stu-id="516cc-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="516cc-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="516cc-116">-Confirm</span></span>
<span data-ttu-id="516cc-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="516cc-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="516cc-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="516cc-118">-ContainerName</span></span>
<span data-ttu-id="516cc-119">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="516cc-119">Container name.</span></span>

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

### <span data-ttu-id="516cc-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="516cc-120">-DatabaseName</span></span>
<span data-ttu-id="516cc-121">Nome database.</span><span class="sxs-lookup"><span data-stu-id="516cc-121">Database name.</span></span>

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

### <span data-ttu-id="516cc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="516cc-122">-DefaultProfile</span></span>
<span data-ttu-id="516cc-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="516cc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="516cc-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="516cc-124">-InputObject</span></span>
<span data-ttu-id="516cc-125">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="516cc-125">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="516cc-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="516cc-126">-Name</span></span>
<span data-ttu-id="516cc-127">Nome Prcodecure archiviato.</span><span class="sxs-lookup"><span data-stu-id="516cc-127">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="516cc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="516cc-128">-ResourceGroupName</span></span>
<span data-ttu-id="516cc-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="516cc-129">Name of resource group.</span></span>

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

### <span data-ttu-id="516cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="516cc-130">-WhatIf</span></span>
<span data-ttu-id="516cc-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="516cc-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="516cc-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="516cc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="516cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="516cc-133">CommonParameters</span></span>
<span data-ttu-id="516cc-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="516cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="516cc-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="516cc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="516cc-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="516cc-136">INPUTS</span></span>

### <span data-ttu-id="516cc-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="516cc-137">None</span></span>

## <span data-ttu-id="516cc-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="516cc-138">OUTPUTS</span></span>

### <span data-ttu-id="516cc-139">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="516cc-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="516cc-140">Note</span><span class="sxs-lookup"><span data-stu-id="516cc-140">NOTES</span></span>

## <span data-ttu-id="516cc-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="516cc-141">RELATED LINKS</span></span>
