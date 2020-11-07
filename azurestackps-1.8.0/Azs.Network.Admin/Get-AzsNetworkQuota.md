---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3def97a3e02e77efd6ec21768b30c855f1ceb34e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859302"
---
# <span data-ttu-id="1c7a3-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="1c7a3-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="1c7a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c7a3-102">SYNOPSIS</span></span>
<span data-ttu-id="1c7a3-103">Elencare tutte le quote.</span><span class="sxs-lookup"><span data-stu-id="1c7a3-103">List all quotas.</span></span>

## <span data-ttu-id="1c7a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c7a3-104">SYNTAX</span></span>

### <span data-ttu-id="1c7a3-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c7a3-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="1c7a3-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="1c7a3-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="1c7a3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c7a3-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1c7a3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c7a3-108">DESCRIPTION</span></span>
<span data-ttu-id="1c7a3-109">Elencare tutte le quote.</span><span class="sxs-lookup"><span data-stu-id="1c7a3-109">List all quotas.</span></span>
<span data-ttu-id="1c7a3-110">Limitare l'elenco passando un nome o un filtro.</span><span class="sxs-lookup"><span data-stu-id="1c7a3-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="1c7a3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c7a3-111">EXAMPLES</span></span>

### <span data-ttu-id="1c7a3-112">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="1c7a3-112">EXAMPLE 1</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="1c7a3-113">Elenca tutte le quote di rete.</span><span class="sxs-lookup"><span data-stu-id="1c7a3-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="1c7a3-114">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="1c7a3-114">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="1c7a3-115">Ottiene la quota di rete specificata.</span><span class="sxs-lookup"><span data-stu-id="1c7a3-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="1c7a3-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c7a3-116">PARAMETERS</span></span>

### <span data-ttu-id="1c7a3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c7a3-117">-Name</span></span>
<span data-ttu-id="1c7a3-118">Nome risorsa della quota di rete.</span><span class="sxs-lookup"><span data-stu-id="1c7a3-118">Network quota resource name.</span></span>

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

### <span data-ttu-id="1c7a3-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1c7a3-119">-Location</span></span>
<span data-ttu-id="1c7a3-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1c7a3-120">Location of the resource.</span></span>

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

### <span data-ttu-id="1c7a3-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c7a3-121">-ResourceId</span></span>
<span data-ttu-id="1c7a3-122">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="1c7a3-122">The resource id.</span></span>

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

### <span data-ttu-id="1c7a3-123">-Filtro</span><span class="sxs-lookup"><span data-stu-id="1c7a3-123">-Filter</span></span>
<span data-ttu-id="1c7a3-124">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="1c7a3-124">OData filter parameter.</span></span>

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

### <span data-ttu-id="1c7a3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c7a3-125">CommonParameters</span></span>
<span data-ttu-id="1c7a3-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c7a3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c7a3-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c7a3-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c7a3-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c7a3-128">INPUTS</span></span>

## <span data-ttu-id="1c7a3-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c7a3-129">OUTPUTS</span></span>

### <span data-ttu-id="1c7a3-130">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="1c7a3-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="1c7a3-131">Note</span><span class="sxs-lookup"><span data-stu-id="1c7a3-131">NOTES</span></span>

## <span data-ttu-id="1c7a3-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c7a3-132">RELATED LINKS</span></span>
