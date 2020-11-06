---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503661f4e50ddd7575cc9c98ef4c19e2028ddf83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491521"
---
# <span data-ttu-id="a142c-101">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="a142c-101">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="a142c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a142c-102">SYNOPSIS</span></span>
<span data-ttu-id="a142c-103">Ottenere l'elenco delle quote del provider di risorse di sottoscrizione in una posizione.</span><span class="sxs-lookup"><span data-stu-id="a142c-103">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="a142c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a142c-104">SYNTAX</span></span>

### <span data-ttu-id="a142c-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a142c-105">List (Default)</span></span>
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="a142c-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="a142c-106">Get</span></span>
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="a142c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a142c-107">ResourceId</span></span>
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a142c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a142c-108">DESCRIPTION</span></span>
<span data-ttu-id="a142c-109">Ottenere l'elenco di quote in una posizione.</span><span class="sxs-lookup"><span data-stu-id="a142c-109">Get the list of quotas at a location.</span></span>

## <span data-ttu-id="a142c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a142c-110">EXAMPLES</span></span>

### <span data-ttu-id="a142c-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a142c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionsQuota
```

<span data-ttu-id="a142c-112">Ottenere l'elenco delle quote del provider di risorse di sottoscrizione in una posizione.</span><span class="sxs-lookup"><span data-stu-id="a142c-112">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="a142c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a142c-113">PARAMETERS</span></span>

### <span data-ttu-id="a142c-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a142c-114">-Location</span></span>
<span data-ttu-id="a142c-115">La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="a142c-115">The AzureStack location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a142c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a142c-116">-Name</span></span>
<span data-ttu-id="a142c-117">Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="a142c-117">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a142c-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a142c-118">-ResourceId</span></span>
<span data-ttu-id="a142c-119">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a142c-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a142c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a142c-120">CommonParameters</span></span>
<span data-ttu-id="a142c-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a142c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a142c-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a142c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a142c-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a142c-123">INPUTS</span></span>

## <span data-ttu-id="a142c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a142c-124">OUTPUTS</span></span>

### <span data-ttu-id="a142c-125">Microsoft. AzureStack. Management. subscriptions. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="a142c-125">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Quota</span></span>

## <span data-ttu-id="a142c-126">Note</span><span class="sxs-lookup"><span data-stu-id="a142c-126">NOTES</span></span>

## <span data-ttu-id="a142c-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a142c-127">RELATED LINKS</span></span>
