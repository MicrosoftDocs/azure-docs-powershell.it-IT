---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 25d973d6a568695fbca7371b229cf9bb18fcd5cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989714"
---
# <span data-ttu-id="13972-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="13972-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="13972-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13972-102">SYNOPSIS</span></span>
<span data-ttu-id="13972-103">Aggiorna una ricerca salvata già esistente.</span><span class="sxs-lookup"><span data-stu-id="13972-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="13972-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13972-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13972-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="13972-105">DESCRIPTION</span></span>
<span data-ttu-id="13972-106">Il cmdlet **Set-AzOperationalInsightsSavedSearch** aggiorna una ricerca salvata già esistente.</span><span class="sxs-lookup"><span data-stu-id="13972-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="13972-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13972-107">EXAMPLES</span></span>

### <span data-ttu-id="13972-108">Esempio 1: Imposta una ricerca salvata con proprietà aggiornate</span><span class="sxs-lookup"><span data-stu-id="13972-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="13972-109">Questo comando imposta una ricerca salvata con proprietà aggiornate.</span><span class="sxs-lookup"><span data-stu-id="13972-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="13972-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13972-110">PARAMETERS</span></span>

### <span data-ttu-id="13972-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="13972-111">-Category</span></span>
<span data-ttu-id="13972-112">Specifica il nome della categoria.</span><span class="sxs-lookup"><span data-stu-id="13972-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="13972-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13972-113">-DefaultProfile</span></span>
<span data-ttu-id="13972-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="13972-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13972-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="13972-115">-DisplayName</span></span>
<span data-ttu-id="13972-116">Specifica il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="13972-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="13972-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="13972-117">-ETag</span></span>
<span data-ttu-id="13972-118">Specifica il nome dell'ETag.</span><span class="sxs-lookup"><span data-stu-id="13972-118">Specifies the ETag name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13972-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="13972-119">-FunctionAlias</span></span>
<span data-ttu-id="13972-120">L'alias della funzione se la query funge da funzione.</span><span class="sxs-lookup"><span data-stu-id="13972-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13972-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="13972-121">-FunctionParameter</span></span>
<span data-ttu-id="13972-122">I parametri facoltativi della funzione se la query funge da funzione.</span><span class="sxs-lookup"><span data-stu-id="13972-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="13972-123">Il valore deve essere nel formato seguente: 'nome-parametro1:tipo1 = default_value1, param-nome2:tipo2 = default_value2'.</span><span class="sxs-lookup"><span data-stu-id="13972-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="13972-124">Per altri esempi e la sintassi corretta, vedere https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="13972-124">For more examples and proper syntax please refer to https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13972-125">-Query</span><span class="sxs-lookup"><span data-stu-id="13972-125">-Query</span></span>
<span data-ttu-id="13972-126">Specifica il nome della query.</span><span class="sxs-lookup"><span data-stu-id="13972-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="13972-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13972-127">-ResourceGroupName</span></span>
<span data-ttu-id="13972-128">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="13972-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="13972-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="13972-129">-SavedSearchId</span></span>
<span data-ttu-id="13972-130">Specifica l'ID di ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="13972-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="13972-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="13972-131">-Tag</span></span>
<span data-ttu-id="13972-132">I tag di ricerca salvati.</span><span class="sxs-lookup"><span data-stu-id="13972-132">The saved search tags.</span></span>

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

### <span data-ttu-id="13972-133">-Version</span><span class="sxs-lookup"><span data-stu-id="13972-133">-Version</span></span>
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

### <span data-ttu-id="13972-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="13972-134">-WorkspaceName</span></span>
<span data-ttu-id="13972-135">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="13972-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="13972-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13972-136">CommonParameters</span></span>
<span data-ttu-id="13972-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13972-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13972-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13972-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13972-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="13972-139">INPUTS</span></span>

### <span data-ttu-id="13972-140">System.String</span><span class="sxs-lookup"><span data-stu-id="13972-140">System.String</span></span>

### <span data-ttu-id="13972-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="13972-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="13972-142">System.Int64</span><span class="sxs-lookup"><span data-stu-id="13972-142">System.Int64</span></span>

## <span data-ttu-id="13972-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13972-143">OUTPUTS</span></span>

### <span data-ttu-id="13972-144">System.Net.HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="13972-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="13972-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="13972-145">NOTES</span></span>

## <span data-ttu-id="13972-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13972-146">RELATED LINKS</span></span>

[<span data-ttu-id="13972-147">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="13972-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


