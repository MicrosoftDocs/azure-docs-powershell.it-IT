---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: 9bd662c5164660f6bc330e3b2ee2eced2893dbce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988846"
---
# <span data-ttu-id="52253-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="52253-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="52253-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52253-102">SYNOPSIS</span></span>
<span data-ttu-id="52253-103">Ottiene le chiavi di query del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="52253-103">Gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="52253-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52253-104">SYNTAX</span></span>

### <span data-ttu-id="52253-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="52253-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52253-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52253-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52253-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52253-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52253-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="52253-108">DESCRIPTION</span></span>
<span data-ttu-id="52253-109">Il cmdlet **Get-AzSearchQueryKey** ottiene le chiavi di query del servizio Di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="52253-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="52253-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52253-110">EXAMPLES</span></span>

### <span data-ttu-id="52253-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="52253-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="52253-112">L'esempio recupera tutte le chiavi di query del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="52253-112">The example gets all query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="52253-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52253-113">PARAMETERS</span></span>

### <span data-ttu-id="52253-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52253-114">-DefaultProfile</span></span>
<span data-ttu-id="52253-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52253-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52253-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="52253-116">-ParentObject</span></span>
<span data-ttu-id="52253-117">Oggetto di input del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="52253-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="52253-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="52253-118">-ParentResourceId</span></span>
<span data-ttu-id="52253-119">ID risorsa del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="52253-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="52253-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52253-120">-ResourceGroupName</span></span>
<span data-ttu-id="52253-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="52253-121">Resource Group name.</span></span>

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

### <span data-ttu-id="52253-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="52253-122">-ServiceName</span></span>
<span data-ttu-id="52253-123">Nome del servizio Di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="52253-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="52253-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52253-124">CommonParameters</span></span>
<span data-ttu-id="52253-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52253-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52253-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="52253-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52253-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="52253-127">INPUTS</span></span>

### <span data-ttu-id="52253-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="52253-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="52253-129">System.String</span><span class="sxs-lookup"><span data-stu-id="52253-129">System.String</span></span>

## <span data-ttu-id="52253-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52253-130">OUTPUTS</span></span>

### <span data-ttu-id="52253-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="52253-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="52253-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="52253-132">NOTES</span></span>

## <span data-ttu-id="52253-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52253-133">RELATED LINKS</span></span>

[<span data-ttu-id="52253-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="52253-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="52253-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="52253-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)