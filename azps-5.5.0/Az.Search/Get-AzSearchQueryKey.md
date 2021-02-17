---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: 1c5845b0273d47f1aa1a18782a9243bc5ee5ca9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208362"
---
# <span data-ttu-id="c7149-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="c7149-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="c7149-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7149-102">SYNOPSIS</span></span>
<span data-ttu-id="c7149-103">Ottiene le chiavi di query del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7149-103">Gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c7149-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7149-104">SYNTAX</span></span>

### <span data-ttu-id="c7149-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c7149-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7149-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7149-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7149-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7149-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7149-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c7149-108">DESCRIPTION</span></span>
<span data-ttu-id="c7149-109">Il cmdlet **Get-AzSearchQueryKey** ottiene le chiavi di query del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7149-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c7149-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7149-110">EXAMPLES</span></span>

### <span data-ttu-id="c7149-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c7149-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="c7149-112">L'esempio ottiene tutte le chiavi di query del servizio ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7149-112">The example gets all query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c7149-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7149-113">PARAMETERS</span></span>

### <span data-ttu-id="c7149-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7149-114">-DefaultProfile</span></span>
<span data-ttu-id="c7149-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7149-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7149-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c7149-116">-ParentObject</span></span>
<span data-ttu-id="c7149-117">Oggetto di input del servizio ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7149-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="c7149-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c7149-118">-ParentResourceId</span></span>
<span data-ttu-id="c7149-119">ID risorsa del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7149-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="c7149-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7149-120">-ResourceGroupName</span></span>
<span data-ttu-id="c7149-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c7149-121">Resource Group name.</span></span>

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

### <span data-ttu-id="c7149-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c7149-122">-ServiceName</span></span>
<span data-ttu-id="c7149-123">Nome del servizio Di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7149-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="c7149-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7149-124">CommonParameters</span></span>
<span data-ttu-id="c7149-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7149-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7149-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c7149-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7149-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="c7149-127">INPUTS</span></span>

### <span data-ttu-id="c7149-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="c7149-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="c7149-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c7149-129">System.String</span></span>

## <span data-ttu-id="c7149-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7149-130">OUTPUTS</span></span>

### <span data-ttu-id="c7149-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="c7149-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="c7149-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="c7149-132">NOTES</span></span>

## <span data-ttu-id="c7149-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7149-133">RELATED LINKS</span></span>

[<span data-ttu-id="c7149-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="c7149-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="c7149-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="c7149-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)