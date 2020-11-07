---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3874c581d1d030f9c0b77abe82b5a5a289d8960d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859554"
---
# <span data-ttu-id="0a2aa-101">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="0a2aa-101">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="0a2aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a2aa-102">SYNOPSIS</span></span>
<span data-ttu-id="0a2aa-103">Ottenere l'elenco delle quote del provider di risorse di sottoscrizione in una posizione.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-103">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="0a2aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a2aa-104">SYNTAX</span></span>

### <span data-ttu-id="0a2aa-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0a2aa-105">List (Default)</span></span>
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="0a2aa-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="0a2aa-106">Get</span></span>
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="0a2aa-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a2aa-107">ResourceId</span></span>
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0a2aa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a2aa-108">DESCRIPTION</span></span>
<span data-ttu-id="0a2aa-109">Ottenere l'elenco di quote in una posizione.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-109">Get the list of quotas at a location.</span></span>

## <span data-ttu-id="0a2aa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a2aa-110">EXAMPLES</span></span>

### <span data-ttu-id="0a2aa-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0a2aa-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionsQuota
```

<span data-ttu-id="0a2aa-112">Ottenere l'elenco delle quote del provider di risorse di sottoscrizione in una posizione.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-112">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="0a2aa-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a2aa-113">PARAMETERS</span></span>

### <span data-ttu-id="0a2aa-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0a2aa-114">-Location</span></span>
<span data-ttu-id="0a2aa-115">La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-115">The AzureStack location.</span></span>

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

### <span data-ttu-id="0a2aa-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a2aa-116">-Name</span></span>
<span data-ttu-id="0a2aa-117">Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-117">Name of the quota.</span></span>

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

### <span data-ttu-id="0a2aa-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a2aa-118">-ResourceId</span></span>
<span data-ttu-id="0a2aa-119">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-119">The resource id.</span></span>

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

### <span data-ttu-id="0a2aa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a2aa-120">CommonParameters</span></span>
<span data-ttu-id="0a2aa-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a2aa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a2aa-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a2aa-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a2aa-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a2aa-123">INPUTS</span></span>

## <span data-ttu-id="0a2aa-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a2aa-124">OUTPUTS</span></span>

### <span data-ttu-id="0a2aa-125">Microsoft. AzureStack. Management. subscriptions. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="0a2aa-125">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Quota</span></span>

## <span data-ttu-id="0a2aa-126">Note</span><span class="sxs-lookup"><span data-stu-id="0a2aa-126">NOTES</span></span>

## <span data-ttu-id="0a2aa-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a2aa-127">RELATED LINKS</span></span>

