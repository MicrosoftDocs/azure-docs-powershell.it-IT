---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 7e93042ab376ff0020067a29f9b0642e0ab04de9
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93865536"
---
# <span data-ttu-id="c5860-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="c5860-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="c5860-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5860-102">SYNOPSIS</span></span>
<span data-ttu-id="c5860-103">Crea una nuova ricerca salvata con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="c5860-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="c5860-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5860-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5860-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5860-105">DESCRIPTION</span></span>
<span data-ttu-id="c5860-106">Il cmdlet **New-AzOperationalInsightsSavedSearch** crea una nuova ricerca salvata con i parametri specificati per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c5860-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="c5860-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5860-107">EXAMPLES</span></span>

### <span data-ttu-id="c5860-108">Esempio 1: creare una nuova ricerca salvata</span><span class="sxs-lookup"><span data-stu-id="c5860-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="c5860-109">Questo comando crea una nuova ricerca salvata.</span><span class="sxs-lookup"><span data-stu-id="c5860-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="c5860-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5860-110">PARAMETERS</span></span>

### <span data-ttu-id="c5860-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="c5860-111">-Category</span></span>
<span data-ttu-id="c5860-112">Specifica il nome della categoria.</span><span class="sxs-lookup"><span data-stu-id="c5860-112">Specifies the category name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5860-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5860-113">-DefaultProfile</span></span>
<span data-ttu-id="c5860-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c5860-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5860-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c5860-115">-DisplayName</span></span>
<span data-ttu-id="c5860-116">Specifica il nome visualizzato della ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="c5860-116">Specifies the saved search display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5860-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c5860-117">-Force</span></span>
<span data-ttu-id="c5860-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c5860-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5860-119">-Query</span><span class="sxs-lookup"><span data-stu-id="c5860-119">-Query</span></span>
<span data-ttu-id="c5860-120">Specifica l'espressione di query per la ricerca salvata.</span><span class="sxs-lookup"><span data-stu-id="c5860-120">Specifies the query expression for the saved search.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5860-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5860-121">-ResourceGroupName</span></span>
<span data-ttu-id="c5860-122">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c5860-122">Specifies the resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5860-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="c5860-123">-SavedSearchId</span></span>
<span data-ttu-id="c5860-124">Specifica l'ID ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="c5860-124">Specifies the saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5860-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="c5860-125">-Tag</span></span>
<span data-ttu-id="c5860-126">I tag di ricerca salvati.</span><span class="sxs-lookup"><span data-stu-id="c5860-126">The saved search tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5860-127">-Versione</span><span class="sxs-lookup"><span data-stu-id="c5860-127">-Version</span></span>
<span data-ttu-id="c5860-128">Specifica la versione.</span><span class="sxs-lookup"><span data-stu-id="c5860-128">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5860-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c5860-129">-WorkspaceName</span></span>
<span data-ttu-id="c5860-130">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c5860-130">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5860-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c5860-131">-Confirm</span></span>
<span data-ttu-id="c5860-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5860-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5860-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5860-133">-WhatIf</span></span>
<span data-ttu-id="c5860-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5860-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5860-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5860-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5860-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5860-136">CommonParameters</span></span>
<span data-ttu-id="c5860-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5860-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5860-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5860-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5860-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5860-139">INPUTS</span></span>

### <span data-ttu-id="c5860-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c5860-140">System.String</span></span>

### <span data-ttu-id="c5860-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c5860-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c5860-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="c5860-142">System.Int64</span></span>

## <span data-ttu-id="c5860-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5860-143">OUTPUTS</span></span>

### <span data-ttu-id="c5860-144">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="c5860-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="c5860-145">Note</span><span class="sxs-lookup"><span data-stu-id="c5860-145">NOTES</span></span>

## <span data-ttu-id="c5860-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5860-146">RELATED LINKS</span></span>

[<span data-ttu-id="c5860-147">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="c5860-147">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


