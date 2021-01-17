---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372917"
---
# <span data-ttu-id="ea0c9-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="ea0c9-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="ea0c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea0c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0c9-103">Aggiorna il CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="ea0c9-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="ea0c9-104">Esegue un'operazione di patch lato client leggendo l'esistente StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="ea0c9-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="ea0c9-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea0c9-105">SYNTAX</span></span>

### <span data-ttu-id="ea0c9-106">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ea0c9-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea0c9-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea0c9-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea0c9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea0c9-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea0c9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea0c9-109">DESCRIPTION</span></span>
<span data-ttu-id="ea0c9-110">Aggiorna il CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="ea0c9-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="ea0c9-111">Esegue un'operazione di patch lato client leggendo l'esistente StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="ea0c9-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="ea0c9-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea0c9-112">EXAMPLES</span></span>

### <span data-ttu-id="ea0c9-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea0c9-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="ea0c9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea0c9-114">PARAMETERS</span></span>

### <span data-ttu-id="ea0c9-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ea0c9-115">-AccountName</span></span>
<span data-ttu-id="ea0c9-116">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="ea0c9-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ea0c9-117">-Body</span><span class="sxs-lookup"><span data-stu-id="ea0c9-117">-Body</span></span>
<span data-ttu-id="ea0c9-118">Corpo della stored procedure.</span><span class="sxs-lookup"><span data-stu-id="ea0c9-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="ea0c9-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ea0c9-119">-Confirm</span></span>
<span data-ttu-id="ea0c9-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea0c9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea0c9-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ea0c9-121">-ContainerName</span></span>
<span data-ttu-id="ea0c9-122">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="ea0c9-122">Container name.</span></span>

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

### <span data-ttu-id="ea0c9-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ea0c9-123">-DatabaseName</span></span>
<span data-ttu-id="ea0c9-124">Nome database.</span><span class="sxs-lookup"><span data-stu-id="ea0c9-124">Database name.</span></span>

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

### <span data-ttu-id="ea0c9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0c9-125">-DefaultProfile</span></span>
<span data-ttu-id="ea0c9-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea0c9-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea0c9-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea0c9-127">-InputObject</span></span>
<span data-ttu-id="ea0c9-128">Oggetto stored procedure SQL</span><span class="sxs-lookup"><span data-stu-id="ea0c9-128">Sql Stored Procedure Object</span></span>

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

### <span data-ttu-id="ea0c9-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea0c9-129">-Name</span></span>
<span data-ttu-id="ea0c9-130">Nome Prcodecure archiviato.</span><span class="sxs-lookup"><span data-stu-id="ea0c9-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="ea0c9-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ea0c9-131">-ParentObject</span></span>
<span data-ttu-id="ea0c9-132">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="ea0c9-132">Sql Container object.</span></span>

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

### <span data-ttu-id="ea0c9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea0c9-133">-ResourceGroupName</span></span>
<span data-ttu-id="ea0c9-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ea0c9-134">Name of resource group.</span></span>

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

### <span data-ttu-id="ea0c9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea0c9-135">-WhatIf</span></span>
<span data-ttu-id="ea0c9-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea0c9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea0c9-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea0c9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea0c9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0c9-138">CommonParameters</span></span>
<span data-ttu-id="ea0c9-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea0c9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0c9-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea0c9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0c9-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea0c9-141">INPUTS</span></span>

### <span data-ttu-id="ea0c9-142">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="ea0c9-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="ea0c9-143">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="ea0c9-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="ea0c9-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea0c9-144">OUTPUTS</span></span>

### <span data-ttu-id="ea0c9-145">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="ea0c9-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="ea0c9-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="ea0c9-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="ea0c9-147">Note</span><span class="sxs-lookup"><span data-stu-id="ea0c9-147">NOTES</span></span>

## <span data-ttu-id="ea0c9-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea0c9-148">RELATED LINKS</span></span>
