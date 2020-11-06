---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef5db457846f6fdf0dcd0a0a32b37cab96a557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491593"
---
# <span data-ttu-id="6644a-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="6644a-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="6644a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6644a-102">SYNOPSIS</span></span>
<span data-ttu-id="6644a-103">Restituisce un elenco di tutte le subnet logiche.</span><span class="sxs-lookup"><span data-stu-id="6644a-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="6644a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6644a-104">SYNTAX</span></span>

### <span data-ttu-id="6644a-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6644a-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6644a-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="6644a-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6644a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6644a-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6644a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6644a-108">DESCRIPTION</span></span>
<span data-ttu-id="6644a-109">Restituisce un elenco di tutte le subnet logiche.</span><span class="sxs-lookup"><span data-stu-id="6644a-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="6644a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6644a-110">EXAMPLES</span></span>

### <span data-ttu-id="6644a-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6644a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="6644a-112">Ottenere un elenco di tutte le subnet logiche per una determinata rete logica e posizione.</span><span class="sxs-lookup"><span data-stu-id="6644a-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="6644a-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6644a-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="6644a-114">Ottenere una subnet logica specifica per una data rete logica e una posizione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="6644a-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="6644a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6644a-115">PARAMETERS</span></span>

### <span data-ttu-id="6644a-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="6644a-116">-Filter</span></span>
<span data-ttu-id="6644a-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="6644a-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="6644a-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6644a-118">-Location</span></span>
<span data-ttu-id="6644a-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6644a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="6644a-120">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="6644a-120">-LogicalNetwork</span></span>
<span data-ttu-id="6644a-121">Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="6644a-121">Name of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6644a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6644a-122">-Name</span></span>
<span data-ttu-id="6644a-123">Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="6644a-123">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="6644a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6644a-124">-ResourceGroupName</span></span>
<span data-ttu-id="6644a-125">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="6644a-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="6644a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6644a-126">-ResourceId</span></span>
<span data-ttu-id="6644a-127">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="6644a-127">The resource id.</span></span>

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

### <span data-ttu-id="6644a-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="6644a-128">-Skip</span></span>
<span data-ttu-id="6644a-129">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="6644a-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6644a-130">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="6644a-130">-Top</span></span>
<span data-ttu-id="6644a-131">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="6644a-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6644a-132">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="6644a-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6644a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6644a-133">CommonParameters</span></span>
<span data-ttu-id="6644a-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6644a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6644a-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6644a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6644a-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6644a-136">INPUTS</span></span>

## <span data-ttu-id="6644a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6644a-137">OUTPUTS</span></span>

### <span data-ttu-id="6644a-138">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="6644a-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="6644a-139">Note</span><span class="sxs-lookup"><span data-stu-id="6644a-139">NOTES</span></span>

## <span data-ttu-id="6644a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6644a-140">RELATED LINKS</span></span>
