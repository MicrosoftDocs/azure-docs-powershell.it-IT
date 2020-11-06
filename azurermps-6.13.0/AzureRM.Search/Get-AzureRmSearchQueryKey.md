---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
ms.openlocfilehash: 3535e9d7723c87e0f528192e47c921d3835ff9e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511452"
---
# <span data-ttu-id="49b0e-101">Get-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="49b0e-101">Get-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="49b0e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="49b0e-103">Ottiene i tasti di query del servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="49b0e-103">Gets query key(s) of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49b0e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49b0e-104">SYNTAX</span></span>

### <span data-ttu-id="49b0e-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="49b0e-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49b0e-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49b0e-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49b0e-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49b0e-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49b0e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49b0e-108">DESCRIPTION</span></span>
<span data-ttu-id="49b0e-109">Il cmdlet **Get-AzureRmSearchQueryKey** ottiene le chiavi di query del servizio di ricerca Azure.</span><span class="sxs-lookup"><span data-stu-id="49b0e-109">The **Get-AzureRmSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="49b0e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49b0e-110">EXAMPLES</span></span>

### <span data-ttu-id="49b0e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="49b0e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="49b0e-112">L'esempio ottiene tutte le chiavi di query del servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="49b0e-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="49b0e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49b0e-113">PARAMETERS</span></span>

### <span data-ttu-id="49b0e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b0e-114">-DefaultProfile</span></span>
<span data-ttu-id="49b0e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49b0e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49b0e-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="49b0e-116">-ParentObject</span></span>
<span data-ttu-id="49b0e-117">Oggetto di input del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="49b0e-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="49b0e-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="49b0e-118">-ParentResourceId</span></span>
<span data-ttu-id="49b0e-119">ID risorsa del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="49b0e-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="49b0e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b0e-120">-ResourceGroupName</span></span>
<span data-ttu-id="49b0e-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="49b0e-121">Resource Group name.</span></span>

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

### <span data-ttu-id="49b0e-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="49b0e-122">-ServiceName</span></span>
<span data-ttu-id="49b0e-123">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="49b0e-123">Search Service name.</span></span>

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

### <span data-ttu-id="49b0e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b0e-124">CommonParameters</span></span>
<span data-ttu-id="49b0e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49b0e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b0e-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49b0e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b0e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49b0e-127">INPUTS</span></span>

### <span data-ttu-id="49b0e-128">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="49b0e-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="49b0e-129">Parametri: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="49b0e-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="49b0e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="49b0e-130">System.String</span></span>

## <span data-ttu-id="49b0e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49b0e-131">OUTPUTS</span></span>

### <span data-ttu-id="49b0e-132">Microsoft. Azure. Commands. Management. search. Models. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="49b0e-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="49b0e-133">Note</span><span class="sxs-lookup"><span data-stu-id="49b0e-133">NOTES</span></span>

## <span data-ttu-id="49b0e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49b0e-134">RELATED LINKS</span></span>

[<span data-ttu-id="49b0e-135">New-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="49b0e-135">New-AzureRmSearchQueryKey.md</span></span>](./New-AzureRmSearchQueryKey.md)

[<span data-ttu-id="49b0e-136">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="49b0e-136">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
