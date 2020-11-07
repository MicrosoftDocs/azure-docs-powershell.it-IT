---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 5853447dfc91511782e99ebafae644e14b6649b3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685384"
---
# <span data-ttu-id="aaedf-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="aaedf-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="aaedf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aaedf-102">SYNOPSIS</span></span>
<span data-ttu-id="aaedf-103">Crea una nuova ricerca salvata con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="aaedf-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="aaedf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aaedf-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aaedf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aaedf-105">DESCRIPTION</span></span>
<span data-ttu-id="aaedf-106">Il cmdlet **New-AzOperationalInsightsSavedSearch** crea una nuova ricerca salvata con i parametri specificati per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="aaedf-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="aaedf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aaedf-107">EXAMPLES</span></span>

### <span data-ttu-id="aaedf-108">Esempio 1: creare una nuova ricerca salvata</span><span class="sxs-lookup"><span data-stu-id="aaedf-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="aaedf-109">Questo comando crea una nuova ricerca salvata.</span><span class="sxs-lookup"><span data-stu-id="aaedf-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="aaedf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aaedf-110">PARAMETERS</span></span>

### <span data-ttu-id="aaedf-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="aaedf-111">-Category</span></span>
<span data-ttu-id="aaedf-112">Specifica il nome della categoria.</span><span class="sxs-lookup"><span data-stu-id="aaedf-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="aaedf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaedf-113">-DefaultProfile</span></span>
<span data-ttu-id="aaedf-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="aaedf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aaedf-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="aaedf-115">-DisplayName</span></span>
<span data-ttu-id="aaedf-116">Specifica il nome visualizzato della ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="aaedf-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="aaedf-117">-Force</span><span class="sxs-lookup"><span data-stu-id="aaedf-117">-Force</span></span>
<span data-ttu-id="aaedf-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="aaedf-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aaedf-119">-Query</span><span class="sxs-lookup"><span data-stu-id="aaedf-119">-Query</span></span>
<span data-ttu-id="aaedf-120">Specifica il nome della query.</span><span class="sxs-lookup"><span data-stu-id="aaedf-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="aaedf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaedf-121">-ResourceGroupName</span></span>
<span data-ttu-id="aaedf-122">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aaedf-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="aaedf-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="aaedf-123">-SavedSearchId</span></span>
<span data-ttu-id="aaedf-124">Specifica l'ID ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="aaedf-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="aaedf-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="aaedf-125">-Tag</span></span>
<span data-ttu-id="aaedf-126">I tag di ricerca salvati.</span><span class="sxs-lookup"><span data-stu-id="aaedf-126">The saved search tags.</span></span>

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

### <span data-ttu-id="aaedf-127">-Versione</span><span class="sxs-lookup"><span data-stu-id="aaedf-127">-Version</span></span>
<span data-ttu-id="aaedf-128">Specifica la versione.</span><span class="sxs-lookup"><span data-stu-id="aaedf-128">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaedf-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aaedf-129">-WorkspaceName</span></span>
<span data-ttu-id="aaedf-130">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="aaedf-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="aaedf-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aaedf-131">-Confirm</span></span>
<span data-ttu-id="aaedf-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaedf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaedf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaedf-133">-WhatIf</span></span>
<span data-ttu-id="aaedf-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aaedf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaedf-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aaedf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaedf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaedf-136">CommonParameters</span></span>
<span data-ttu-id="aaedf-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaedf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaedf-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaedf-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaedf-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aaedf-139">INPUTS</span></span>

### <span data-ttu-id="aaedf-140">System. String</span><span class="sxs-lookup"><span data-stu-id="aaedf-140">System.String</span></span>

### <span data-ttu-id="aaedf-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="aaedf-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="aaedf-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="aaedf-142">System.Int64</span></span>

## <span data-ttu-id="aaedf-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aaedf-143">OUTPUTS</span></span>

### <span data-ttu-id="aaedf-144">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="aaedf-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="aaedf-145">Note</span><span class="sxs-lookup"><span data-stu-id="aaedf-145">NOTES</span></span>

## <span data-ttu-id="aaedf-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aaedf-146">RELATED LINKS</span></span>

[<span data-ttu-id="aaedf-147">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="aaedf-147">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


