---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192144"
---
# <span data-ttu-id="a5815-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="a5815-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="a5815-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5815-102">SYNOPSIS</span></span>
<span data-ttu-id="a5815-103">Aggiorna il CosmosDB SQL.</span><span class="sxs-lookup"><span data-stu-id="a5815-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="a5815-104">Consente di eseguire un'operazione di patch lato client leggendo il valore esistente.</span><span class="sxs-lookup"><span data-stu-id="a5815-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="a5815-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5815-105">SYNTAX</span></span>

### <span data-ttu-id="a5815-106">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a5815-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5815-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5815-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5815-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5815-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5815-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5815-109">DESCRIPTION</span></span>
<span data-ttu-id="a5815-110">Aggiorna il CosmosDB SQL.</span><span class="sxs-lookup"><span data-stu-id="a5815-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="a5815-111">Consente di eseguire un'operazione di patch lato client leggendo il valore esistente.</span><span class="sxs-lookup"><span data-stu-id="a5815-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="a5815-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5815-112">EXAMPLES</span></span>

### <span data-ttu-id="a5815-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a5815-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="a5815-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5815-114">PARAMETERS</span></span>

### <span data-ttu-id="a5815-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a5815-115">-AccountName</span></span>
<span data-ttu-id="a5815-116">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="a5815-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a5815-117">-Body</span><span class="sxs-lookup"><span data-stu-id="a5815-117">-Body</span></span>
<span data-ttu-id="a5815-118">Il corpo della funzione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a5815-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="a5815-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a5815-119">-Confirm</span></span>
<span data-ttu-id="a5815-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5815-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5815-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a5815-121">-ContainerName</span></span>
<span data-ttu-id="a5815-122">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="a5815-122">Container name.</span></span>

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

### <span data-ttu-id="a5815-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a5815-123">-DatabaseName</span></span>
<span data-ttu-id="a5815-124">Nome database.</span><span class="sxs-lookup"><span data-stu-id="a5815-124">Database name.</span></span>

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

### <span data-ttu-id="a5815-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5815-125">-DefaultProfile</span></span>
<span data-ttu-id="a5815-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5815-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5815-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5815-127">-InputObject</span></span>
<span data-ttu-id="a5815-128">Oggetto funzione definito dall'utente SQL</span><span class="sxs-lookup"><span data-stu-id="a5815-128">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="a5815-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5815-129">-Name</span></span>
<span data-ttu-id="a5815-130">Nome della funzione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a5815-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="a5815-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a5815-131">-ParentObject</span></span>
<span data-ttu-id="a5815-132">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="a5815-132">Sql Container object.</span></span>

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

### <span data-ttu-id="a5815-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5815-133">-ResourceGroupName</span></span>
<span data-ttu-id="a5815-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a5815-134">Name of resource group.</span></span>

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

### <span data-ttu-id="a5815-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5815-135">-WhatIf</span></span>
<span data-ttu-id="a5815-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5815-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5815-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5815-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5815-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5815-138">CommonParameters</span></span>
<span data-ttu-id="a5815-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5815-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5815-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5815-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5815-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5815-141">INPUTS</span></span>

### <span data-ttu-id="a5815-142">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="a5815-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="a5815-143">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="a5815-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="a5815-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5815-144">OUTPUTS</span></span>

### <span data-ttu-id="a5815-145">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="a5815-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="a5815-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="a5815-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="a5815-147">Note</span><span class="sxs-lookup"><span data-stu-id="a5815-147">NOTES</span></span>

## <span data-ttu-id="a5815-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5815-148">RELATED LINKS</span></span>
