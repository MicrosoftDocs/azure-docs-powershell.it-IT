---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: a0dddf6e7cc5080ca4028b1348381c1b5fb72df6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190117"
---
# <span data-ttu-id="aabf4-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="aabf4-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="aabf4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aabf4-102">SYNOPSIS</span></span>
<span data-ttu-id="aabf4-103">Ottiene i tasti di query del servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="aabf4-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="aabf4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aabf4-104">SYNTAX</span></span>

### <span data-ttu-id="aabf4-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aabf4-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aabf4-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aabf4-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aabf4-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aabf4-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aabf4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aabf4-108">DESCRIPTION</span></span>
<span data-ttu-id="aabf4-109">Il cmdlet **Get-AzSearchQueryKey** ottiene le chiavi di query del servizio di ricerca Azure.</span><span class="sxs-lookup"><span data-stu-id="aabf4-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="aabf4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aabf4-110">EXAMPLES</span></span>

### <span data-ttu-id="aabf4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aabf4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="aabf4-112">L'esempio ottiene tutte le chiavi di query del servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="aabf4-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="aabf4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aabf4-113">PARAMETERS</span></span>

### <span data-ttu-id="aabf4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aabf4-114">-DefaultProfile</span></span>
<span data-ttu-id="aabf4-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aabf4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aabf4-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="aabf4-116">-ParentObject</span></span>
<span data-ttu-id="aabf4-117">Oggetto di input del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="aabf4-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="aabf4-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="aabf4-118">-ParentResourceId</span></span>
<span data-ttu-id="aabf4-119">ID risorsa del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="aabf4-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="aabf4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aabf4-120">-ResourceGroupName</span></span>
<span data-ttu-id="aabf4-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aabf4-121">Resource Group name.</span></span>

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

### <span data-ttu-id="aabf4-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="aabf4-122">-ServiceName</span></span>
<span data-ttu-id="aabf4-123">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="aabf4-123">Search Service name.</span></span>

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

### <span data-ttu-id="aabf4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aabf4-124">CommonParameters</span></span>
<span data-ttu-id="aabf4-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aabf4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aabf4-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aabf4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aabf4-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aabf4-127">INPUTS</span></span>

### <span data-ttu-id="aabf4-128">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="aabf4-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="aabf4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="aabf4-129">System.String</span></span>

## <span data-ttu-id="aabf4-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aabf4-130">OUTPUTS</span></span>

### <span data-ttu-id="aabf4-131">Microsoft. Azure. Commands. Management. search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="aabf4-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="aabf4-132">Note</span><span class="sxs-lookup"><span data-stu-id="aabf4-132">NOTES</span></span>

## <span data-ttu-id="aabf4-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aabf4-133">RELATED LINKS</span></span>

[<span data-ttu-id="aabf4-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="aabf4-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="aabf4-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="aabf4-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)