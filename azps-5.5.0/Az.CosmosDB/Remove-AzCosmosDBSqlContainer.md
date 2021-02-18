---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204603"
---
# <span data-ttu-id="685a2-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="685a2-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="685a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="685a2-102">SYNOPSIS</span></span>
<span data-ttu-id="685a2-103">Elimina il contenitore sql per database database.</span><span class="sxs-lookup"><span data-stu-id="685a2-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="685a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="685a2-104">SYNTAX</span></span>

### <span data-ttu-id="685a2-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="685a2-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="685a2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="685a2-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="685a2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="685a2-107">DESCRIPTION</span></span>
<span data-ttu-id="685a2-108">Il cmdlet **Remove-AzCosmosDBSqlContainer** elimina il contenitore Sql DiBDb corrispondente al nome di gruppo di risorse, al nome dell'account, al nome database e al nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="685a2-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="685a2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="685a2-109">EXAMPLES</span></span>

### <span data-ttu-id="685a2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="685a2-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="685a2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="685a2-111">PARAMETERS</span></span>

### <span data-ttu-id="685a2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="685a2-112">-AccountName</span></span>
<span data-ttu-id="685a2-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="685a2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="685a2-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="685a2-114">-Confirm</span></span>
<span data-ttu-id="685a2-115">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="685a2-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="685a2-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="685a2-116">-DatabaseName</span></span>
<span data-ttu-id="685a2-117">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="685a2-117">Database name.</span></span>

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

### <span data-ttu-id="685a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="685a2-118">-DefaultProfile</span></span>
<span data-ttu-id="685a2-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="685a2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="685a2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="685a2-120">-InputObject</span></span>
<span data-ttu-id="685a2-121">Oggetto Contenitore Sql.</span><span class="sxs-lookup"><span data-stu-id="685a2-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="685a2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="685a2-122">-Name</span></span>
<span data-ttu-id="685a2-123">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="685a2-123">Container name.</span></span>

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

### <span data-ttu-id="685a2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="685a2-124">-PassThru</span></span>
<span data-ttu-id="685a2-125">Per essere impostato su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="685a2-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="685a2-126">L'output è true se l'operazione è riuscita e in caso contrario viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="685a2-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="685a2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="685a2-127">-ResourceGroupName</span></span>
<span data-ttu-id="685a2-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="685a2-128">Name of resource group.</span></span>

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

### <span data-ttu-id="685a2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="685a2-129">-WhatIf</span></span>
<span data-ttu-id="685a2-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="685a2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="685a2-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="685a2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="685a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="685a2-132">CommonParameters</span></span>
<span data-ttu-id="685a2-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="685a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="685a2-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="685a2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="685a2-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="685a2-135">INPUTS</span></span>

### <span data-ttu-id="685a2-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="685a2-136">None</span></span>

## <span data-ttu-id="685a2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="685a2-137">OUTPUTS</span></span>

### <span data-ttu-id="685a2-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="685a2-138">System.Void</span></span>

### <span data-ttu-id="685a2-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="685a2-139">System.Boolean</span></span>

## <span data-ttu-id="685a2-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="685a2-140">NOTES</span></span>

## <span data-ttu-id="685a2-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="685a2-141">RELATED LINKS</span></span>
