---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: a56a7a091544bef7c66ab26c66c54aded8bebdf1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963149"
---
# <span data-ttu-id="ffc1e-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ffc1e-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="ffc1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffc1e-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc1e-103">Elimina il database Sql database DatabaseDb.</span><span class="sxs-lookup"><span data-stu-id="ffc1e-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="ffc1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ffc1e-104">SYNTAX</span></span>

### <span data-ttu-id="ffc1e-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffc1e-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffc1e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffc1e-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffc1e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ffc1e-107">DESCRIPTION</span></span>
<span data-ttu-id="ffc1e-108">Il cmdlet **Remove-AzCosmosDBSqlDatabase** elimina il database Sql Della BancaDb corrispondente ai valori di ResourceGroupName, AccountName e DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="ffc1e-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="ffc1e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ffc1e-109">EXAMPLES</span></span>

### <span data-ttu-id="ffc1e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ffc1e-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="ffc1e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffc1e-111">PARAMETERS</span></span>

### <span data-ttu-id="ffc1e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ffc1e-112">-AccountName</span></span>
<span data-ttu-id="ffc1e-113">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="ffc1e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ffc1e-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffc1e-114">-Confirm</span></span>
<span data-ttu-id="ffc1e-115">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffc1e-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffc1e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc1e-116">-DefaultProfile</span></span>
<span data-ttu-id="ffc1e-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ffc1e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffc1e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffc1e-118">-InputObject</span></span>
<span data-ttu-id="ffc1e-119">Oggetto database Sql.</span><span class="sxs-lookup"><span data-stu-id="ffc1e-119">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc1e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ffc1e-120">-Name</span></span>
<span data-ttu-id="ffc1e-121">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="ffc1e-121">Database name.</span></span>

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

### <span data-ttu-id="ffc1e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ffc1e-122">-PassThru</span></span>
<span data-ttu-id="ffc1e-123">Per essere impostato su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="ffc1e-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="ffc1e-124">L'output è true se l'operazione è riuscita e in caso contrario viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="ffc1e-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="ffc1e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffc1e-125">-ResourceGroupName</span></span>
<span data-ttu-id="ffc1e-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ffc1e-126">Name of resource group.</span></span>

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

### <span data-ttu-id="ffc1e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffc1e-127">-WhatIf</span></span>
<span data-ttu-id="ffc1e-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ffc1e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffc1e-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ffc1e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffc1e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc1e-130">CommonParameters</span></span>
<span data-ttu-id="ffc1e-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffc1e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc1e-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ffc1e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc1e-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="ffc1e-133">INPUTS</span></span>

### <span data-ttu-id="ffc1e-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ffc1e-134">None</span></span>

## <span data-ttu-id="ffc1e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ffc1e-135">OUTPUTS</span></span>

### <span data-ttu-id="ffc1e-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="ffc1e-136">System.Void</span></span>

### <span data-ttu-id="ffc1e-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ffc1e-137">System.Boolean</span></span>

## <span data-ttu-id="ffc1e-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="ffc1e-138">NOTES</span></span>

## <span data-ttu-id="ffc1e-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ffc1e-139">RELATED LINKS</span></span>
