---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 2b29b0f7976f8abba8c2f1d664a40d9a67c03c5a
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93865555"
---
# <span data-ttu-id="8bd6c-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="8bd6c-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="8bd6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8bd6c-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd6c-103">Aggiorna una ricerca salvata già esistente.</span><span class="sxs-lookup"><span data-stu-id="8bd6c-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="8bd6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8bd6c-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bd6c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bd6c-105">DESCRIPTION</span></span>
<span data-ttu-id="8bd6c-106">Il cmdlet **set-AzOperationalInsightsSavedSearch** aggiorna una ricerca salvata già esistente.</span><span class="sxs-lookup"><span data-stu-id="8bd6c-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="8bd6c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8bd6c-107">EXAMPLES</span></span>

### <span data-ttu-id="8bd6c-108">Esempio 1: imposta una ricerca salvata con le proprietà aggiornate</span><span class="sxs-lookup"><span data-stu-id="8bd6c-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="8bd6c-109">Questo comando imposta una ricerca salvata con le proprietà aggiornate.</span><span class="sxs-lookup"><span data-stu-id="8bd6c-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="8bd6c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8bd6c-110">PARAMETERS</span></span>

### <span data-ttu-id="8bd6c-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="8bd6c-111">-Category</span></span>
<span data-ttu-id="8bd6c-112">Specifica il nome della categoria.</span><span class="sxs-lookup"><span data-stu-id="8bd6c-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="8bd6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd6c-113">-DefaultProfile</span></span>
<span data-ttu-id="8bd6c-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8bd6c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8bd6c-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8bd6c-115">-DisplayName</span></span>
<span data-ttu-id="8bd6c-116">Specifica il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="8bd6c-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="8bd6c-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="8bd6c-117">-ETag</span></span>
<span data-ttu-id="8bd6c-118">Specifica il nome ETag.</span><span class="sxs-lookup"><span data-stu-id="8bd6c-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="8bd6c-119">-Query</span><span class="sxs-lookup"><span data-stu-id="8bd6c-119">-Query</span></span>
<span data-ttu-id="8bd6c-120">Specifica il nome della query.</span><span class="sxs-lookup"><span data-stu-id="8bd6c-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="8bd6c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bd6c-121">-ResourceGroupName</span></span>
<span data-ttu-id="8bd6c-122">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8bd6c-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="8bd6c-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="8bd6c-123">-SavedSearchId</span></span>
<span data-ttu-id="8bd6c-124">Specifica l'ID ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="8bd6c-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="8bd6c-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="8bd6c-125">-Tag</span></span>
<span data-ttu-id="8bd6c-126">I tag di ricerca salvati.</span><span class="sxs-lookup"><span data-stu-id="8bd6c-126">The saved search tags.</span></span>

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

### <span data-ttu-id="8bd6c-127">-Versione</span><span class="sxs-lookup"><span data-stu-id="8bd6c-127">-Version</span></span>
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

### <span data-ttu-id="8bd6c-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8bd6c-128">-WorkspaceName</span></span>
<span data-ttu-id="8bd6c-129">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8bd6c-129">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="8bd6c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd6c-130">CommonParameters</span></span>
<span data-ttu-id="8bd6c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bd6c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd6c-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bd6c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd6c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8bd6c-133">INPUTS</span></span>

### <span data-ttu-id="8bd6c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8bd6c-134">System.String</span></span>

### <span data-ttu-id="8bd6c-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8bd6c-135">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8bd6c-136">System. Int64</span><span class="sxs-lookup"><span data-stu-id="8bd6c-136">System.Int64</span></span>

## <span data-ttu-id="8bd6c-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8bd6c-137">OUTPUTS</span></span>

### <span data-ttu-id="8bd6c-138">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="8bd6c-138">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="8bd6c-139">Note</span><span class="sxs-lookup"><span data-stu-id="8bd6c-139">NOTES</span></span>

## <span data-ttu-id="8bd6c-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8bd6c-140">RELATED LINKS</span></span>

[<span data-ttu-id="8bd6c-141">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="8bd6c-141">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


