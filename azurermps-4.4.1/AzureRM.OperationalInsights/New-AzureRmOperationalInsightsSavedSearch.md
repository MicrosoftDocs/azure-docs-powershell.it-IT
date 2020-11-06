---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: a233e41ed91a40e8fb16ccda7ed640f8ad5239ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513127"
---
# <span data-ttu-id="62a9f-101">New-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="62a9f-101">New-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="62a9f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62a9f-102">SYNOPSIS</span></span>
<span data-ttu-id="62a9f-103">Crea una nuova ricerca salvata con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="62a9f-103">Creates a new saved search with the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62a9f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62a9f-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tags] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62a9f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62a9f-105">DESCRIPTION</span></span>
<span data-ttu-id="62a9f-106">Il cmdlet **New-AzureRmOperationalInsightsSavedSearch** crea una nuova ricerca salvata con i parametri specificati per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="62a9f-106">The **New-AzureRmOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="62a9f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62a9f-107">EXAMPLES</span></span>

### <span data-ttu-id="62a9f-108">Esempio 1: creare una nuova ricerca salvata</span><span class="sxs-lookup"><span data-stu-id="62a9f-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzureRmOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="62a9f-109">Questo comando crea una nuova ricerca salvata.</span><span class="sxs-lookup"><span data-stu-id="62a9f-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="62a9f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62a9f-110">PARAMETERS</span></span>

### <span data-ttu-id="62a9f-111">-Categoria</span><span class="sxs-lookup"><span data-stu-id="62a9f-111">-Category</span></span>
<span data-ttu-id="62a9f-112">Specifica il nome della categoria.</span><span class="sxs-lookup"><span data-stu-id="62a9f-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="62a9f-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="62a9f-113">-DisplayName</span></span>
<span data-ttu-id="62a9f-114">Specifica il nome visualizzato della ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="62a9f-114">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="62a9f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="62a9f-115">-Force</span></span>
<span data-ttu-id="62a9f-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="62a9f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="62a9f-117">-Query</span><span class="sxs-lookup"><span data-stu-id="62a9f-117">-Query</span></span>
<span data-ttu-id="62a9f-118">Specifica il nome della query.</span><span class="sxs-lookup"><span data-stu-id="62a9f-118">Specifies the query name.</span></span>

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

### <span data-ttu-id="62a9f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62a9f-119">-ResourceGroupName</span></span>
<span data-ttu-id="62a9f-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="62a9f-120">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="62a9f-121">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="62a9f-121">-SavedSearchId</span></span>
<span data-ttu-id="62a9f-122">Specifica l'ID ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="62a9f-122">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="62a9f-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="62a9f-123">-Tags</span></span>
<span data-ttu-id="62a9f-124">Specifica i tag delle risorse per la ricerca salvata.</span><span class="sxs-lookup"><span data-stu-id="62a9f-124">Specifies the resource tags for the saved search.</span></span>

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

### <span data-ttu-id="62a9f-125">-Versione</span><span class="sxs-lookup"><span data-stu-id="62a9f-125">-Version</span></span>
<span data-ttu-id="62a9f-126">Specifica la versione.</span><span class="sxs-lookup"><span data-stu-id="62a9f-126">Specifies the version.</span></span>

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

### <span data-ttu-id="62a9f-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="62a9f-127">-WorkspaceName</span></span>
<span data-ttu-id="62a9f-128">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="62a9f-128">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="62a9f-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62a9f-129">-Confirm</span></span>
<span data-ttu-id="62a9f-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62a9f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62a9f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62a9f-131">-WhatIf</span></span>
<span data-ttu-id="62a9f-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62a9f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62a9f-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62a9f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62a9f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a9f-134">-DefaultProfile</span></span>
<span data-ttu-id="62a9f-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62a9f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62a9f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a9f-136">CommonParameters</span></span>
<span data-ttu-id="62a9f-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62a9f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a9f-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62a9f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a9f-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62a9f-139">INPUTS</span></span>

## <span data-ttu-id="62a9f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62a9f-140">OUTPUTS</span></span>

## <span data-ttu-id="62a9f-141">Note</span><span class="sxs-lookup"><span data-stu-id="62a9f-141">NOTES</span></span>

## <span data-ttu-id="62a9f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62a9f-142">RELATED LINKS</span></span>

[<span data-ttu-id="62a9f-143">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="62a9f-143">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


