---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb535146787c4c33a57ad406f05544f18ba74eb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93858962"
---
# <span data-ttu-id="8cacc-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="8cacc-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="8cacc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cacc-102">SYNOPSIS</span></span>
<span data-ttu-id="8cacc-103">Restituisce un elenco di tutte le subnet logiche.</span><span class="sxs-lookup"><span data-stu-id="8cacc-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="8cacc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cacc-104">SYNTAX</span></span>

### <span data-ttu-id="8cacc-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8cacc-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8cacc-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="8cacc-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8cacc-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cacc-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8cacc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cacc-108">DESCRIPTION</span></span>
<span data-ttu-id="8cacc-109">Restituisce un elenco di tutte le subnet logiche.</span><span class="sxs-lookup"><span data-stu-id="8cacc-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="8cacc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cacc-110">EXAMPLES</span></span>

### <span data-ttu-id="8cacc-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="8cacc-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="8cacc-112">Ottenere un elenco di tutte le subnet logiche per una determinata rete logica e posizione.</span><span class="sxs-lookup"><span data-stu-id="8cacc-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="8cacc-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="8cacc-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="8cacc-114">Ottenere una subnet logica specifica per una data rete logica e una posizione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="8cacc-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="8cacc-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cacc-115">PARAMETERS</span></span>

### <span data-ttu-id="8cacc-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cacc-116">-Name</span></span>
<span data-ttu-id="8cacc-117">Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="8cacc-117">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="8cacc-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="8cacc-118">-LogicalNetwork</span></span>
<span data-ttu-id="8cacc-119">Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="8cacc-119">Name of the logical network.</span></span>

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

### <span data-ttu-id="8cacc-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8cacc-120">-Location</span></span>
<span data-ttu-id="8cacc-121">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8cacc-121">Location of the resource.</span></span>

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

### <span data-ttu-id="8cacc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cacc-122">-ResourceGroupName</span></span>
<span data-ttu-id="8cacc-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="8cacc-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="8cacc-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cacc-124">-ResourceId</span></span>
<span data-ttu-id="8cacc-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="8cacc-125">The resource id.</span></span>

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

### <span data-ttu-id="8cacc-126">-Filtro</span><span class="sxs-lookup"><span data-stu-id="8cacc-126">-Filter</span></span>
<span data-ttu-id="8cacc-127">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="8cacc-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="8cacc-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="8cacc-128">-Skip</span></span>
<span data-ttu-id="8cacc-129">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="8cacc-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="8cacc-130">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="8cacc-130">-Top</span></span>
<span data-ttu-id="8cacc-131">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="8cacc-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="8cacc-132">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="8cacc-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="8cacc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cacc-133">CommonParameters</span></span>
<span data-ttu-id="8cacc-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cacc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cacc-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cacc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cacc-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cacc-136">INPUTS</span></span>

## <span data-ttu-id="8cacc-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cacc-137">OUTPUTS</span></span>

### <span data-ttu-id="8cacc-138">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="8cacc-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="8cacc-139">Note</span><span class="sxs-lookup"><span data-stu-id="8cacc-139">NOTES</span></span>

## <span data-ttu-id="8cacc-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cacc-140">RELATED LINKS</span></span>
