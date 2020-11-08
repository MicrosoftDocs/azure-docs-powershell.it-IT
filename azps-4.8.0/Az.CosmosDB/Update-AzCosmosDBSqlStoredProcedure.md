---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190322"
---
# <span data-ttu-id="8206c-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="8206c-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="8206c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8206c-102">SYNOPSIS</span></span>
<span data-ttu-id="8206c-103">Aggiorna il CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="8206c-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="8206c-104">Esegue un'operazione di patch lato client leggendo l'esistente StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="8206c-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="8206c-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8206c-105">SYNTAX</span></span>

### <span data-ttu-id="8206c-106">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8206c-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8206c-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8206c-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8206c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8206c-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8206c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8206c-109">DESCRIPTION</span></span>
<span data-ttu-id="8206c-110">Aggiorna il CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="8206c-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="8206c-111">Esegue un'operazione di patch lato client leggendo l'esistente StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="8206c-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="8206c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8206c-112">EXAMPLES</span></span>

### <span data-ttu-id="8206c-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8206c-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="8206c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8206c-114">PARAMETERS</span></span>

### <span data-ttu-id="8206c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8206c-115">-AccountName</span></span>
<span data-ttu-id="8206c-116">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="8206c-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8206c-117">-Body</span><span class="sxs-lookup"><span data-stu-id="8206c-117">-Body</span></span>
<span data-ttu-id="8206c-118">Corpo della stored procedure.</span><span class="sxs-lookup"><span data-stu-id="8206c-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="8206c-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8206c-119">-Confirm</span></span>
<span data-ttu-id="8206c-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8206c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8206c-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="8206c-121">-ContainerName</span></span>
<span data-ttu-id="8206c-122">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="8206c-122">Container name.</span></span>

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

### <span data-ttu-id="8206c-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8206c-123">-DatabaseName</span></span>
<span data-ttu-id="8206c-124">Nome database.</span><span class="sxs-lookup"><span data-stu-id="8206c-124">Database name.</span></span>

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

### <span data-ttu-id="8206c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8206c-125">-DefaultProfile</span></span>
<span data-ttu-id="8206c-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8206c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8206c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8206c-127">-InputObject</span></span>
<span data-ttu-id="8206c-128">Oggetto stored procedure SQL</span><span class="sxs-lookup"><span data-stu-id="8206c-128">Sql Stored Procedure Object</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8206c-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="8206c-129">-Name</span></span>
<span data-ttu-id="8206c-130">Nome Prcodecure archiviato.</span><span class="sxs-lookup"><span data-stu-id="8206c-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="8206c-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8206c-131">-ParentObject</span></span>
<span data-ttu-id="8206c-132">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="8206c-132">Sql Container object.</span></span>

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

### <span data-ttu-id="8206c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8206c-133">-ResourceGroupName</span></span>
<span data-ttu-id="8206c-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8206c-134">Name of resource group.</span></span>

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

### <span data-ttu-id="8206c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8206c-135">-WhatIf</span></span>
<span data-ttu-id="8206c-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8206c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8206c-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8206c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8206c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8206c-138">CommonParameters</span></span>
<span data-ttu-id="8206c-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8206c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8206c-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8206c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8206c-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8206c-141">INPUTS</span></span>

### <span data-ttu-id="8206c-142">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="8206c-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="8206c-143">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="8206c-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="8206c-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8206c-144">OUTPUTS</span></span>

### <span data-ttu-id="8206c-145">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="8206c-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="8206c-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="8206c-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="8206c-147">Note</span><span class="sxs-lookup"><span data-stu-id="8206c-147">NOTES</span></span>

## <span data-ttu-id="8206c-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8206c-148">RELATED LINKS</span></span>
