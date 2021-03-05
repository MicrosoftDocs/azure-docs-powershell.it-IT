---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
ms.openlocfilehash: ff294af7e4305facd3265d96151c97b82ff9c052
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010750"
---
# <span data-ttu-id="e5679-101">Remove-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="e5679-101">Remove-AzCosmosDBTable</span></span>

## <span data-ttu-id="e5679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5679-102">SYNOPSIS</span></span>
<span data-ttu-id="e5679-103">Elimina la tabella AMMORT.</span><span class="sxs-lookup"><span data-stu-id="e5679-103">Deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="e5679-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5679-104">SYNTAX</span></span>

### <span data-ttu-id="e5679-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5679-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBTable -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5679-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5679-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBTable -InputObject <PSTableGetResults> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5679-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e5679-107">DESCRIPTION</span></span>
<span data-ttu-id="e5679-108">Il cmdlet **Remove-AzCosmosDBTable** elimina la tabellaDbDb.</span><span class="sxs-lookup"><span data-stu-id="e5679-108">The **Remove-AzCosmosDBTable** cmdlet deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="e5679-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5679-109">EXAMPLES</span></span>

### <span data-ttu-id="e5679-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e5679-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}
```

<span data-ttu-id="e5679-111">Il cmdlet restituisce un oggetto di tipo bool(when -PassThru is passed), che è true se l'eliminazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="e5679-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="e5679-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5679-112">PARAMETERS</span></span>

### <span data-ttu-id="e5679-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e5679-113">-AccountName</span></span>
<span data-ttu-id="e5679-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="e5679-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e5679-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5679-115">-Confirm</span></span>
<span data-ttu-id="e5679-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5679-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5679-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5679-117">-DefaultProfile</span></span>
<span data-ttu-id="e5679-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5679-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5679-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5679-119">-InputObject</span></span>
<span data-ttu-id="e5679-120">Oggetto Database Sql.</span><span class="sxs-lookup"><span data-stu-id="e5679-120">Sql Database object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5679-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e5679-121">-Name</span></span>
<span data-ttu-id="e5679-122">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="e5679-122">Name of the Table.</span></span>

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

### <span data-ttu-id="e5679-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5679-123">-PassThru</span></span>
<span data-ttu-id="e5679-124">Per essere impostato su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="e5679-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="e5679-125">L'output è true se l'operazione è riuscita e in caso contrario viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="e5679-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="e5679-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5679-126">-ResourceGroupName</span></span>
<span data-ttu-id="e5679-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e5679-127">Name of resource group.</span></span>

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

### <span data-ttu-id="e5679-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5679-128">-WhatIf</span></span>
<span data-ttu-id="e5679-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5679-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5679-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5679-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5679-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5679-131">CommonParameters</span></span>
<span data-ttu-id="e5679-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5679-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5679-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e5679-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5679-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="e5679-134">INPUTS</span></span>

### <span data-ttu-id="e5679-135">Microsoft.Azure.Commands.EnterpriseDb.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="e5679-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="e5679-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5679-136">OUTPUTS</span></span>

### <span data-ttu-id="e5679-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="e5679-137">System.Void</span></span>

### <span data-ttu-id="e5679-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e5679-138">System.Boolean</span></span>

## <span data-ttu-id="e5679-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="e5679-139">NOTES</span></span>

## <span data-ttu-id="e5679-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5679-140">RELATED LINKS</span></span>
