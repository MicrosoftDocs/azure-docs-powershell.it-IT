---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 46427a53a04e94fe42c20cfa2e6ab016a6b8c613
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190903"
---
# <span data-ttu-id="0f072-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="0f072-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="0f072-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f072-102">SYNOPSIS</span></span>
<span data-ttu-id="0f072-103">Aggiorna una ricerca salvata già esistente.</span><span class="sxs-lookup"><span data-stu-id="0f072-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="0f072-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f072-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f072-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f072-105">DESCRIPTION</span></span>
<span data-ttu-id="0f072-106">Il cmdlet **set-AzOperationalInsightsSavedSearch** aggiorna una ricerca salvata già esistente.</span><span class="sxs-lookup"><span data-stu-id="0f072-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="0f072-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f072-107">EXAMPLES</span></span>

### <span data-ttu-id="0f072-108">Esempio 1: imposta una ricerca salvata con le proprietà aggiornate</span><span class="sxs-lookup"><span data-stu-id="0f072-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="0f072-109">Questo comando imposta una ricerca salvata con le proprietà aggiornate.</span><span class="sxs-lookup"><span data-stu-id="0f072-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="0f072-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f072-110">PARAMETERS</span></span>

### <span data-ttu-id="0f072-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="0f072-111">-Category</span></span>
<span data-ttu-id="0f072-112">Specifica il nome della categoria.</span><span class="sxs-lookup"><span data-stu-id="0f072-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="0f072-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f072-113">-DefaultProfile</span></span>
<span data-ttu-id="0f072-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0f072-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f072-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0f072-115">-DisplayName</span></span>
<span data-ttu-id="0f072-116">Specifica il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="0f072-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="0f072-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="0f072-117">-ETag</span></span>
<span data-ttu-id="0f072-118">Specifica il nome ETag.</span><span class="sxs-lookup"><span data-stu-id="0f072-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="0f072-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="0f072-119">-FunctionAlias</span></span>
<span data-ttu-id="0f072-120">L'alias di funzione se query funge da funzione.</span><span class="sxs-lookup"><span data-stu-id="0f072-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="0f072-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="0f072-121">-FunctionParameter</span></span>
<span data-ttu-id="0f072-122">I parametri di funzione facoltativi se query funge da funzione.</span><span class="sxs-lookup"><span data-stu-id="0f072-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="0f072-123">Il valore deve essere il formato seguente:' param-name1: tipo1 = default_value1, param-name2: tipo2 = default_value2'.</span><span class="sxs-lookup"><span data-stu-id="0f072-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="0f072-124">Per altri esempi e per la sintassi corretta, fare riferimento a https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="0f072-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="0f072-125">-Query</span><span class="sxs-lookup"><span data-stu-id="0f072-125">-Query</span></span>
<span data-ttu-id="0f072-126">Specifica il nome della query.</span><span class="sxs-lookup"><span data-stu-id="0f072-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="0f072-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f072-127">-ResourceGroupName</span></span>
<span data-ttu-id="0f072-128">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0f072-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="0f072-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="0f072-129">-SavedSearchId</span></span>
<span data-ttu-id="0f072-130">Specifica l'ID ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="0f072-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="0f072-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="0f072-131">-Tag</span></span>
<span data-ttu-id="0f072-132">I tag di ricerca salvati.</span><span class="sxs-lookup"><span data-stu-id="0f072-132">The saved search tags.</span></span>

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

### <span data-ttu-id="0f072-133">-Versione</span><span class="sxs-lookup"><span data-stu-id="0f072-133">-Version</span></span>
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

### <span data-ttu-id="0f072-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0f072-134">-WorkspaceName</span></span>
<span data-ttu-id="0f072-135">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0f072-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="0f072-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f072-136">CommonParameters</span></span>
<span data-ttu-id="0f072-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f072-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f072-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f072-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f072-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f072-139">INPUTS</span></span>

### <span data-ttu-id="0f072-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0f072-140">System.String</span></span>

### <span data-ttu-id="0f072-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0f072-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0f072-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="0f072-142">System.Int64</span></span>

## <span data-ttu-id="0f072-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f072-143">OUTPUTS</span></span>

### <span data-ttu-id="0f072-144">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="0f072-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="0f072-145">Note</span><span class="sxs-lookup"><span data-stu-id="0f072-145">NOTES</span></span>

## <span data-ttu-id="0f072-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f072-146">RELATED LINKS</span></span>

[<span data-ttu-id="0f072-147">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="0f072-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

