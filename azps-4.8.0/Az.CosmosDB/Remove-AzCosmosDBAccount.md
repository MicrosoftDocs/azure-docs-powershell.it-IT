---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: d10ed161ddab638e32126374d106eeffe3969a8e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190817"
---
# <span data-ttu-id="16735-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="16735-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="16735-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16735-102">SYNOPSIS</span></span>
<span data-ttu-id="16735-103">Rimuovere un account di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="16735-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="16735-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16735-104">SYNTAX</span></span>

### <span data-ttu-id="16735-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="16735-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16735-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16735-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16735-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16735-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16735-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16735-108">DESCRIPTION</span></span>
<span data-ttu-id="16735-109">Rimuovere un account di CosmosDB con un nome specifico nella ResourceGroup specificata.</span><span class="sxs-lookup"><span data-stu-id="16735-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="16735-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16735-110">EXAMPLES</span></span>

### <span data-ttu-id="16735-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="16735-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="16735-112">L'account con nome account dbname in ResourceGroup RG viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="16735-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="16735-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16735-113">PARAMETERS</span></span>

### <span data-ttu-id="16735-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16735-114">-AsJob</span></span>
<span data-ttu-id="16735-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="16735-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16735-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="16735-116">-Confirm</span></span>
<span data-ttu-id="16735-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16735-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16735-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16735-118">-DefaultProfile</span></span>
<span data-ttu-id="16735-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16735-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16735-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16735-120">-InputObject</span></span>
<span data-ttu-id="16735-121">Oggetto account di database</span><span class="sxs-lookup"><span data-stu-id="16735-121">The Database Account object</span></span>

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

### <span data-ttu-id="16735-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="16735-122">-Name</span></span>
<span data-ttu-id="16735-123">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="16735-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="16735-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16735-124">-PassThru</span></span>
<span data-ttu-id="16735-125">Da impostare su true se l'utente vuole ricevere un output.</span><span class="sxs-lookup"><span data-stu-id="16735-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="16735-126">L'output è true se l'operazione è stata eseguita correttamente e se non viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="16735-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="16735-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16735-127">-ResourceGroupName</span></span>
<span data-ttu-id="16735-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="16735-128">Name of resource group.</span></span>

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

### <span data-ttu-id="16735-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16735-129">-ResourceId</span></span>
<span data-ttu-id="16735-130">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="16735-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="16735-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16735-131">-WhatIf</span></span>
<span data-ttu-id="16735-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16735-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16735-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16735-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16735-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16735-134">CommonParameters</span></span>
<span data-ttu-id="16735-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16735-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16735-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16735-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16735-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16735-137">INPUTS</span></span>

### <span data-ttu-id="16735-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="16735-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="16735-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16735-139">OUTPUTS</span></span>

### <span data-ttu-id="16735-140">System. void</span><span class="sxs-lookup"><span data-stu-id="16735-140">System.Void</span></span>

## <span data-ttu-id="16735-141">Note</span><span class="sxs-lookup"><span data-stu-id="16735-141">NOTES</span></span>

## <span data-ttu-id="16735-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16735-142">RELATED LINKS</span></span>