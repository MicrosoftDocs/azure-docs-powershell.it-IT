---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 6a1c155a33ef704895a76dc35bf342aa47cd47ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177230"
---
# <span data-ttu-id="e25f1-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="e25f1-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="e25f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e25f1-102">SYNOPSIS</span></span>
<span data-ttu-id="e25f1-103">{{ Fill in the Synopsis }}</span><span class="sxs-lookup"><span data-stu-id="e25f1-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="e25f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e25f1-104">SYNTAX</span></span>

### <span data-ttu-id="e25f1-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e25f1-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e25f1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e25f1-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e25f1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e25f1-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e25f1-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e25f1-108">DESCRIPTION</span></span>
<span data-ttu-id="e25f1-109">{{ Compila la descrizione }}</span><span class="sxs-lookup"><span data-stu-id="e25f1-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="e25f1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e25f1-110">EXAMPLES</span></span>

### <span data-ttu-id="e25f1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e25f1-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="e25f1-112">FailoverPolicies aggiornato con region1 come FailoverPriority 1, region2 come FailoverPriority 2 e region3 come FailoverPriority 3.</span><span class="sxs-lookup"><span data-stu-id="e25f1-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="e25f1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e25f1-113">PARAMETERS</span></span>

### <span data-ttu-id="e25f1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e25f1-114">-AsJob</span></span>
<span data-ttu-id="e25f1-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e25f1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e25f1-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e25f1-116">-Confirm</span></span>
<span data-ttu-id="e25f1-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e25f1-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e25f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e25f1-118">-DefaultProfile</span></span>
<span data-ttu-id="e25f1-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e25f1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e25f1-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="e25f1-120">-FailoverPolicy</span></span>
<span data-ttu-id="e25f1-121">Matrice di stringhe con nomi di aree, ordinate in base alla priorità di failover.</span><span class="sxs-lookup"><span data-stu-id="e25f1-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="e25f1-122">Ad esempio eastus, westus</span><span class="sxs-lookup"><span data-stu-id="e25f1-122">E.g eastus, westus</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25f1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e25f1-123">-InputObject</span></span>
<span data-ttu-id="e25f1-124">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="e25f1-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e25f1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e25f1-125">-Name</span></span>
<span data-ttu-id="e25f1-126">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="e25f1-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e25f1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e25f1-127">-ResourceGroupName</span></span>
<span data-ttu-id="e25f1-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e25f1-128">Name of resource group.</span></span>

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

### <span data-ttu-id="e25f1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e25f1-129">-ResourceId</span></span>
<span data-ttu-id="e25f1-130">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e25f1-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="e25f1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e25f1-131">-WhatIf</span></span>
<span data-ttu-id="e25f1-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e25f1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e25f1-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e25f1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e25f1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e25f1-134">CommonParameters</span></span>
<span data-ttu-id="e25f1-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e25f1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e25f1-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e25f1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e25f1-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="e25f1-137">INPUTS</span></span>

### <span data-ttu-id="e25f1-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e25f1-138">None</span></span>

## <span data-ttu-id="e25f1-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e25f1-139">OUTPUTS</span></span>

### <span data-ttu-id="e25f1-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="e25f1-140">System.Void</span></span>

## <span data-ttu-id="e25f1-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="e25f1-141">NOTES</span></span>

## <span data-ttu-id="e25f1-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e25f1-142">RELATED LINKS</span></span>
