---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: dafc9da9669a7c07f982e4fee87a37e1581af40a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190118"
---
# <span data-ttu-id="459b1-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="459b1-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="459b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="459b1-102">SYNOPSIS</span></span>
<span data-ttu-id="459b1-103">Ottiene la coppia di chiavi di amministrazione del servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="459b1-103">Gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="459b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="459b1-104">SYNTAX</span></span>

### <span data-ttu-id="459b1-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="459b1-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="459b1-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="459b1-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="459b1-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="459b1-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="459b1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="459b1-108">DESCRIPTION</span></span>
<span data-ttu-id="459b1-109">Il cmdlet **Get-AzSearchAdminKeyPair** ottiene la coppia di chiavi di amministrazione del servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="459b1-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="459b1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="459b1-110">EXAMPLES</span></span>

### <span data-ttu-id="459b1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="459b1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="459b1-112">L'esempio ottiene una coppia di chiavi di amministrazione del servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="459b1-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="459b1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="459b1-113">PARAMETERS</span></span>

### <span data-ttu-id="459b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="459b1-114">-DefaultProfile</span></span>
<span data-ttu-id="459b1-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="459b1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="459b1-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="459b1-116">-ParentObject</span></span>
<span data-ttu-id="459b1-117">Oggetto di input del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="459b1-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="459b1-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="459b1-118">-ParentResourceId</span></span>
<span data-ttu-id="459b1-119">ID risorsa del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="459b1-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="459b1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="459b1-120">-ResourceGroupName</span></span>
<span data-ttu-id="459b1-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="459b1-121">Resource Group name.</span></span>

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

### <span data-ttu-id="459b1-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="459b1-122">-ServiceName</span></span>
<span data-ttu-id="459b1-123">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="459b1-123">Search Service name.</span></span>

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

### <span data-ttu-id="459b1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="459b1-124">CommonParameters</span></span>
<span data-ttu-id="459b1-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="459b1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="459b1-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="459b1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="459b1-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="459b1-127">INPUTS</span></span>

### <span data-ttu-id="459b1-128">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="459b1-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="459b1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="459b1-129">System.String</span></span>

## <span data-ttu-id="459b1-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="459b1-130">OUTPUTS</span></span>

### <span data-ttu-id="459b1-131">Microsoft. Azure. Commands. Management. search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="459b1-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="459b1-132">Note</span><span class="sxs-lookup"><span data-stu-id="459b1-132">NOTES</span></span>

## <span data-ttu-id="459b1-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="459b1-133">RELATED LINKS</span></span>

[<span data-ttu-id="459b1-134">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="459b1-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
