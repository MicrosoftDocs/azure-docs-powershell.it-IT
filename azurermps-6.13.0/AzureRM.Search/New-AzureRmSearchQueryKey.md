---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
ms.openlocfilehash: 417e1a546777824df86b72f3740079ac91835192
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519226"
---
# <span data-ttu-id="563da-101">New-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="563da-101">New-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="563da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="563da-102">SYNOPSIS</span></span>
<span data-ttu-id="563da-103">Creare una nuova chiave di query per il servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="563da-103">Create a new query key for the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="563da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="563da-104">SYNTAX</span></span>

### <span data-ttu-id="563da-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="563da-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="563da-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="563da-106">ParentObjectParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="563da-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="563da-107">ParentResourceIdParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentResourceId] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="563da-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="563da-108">DESCRIPTION</span></span>
<span data-ttu-id="563da-109">Il cmdlet **New-AzureRmSearchQueryKey** crea una nuova chiave di query per il servizio di ricerca Azure.</span><span class="sxs-lookup"><span data-stu-id="563da-109">The **New-AzureRmSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="563da-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="563da-110">EXAMPLES</span></span>

### <span data-ttu-id="563da-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="563da-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="563da-112">L'esempio crea una nuova chiave di query per il servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="563da-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="563da-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="563da-113">PARAMETERS</span></span>

### <span data-ttu-id="563da-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="563da-114">-DefaultProfile</span></span>
<span data-ttu-id="563da-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="563da-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="563da-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="563da-116">-Name</span></span>
<span data-ttu-id="563da-117">Nome della chiave query del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="563da-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="563da-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="563da-118">-ParentObject</span></span>
<span data-ttu-id="563da-119">Oggetto di input del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="563da-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="563da-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="563da-120">-ParentResourceId</span></span>
<span data-ttu-id="563da-121">ID risorsa del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="563da-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="563da-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="563da-122">-ResourceGroupName</span></span>
<span data-ttu-id="563da-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="563da-123">Resource Group name.</span></span>

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

### <span data-ttu-id="563da-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="563da-124">-ServiceName</span></span>
<span data-ttu-id="563da-125">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="563da-125">Search Service name.</span></span>

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

### <span data-ttu-id="563da-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="563da-126">-Confirm</span></span>
<span data-ttu-id="563da-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="563da-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="563da-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="563da-128">-WhatIf</span></span>
<span data-ttu-id="563da-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="563da-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="563da-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="563da-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="563da-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="563da-131">CommonParameters</span></span>
<span data-ttu-id="563da-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="563da-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="563da-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="563da-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="563da-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="563da-134">INPUTS</span></span>

### <span data-ttu-id="563da-135">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="563da-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="563da-136">Parametri: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="563da-136">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="563da-137">System. String</span><span class="sxs-lookup"><span data-stu-id="563da-137">System.String</span></span>

## <span data-ttu-id="563da-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="563da-138">OUTPUTS</span></span>

### <span data-ttu-id="563da-139">Microsoft. Azure. Commands. Management. search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="563da-139">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="563da-140">Note</span><span class="sxs-lookup"><span data-stu-id="563da-140">NOTES</span></span>

## <span data-ttu-id="563da-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="563da-141">RELATED LINKS</span></span>

[<span data-ttu-id="563da-142">Get-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="563da-142">Get-AzureRmSearchQueryKey.md</span></span>](./Get-AzureRmSearchQueryKey.md)

[<span data-ttu-id="563da-143">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="563da-143">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
