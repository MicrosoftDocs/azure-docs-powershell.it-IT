---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 3426b93ec9551ba6218634fa87adeff09b5872af
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366785"
---
# <span data-ttu-id="64231-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="64231-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="64231-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64231-102">SYNOPSIS</span></span>
<span data-ttu-id="64231-103">Crea una nuova ricerca salvata con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="64231-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="64231-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64231-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64231-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64231-105">DESCRIPTION</span></span>
<span data-ttu-id="64231-106">Il cmdlet **New-AzOperationalInsightsSavedSearch** crea una nuova ricerca salvata con i parametri specificati per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="64231-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="64231-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64231-107">EXAMPLES</span></span>

### <span data-ttu-id="64231-108">Esempio 1: creare una nuova ricerca salvata</span><span class="sxs-lookup"><span data-stu-id="64231-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="64231-109">Questo comando crea una nuova ricerca salvata.</span><span class="sxs-lookup"><span data-stu-id="64231-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="64231-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64231-110">PARAMETERS</span></span>

### <span data-ttu-id="64231-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="64231-111">-Category</span></span>
<span data-ttu-id="64231-112">Specifica il nome della categoria.</span><span class="sxs-lookup"><span data-stu-id="64231-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="64231-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64231-113">-DefaultProfile</span></span>
<span data-ttu-id="64231-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="64231-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64231-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="64231-115">-DisplayName</span></span>
<span data-ttu-id="64231-116">Specifica il nome visualizzato della ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="64231-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="64231-117">-Force</span><span class="sxs-lookup"><span data-stu-id="64231-117">-Force</span></span>
<span data-ttu-id="64231-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="64231-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="64231-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="64231-119">-FunctionAlias</span></span>
<span data-ttu-id="64231-120">L'alias di funzione se query funge da funzione.</span><span class="sxs-lookup"><span data-stu-id="64231-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="64231-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="64231-121">-FunctionParameter</span></span>
<span data-ttu-id="64231-122">I parametri di funzione facoltativi se query funge da funzione.</span><span class="sxs-lookup"><span data-stu-id="64231-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="64231-123">Il valore deve essere il formato seguente:' param-name1: tipo1 = default_value1, param-name2: tipo2 = default_value2'.</span><span class="sxs-lookup"><span data-stu-id="64231-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="64231-124">Per altri esempi e per la sintassi corretta, fare riferimento a https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="64231-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="64231-125">-Query</span><span class="sxs-lookup"><span data-stu-id="64231-125">-Query</span></span>
<span data-ttu-id="64231-126">Specifica l'espressione di query per la ricerca salvata.</span><span class="sxs-lookup"><span data-stu-id="64231-126">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="64231-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64231-127">-ResourceGroupName</span></span>
<span data-ttu-id="64231-128">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="64231-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="64231-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="64231-129">-SavedSearchId</span></span>
<span data-ttu-id="64231-130">Specifica l'ID ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="64231-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="64231-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="64231-131">-Tag</span></span>
<span data-ttu-id="64231-132">I tag di ricerca salvati.</span><span class="sxs-lookup"><span data-stu-id="64231-132">The saved search tags.</span></span>

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

### <span data-ttu-id="64231-133">-Versione</span><span class="sxs-lookup"><span data-stu-id="64231-133">-Version</span></span>
<span data-ttu-id="64231-134">Specifica la versione.</span><span class="sxs-lookup"><span data-stu-id="64231-134">Specifies the version.</span></span>

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

### <span data-ttu-id="64231-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="64231-135">-WorkspaceName</span></span>
<span data-ttu-id="64231-136">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="64231-136">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="64231-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="64231-137">-Confirm</span></span>
<span data-ttu-id="64231-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64231-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64231-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64231-139">-WhatIf</span></span>
<span data-ttu-id="64231-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64231-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64231-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64231-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64231-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64231-142">CommonParameters</span></span>
<span data-ttu-id="64231-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64231-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64231-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64231-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64231-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64231-145">INPUTS</span></span>

### <span data-ttu-id="64231-146">System. String</span><span class="sxs-lookup"><span data-stu-id="64231-146">System.String</span></span>

### <span data-ttu-id="64231-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="64231-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="64231-148">System. Int64</span><span class="sxs-lookup"><span data-stu-id="64231-148">System.Int64</span></span>

## <span data-ttu-id="64231-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64231-149">OUTPUTS</span></span>

### <span data-ttu-id="64231-150">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="64231-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="64231-151">Note</span><span class="sxs-lookup"><span data-stu-id="64231-151">NOTES</span></span>

## <span data-ttu-id="64231-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64231-152">RELATED LINKS</span></span>

[<span data-ttu-id="64231-153">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="64231-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


