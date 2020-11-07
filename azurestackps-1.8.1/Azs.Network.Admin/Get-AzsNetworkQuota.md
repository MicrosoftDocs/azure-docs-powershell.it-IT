---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3def97a3e02e77efd6ec21768b30c855f1ceb34e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859882"
---
# <span data-ttu-id="77446-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="77446-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="77446-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77446-102">SYNOPSIS</span></span>
<span data-ttu-id="77446-103">Elencare tutte le quote.</span><span class="sxs-lookup"><span data-stu-id="77446-103">List all quotas.</span></span>

## <span data-ttu-id="77446-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77446-104">SYNTAX</span></span>

### <span data-ttu-id="77446-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="77446-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="77446-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="77446-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="77446-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="77446-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="77446-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77446-108">DESCRIPTION</span></span>
<span data-ttu-id="77446-109">Elencare tutte le quote.</span><span class="sxs-lookup"><span data-stu-id="77446-109">List all quotas.</span></span>
<span data-ttu-id="77446-110">Limitare l'elenco passando un nome o un filtro.</span><span class="sxs-lookup"><span data-stu-id="77446-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="77446-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77446-111">EXAMPLES</span></span>

### <span data-ttu-id="77446-112">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="77446-112">EXAMPLE 1</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="77446-113">Elenca tutte le quote di rete.</span><span class="sxs-lookup"><span data-stu-id="77446-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="77446-114">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="77446-114">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="77446-115">Ottiene la quota di rete specificata.</span><span class="sxs-lookup"><span data-stu-id="77446-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="77446-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77446-116">PARAMETERS</span></span>

### <span data-ttu-id="77446-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="77446-117">-Name</span></span>
<span data-ttu-id="77446-118">Nome risorsa della quota di rete.</span><span class="sxs-lookup"><span data-stu-id="77446-118">Network quota resource name.</span></span>

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

### <span data-ttu-id="77446-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="77446-119">-Location</span></span>
<span data-ttu-id="77446-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="77446-120">Location of the resource.</span></span>

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

### <span data-ttu-id="77446-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77446-121">-ResourceId</span></span>
<span data-ttu-id="77446-122">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="77446-122">The resource id.</span></span>

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

### <span data-ttu-id="77446-123">-Filtro</span><span class="sxs-lookup"><span data-stu-id="77446-123">-Filter</span></span>
<span data-ttu-id="77446-124">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="77446-124">OData filter parameter.</span></span>

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

### <span data-ttu-id="77446-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77446-125">CommonParameters</span></span>
<span data-ttu-id="77446-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77446-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77446-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77446-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77446-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77446-128">INPUTS</span></span>

## <span data-ttu-id="77446-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77446-129">OUTPUTS</span></span>

### <span data-ttu-id="77446-130">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="77446-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="77446-131">Note</span><span class="sxs-lookup"><span data-stu-id="77446-131">NOTES</span></span>

## <span data-ttu-id="77446-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77446-132">RELATED LINKS</span></span>
