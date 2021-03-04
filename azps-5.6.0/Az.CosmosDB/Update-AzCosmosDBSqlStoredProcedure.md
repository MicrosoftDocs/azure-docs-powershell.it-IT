---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 8a717b15268090a7e5ea356c49b11d9aba1ab009
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977150"
---
# <span data-ttu-id="61cc8-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="61cc8-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="61cc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61cc8-102">SYNOPSIS</span></span>
<span data-ttu-id="61cc8-103">Aggiorna la sintassi Sql StoredProcedure di Sql StoredProcedure del database database.</span><span class="sxs-lookup"><span data-stu-id="61cc8-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="61cc8-104">Esegue un'operazione di patch sul lato client leggendo storedprocedure esistente.</span><span class="sxs-lookup"><span data-stu-id="61cc8-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="61cc8-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61cc8-105">SYNTAX</span></span>

### <span data-ttu-id="61cc8-106">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61cc8-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61cc8-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61cc8-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61cc8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61cc8-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61cc8-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="61cc8-109">DESCRIPTION</span></span>
<span data-ttu-id="61cc8-110">Aggiorna la sintassi Sql StoredProcedure di Sql StoredProcedure del database database.</span><span class="sxs-lookup"><span data-stu-id="61cc8-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="61cc8-111">Esegue un'operazione di patch sul lato client leggendo storedprocedure esistente.</span><span class="sxs-lookup"><span data-stu-id="61cc8-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="61cc8-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61cc8-112">EXAMPLES</span></span>

### <span data-ttu-id="61cc8-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61cc8-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="61cc8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61cc8-114">PARAMETERS</span></span>

### <span data-ttu-id="61cc8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="61cc8-115">-AccountName</span></span>
<span data-ttu-id="61cc8-116">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="61cc8-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="61cc8-117">-Body</span><span class="sxs-lookup"><span data-stu-id="61cc8-117">-Body</span></span>
<span data-ttu-id="61cc8-118">Corpo della stored procedure.</span><span class="sxs-lookup"><span data-stu-id="61cc8-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="61cc8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61cc8-119">-Confirm</span></span>
<span data-ttu-id="61cc8-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61cc8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61cc8-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="61cc8-121">-ContainerName</span></span>
<span data-ttu-id="61cc8-122">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="61cc8-122">Container name.</span></span>

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

### <span data-ttu-id="61cc8-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="61cc8-123">-DatabaseName</span></span>
<span data-ttu-id="61cc8-124">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="61cc8-124">Database name.</span></span>

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

### <span data-ttu-id="61cc8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61cc8-125">-DefaultProfile</span></span>
<span data-ttu-id="61cc8-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61cc8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61cc8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61cc8-127">-InputObject</span></span>
<span data-ttu-id="61cc8-128">Oggetto Stored Procedure Sql</span><span class="sxs-lookup"><span data-stu-id="61cc8-128">Sql Stored Procedure Object</span></span>

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

### <span data-ttu-id="61cc8-129">-Name</span><span class="sxs-lookup"><span data-stu-id="61cc8-129">-Name</span></span>
<span data-ttu-id="61cc8-130">Nome Prcodecure archiviato.</span><span class="sxs-lookup"><span data-stu-id="61cc8-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="61cc8-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="61cc8-131">-ParentObject</span></span>
<span data-ttu-id="61cc8-132">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="61cc8-132">Sql Container object.</span></span>

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

### <span data-ttu-id="61cc8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61cc8-133">-ResourceGroupName</span></span>
<span data-ttu-id="61cc8-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="61cc8-134">Name of resource group.</span></span>

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

### <span data-ttu-id="61cc8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61cc8-135">-WhatIf</span></span>
<span data-ttu-id="61cc8-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61cc8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61cc8-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61cc8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61cc8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61cc8-138">CommonParameters</span></span>
<span data-ttu-id="61cc8-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61cc8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61cc8-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61cc8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61cc8-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="61cc8-141">INPUTS</span></span>

### <span data-ttu-id="61cc8-142">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="61cc8-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="61cc8-143">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="61cc8-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="61cc8-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61cc8-144">OUTPUTS</span></span>

### <span data-ttu-id="61cc8-145">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="61cc8-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="61cc8-146">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="61cc8-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="61cc8-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="61cc8-147">NOTES</span></span>

## <span data-ttu-id="61cc8-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61cc8-148">RELATED LINKS</span></span>
