---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3874c581d1d030f9c0b77abe82b5a5a289d8960d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030446"
---
# <span data-ttu-id="469ef-101">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="469ef-101">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="469ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="469ef-102">SYNOPSIS</span></span>
<span data-ttu-id="469ef-103">Ottenere l'elenco delle quote del provider di risorse di sottoscrizione in una posizione.</span><span class="sxs-lookup"><span data-stu-id="469ef-103">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="469ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="469ef-104">SYNTAX</span></span>

### <span data-ttu-id="469ef-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="469ef-105">List (Default)</span></span>
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="469ef-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="469ef-106">Get</span></span>
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="469ef-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="469ef-107">ResourceId</span></span>
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="469ef-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="469ef-108">DESCRIPTION</span></span>
<span data-ttu-id="469ef-109">Ottenere l'elenco di quote in una posizione.</span><span class="sxs-lookup"><span data-stu-id="469ef-109">Get the list of quotas at a location.</span></span>

## <span data-ttu-id="469ef-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="469ef-110">EXAMPLES</span></span>

### <span data-ttu-id="469ef-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="469ef-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionsQuota
```

<span data-ttu-id="469ef-112">Ottenere l'elenco delle quote del provider di risorse di sottoscrizione in una posizione.</span><span class="sxs-lookup"><span data-stu-id="469ef-112">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="469ef-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="469ef-113">PARAMETERS</span></span>

### <span data-ttu-id="469ef-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="469ef-114">-Location</span></span>
<span data-ttu-id="469ef-115">La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="469ef-115">The AzureStack location.</span></span>

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

### <span data-ttu-id="469ef-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="469ef-116">-Name</span></span>
<span data-ttu-id="469ef-117">Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="469ef-117">Name of the quota.</span></span>

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

### <span data-ttu-id="469ef-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="469ef-118">-ResourceId</span></span>
<span data-ttu-id="469ef-119">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="469ef-119">The resource id.</span></span>

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

### <span data-ttu-id="469ef-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="469ef-120">CommonParameters</span></span>
<span data-ttu-id="469ef-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="469ef-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="469ef-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="469ef-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="469ef-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="469ef-123">INPUTS</span></span>

## <span data-ttu-id="469ef-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="469ef-124">OUTPUTS</span></span>

### <span data-ttu-id="469ef-125">Microsoft. AzureStack. Management. subscriptions. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="469ef-125">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Quota</span></span>

## <span data-ttu-id="469ef-126">Note</span><span class="sxs-lookup"><span data-stu-id="469ef-126">NOTES</span></span>

## <span data-ttu-id="469ef-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="469ef-127">RELATED LINKS</span></span>

