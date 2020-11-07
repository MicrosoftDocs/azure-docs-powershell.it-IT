---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: 4836a7c016a86ad5fcbb1c926bc27f43215a44f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854745"
---
# <span data-ttu-id="d15dd-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="d15dd-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="d15dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d15dd-102">SYNOPSIS</span></span>
<span data-ttu-id="d15dd-103">Creare una nuova chiave di query per il servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="d15dd-103">Create a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="d15dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d15dd-104">SYNTAX</span></span>

### <span data-ttu-id="d15dd-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d15dd-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d15dd-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d15dd-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d15dd-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d15dd-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d15dd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d15dd-108">DESCRIPTION</span></span>
<span data-ttu-id="d15dd-109">Il cmdlet **New-AzSearchQueryKey** crea una nuova chiave di query per il servizio di ricerca Azure.</span><span class="sxs-lookup"><span data-stu-id="d15dd-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="d15dd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d15dd-110">EXAMPLES</span></span>

### <span data-ttu-id="d15dd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d15dd-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="d15dd-112">L'esempio crea una nuova chiave di query per il servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="d15dd-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="d15dd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d15dd-113">PARAMETERS</span></span>

### <span data-ttu-id="d15dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d15dd-114">-DefaultProfile</span></span>
<span data-ttu-id="d15dd-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d15dd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d15dd-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d15dd-116">-Name</span></span>
<span data-ttu-id="d15dd-117">Nome della chiave query del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d15dd-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="d15dd-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d15dd-118">-ParentObject</span></span>
<span data-ttu-id="d15dd-119">Oggetto di input del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d15dd-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="d15dd-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d15dd-120">-ParentResourceId</span></span>
<span data-ttu-id="d15dd-121">ID risorsa del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d15dd-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="d15dd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d15dd-122">-ResourceGroupName</span></span>
<span data-ttu-id="d15dd-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d15dd-123">Resource Group name.</span></span>

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

### <span data-ttu-id="d15dd-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d15dd-124">-ServiceName</span></span>
<span data-ttu-id="d15dd-125">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d15dd-125">Search Service name.</span></span>

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

### <span data-ttu-id="d15dd-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d15dd-126">-Confirm</span></span>
<span data-ttu-id="d15dd-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d15dd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d15dd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d15dd-128">-WhatIf</span></span>
<span data-ttu-id="d15dd-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d15dd-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d15dd-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d15dd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d15dd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d15dd-131">CommonParameters</span></span>
<span data-ttu-id="d15dd-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d15dd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d15dd-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d15dd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d15dd-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d15dd-134">INPUTS</span></span>

### <span data-ttu-id="d15dd-135">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="d15dd-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="d15dd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d15dd-136">System.String</span></span>

## <span data-ttu-id="d15dd-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d15dd-137">OUTPUTS</span></span>

### <span data-ttu-id="d15dd-138">Microsoft. Azure. Commands. Management. search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="d15dd-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="d15dd-139">Note</span><span class="sxs-lookup"><span data-stu-id="d15dd-139">NOTES</span></span>

## <span data-ttu-id="d15dd-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d15dd-140">RELATED LINKS</span></span>

[<span data-ttu-id="d15dd-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="d15dd-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="d15dd-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="d15dd-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
