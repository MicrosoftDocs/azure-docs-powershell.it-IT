---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: 3c6335264c0d658b0c068efba30c39b4caca407b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971757"
---
# <span data-ttu-id="2075d-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="2075d-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="2075d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2075d-102">SYNOPSIS</span></span>
<span data-ttu-id="2075d-103">Creare una nuova chiave di query per il servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="2075d-103">Create a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="2075d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2075d-104">SYNTAX</span></span>

### <span data-ttu-id="2075d-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2075d-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2075d-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2075d-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2075d-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2075d-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2075d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2075d-108">DESCRIPTION</span></span>
<span data-ttu-id="2075d-109">Il cmdlet **New-AzSearchQueryKey** crea una nuova chiave di query per il servizio Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="2075d-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="2075d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2075d-110">EXAMPLES</span></span>

### <span data-ttu-id="2075d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2075d-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="2075d-112">L'esempio crea una nuova chiave di query per il servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="2075d-112">The example creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="2075d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2075d-113">PARAMETERS</span></span>

### <span data-ttu-id="2075d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2075d-114">-DefaultProfile</span></span>
<span data-ttu-id="2075d-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2075d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2075d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2075d-116">-Name</span></span>
<span data-ttu-id="2075d-117">Nome della chiave della chiave della query del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="2075d-117">Azure Cognitive Search Service query key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2075d-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2075d-118">-ParentObject</span></span>
<span data-ttu-id="2075d-119">Oggetto di input del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="2075d-119">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2075d-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2075d-120">-ParentResourceId</span></span>
<span data-ttu-id="2075d-121">ID risorsa del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="2075d-121">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2075d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2075d-122">-ResourceGroupName</span></span>
<span data-ttu-id="2075d-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2075d-123">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2075d-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2075d-124">-ServiceName</span></span>
<span data-ttu-id="2075d-125">Nome del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="2075d-125">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2075d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2075d-126">-Confirm</span></span>
<span data-ttu-id="2075d-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2075d-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2075d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2075d-128">-WhatIf</span></span>
<span data-ttu-id="2075d-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2075d-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2075d-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2075d-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2075d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2075d-131">CommonParameters</span></span>
<span data-ttu-id="2075d-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2075d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2075d-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2075d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2075d-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="2075d-134">INPUTS</span></span>

### <span data-ttu-id="2075d-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="2075d-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="2075d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2075d-136">System.String</span></span>

## <span data-ttu-id="2075d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2075d-137">OUTPUTS</span></span>

### <span data-ttu-id="2075d-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="2075d-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="2075d-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="2075d-139">NOTES</span></span>

## <span data-ttu-id="2075d-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2075d-140">RELATED LINKS</span></span>

[<span data-ttu-id="2075d-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="2075d-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="2075d-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="2075d-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
