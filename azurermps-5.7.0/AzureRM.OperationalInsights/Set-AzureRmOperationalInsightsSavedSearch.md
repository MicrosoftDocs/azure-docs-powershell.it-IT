---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: fdfe52151346bbf173226213c9450484d49fe040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511019"
---
# <span data-ttu-id="d1ea2-101">Set-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="d1ea2-101">Set-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="d1ea2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ea2-103">Aggiorna una ricerca salvata già esistente.</span><span class="sxs-lookup"><span data-stu-id="d1ea2-103">Updates a saved search that already exists.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1ea2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1ea2-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1ea2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1ea2-105">DESCRIPTION</span></span>
<span data-ttu-id="d1ea2-106">Il cmdlet **set-AzureRmOperationalInsightsSavedSearch** aggiorna una ricerca salvata già esistente.</span><span class="sxs-lookup"><span data-stu-id="d1ea2-106">The **Set-AzureRmOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="d1ea2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1ea2-107">EXAMPLES</span></span>

### <span data-ttu-id="d1ea2-108">Esempio 1: imposta una ricerca salvata con le proprietà aggiornate</span><span class="sxs-lookup"><span data-stu-id="d1ea2-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="d1ea2-109">Questo comando imposta una ricerca salvata con le proprietà aggiornate.</span><span class="sxs-lookup"><span data-stu-id="d1ea2-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="d1ea2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1ea2-110">PARAMETERS</span></span>

### <span data-ttu-id="d1ea2-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="d1ea2-111">-Category</span></span>
<span data-ttu-id="d1ea2-112">Specifica il nome della categoria.</span><span class="sxs-lookup"><span data-stu-id="d1ea2-112">Specifies the category name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ea2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ea2-113">-DefaultProfile</span></span>
<span data-ttu-id="d1ea2-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d1ea2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ea2-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d1ea2-115">-DisplayName</span></span>
<span data-ttu-id="d1ea2-116">Specifica il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="d1ea2-116">Specifies the display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ea2-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="d1ea2-117">-ETag</span></span>
<span data-ttu-id="d1ea2-118">Specifica il nome ETag.</span><span class="sxs-lookup"><span data-stu-id="d1ea2-118">Specifies the ETag name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ea2-119">-Query</span><span class="sxs-lookup"><span data-stu-id="d1ea2-119">-Query</span></span>
<span data-ttu-id="d1ea2-120">Specifica il nome della query.</span><span class="sxs-lookup"><span data-stu-id="d1ea2-120">Specifies the query name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ea2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1ea2-121">-ResourceGroupName</span></span>
<span data-ttu-id="d1ea2-122">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d1ea2-122">Specifies the resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ea2-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="d1ea2-123">-SavedSearchId</span></span>
<span data-ttu-id="d1ea2-124">Specifica l'ID ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="d1ea2-124">Specifies the saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ea2-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1ea2-125">-Tag</span></span>
<span data-ttu-id="d1ea2-126">I tag di ricerca salvati.</span><span class="sxs-lookup"><span data-stu-id="d1ea2-126">The saved search tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ea2-127">-Versione</span><span class="sxs-lookup"><span data-stu-id="d1ea2-127">-Version</span></span>
```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ea2-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d1ea2-128">-WorkspaceName</span></span>
<span data-ttu-id="d1ea2-129">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d1ea2-129">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ea2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ea2-130">CommonParameters</span></span>
<span data-ttu-id="d1ea2-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1ea2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ea2-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1ea2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ea2-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1ea2-133">INPUTS</span></span>

### <span data-ttu-id="d1ea2-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d1ea2-134">None</span></span>
<span data-ttu-id="d1ea2-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d1ea2-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d1ea2-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1ea2-136">OUTPUTS</span></span>

## <span data-ttu-id="d1ea2-137">Note</span><span class="sxs-lookup"><span data-stu-id="d1ea2-137">NOTES</span></span>

## <span data-ttu-id="d1ea2-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1ea2-138">RELATED LINKS</span></span>

[<span data-ttu-id="d1ea2-139">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="d1ea2-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


