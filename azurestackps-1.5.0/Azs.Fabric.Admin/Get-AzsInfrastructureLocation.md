---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcd5d112fea0ec68e372a5ad282b3d661f9481ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491430"
---
# <span data-ttu-id="e45c1-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="e45c1-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="e45c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e45c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e45c1-103">Restituisce un elenco di tutte le posizioni in tessuto.</span><span class="sxs-lookup"><span data-stu-id="e45c1-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="e45c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e45c1-104">SYNTAX</span></span>

### <span data-ttu-id="e45c1-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e45c1-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="e45c1-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="e45c1-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e45c1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e45c1-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e45c1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e45c1-108">DESCRIPTION</span></span>
<span data-ttu-id="e45c1-109">Restituisce un elenco di tutte le posizioni in tessuto.</span><span class="sxs-lookup"><span data-stu-id="e45c1-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="e45c1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e45c1-110">EXAMPLES</span></span>

### <span data-ttu-id="e45c1-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e45c1-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="e45c1-112">Restituisce un elenco di tutte le posizioni in tessuto.</span><span class="sxs-lookup"><span data-stu-id="e45c1-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="e45c1-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e45c1-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="e45c1-114">Restituire una posizione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="e45c1-114">Return a location based on the name.</span></span>

## <span data-ttu-id="e45c1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e45c1-115">PARAMETERS</span></span>

### <span data-ttu-id="e45c1-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="e45c1-116">-Filter</span></span>
<span data-ttu-id="e45c1-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="e45c1-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="e45c1-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e45c1-118">-Location</span></span>
<span data-ttu-id="e45c1-119">Posizione del tessuto.</span><span class="sxs-lookup"><span data-stu-id="e45c1-119">Fabric location.</span></span>

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

### <span data-ttu-id="e45c1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e45c1-120">-ResourceGroupName</span></span>
<span data-ttu-id="e45c1-121">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="e45c1-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e45c1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e45c1-122">-ResourceId</span></span>
<span data-ttu-id="e45c1-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e45c1-123">The resource id.</span></span>

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

### <span data-ttu-id="e45c1-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="e45c1-124">-Skip</span></span>
<span data-ttu-id="e45c1-125">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="e45c1-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e45c1-126">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="e45c1-126">-Top</span></span>
<span data-ttu-id="e45c1-127">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="e45c1-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e45c1-128">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="e45c1-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e45c1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e45c1-129">CommonParameters</span></span>
<span data-ttu-id="e45c1-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e45c1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e45c1-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e45c1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e45c1-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e45c1-132">INPUTS</span></span>

## <span data-ttu-id="e45c1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e45c1-133">OUTPUTS</span></span>

### <span data-ttu-id="e45c1-134">Microsoft. AzureStack. Management. Fabric. admin. Models. FabricLocation</span><span class="sxs-lookup"><span data-stu-id="e45c1-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="e45c1-135">Note</span><span class="sxs-lookup"><span data-stu-id="e45c1-135">NOTES</span></span>

## <span data-ttu-id="e45c1-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e45c1-136">RELATED LINKS</span></span>

