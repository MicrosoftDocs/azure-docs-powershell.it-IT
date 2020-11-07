---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1f1be36f51aab748ec790c56aea7092f1d3d877
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859678"
---
# <span data-ttu-id="a2ce8-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="a2ce8-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="a2ce8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ce8-103">Restituisce gli oggetti del pool di gateway in una posizione.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-103">Returns gateway pool objects at a location.</span></span>

## <span data-ttu-id="a2ce8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2ce8-104">SYNTAX</span></span>

### <span data-ttu-id="a2ce8-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a2ce8-105">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a2ce8-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="a2ce8-106">Get</span></span>
```
Get-AzsEdgeGatewayPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="a2ce8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2ce8-107">ResourceId</span></span>
```
Get-AzsEdgeGatewayPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a2ce8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2ce8-108">DESCRIPTION</span></span>
<span data-ttu-id="a2ce8-109">Restituisce gli oggetti del pool del gateway Edge in una posizione.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-109">Returns edge gateway pool objects at a location.</span></span>

## <span data-ttu-id="a2ce8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2ce8-110">EXAMPLES</span></span>

### <span data-ttu-id="a2ce8-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="a2ce8-111">EXAMPLE 1</span></span>
```
Get-AzsEdgeGatewayPool
```

<span data-ttu-id="a2ce8-112">Ottenere un elenco di tutti i pool di gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-112">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="a2ce8-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="a2ce8-113">EXAMPLE 2</span></span>
```
Get-AzsEdgeGatewayPool -Name "AzS-Gwy01"
```

<span data-ttu-id="a2ce8-114">Ottenere un pool di gateway Edge specifico.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-114">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="a2ce8-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2ce8-115">PARAMETERS</span></span>

### <span data-ttu-id="a2ce8-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a2ce8-116">-Name</span></span>
<span data-ttu-id="a2ce8-117">Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-117">Name of the edge gateway pool.</span></span>

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

### <span data-ttu-id="a2ce8-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a2ce8-118">-Location</span></span>
<span data-ttu-id="a2ce8-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-119">Location of the resource.</span></span>

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

### <span data-ttu-id="a2ce8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2ce8-120">-ResourceGroupName</span></span>
<span data-ttu-id="a2ce8-121">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a2ce8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2ce8-122">-ResourceId</span></span>
<span data-ttu-id="a2ce8-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-123">The resource id.</span></span>

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

### <span data-ttu-id="a2ce8-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="a2ce8-124">-Filter</span></span>
<span data-ttu-id="a2ce8-125">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="a2ce8-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="a2ce8-126">-Skip</span></span>
<span data-ttu-id="a2ce8-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a2ce8-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="a2ce8-128">-Top</span></span>
<span data-ttu-id="a2ce8-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a2ce8-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a2ce8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ce8-131">CommonParameters</span></span>
<span data-ttu-id="a2ce8-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2ce8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ce8-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2ce8-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ce8-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2ce8-134">INPUTS</span></span>

## <span data-ttu-id="a2ce8-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2ce8-135">OUTPUTS</span></span>

### <span data-ttu-id="a2ce8-136">Microsoft. AzureStack. Management. Fabric. admin. Models. EdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="a2ce8-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGatewayPool</span></span>

## <span data-ttu-id="a2ce8-137">Note</span><span class="sxs-lookup"><span data-stu-id="a2ce8-137">NOTES</span></span>

## <span data-ttu-id="a2ce8-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2ce8-138">RELATED LINKS</span></span>
