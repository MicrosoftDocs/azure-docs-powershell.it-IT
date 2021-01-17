---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 46427a53a04e94fe42c20cfa2e6ab016a6b8c613
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372074"
---
# <span data-ttu-id="f573c-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="f573c-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="f573c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f573c-102">SYNOPSIS</span></span>
<span data-ttu-id="f573c-103">Aggiorna una ricerca salvata già esistente.</span><span class="sxs-lookup"><span data-stu-id="f573c-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="f573c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f573c-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f573c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f573c-105">DESCRIPTION</span></span>
<span data-ttu-id="f573c-106">Il cmdlet **set-AzOperationalInsightsSavedSearch** aggiorna una ricerca salvata già esistente.</span><span class="sxs-lookup"><span data-stu-id="f573c-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="f573c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f573c-107">EXAMPLES</span></span>

### <span data-ttu-id="f573c-108">Esempio 1: imposta una ricerca salvata con le proprietà aggiornate</span><span class="sxs-lookup"><span data-stu-id="f573c-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="f573c-109">Questo comando imposta una ricerca salvata con le proprietà aggiornate.</span><span class="sxs-lookup"><span data-stu-id="f573c-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="f573c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f573c-110">PARAMETERS</span></span>

### <span data-ttu-id="f573c-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="f573c-111">-Category</span></span>
<span data-ttu-id="f573c-112">Specifica il nome della categoria.</span><span class="sxs-lookup"><span data-stu-id="f573c-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="f573c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f573c-113">-DefaultProfile</span></span>
<span data-ttu-id="f573c-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f573c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f573c-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f573c-115">-DisplayName</span></span>
<span data-ttu-id="f573c-116">Specifica il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="f573c-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="f573c-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="f573c-117">-ETag</span></span>
<span data-ttu-id="f573c-118">Specifica il nome ETag.</span><span class="sxs-lookup"><span data-stu-id="f573c-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="f573c-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="f573c-119">-FunctionAlias</span></span>
<span data-ttu-id="f573c-120">L'alias di funzione se query funge da funzione.</span><span class="sxs-lookup"><span data-stu-id="f573c-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="f573c-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="f573c-121">-FunctionParameter</span></span>
<span data-ttu-id="f573c-122">I parametri di funzione facoltativi se query funge da funzione.</span><span class="sxs-lookup"><span data-stu-id="f573c-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="f573c-123">Il valore deve essere il formato seguente:' param-name1: tipo1 = default_value1, param-name2: tipo2 = default_value2'.</span><span class="sxs-lookup"><span data-stu-id="f573c-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="f573c-124">Per altri esempi e per la sintassi corretta, fare riferimento a https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="f573c-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="f573c-125">-Query</span><span class="sxs-lookup"><span data-stu-id="f573c-125">-Query</span></span>
<span data-ttu-id="f573c-126">Specifica il nome della query.</span><span class="sxs-lookup"><span data-stu-id="f573c-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="f573c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f573c-127">-ResourceGroupName</span></span>
<span data-ttu-id="f573c-128">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f573c-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="f573c-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="f573c-129">-SavedSearchId</span></span>
<span data-ttu-id="f573c-130">Specifica l'ID ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="f573c-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="f573c-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="f573c-131">-Tag</span></span>
<span data-ttu-id="f573c-132">I tag di ricerca salvati.</span><span class="sxs-lookup"><span data-stu-id="f573c-132">The saved search tags.</span></span>

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

### <span data-ttu-id="f573c-133">-Versione</span><span class="sxs-lookup"><span data-stu-id="f573c-133">-Version</span></span>
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

### <span data-ttu-id="f573c-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f573c-134">-WorkspaceName</span></span>
<span data-ttu-id="f573c-135">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f573c-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="f573c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f573c-136">CommonParameters</span></span>
<span data-ttu-id="f573c-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f573c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f573c-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f573c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f573c-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f573c-139">INPUTS</span></span>

### <span data-ttu-id="f573c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f573c-140">System.String</span></span>

### <span data-ttu-id="f573c-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f573c-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f573c-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="f573c-142">System.Int64</span></span>

## <span data-ttu-id="f573c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f573c-143">OUTPUTS</span></span>

### <span data-ttu-id="f573c-144">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="f573c-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="f573c-145">Note</span><span class="sxs-lookup"><span data-stu-id="f573c-145">NOTES</span></span>

## <span data-ttu-id="f573c-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f573c-146">RELATED LINKS</span></span>

[<span data-ttu-id="f573c-147">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="f573c-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


