---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d07aad989b08909228aebca7538b007f36bfcab
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859101"
---
# <span data-ttu-id="bdd86-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="bdd86-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="bdd86-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bdd86-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd86-103">Restituisce un elenco di stato di integrità dell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="bdd86-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="bdd86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bdd86-104">SYNTAX</span></span>

### <span data-ttu-id="bdd86-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bdd86-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="bdd86-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="bdd86-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="bdd86-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdd86-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="bdd86-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdd86-108">DESCRIPTION</span></span>
<span data-ttu-id="bdd86-109">Restituisce un elenco di stato di integrità dell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="bdd86-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="bdd86-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bdd86-110">EXAMPLES</span></span>

### <span data-ttu-id="bdd86-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="bdd86-111">EXAMPLE 1</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="bdd86-112">Restituisce un elenco di stato di integrità dell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="bdd86-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="bdd86-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bdd86-113">PARAMETERS</span></span>

### <span data-ttu-id="bdd86-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bdd86-114">-Location</span></span>
<span data-ttu-id="bdd86-115">Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="bdd86-115">Name of the region</span></span>

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

### <span data-ttu-id="bdd86-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdd86-116">-ResourceGroupName</span></span>
<span data-ttu-id="bdd86-117">Nome del gruppo di risorse facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bdd86-117">Resource group name, optional.</span></span>

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

### <span data-ttu-id="bdd86-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdd86-118">-ResourceId</span></span>
<span data-ttu-id="bdd86-119">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="bdd86-119">The resource id.</span></span>

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

### <span data-ttu-id="bdd86-120">-Filtro</span><span class="sxs-lookup"><span data-stu-id="bdd86-120">-Filter</span></span>
<span data-ttu-id="bdd86-121">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="bdd86-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="bdd86-122">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="bdd86-122">-Top</span></span>
<span data-ttu-id="bdd86-123">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="bdd86-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="bdd86-124">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="bdd86-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd86-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="bdd86-125">-Skip</span></span>
<span data-ttu-id="bdd86-126">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="bdd86-126">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd86-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd86-127">CommonParameters</span></span>
<span data-ttu-id="bdd86-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdd86-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd86-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdd86-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd86-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bdd86-130">INPUTS</span></span>

## <span data-ttu-id="bdd86-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bdd86-131">OUTPUTS</span></span>

### <span data-ttu-id="bdd86-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="bdd86-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="bdd86-133">Note</span><span class="sxs-lookup"><span data-stu-id="bdd86-133">NOTES</span></span>

## <span data-ttu-id="bdd86-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bdd86-134">RELATED LINKS</span></span>
