---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6713b912f962a7a85627ca2280d6195cc5c5d88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491373"
---
# <span data-ttu-id="ee78b-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="ee78b-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="ee78b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee78b-102">SYNOPSIS</span></span>
<span data-ttu-id="ee78b-103">Restituisce un elenco di stato di integrità dell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="ee78b-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="ee78b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee78b-104">SYNTAX</span></span>

### <span data-ttu-id="ee78b-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ee78b-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee78b-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="ee78b-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ee78b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee78b-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ee78b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee78b-108">DESCRIPTION</span></span>
<span data-ttu-id="ee78b-109">Restituisce un elenco di stato di integrità dell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="ee78b-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="ee78b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee78b-110">EXAMPLES</span></span>

### <span data-ttu-id="ee78b-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ee78b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="ee78b-112">Restituisce un elenco di stato di integrità dell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="ee78b-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="ee78b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee78b-113">PARAMETERS</span></span>

### <span data-ttu-id="ee78b-114">-Filtro</span><span class="sxs-lookup"><span data-stu-id="ee78b-114">-Filter</span></span>
<span data-ttu-id="ee78b-115">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="ee78b-115">OData filter parameter.</span></span>

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

### <span data-ttu-id="ee78b-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ee78b-116">-Location</span></span>
<span data-ttu-id="ee78b-117">Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="ee78b-117">Name of the region</span></span>

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

### <span data-ttu-id="ee78b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee78b-118">-ResourceGroupName</span></span>
<span data-ttu-id="ee78b-119">Nome del gruppo di risorse che la risorsa risiede.</span><span class="sxs-lookup"><span data-stu-id="ee78b-119">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="ee78b-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee78b-120">-ResourceId</span></span>
<span data-ttu-id="ee78b-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="ee78b-121">The resource id.</span></span>

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

### <span data-ttu-id="ee78b-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="ee78b-122">-Skip</span></span>
<span data-ttu-id="ee78b-123">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="ee78b-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ee78b-124">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="ee78b-124">-Top</span></span>
<span data-ttu-id="ee78b-125">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="ee78b-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ee78b-126">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="ee78b-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ee78b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee78b-127">CommonParameters</span></span>
<span data-ttu-id="ee78b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee78b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee78b-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee78b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee78b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee78b-130">INPUTS</span></span>

## <span data-ttu-id="ee78b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee78b-131">OUTPUTS</span></span>

### <span data-ttu-id="ee78b-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="ee78b-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="ee78b-133">Note</span><span class="sxs-lookup"><span data-stu-id="ee78b-133">NOTES</span></span>

## <span data-ttu-id="ee78b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee78b-134">RELATED LINKS</span></span>

