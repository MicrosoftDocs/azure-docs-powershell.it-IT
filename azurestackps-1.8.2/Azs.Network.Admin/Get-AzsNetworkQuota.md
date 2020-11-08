---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3def97a3e02e77efd6ec21768b30c855f1ceb34e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030453"
---
# <span data-ttu-id="ad1c6-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="ad1c6-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="ad1c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad1c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ad1c6-103">Elencare tutte le quote.</span><span class="sxs-lookup"><span data-stu-id="ad1c6-103">List all quotas.</span></span>

## <span data-ttu-id="ad1c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad1c6-104">SYNTAX</span></span>

### <span data-ttu-id="ad1c6-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad1c6-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="ad1c6-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="ad1c6-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="ad1c6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad1c6-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ad1c6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad1c6-108">DESCRIPTION</span></span>
<span data-ttu-id="ad1c6-109">Elencare tutte le quote.</span><span class="sxs-lookup"><span data-stu-id="ad1c6-109">List all quotas.</span></span>
<span data-ttu-id="ad1c6-110">Limitare l'elenco passando un nome o un filtro.</span><span class="sxs-lookup"><span data-stu-id="ad1c6-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="ad1c6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad1c6-111">EXAMPLES</span></span>

### <span data-ttu-id="ad1c6-112">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="ad1c6-112">EXAMPLE 1</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="ad1c6-113">Elenca tutte le quote di rete.</span><span class="sxs-lookup"><span data-stu-id="ad1c6-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="ad1c6-114">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="ad1c6-114">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="ad1c6-115">Ottiene la quota di rete specificata.</span><span class="sxs-lookup"><span data-stu-id="ad1c6-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="ad1c6-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad1c6-116">PARAMETERS</span></span>

### <span data-ttu-id="ad1c6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad1c6-117">-Name</span></span>
<span data-ttu-id="ad1c6-118">Nome risorsa della quota di rete.</span><span class="sxs-lookup"><span data-stu-id="ad1c6-118">Network quota resource name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1c6-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ad1c6-119">-Location</span></span>
<span data-ttu-id="ad1c6-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ad1c6-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1c6-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad1c6-121">-ResourceId</span></span>
<span data-ttu-id="ad1c6-122">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="ad1c6-122">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1c6-123">-Filtro</span><span class="sxs-lookup"><span data-stu-id="ad1c6-123">-Filter</span></span>
<span data-ttu-id="ad1c6-124">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="ad1c6-124">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1c6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad1c6-125">CommonParameters</span></span>
<span data-ttu-id="ad1c6-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad1c6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad1c6-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad1c6-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad1c6-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad1c6-128">INPUTS</span></span>

## <span data-ttu-id="ad1c6-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad1c6-129">OUTPUTS</span></span>

### <span data-ttu-id="ad1c6-130">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="ad1c6-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="ad1c6-131">Note</span><span class="sxs-lookup"><span data-stu-id="ad1c6-131">NOTES</span></span>

## <span data-ttu-id="ad1c6-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad1c6-132">RELATED LINKS</span></span>
