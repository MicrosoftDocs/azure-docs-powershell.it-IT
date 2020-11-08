---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: bb0d19d7b2ba0d0af9c5686f1ac6d5cf30dbfc7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031830"
---
# <span data-ttu-id="e8aca-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="e8aca-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="e8aca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8aca-102">SYNOPSIS</span></span>
<span data-ttu-id="e8aca-103">Crea un nuovo CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="e8aca-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="e8aca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8aca-104">SYNTAX</span></span>

### <span data-ttu-id="e8aca-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e8aca-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8aca-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8aca-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8aca-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8aca-107">DESCRIPTION</span></span>
<span data-ttu-id="e8aca-108">Crea un nuovo CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="e8aca-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="e8aca-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8aca-109">EXAMPLES</span></span>

### <span data-ttu-id="e8aca-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e8aca-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="e8aca-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8aca-111">PARAMETERS</span></span>

### <span data-ttu-id="e8aca-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e8aca-112">-AccountName</span></span>
<span data-ttu-id="e8aca-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e8aca-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e8aca-114">-Body</span><span class="sxs-lookup"><span data-stu-id="e8aca-114">-Body</span></span>
<span data-ttu-id="e8aca-115">Corpo della stored procedure.</span><span class="sxs-lookup"><span data-stu-id="e8aca-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="e8aca-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e8aca-116">-Confirm</span></span>
<span data-ttu-id="e8aca-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8aca-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8aca-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="e8aca-118">-ContainerName</span></span>
<span data-ttu-id="e8aca-119">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="e8aca-119">Container name.</span></span>

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

### <span data-ttu-id="e8aca-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e8aca-120">-DatabaseName</span></span>
<span data-ttu-id="e8aca-121">Nome database.</span><span class="sxs-lookup"><span data-stu-id="e8aca-121">Database name.</span></span>

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

### <span data-ttu-id="e8aca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8aca-122">-DefaultProfile</span></span>
<span data-ttu-id="e8aca-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8aca-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8aca-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8aca-124">-Name</span></span>
<span data-ttu-id="e8aca-125">Nome Prcodecure archiviato.</span><span class="sxs-lookup"><span data-stu-id="e8aca-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="e8aca-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e8aca-126">-ParentObject</span></span>
<span data-ttu-id="e8aca-127">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="e8aca-127">Sql Container object.</span></span>

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

### <span data-ttu-id="e8aca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8aca-128">-ResourceGroupName</span></span>
<span data-ttu-id="e8aca-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e8aca-129">Name of resource group.</span></span>

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

### <span data-ttu-id="e8aca-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8aca-130">-WhatIf</span></span>
<span data-ttu-id="e8aca-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8aca-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8aca-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8aca-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8aca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8aca-133">CommonParameters</span></span>
<span data-ttu-id="e8aca-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8aca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8aca-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8aca-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8aca-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8aca-136">INPUTS</span></span>

### <span data-ttu-id="e8aca-137">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="e8aca-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="e8aca-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8aca-138">OUTPUTS</span></span>

### <span data-ttu-id="e8aca-139">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="e8aca-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="e8aca-140">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="e8aca-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="e8aca-141">Note</span><span class="sxs-lookup"><span data-stu-id="e8aca-141">NOTES</span></span>

## <span data-ttu-id="e8aca-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8aca-142">RELATED LINKS</span></span>
