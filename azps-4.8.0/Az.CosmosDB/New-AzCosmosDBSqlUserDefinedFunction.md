---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: cc7c443ad4447abfa1c31ebb335d3d1ae602f1b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192572"
---
# <span data-ttu-id="2fe3e-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="2fe3e-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="2fe3e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fe3e-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe3e-103">Crea un nuovo CosmosDB SQL.</span><span class="sxs-lookup"><span data-stu-id="2fe3e-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="2fe3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fe3e-104">SYNTAX</span></span>

### <span data-ttu-id="2fe3e-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2fe3e-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fe3e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fe3e-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fe3e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fe3e-107">DESCRIPTION</span></span>
<span data-ttu-id="2fe3e-108">Crea un nuovo CosmosDB SQL.</span><span class="sxs-lookup"><span data-stu-id="2fe3e-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="2fe3e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fe3e-109">EXAMPLES</span></span>

### <span data-ttu-id="2fe3e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2fe3e-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="2fe3e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fe3e-111">PARAMETERS</span></span>

### <span data-ttu-id="2fe3e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2fe3e-112">-AccountName</span></span>
<span data-ttu-id="2fe3e-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="2fe3e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2fe3e-114">-Body</span><span class="sxs-lookup"><span data-stu-id="2fe3e-114">-Body</span></span>
<span data-ttu-id="2fe3e-115">Il corpo della funzione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2fe3e-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="2fe3e-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2fe3e-116">-Confirm</span></span>
<span data-ttu-id="2fe3e-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fe3e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fe3e-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="2fe3e-118">-ContainerName</span></span>
<span data-ttu-id="2fe3e-119">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="2fe3e-119">Container name.</span></span>

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

### <span data-ttu-id="2fe3e-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2fe3e-120">-DatabaseName</span></span>
<span data-ttu-id="2fe3e-121">Nome database.</span><span class="sxs-lookup"><span data-stu-id="2fe3e-121">Database name.</span></span>

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

### <span data-ttu-id="2fe3e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fe3e-122">-DefaultProfile</span></span>
<span data-ttu-id="2fe3e-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2fe3e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fe3e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fe3e-124">-Name</span></span>
<span data-ttu-id="2fe3e-125">Nome della funzione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2fe3e-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="2fe3e-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2fe3e-126">-ParentObject</span></span>
<span data-ttu-id="2fe3e-127">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="2fe3e-127">Sql Container object.</span></span>

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

### <span data-ttu-id="2fe3e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fe3e-128">-ResourceGroupName</span></span>
<span data-ttu-id="2fe3e-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2fe3e-129">Name of resource group.</span></span>

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

### <span data-ttu-id="2fe3e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fe3e-130">-WhatIf</span></span>
<span data-ttu-id="2fe3e-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fe3e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fe3e-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fe3e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fe3e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe3e-133">CommonParameters</span></span>
<span data-ttu-id="2fe3e-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fe3e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe3e-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fe3e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe3e-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fe3e-136">INPUTS</span></span>

### <span data-ttu-id="2fe3e-137">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="2fe3e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="2fe3e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fe3e-138">OUTPUTS</span></span>

### <span data-ttu-id="2fe3e-139">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="2fe3e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="2fe3e-140">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="2fe3e-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="2fe3e-141">Note</span><span class="sxs-lookup"><span data-stu-id="2fe3e-141">NOTES</span></span>

## <span data-ttu-id="2fe3e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fe3e-142">RELATED LINKS</span></span>
