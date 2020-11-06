---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchAdminKeyPair.md
ms.openlocfilehash: 92b2e7304c0f837e47f7464e84769478902c973a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518572"
---
# <span data-ttu-id="74b21-101">Get-AzureRmSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="74b21-101">Get-AzureRmSearchAdminKeyPair</span></span>

## <span data-ttu-id="74b21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74b21-102">SYNOPSIS</span></span>
<span data-ttu-id="74b21-103">Ottiene la coppia di chiavi di amministrazione del servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="74b21-103">Gets admin key pair of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74b21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74b21-104">SYNTAX</span></span>

### <span data-ttu-id="74b21-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="74b21-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74b21-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74b21-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="74b21-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74b21-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74b21-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74b21-108">DESCRIPTION</span></span>
<span data-ttu-id="74b21-109">Il cmdlet **Get-AzureRmSearchAdminKeyPair** ottiene la coppia di chiavi di amministrazione del servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="74b21-109">The **Get-AzureRmSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="74b21-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74b21-110">EXAMPLES</span></span>

### <span data-ttu-id="74b21-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="74b21-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="74b21-112">L'esempio ottiene una coppia di chiavi di amministrazione del servizio di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="74b21-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="74b21-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74b21-113">PARAMETERS</span></span>

### <span data-ttu-id="74b21-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b21-114">-DefaultProfile</span></span>
<span data-ttu-id="74b21-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="74b21-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74b21-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="74b21-116">-ParentObject</span></span>
<span data-ttu-id="74b21-117">Oggetto di input del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="74b21-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="74b21-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="74b21-118">-ParentResourceId</span></span>
<span data-ttu-id="74b21-119">ID risorsa del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="74b21-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="74b21-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b21-120">-ResourceGroupName</span></span>
<span data-ttu-id="74b21-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="74b21-121">Resource Group name.</span></span>

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

### <span data-ttu-id="74b21-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="74b21-122">-ServiceName</span></span>
<span data-ttu-id="74b21-123">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="74b21-123">Search Service name.</span></span>

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

### <span data-ttu-id="74b21-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b21-124">CommonParameters</span></span>
<span data-ttu-id="74b21-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74b21-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b21-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74b21-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b21-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74b21-127">INPUTS</span></span>

### <span data-ttu-id="74b21-128">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="74b21-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="74b21-129">Parametri: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="74b21-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="74b21-130">System. String</span><span class="sxs-lookup"><span data-stu-id="74b21-130">System.String</span></span>

## <span data-ttu-id="74b21-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74b21-131">OUTPUTS</span></span>

### <span data-ttu-id="74b21-132">Microsoft. Azure. Commands. Management. search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="74b21-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="74b21-133">Note</span><span class="sxs-lookup"><span data-stu-id="74b21-133">NOTES</span></span>

## <span data-ttu-id="74b21-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74b21-134">RELATED LINKS</span></span>

[<span data-ttu-id="74b21-135">New-AzureRmSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="74b21-135">New-AzureRmSearchAdminKey</span></span>](./New-AzureRmSearchAdminKey.md)
