---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 3426b93ec9551ba6218634fa87adeff09b5872af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032878"
---
# <span data-ttu-id="f3dc4-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="f3dc4-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="f3dc4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="f3dc4-103">Crea una nuova ricerca salvata con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="f3dc4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3dc4-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3dc4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3dc4-105">DESCRIPTION</span></span>
<span data-ttu-id="f3dc4-106">Il cmdlet **New-AzOperationalInsightsSavedSearch** crea una nuova ricerca salvata con i parametri specificati per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="f3dc4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3dc4-107">EXAMPLES</span></span>

### <span data-ttu-id="f3dc4-108">Esempio 1: creare una nuova ricerca salvata</span><span class="sxs-lookup"><span data-stu-id="f3dc4-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="f3dc4-109">Questo comando crea una nuova ricerca salvata.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="f3dc4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3dc4-110">PARAMETERS</span></span>

### <span data-ttu-id="f3dc4-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="f3dc4-111">-Category</span></span>
<span data-ttu-id="f3dc4-112">Specifica il nome della categoria.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="f3dc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3dc4-113">-DefaultProfile</span></span>
<span data-ttu-id="f3dc4-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f3dc4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3dc4-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f3dc4-115">-DisplayName</span></span>
<span data-ttu-id="f3dc4-116">Specifica il nome visualizzato della ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="f3dc4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f3dc4-117">-Force</span></span>
<span data-ttu-id="f3dc4-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f3dc4-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="f3dc4-119">-FunctionAlias</span></span>
<span data-ttu-id="f3dc4-120">L'alias di funzione se query funge da funzione.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="f3dc4-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="f3dc4-121">-FunctionParameter</span></span>
<span data-ttu-id="f3dc4-122">I parametri di funzione facoltativi se query funge da funzione.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="f3dc4-123">Il valore deve essere il formato seguente:' param-name1: tipo1 = default_value1, param-name2: tipo2 = default_value2'.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="f3dc4-124">Per altri esempi e per la sintassi corretta, fare riferimento a https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="f3dc4-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="f3dc4-125">-Query</span><span class="sxs-lookup"><span data-stu-id="f3dc4-125">-Query</span></span>
<span data-ttu-id="f3dc4-126">Specifica l'espressione di query per la ricerca salvata.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-126">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="f3dc4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3dc4-127">-ResourceGroupName</span></span>
<span data-ttu-id="f3dc4-128">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="f3dc4-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="f3dc4-129">-SavedSearchId</span></span>
<span data-ttu-id="f3dc4-130">Specifica l'ID ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="f3dc4-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="f3dc4-131">-Tag</span></span>
<span data-ttu-id="f3dc4-132">I tag di ricerca salvati.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-132">The saved search tags.</span></span>

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

### <span data-ttu-id="f3dc4-133">-Versione</span><span class="sxs-lookup"><span data-stu-id="f3dc4-133">-Version</span></span>
<span data-ttu-id="f3dc4-134">Specifica la versione.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-134">Specifies the version.</span></span>

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

### <span data-ttu-id="f3dc4-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f3dc4-135">-WorkspaceName</span></span>
<span data-ttu-id="f3dc4-136">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-136">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="f3dc4-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f3dc4-137">-Confirm</span></span>
<span data-ttu-id="f3dc4-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3dc4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3dc4-139">-WhatIf</span></span>
<span data-ttu-id="f3dc4-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3dc4-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3dc4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3dc4-142">CommonParameters</span></span>
<span data-ttu-id="f3dc4-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3dc4-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3dc4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3dc4-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3dc4-145">INPUTS</span></span>

### <span data-ttu-id="f3dc4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f3dc4-146">System.String</span></span>

### <span data-ttu-id="f3dc4-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f3dc4-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f3dc4-148">System. Int64</span><span class="sxs-lookup"><span data-stu-id="f3dc4-148">System.Int64</span></span>

## <span data-ttu-id="f3dc4-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3dc4-149">OUTPUTS</span></span>

### <span data-ttu-id="f3dc4-150">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="f3dc4-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="f3dc4-151">Note</span><span class="sxs-lookup"><span data-stu-id="f3dc4-151">NOTES</span></span>

## <span data-ttu-id="f3dc4-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3dc4-152">RELATED LINKS</span></span>

[<span data-ttu-id="f3dc4-153">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="f3dc4-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


