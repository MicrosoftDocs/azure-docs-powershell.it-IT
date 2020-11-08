---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
ms.openlocfilehash: a9cea343a67e7e23e820c0995484aab9a1434f90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019875"
---
# <span data-ttu-id="6de5f-101">New-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="6de5f-101">New-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="6de5f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6de5f-102">SYNOPSIS</span></span>
<span data-ttu-id="6de5f-103">Rigenerare una determinata chiave dell'account di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="6de5f-103">Regenerate a given CosmosDB Account Key.</span></span>

## <span data-ttu-id="6de5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6de5f-104">SYNTAX</span></span>

### <span data-ttu-id="6de5f-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6de5f-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-KeyKind <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6de5f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6de5f-106">ByResourceIdParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6de5f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6de5f-107">ByObjectParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -InputObject <PSDatabaseAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6de5f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6de5f-108">DESCRIPTION</span></span>
<span data-ttu-id="6de5f-109">Creare un nuovo account di CosmosDB nella ResourceGroup specificata.</span><span class="sxs-lookup"><span data-stu-id="6de5f-109">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="6de5f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6de5f-110">EXAMPLES</span></span>

### <span data-ttu-id="6de5f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6de5f-111">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccountKey -ResourceGroupName rg -Name dbname
```

<span data-ttu-id="6de5f-112">Le nuove chiavi vengono generate per account con il nome dell'account dbname in ResourceGroup RG.</span><span class="sxs-lookup"><span data-stu-id="6de5f-112">New keys are generated for Account with account name dbname in ResourceGroup rg.</span></span>

## <span data-ttu-id="6de5f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6de5f-113">PARAMETERS</span></span>

### <span data-ttu-id="6de5f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6de5f-114">-AsJob</span></span>
<span data-ttu-id="6de5f-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6de5f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6de5f-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6de5f-116">-Confirm</span></span>
<span data-ttu-id="6de5f-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6de5f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6de5f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de5f-118">-DefaultProfile</span></span>
<span data-ttu-id="6de5f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6de5f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6de5f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6de5f-120">-InputObject</span></span>
<span data-ttu-id="6de5f-121">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="6de5f-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6de5f-122">-Tipi di tipo</span><span class="sxs-lookup"><span data-stu-id="6de5f-122">-KeyKind</span></span>
<span data-ttu-id="6de5f-123">Il tasto di scelta per la rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="6de5f-123">The access key to regenerate.</span></span>
<span data-ttu-id="6de5f-124">Valori accettati: Primary, primaryReadonly, Secondary, secondaryReadonly</span><span class="sxs-lookup"><span data-stu-id="6de5f-124">Accepted values: primary, primaryReadonly, secondary, secondaryReadonly</span></span>

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

### <span data-ttu-id="6de5f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="6de5f-125">-Name</span></span>
<span data-ttu-id="6de5f-126">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="6de5f-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6de5f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6de5f-127">-ResourceGroupName</span></span>
<span data-ttu-id="6de5f-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6de5f-128">Name of resource group.</span></span>

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

### <span data-ttu-id="6de5f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6de5f-129">-ResourceId</span></span>
<span data-ttu-id="6de5f-130">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6de5f-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="6de5f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6de5f-131">-WhatIf</span></span>
<span data-ttu-id="6de5f-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6de5f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6de5f-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6de5f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6de5f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de5f-134">CommonParameters</span></span>
<span data-ttu-id="6de5f-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de5f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de5f-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6de5f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de5f-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6de5f-137">INPUTS</span></span>

### <span data-ttu-id="6de5f-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6de5f-138">None</span></span>

## <span data-ttu-id="6de5f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6de5f-139">OUTPUTS</span></span>

### <span data-ttu-id="6de5f-140">System. void</span><span class="sxs-lookup"><span data-stu-id="6de5f-140">System.Void</span></span>

## <span data-ttu-id="6de5f-141">Note</span><span class="sxs-lookup"><span data-stu-id="6de5f-141">NOTES</span></span>

## <span data-ttu-id="6de5f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6de5f-142">RELATED LINKS</span></span>
