---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: cba56fd21263d4accba296cd7aab181f18b09200
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989909"
---
# <span data-ttu-id="db693-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="db693-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="db693-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db693-102">SYNOPSIS</span></span>
<span data-ttu-id="db693-103">Crea una nuova ricerca salvata con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="db693-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="db693-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db693-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db693-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="db693-105">DESCRIPTION</span></span>
<span data-ttu-id="db693-106">Il cmdlet **New-AzOperationalInsightsSavedSearch** crea una nuova ricerca salvata con i parametri specificati per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="db693-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="db693-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db693-107">EXAMPLES</span></span>

### <span data-ttu-id="db693-108">Esempio 1: Creare una nuova ricerca salvata</span><span class="sxs-lookup"><span data-stu-id="db693-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="db693-109">Questo comando crea una nuova ricerca salvata.</span><span class="sxs-lookup"><span data-stu-id="db693-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="db693-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db693-110">PARAMETERS</span></span>

### <span data-ttu-id="db693-111">-Category</span><span class="sxs-lookup"><span data-stu-id="db693-111">-Category</span></span>
<span data-ttu-id="db693-112">Specifica il nome della categoria.</span><span class="sxs-lookup"><span data-stu-id="db693-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="db693-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db693-113">-DefaultProfile</span></span>
<span data-ttu-id="db693-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="db693-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db693-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="db693-115">-DisplayName</span></span>
<span data-ttu-id="db693-116">Specifica il nome visualizzato della ricerca salvata.</span><span class="sxs-lookup"><span data-stu-id="db693-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="db693-117">-Force</span><span class="sxs-lookup"><span data-stu-id="db693-117">-Force</span></span>
<span data-ttu-id="db693-118">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="db693-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="db693-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="db693-119">-FunctionAlias</span></span>
<span data-ttu-id="db693-120">L'alias della funzione se la query funge da funzione.</span><span class="sxs-lookup"><span data-stu-id="db693-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db693-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="db693-121">-FunctionParameter</span></span>
<span data-ttu-id="db693-122">I parametri facoltativi della funzione se la query funge da funzione.</span><span class="sxs-lookup"><span data-stu-id="db693-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="db693-123">Il valore deve essere nel formato seguente: 'nome-parametro1:tipo1 = default_value1, param-nome2:tipo2 = default_value2'.</span><span class="sxs-lookup"><span data-stu-id="db693-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="db693-124">Per altri esempi e la sintassi corretta, vedere https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="db693-124">For more examples and proper syntax please refer to https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db693-125">-Query</span><span class="sxs-lookup"><span data-stu-id="db693-125">-Query</span></span>
<span data-ttu-id="db693-126">Specifica l'espressione di query per la ricerca salvata.</span><span class="sxs-lookup"><span data-stu-id="db693-126">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="db693-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db693-127">-ResourceGroupName</span></span>
<span data-ttu-id="db693-128">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db693-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="db693-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="db693-129">-SavedSearchId</span></span>
<span data-ttu-id="db693-130">Specifica l'ID di ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="db693-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="db693-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="db693-131">-Tag</span></span>
<span data-ttu-id="db693-132">I tag di ricerca salvati.</span><span class="sxs-lookup"><span data-stu-id="db693-132">The saved search tags.</span></span>

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

### <span data-ttu-id="db693-133">-Version</span><span class="sxs-lookup"><span data-stu-id="db693-133">-Version</span></span>
<span data-ttu-id="db693-134">Specifica la versione.</span><span class="sxs-lookup"><span data-stu-id="db693-134">Specifies the version.</span></span>

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

### <span data-ttu-id="db693-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="db693-135">-WorkspaceName</span></span>
<span data-ttu-id="db693-136">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="db693-136">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="db693-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db693-137">-Confirm</span></span>
<span data-ttu-id="db693-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db693-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db693-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db693-139">-WhatIf</span></span>
<span data-ttu-id="db693-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db693-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db693-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db693-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db693-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db693-142">CommonParameters</span></span>
<span data-ttu-id="db693-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db693-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db693-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="db693-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db693-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="db693-145">INPUTS</span></span>

### <span data-ttu-id="db693-146">System.String</span><span class="sxs-lookup"><span data-stu-id="db693-146">System.String</span></span>

### <span data-ttu-id="db693-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="db693-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="db693-148">System.Int64</span><span class="sxs-lookup"><span data-stu-id="db693-148">System.Int64</span></span>

## <span data-ttu-id="db693-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db693-149">OUTPUTS</span></span>

### <span data-ttu-id="db693-150">System.Net.HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="db693-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="db693-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="db693-151">NOTES</span></span>

## <span data-ttu-id="db693-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db693-152">RELATED LINKS</span></span>

[<span data-ttu-id="db693-153">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="db693-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


