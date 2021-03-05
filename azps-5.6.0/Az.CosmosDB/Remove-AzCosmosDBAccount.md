---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: 64d6f0bd604e8074d593f20a572768b54ced8a59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960782"
---
# <span data-ttu-id="25788-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="25788-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="25788-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25788-102">SYNOPSIS</span></span>
<span data-ttu-id="25788-103">Rimuovere un account diDbDb.</span><span class="sxs-lookup"><span data-stu-id="25788-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="25788-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25788-104">SYNTAX</span></span>

### <span data-ttu-id="25788-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="25788-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25788-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25788-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25788-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25788-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25788-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="25788-108">DESCRIPTION</span></span>
<span data-ttu-id="25788-109">Rimuovere un accountDbDb con un nome specificato nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="25788-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="25788-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25788-110">EXAMPLES</span></span>

### <span data-ttu-id="25788-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="25788-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="25788-112">L'account con nome account dbname in ResourceGroup rg viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="25788-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="25788-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25788-113">PARAMETERS</span></span>

### <span data-ttu-id="25788-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25788-114">-AsJob</span></span>
<span data-ttu-id="25788-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="25788-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25788-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25788-116">-Confirm</span></span>
<span data-ttu-id="25788-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25788-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25788-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25788-118">-DefaultProfile</span></span>
<span data-ttu-id="25788-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25788-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25788-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25788-120">-InputObject</span></span>
<span data-ttu-id="25788-121">Oggetto Account di database</span><span class="sxs-lookup"><span data-stu-id="25788-121">The Database Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25788-122">-Name</span><span class="sxs-lookup"><span data-stu-id="25788-122">-Name</span></span>
<span data-ttu-id="25788-123">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="25788-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="25788-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25788-124">-PassThru</span></span>
<span data-ttu-id="25788-125">Per essere impostato su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="25788-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="25788-126">L'output è true se l'operazione è riuscita e in caso contrario viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="25788-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="25788-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25788-127">-ResourceGroupName</span></span>
<span data-ttu-id="25788-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="25788-128">Name of resource group.</span></span>

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

### <span data-ttu-id="25788-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25788-129">-ResourceId</span></span>
<span data-ttu-id="25788-130">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="25788-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25788-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25788-131">-WhatIf</span></span>
<span data-ttu-id="25788-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25788-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25788-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25788-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25788-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25788-134">CommonParameters</span></span>
<span data-ttu-id="25788-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25788-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25788-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="25788-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25788-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="25788-137">INPUTS</span></span>

### <span data-ttu-id="25788-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="25788-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="25788-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25788-139">OUTPUTS</span></span>

### <span data-ttu-id="25788-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="25788-140">System.Void</span></span>

## <span data-ttu-id="25788-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="25788-141">NOTES</span></span>

## <span data-ttu-id="25788-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25788-142">RELATED LINKS</span></span>
