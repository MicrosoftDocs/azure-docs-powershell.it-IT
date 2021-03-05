---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b088eaf9e09408b8a294965c66acf88ac2715dee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963150"
---
# <span data-ttu-id="4cb7a-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="4cb7a-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="4cb7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cb7a-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb7a-103">Crea una nuova istanza di Sql StoredProcedure di Sql StoredProcedure diDb.</span><span class="sxs-lookup"><span data-stu-id="4cb7a-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="4cb7a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cb7a-104">SYNTAX</span></span>

### <span data-ttu-id="4cb7a-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4cb7a-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cb7a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cb7a-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cb7a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4cb7a-107">DESCRIPTION</span></span>
<span data-ttu-id="4cb7a-108">Crea una nuova istanza di Sql StoredProcedure sql diDbDb.</span><span class="sxs-lookup"><span data-stu-id="4cb7a-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="4cb7a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cb7a-109">EXAMPLES</span></span>

### <span data-ttu-id="4cb7a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4cb7a-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="4cb7a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cb7a-111">PARAMETERS</span></span>

### <span data-ttu-id="4cb7a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4cb7a-112">-AccountName</span></span>
<span data-ttu-id="4cb7a-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="4cb7a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4cb7a-114">-Body</span><span class="sxs-lookup"><span data-stu-id="4cb7a-114">-Body</span></span>
<span data-ttu-id="4cb7a-115">Corpo della stored procedure.</span><span class="sxs-lookup"><span data-stu-id="4cb7a-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="4cb7a-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4cb7a-116">-Confirm</span></span>
<span data-ttu-id="4cb7a-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cb7a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cb7a-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="4cb7a-118">-ContainerName</span></span>
<span data-ttu-id="4cb7a-119">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="4cb7a-119">Container name.</span></span>

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

### <span data-ttu-id="4cb7a-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4cb7a-120">-DatabaseName</span></span>
<span data-ttu-id="4cb7a-121">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="4cb7a-121">Database name.</span></span>

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

### <span data-ttu-id="4cb7a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cb7a-122">-DefaultProfile</span></span>
<span data-ttu-id="4cb7a-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4cb7a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cb7a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4cb7a-124">-Name</span></span>
<span data-ttu-id="4cb7a-125">Nome Prcodecure archiviato.</span><span class="sxs-lookup"><span data-stu-id="4cb7a-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="4cb7a-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4cb7a-126">-ParentObject</span></span>
<span data-ttu-id="4cb7a-127">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="4cb7a-127">Sql Container object.</span></span>

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

### <span data-ttu-id="4cb7a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cb7a-128">-ResourceGroupName</span></span>
<span data-ttu-id="4cb7a-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4cb7a-129">Name of resource group.</span></span>

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

### <span data-ttu-id="4cb7a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cb7a-130">-WhatIf</span></span>
<span data-ttu-id="4cb7a-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4cb7a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cb7a-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4cb7a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cb7a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb7a-133">CommonParameters</span></span>
<span data-ttu-id="4cb7a-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cb7a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb7a-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4cb7a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb7a-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="4cb7a-136">INPUTS</span></span>

### <span data-ttu-id="4cb7a-137">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="4cb7a-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="4cb7a-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cb7a-138">OUTPUTS</span></span>

### <span data-ttu-id="4cb7a-139">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="4cb7a-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="4cb7a-140">Microsoft.Azure.Commands.CpsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="4cb7a-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="4cb7a-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="4cb7a-141">NOTES</span></span>

## <span data-ttu-id="4cb7a-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cb7a-142">RELATED LINKS</span></span>
