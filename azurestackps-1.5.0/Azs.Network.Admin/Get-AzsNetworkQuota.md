---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb5d980efc5f4e4ad7aff13a8f91832589175039
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491113"
---
# <span data-ttu-id="7730e-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="7730e-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="7730e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7730e-102">SYNOPSIS</span></span>
<span data-ttu-id="7730e-103">Elencare tutte le quote.</span><span class="sxs-lookup"><span data-stu-id="7730e-103">List all quotas.</span></span>

## <span data-ttu-id="7730e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7730e-104">SYNTAX</span></span>

### <span data-ttu-id="7730e-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7730e-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="7730e-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="7730e-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="7730e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7730e-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7730e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7730e-108">DESCRIPTION</span></span>
<span data-ttu-id="7730e-109">Elencare tutte le quote.</span><span class="sxs-lookup"><span data-stu-id="7730e-109">List all quotas.</span></span>
<span data-ttu-id="7730e-110">Limitare l'elenco passando un nome o un filtro.</span><span class="sxs-lookup"><span data-stu-id="7730e-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="7730e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7730e-111">EXAMPLES</span></span>

### <span data-ttu-id="7730e-112">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7730e-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="7730e-113">Elenca tutte le quote di rete.</span><span class="sxs-lookup"><span data-stu-id="7730e-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="7730e-114">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7730e-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="7730e-115">Ottiene la quota di rete specificata.</span><span class="sxs-lookup"><span data-stu-id="7730e-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="7730e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7730e-116">PARAMETERS</span></span>

### <span data-ttu-id="7730e-117">-Filtro</span><span class="sxs-lookup"><span data-stu-id="7730e-117">-Filter</span></span>
<span data-ttu-id="7730e-118">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="7730e-118">OData filter parameter.</span></span>

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

### <span data-ttu-id="7730e-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7730e-119">-Location</span></span>
<span data-ttu-id="7730e-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7730e-120">Location of the resource.</span></span>

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

### <span data-ttu-id="7730e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7730e-121">-Name</span></span>
<span data-ttu-id="7730e-122">Nome risorsa della quota di rete.</span><span class="sxs-lookup"><span data-stu-id="7730e-122">Network quota resource name.</span></span>

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

### <span data-ttu-id="7730e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7730e-123">-ResourceId</span></span>
<span data-ttu-id="7730e-124">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="7730e-124">The resource id.</span></span>

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

### <span data-ttu-id="7730e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7730e-125">CommonParameters</span></span>
<span data-ttu-id="7730e-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7730e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7730e-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7730e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7730e-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7730e-128">INPUTS</span></span>

## <span data-ttu-id="7730e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7730e-129">OUTPUTS</span></span>

### <span data-ttu-id="7730e-130">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="7730e-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="7730e-131">Note</span><span class="sxs-lookup"><span data-stu-id="7730e-131">NOTES</span></span>

## <span data-ttu-id="7730e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7730e-132">RELATED LINKS</span></span>

