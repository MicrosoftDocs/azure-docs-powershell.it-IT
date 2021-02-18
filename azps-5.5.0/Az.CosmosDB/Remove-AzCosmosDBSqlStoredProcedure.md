---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 6abad7d11da1ba73f1f34804c32bddeb779b0b1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204578"
---
# <span data-ttu-id="ad1b6-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="ad1b6-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="ad1b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad1b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ad1b6-103">Elimina il database di database sql storedprocedure.</span><span class="sxs-lookup"><span data-stu-id="ad1b6-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="ad1b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad1b6-104">SYNTAX</span></span>

### <span data-ttu-id="ad1b6-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad1b6-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad1b6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad1b6-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad1b6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ad1b6-107">DESCRIPTION</span></span>
<span data-ttu-id="ad1b6-108">Il cmdlet **Remove-AzCosmosDBSqlStoredProcedure** elimina il cmdletSqlDb Sql StoredProcedure corrispondente ai valori ResourceGroupName, AccountName e DatabaseName corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="ad1b6-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="ad1b6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad1b6-109">EXAMPLES</span></span>

### <span data-ttu-id="ad1b6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ad1b6-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="ad1b6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad1b6-111">PARAMETERS</span></span>

### <span data-ttu-id="ad1b6-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ad1b6-112">-AccountName</span></span>
<span data-ttu-id="ad1b6-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="ad1b6-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ad1b6-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad1b6-114">-Confirm</span></span>
<span data-ttu-id="ad1b6-115">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad1b6-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad1b6-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ad1b6-116">-ContainerName</span></span>
<span data-ttu-id="ad1b6-117">Nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="ad1b6-117">Container name.</span></span>

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

### <span data-ttu-id="ad1b6-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ad1b6-118">-DatabaseName</span></span>
<span data-ttu-id="ad1b6-119">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="ad1b6-119">Database name.</span></span>

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

### <span data-ttu-id="ad1b6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad1b6-120">-DefaultProfile</span></span>
<span data-ttu-id="ad1b6-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad1b6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad1b6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad1b6-122">-InputObject</span></span>
<span data-ttu-id="ad1b6-123">Oggetto Database Sql.</span><span class="sxs-lookup"><span data-stu-id="ad1b6-123">Sql Database object.</span></span>

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

### <span data-ttu-id="ad1b6-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ad1b6-124">-Name</span></span>
<span data-ttu-id="ad1b6-125">Nome Prcodecure archiviato.</span><span class="sxs-lookup"><span data-stu-id="ad1b6-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="ad1b6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad1b6-126">-PassThru</span></span>
<span data-ttu-id="ad1b6-127">Per essere impostato su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="ad1b6-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="ad1b6-128">L'output è true se l'operazione è riuscita e in caso contrario viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="ad1b6-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="ad1b6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad1b6-129">-ResourceGroupName</span></span>
<span data-ttu-id="ad1b6-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad1b6-130">Name of resource group.</span></span>

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

### <span data-ttu-id="ad1b6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad1b6-131">-WhatIf</span></span>
<span data-ttu-id="ad1b6-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad1b6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad1b6-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad1b6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad1b6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad1b6-134">CommonParameters</span></span>
<span data-ttu-id="ad1b6-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad1b6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad1b6-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ad1b6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad1b6-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="ad1b6-137">INPUTS</span></span>

### <span data-ttu-id="ad1b6-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ad1b6-138">None</span></span>

## <span data-ttu-id="ad1b6-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad1b6-139">OUTPUTS</span></span>

### <span data-ttu-id="ad1b6-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="ad1b6-140">System.Void</span></span>

### <span data-ttu-id="ad1b6-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ad1b6-141">System.Boolean</span></span>

## <span data-ttu-id="ad1b6-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="ad1b6-142">NOTES</span></span>

## <span data-ttu-id="ad1b6-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad1b6-143">RELATED LINKS</span></span>
