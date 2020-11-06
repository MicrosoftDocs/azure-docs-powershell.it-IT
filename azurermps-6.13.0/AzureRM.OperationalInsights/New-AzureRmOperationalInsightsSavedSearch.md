---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 247589f50028fb8d4cebf78f0ad45bb2124e43cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513559"
---
# <span data-ttu-id="75aa5-101">New-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="75aa5-101">New-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="75aa5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="75aa5-103">Crea una nuova ricerca salvata con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="75aa5-103">Creates a new saved search with the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75aa5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75aa5-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75aa5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75aa5-105">DESCRIPTION</span></span>
<span data-ttu-id="75aa5-106">Il cmdlet **New-AzureRmOperationalInsightsSavedSearch** crea una nuova ricerca salvata con i parametri specificati per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="75aa5-106">The **New-AzureRmOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="75aa5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75aa5-107">EXAMPLES</span></span>

### <span data-ttu-id="75aa5-108">Esempio 1: creare una nuova ricerca salvata</span><span class="sxs-lookup"><span data-stu-id="75aa5-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzureRmOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="75aa5-109">Questo comando crea una nuova ricerca salvata.</span><span class="sxs-lookup"><span data-stu-id="75aa5-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="75aa5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75aa5-110">PARAMETERS</span></span>

### <span data-ttu-id="75aa5-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="75aa5-111">-Category</span></span>
<span data-ttu-id="75aa5-112">Specifica il nome della categoria.</span><span class="sxs-lookup"><span data-stu-id="75aa5-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="75aa5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75aa5-113">-DefaultProfile</span></span>
<span data-ttu-id="75aa5-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="75aa5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75aa5-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="75aa5-115">-DisplayName</span></span>
<span data-ttu-id="75aa5-116">Specifica il nome visualizzato della ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="75aa5-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="75aa5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="75aa5-117">-Force</span></span>
<span data-ttu-id="75aa5-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="75aa5-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="75aa5-119">-Query</span><span class="sxs-lookup"><span data-stu-id="75aa5-119">-Query</span></span>
<span data-ttu-id="75aa5-120">Specifica il nome della query.</span><span class="sxs-lookup"><span data-stu-id="75aa5-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="75aa5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75aa5-121">-ResourceGroupName</span></span>
<span data-ttu-id="75aa5-122">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="75aa5-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="75aa5-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="75aa5-123">-SavedSearchId</span></span>
<span data-ttu-id="75aa5-124">Specifica l'ID ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="75aa5-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="75aa5-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="75aa5-125">-Tag</span></span>
<span data-ttu-id="75aa5-126">I tag di ricerca salvati.</span><span class="sxs-lookup"><span data-stu-id="75aa5-126">The saved search tags.</span></span>

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

### <span data-ttu-id="75aa5-127">-Versione</span><span class="sxs-lookup"><span data-stu-id="75aa5-127">-Version</span></span>
<span data-ttu-id="75aa5-128">Specifica la versione.</span><span class="sxs-lookup"><span data-stu-id="75aa5-128">Specifies the version.</span></span>

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

### <span data-ttu-id="75aa5-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="75aa5-129">-WorkspaceName</span></span>
<span data-ttu-id="75aa5-130">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="75aa5-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="75aa5-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="75aa5-131">-Confirm</span></span>
<span data-ttu-id="75aa5-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75aa5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75aa5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75aa5-133">-WhatIf</span></span>
<span data-ttu-id="75aa5-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75aa5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75aa5-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75aa5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75aa5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75aa5-136">CommonParameters</span></span>
<span data-ttu-id="75aa5-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75aa5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75aa5-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75aa5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75aa5-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75aa5-139">INPUTS</span></span>

### <span data-ttu-id="75aa5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="75aa5-140">System.String</span></span>

### <span data-ttu-id="75aa5-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="75aa5-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="75aa5-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="75aa5-142">System.Int64</span></span>

## <span data-ttu-id="75aa5-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75aa5-143">OUTPUTS</span></span>

### <span data-ttu-id="75aa5-144">System .NET. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="75aa5-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="75aa5-145">Note</span><span class="sxs-lookup"><span data-stu-id="75aa5-145">NOTES</span></span>

## <span data-ttu-id="75aa5-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75aa5-146">RELATED LINKS</span></span>

[<span data-ttu-id="75aa5-147">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="75aa5-147">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


