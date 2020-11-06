---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 103012f25baa67cbd8faeab4a9cc0c22297e7922
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513108"
---
# <span data-ttu-id="7bc45-101">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="7bc45-101">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="7bc45-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7bc45-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc45-103">Rimuove una ricerca salvata dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7bc45-103">Removes a saved search from the workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bc45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7bc45-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bc45-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bc45-105">DESCRIPTION</span></span>
<span data-ttu-id="7bc45-106">Il cmdlet **Remove-AzureRmOperationalInsightsSavedSearch** rimuove una ricerca salvata dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7bc45-106">The **Remove-AzureRmOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="7bc45-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7bc45-107">EXAMPLES</span></span>

### <span data-ttu-id="7bc45-108">Esempio 1: rimuovere una ricerca salvata</span><span class="sxs-lookup"><span data-stu-id="7bc45-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="7bc45-109">Questo comando rimuove una ricerca salvata dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7bc45-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="7bc45-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7bc45-110">PARAMETERS</span></span>

### <span data-ttu-id="7bc45-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bc45-111">-ResourceGroupName</span></span>
<span data-ttu-id="7bc45-112">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7bc45-112">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="7bc45-113">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="7bc45-113">-SavedSearchId</span></span>
<span data-ttu-id="7bc45-114">Specifica l'ID ricerca salvato.</span><span class="sxs-lookup"><span data-stu-id="7bc45-114">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="7bc45-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7bc45-115">-WorkspaceName</span></span>
<span data-ttu-id="7bc45-116">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7bc45-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="7bc45-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7bc45-117">-Confirm</span></span>
<span data-ttu-id="7bc45-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bc45-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bc45-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bc45-119">-WhatIf</span></span>
<span data-ttu-id="7bc45-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bc45-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bc45-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bc45-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bc45-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc45-122">-DefaultProfile</span></span>
<span data-ttu-id="7bc45-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7bc45-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bc45-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc45-124">CommonParameters</span></span>
<span data-ttu-id="7bc45-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc45-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc45-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bc45-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc45-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7bc45-127">INPUTS</span></span>

## <span data-ttu-id="7bc45-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7bc45-128">OUTPUTS</span></span>

## <span data-ttu-id="7bc45-129">Note</span><span class="sxs-lookup"><span data-stu-id="7bc45-129">NOTES</span></span>

## <span data-ttu-id="7bc45-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7bc45-130">RELATED LINKS</span></span>

[<span data-ttu-id="7bc45-131">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="7bc45-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


