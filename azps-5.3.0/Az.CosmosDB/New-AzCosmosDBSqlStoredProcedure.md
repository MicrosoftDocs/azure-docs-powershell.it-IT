---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: bb0d19d7b2ba0d0af9c5686f1ac6d5cf30dbfc7d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477415"
---
# <span data-ttu-id="ca182-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="ca182-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="ca182-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca182-102">SYNOPSIS</span></span>
<span data-ttu-id="ca182-103">Crea un nuovo CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="ca182-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="ca182-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca182-104">SYNTAX</span></span>

### <span data-ttu-id="ca182-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca182-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca182-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca182-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca182-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca182-107">DESCRIPTION</span></span>
<span data-ttu-id="ca182-108">Crea un nuovo CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="ca182-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="ca182-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca182-109">EXAMPLES</span></span>

### <span data-ttu-id="ca182-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ca182-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="ca182-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca182-111">PARAMETERS</span></span>

### <span data-ttu-id="ca182-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ca182-112">-AccountName</span></span>
<span data-ttu-id="ca182-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="ca182-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ca182-114">-Body</span><span class="sxs-lookup"><span data-stu-id="ca182-114">-Body</span></span>
<span data-ttu-id="ca182-115">Corpo della stored procedure.</span><span class="sxs-lookup"><span data-stu-id="ca182-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="ca182-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca182-116">-Confirm</span></span>
<span data-ttu-id="ca182-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca182-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca182-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ca182-118">-ContainerName</span></span>
<span data-ttu-id="ca182-119">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="ca182-119">Container name.</span></span>

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

### <span data-ttu-id="ca182-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ca182-120">-DatabaseName</span></span>
<span data-ttu-id="ca182-121">Nome database.</span><span class="sxs-lookup"><span data-stu-id="ca182-121">Database name.</span></span>

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

### <span data-ttu-id="ca182-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca182-122">-DefaultProfile</span></span>
<span data-ttu-id="ca182-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca182-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca182-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca182-124">-Name</span></span>
<span data-ttu-id="ca182-125">Nome Prcodecure archiviato.</span><span class="sxs-lookup"><span data-stu-id="ca182-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="ca182-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ca182-126">-ParentObject</span></span>
<span data-ttu-id="ca182-127">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="ca182-127">Sql Container object.</span></span>

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

### <span data-ttu-id="ca182-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca182-128">-ResourceGroupName</span></span>
<span data-ttu-id="ca182-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca182-129">Name of resource group.</span></span>

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

### <span data-ttu-id="ca182-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca182-130">-WhatIf</span></span>
<span data-ttu-id="ca182-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca182-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca182-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca182-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca182-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca182-133">CommonParameters</span></span>
<span data-ttu-id="ca182-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca182-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca182-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca182-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca182-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca182-136">INPUTS</span></span>

### <span data-ttu-id="ca182-137">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="ca182-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="ca182-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca182-138">OUTPUTS</span></span>

### <span data-ttu-id="ca182-139">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="ca182-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="ca182-140">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="ca182-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="ca182-141">Note</span><span class="sxs-lookup"><span data-stu-id="ca182-141">NOTES</span></span>

## <span data-ttu-id="ca182-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca182-142">RELATED LINKS</span></span>
