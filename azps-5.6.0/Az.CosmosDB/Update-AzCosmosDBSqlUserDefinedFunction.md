---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: d1f4e4c5c48e33a1b3c2ac882b0c561bb50f9bed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009694"
---
# <span data-ttu-id="73c89-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="73c89-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="73c89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73c89-102">SYNOPSIS</span></span>
<span data-ttu-id="73c89-103">Aggiorna la funzione Sql UserDefinedFunction di DatabaseDb.</span><span class="sxs-lookup"><span data-stu-id="73c89-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="73c89-104">Esegue un'operazione di patch sul lato client leggendo la funzione UserDefinedFunction esistente.</span><span class="sxs-lookup"><span data-stu-id="73c89-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="73c89-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73c89-105">SYNTAX</span></span>

### <span data-ttu-id="73c89-106">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="73c89-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73c89-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73c89-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73c89-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73c89-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73c89-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="73c89-109">DESCRIPTION</span></span>
<span data-ttu-id="73c89-110">Aggiorna la funzione Sql UserDefinedFunction di DatabaseDb.</span><span class="sxs-lookup"><span data-stu-id="73c89-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="73c89-111">Esegue un'operazione di patch sul lato client leggendo la funzione UserDefinedFunction esistente.</span><span class="sxs-lookup"><span data-stu-id="73c89-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="73c89-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73c89-112">EXAMPLES</span></span>

### <span data-ttu-id="73c89-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="73c89-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="73c89-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73c89-114">PARAMETERS</span></span>

### <span data-ttu-id="73c89-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="73c89-115">-AccountName</span></span>
<span data-ttu-id="73c89-116">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="73c89-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="73c89-117">-Body</span><span class="sxs-lookup"><span data-stu-id="73c89-117">-Body</span></span>
<span data-ttu-id="73c89-118">Corpo della funzione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="73c89-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="73c89-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73c89-119">-Confirm</span></span>
<span data-ttu-id="73c89-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73c89-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73c89-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="73c89-121">-ContainerName</span></span>
<span data-ttu-id="73c89-122">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="73c89-122">Container name.</span></span>

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

### <span data-ttu-id="73c89-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="73c89-123">-DatabaseName</span></span>
<span data-ttu-id="73c89-124">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="73c89-124">Database name.</span></span>

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

### <span data-ttu-id="73c89-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73c89-125">-DefaultProfile</span></span>
<span data-ttu-id="73c89-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73c89-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73c89-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73c89-127">-InputObject</span></span>
<span data-ttu-id="73c89-128">Oggetto Funzione definita dall'utente SQL</span><span class="sxs-lookup"><span data-stu-id="73c89-128">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73c89-129">-Name</span><span class="sxs-lookup"><span data-stu-id="73c89-129">-Name</span></span>
<span data-ttu-id="73c89-130">Nome funzione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="73c89-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="73c89-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="73c89-131">-ParentObject</span></span>
<span data-ttu-id="73c89-132">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="73c89-132">Sql Container object.</span></span>

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

### <span data-ttu-id="73c89-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73c89-133">-ResourceGroupName</span></span>
<span data-ttu-id="73c89-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="73c89-134">Name of resource group.</span></span>

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

### <span data-ttu-id="73c89-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73c89-135">-WhatIf</span></span>
<span data-ttu-id="73c89-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73c89-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73c89-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73c89-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73c89-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c89-138">CommonParameters</span></span>
<span data-ttu-id="73c89-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73c89-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c89-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="73c89-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c89-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="73c89-141">INPUTS</span></span>

### <span data-ttu-id="73c89-142">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="73c89-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="73c89-143">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="73c89-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="73c89-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73c89-144">OUTPUTS</span></span>

### <span data-ttu-id="73c89-145">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="73c89-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="73c89-146">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="73c89-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="73c89-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="73c89-147">NOTES</span></span>

## <span data-ttu-id="73c89-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73c89-148">RELATED LINKS</span></span>
