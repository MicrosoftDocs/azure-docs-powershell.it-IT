---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: cc7c443ad4447abfa1c31ebb335d3d1ae602f1b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204611"
---
# <span data-ttu-id="e3ecd-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="e3ecd-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="e3ecd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3ecd-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ecd-103">Crea una nuova funzione Sql UserDefinedFunction diDb.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="e3ecd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3ecd-104">SYNTAX</span></span>

### <span data-ttu-id="e3ecd-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3ecd-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3ecd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3ecd-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3ecd-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3ecd-107">DESCRIPTION</span></span>
<span data-ttu-id="e3ecd-108">Crea una nuova funzione Sql UserDefinedFunction diDb.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="e3ecd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3ecd-109">EXAMPLES</span></span>

### <span data-ttu-id="e3ecd-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e3ecd-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="e3ecd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3ecd-111">PARAMETERS</span></span>

### <span data-ttu-id="e3ecd-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e3ecd-112">-AccountName</span></span>
<span data-ttu-id="e3ecd-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e3ecd-114">-Body</span><span class="sxs-lookup"><span data-stu-id="e3ecd-114">-Body</span></span>
<span data-ttu-id="e3ecd-115">Corpo della funzione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="e3ecd-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3ecd-116">-Confirm</span></span>
<span data-ttu-id="e3ecd-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3ecd-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="e3ecd-118">-ContainerName</span></span>
<span data-ttu-id="e3ecd-119">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-119">Container name.</span></span>

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

### <span data-ttu-id="e3ecd-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e3ecd-120">-DatabaseName</span></span>
<span data-ttu-id="e3ecd-121">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-121">Database name.</span></span>

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

### <span data-ttu-id="e3ecd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ecd-122">-DefaultProfile</span></span>
<span data-ttu-id="e3ecd-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3ecd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e3ecd-124">-Name</span></span>
<span data-ttu-id="e3ecd-125">Nome funzione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="e3ecd-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e3ecd-126">-ParentObject</span></span>
<span data-ttu-id="e3ecd-127">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-127">Sql Container object.</span></span>

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

### <span data-ttu-id="e3ecd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3ecd-128">-ResourceGroupName</span></span>
<span data-ttu-id="e3ecd-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-129">Name of resource group.</span></span>

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

### <span data-ttu-id="e3ecd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3ecd-130">-WhatIf</span></span>
<span data-ttu-id="e3ecd-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3ecd-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3ecd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ecd-133">CommonParameters</span></span>
<span data-ttu-id="e3ecd-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ecd-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ecd-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3ecd-136">INPUTS</span></span>

### <span data-ttu-id="e3ecd-137">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="e3ecd-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="e3ecd-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3ecd-138">OUTPUTS</span></span>

### <span data-ttu-id="e3ecd-139">Microsoft.Azure.Commands.SqlsDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="e3ecd-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="e3ecd-140">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="e3ecd-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="e3ecd-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3ecd-141">NOTES</span></span>

## <span data-ttu-id="e3ecd-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3ecd-142">RELATED LINKS</span></span>
