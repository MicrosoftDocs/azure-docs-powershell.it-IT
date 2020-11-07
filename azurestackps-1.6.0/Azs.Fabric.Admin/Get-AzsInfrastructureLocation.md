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
ms.locfileid: "93685146"
---
# <span data-ttu-id="ff106-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="ff106-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="ff106-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff106-102">SYNOPSIS</span></span>
<span data-ttu-id="ff106-103">Restituisce un elenco di tutte le posizioni in tessuto.</span><span class="sxs-lookup"><span data-stu-id="ff106-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="ff106-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff106-104">SYNTAX</span></span>

### <span data-ttu-id="ff106-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ff106-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff106-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="ff106-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ff106-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff106-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ff106-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff106-108">DESCRIPTION</span></span>
<span data-ttu-id="ff106-109">Restituisce un elenco di tutte le posizioni in tessuto.</span><span class="sxs-lookup"><span data-stu-id="ff106-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="ff106-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff106-110">EXAMPLES</span></span>

### <span data-ttu-id="ff106-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ff106-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="ff106-112">Restituisce un elenco di tutte le posizioni in tessuto.</span><span class="sxs-lookup"><span data-stu-id="ff106-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="ff106-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ff106-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="ff106-114">Restituire una posizione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="ff106-114">Return a location based on the name.</span></span>

## <span data-ttu-id="ff106-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff106-115">PARAMETERS</span></span>

### <span data-ttu-id="ff106-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="ff106-116">-Filter</span></span>
<span data-ttu-id="ff106-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="ff106-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="ff106-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ff106-118">-Location</span></span>
<span data-ttu-id="ff106-119">Posizione del tessuto.</span><span class="sxs-lookup"><span data-stu-id="ff106-119">Fabric location.</span></span>

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

### <span data-ttu-id="ff106-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff106-120">-ResourceGroupName</span></span>
<span data-ttu-id="ff106-121">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="ff106-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ff106-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff106-122">-ResourceId</span></span>
<span data-ttu-id="ff106-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="ff106-123">The resource id.</span></span>

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

### <span data-ttu-id="ff106-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="ff106-124">-Skip</span></span>
<span data-ttu-id="ff106-125">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="ff106-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ff106-126">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="ff106-126">-Top</span></span>
<span data-ttu-id="ff106-127">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="ff106-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ff106-128">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="ff106-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ff106-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff106-129">CommonParameters</span></span>
<span data-ttu-id="ff106-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff106-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff106-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff106-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff106-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff106-132">INPUTS</span></span>

## <span data-ttu-id="ff106-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff106-133">OUTPUTS</span></span>

### <span data-ttu-id="ff106-134">Microsoft. AzureStack. Management. Fabric. admin. Models. FabricLocation</span><span class="sxs-lookup"><span data-stu-id="ff106-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="ff106-135">Note</span><span class="sxs-lookup"><span data-stu-id="ff106-135">NOTES</span></span>

## <span data-ttu-id="ff106-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff106-136">RELATED LINKS</span></span>

