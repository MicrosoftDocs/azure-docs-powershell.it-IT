---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc074d17ea73bf54f623ea3e8ec72567ef2bcffe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859673"
---
# <span data-ttu-id="24251-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="24251-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="24251-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24251-102">SYNOPSIS</span></span>
<span data-ttu-id="24251-103">Restituisce un elenco di tutte le posizioni in tessuto.</span><span class="sxs-lookup"><span data-stu-id="24251-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="24251-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24251-104">SYNTAX</span></span>

### <span data-ttu-id="24251-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="24251-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="24251-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="24251-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="24251-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="24251-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="24251-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24251-108">DESCRIPTION</span></span>
<span data-ttu-id="24251-109">Restituisce un elenco di tutte le posizioni in tessuto.</span><span class="sxs-lookup"><span data-stu-id="24251-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="24251-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24251-110">EXAMPLES</span></span>

### <span data-ttu-id="24251-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="24251-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="24251-112">Restituisce un elenco di tutte le posizioni in tessuto.</span><span class="sxs-lookup"><span data-stu-id="24251-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="24251-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="24251-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="24251-114">Restituire una posizione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="24251-114">Return a location based on the name.</span></span>

## <span data-ttu-id="24251-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24251-115">PARAMETERS</span></span>

### <span data-ttu-id="24251-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="24251-116">-Location</span></span>
<span data-ttu-id="24251-117">Posizione del tessuto.</span><span class="sxs-lookup"><span data-stu-id="24251-117">Fabric location.</span></span>

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

### <span data-ttu-id="24251-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24251-118">-ResourceGroupName</span></span>
<span data-ttu-id="24251-119">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="24251-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="24251-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24251-120">-ResourceId</span></span>
<span data-ttu-id="24251-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="24251-121">The resource id.</span></span>

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

### <span data-ttu-id="24251-122">-Filtro</span><span class="sxs-lookup"><span data-stu-id="24251-122">-Filter</span></span>
<span data-ttu-id="24251-123">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="24251-123">OData filter parameter.</span></span>

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

### <span data-ttu-id="24251-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="24251-124">-Skip</span></span>
<span data-ttu-id="24251-125">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="24251-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="24251-126">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="24251-126">-Top</span></span>
<span data-ttu-id="24251-127">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="24251-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="24251-128">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="24251-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="24251-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24251-129">CommonParameters</span></span>
<span data-ttu-id="24251-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24251-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24251-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24251-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24251-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24251-132">INPUTS</span></span>

## <span data-ttu-id="24251-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24251-133">OUTPUTS</span></span>

### <span data-ttu-id="24251-134">Microsoft. AzureStack. Management. Fabric. admin. Models. FabricLocation</span><span class="sxs-lookup"><span data-stu-id="24251-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="24251-135">Note</span><span class="sxs-lookup"><span data-stu-id="24251-135">NOTES</span></span>

## <span data-ttu-id="24251-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24251-136">RELATED LINKS</span></span>
