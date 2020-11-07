---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb535146787c4c33a57ad406f05544f18ba74eb0
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859642"
---
# <span data-ttu-id="b3e6e-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="b3e6e-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="b3e6e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3e6e-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e6e-103">Restituisce un elenco di tutte le subnet logiche.</span><span class="sxs-lookup"><span data-stu-id="b3e6e-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="b3e6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3e6e-104">SYNTAX</span></span>

### <span data-ttu-id="b3e6e-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b3e6e-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b3e6e-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="b3e6e-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3e6e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3e6e-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b3e6e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3e6e-108">DESCRIPTION</span></span>
<span data-ttu-id="b3e6e-109">Restituisce un elenco di tutte le subnet logiche.</span><span class="sxs-lookup"><span data-stu-id="b3e6e-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="b3e6e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3e6e-110">EXAMPLES</span></span>

### <span data-ttu-id="b3e6e-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="b3e6e-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="b3e6e-112">Ottenere un elenco di tutte le subnet logiche per una determinata rete logica e posizione.</span><span class="sxs-lookup"><span data-stu-id="b3e6e-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="b3e6e-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="b3e6e-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="b3e6e-114">Ottenere una subnet logica specifica per una data rete logica e una posizione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="b3e6e-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="b3e6e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3e6e-115">PARAMETERS</span></span>

### <span data-ttu-id="b3e6e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3e6e-116">-Name</span></span>
<span data-ttu-id="b3e6e-117">Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="b3e6e-117">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="b3e6e-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="b3e6e-118">-LogicalNetwork</span></span>
<span data-ttu-id="b3e6e-119">Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="b3e6e-119">Name of the logical network.</span></span>

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

### <span data-ttu-id="b3e6e-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b3e6e-120">-Location</span></span>
<span data-ttu-id="b3e6e-121">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b3e6e-121">Location of the resource.</span></span>

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

### <span data-ttu-id="b3e6e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3e6e-122">-ResourceGroupName</span></span>
<span data-ttu-id="b3e6e-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="b3e6e-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b3e6e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3e6e-124">-ResourceId</span></span>
<span data-ttu-id="b3e6e-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b3e6e-125">The resource id.</span></span>

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

### <span data-ttu-id="b3e6e-126">-Filtro</span><span class="sxs-lookup"><span data-stu-id="b3e6e-126">-Filter</span></span>
<span data-ttu-id="b3e6e-127">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="b3e6e-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="b3e6e-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="b3e6e-128">-Skip</span></span>
<span data-ttu-id="b3e6e-129">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="b3e6e-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b3e6e-130">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="b3e6e-130">-Top</span></span>
<span data-ttu-id="b3e6e-131">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="b3e6e-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b3e6e-132">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="b3e6e-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b3e6e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e6e-133">CommonParameters</span></span>
<span data-ttu-id="b3e6e-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3e6e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e6e-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3e6e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e6e-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3e6e-136">INPUTS</span></span>

## <span data-ttu-id="b3e6e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3e6e-137">OUTPUTS</span></span>

### <span data-ttu-id="b3e6e-138">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="b3e6e-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="b3e6e-139">Note</span><span class="sxs-lookup"><span data-stu-id="b3e6e-139">NOTES</span></span>

## <span data-ttu-id="b3e6e-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3e6e-140">RELATED LINKS</span></span>
