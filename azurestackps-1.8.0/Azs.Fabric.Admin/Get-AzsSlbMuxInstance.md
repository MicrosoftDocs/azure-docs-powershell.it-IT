---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821495581589eff356cd0d88fc98311b5f566d61
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93858937"
---
# <span data-ttu-id="9ab8a-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="9ab8a-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="9ab8a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9ab8a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab8a-103">Restituisce un elenco di tutte le istanze di bilanciamento del carico software in una posizione.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-103">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="9ab8a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ab8a-104">SYNTAX</span></span>

### <span data-ttu-id="9ab8a-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9ab8a-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9ab8a-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="9ab8a-106">Get</span></span>
```
Get-AzsSlbMuxInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="9ab8a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ab8a-107">ResourceId</span></span>
```
Get-AzsSlbMuxInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="9ab8a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ab8a-108">DESCRIPTION</span></span>
<span data-ttu-id="9ab8a-109">Restituisce un elenco di tutte le istanze di bilanciamento del carico software in una posizione.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-109">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="9ab8a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ab8a-110">EXAMPLES</span></span>

### <span data-ttu-id="9ab8a-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="9ab8a-111">EXAMPLE 1</span></span>
```
Get-AzsSlbMuxInstance
```

<span data-ttu-id="9ab8a-112">Ottenere tutte le istanze del multiplatore del bilanciamento del carico software in una posizione.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="9ab8a-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="9ab8a-113">EXAMPLE 2</span></span>
```
Get-AzsSlbMuxInstance -Name "AzS-SLB01"
```

<span data-ttu-id="9ab8a-114">Ottenere una specifica istanza del programma di bilanciamento del carico del software in una posizione assegnata un nome.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="9ab8a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ab8a-115">PARAMETERS</span></span>

### <span data-ttu-id="9ab8a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ab8a-116">-Name</span></span>
<span data-ttu-id="9ab8a-117">Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-117">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="9ab8a-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9ab8a-118">-Location</span></span>
<span data-ttu-id="9ab8a-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="9ab8a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ab8a-120">-ResourceGroupName</span></span>
<span data-ttu-id="9ab8a-121">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="9ab8a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ab8a-122">-ResourceId</span></span>
<span data-ttu-id="9ab8a-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-123">The resource id.</span></span>

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

### <span data-ttu-id="9ab8a-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="9ab8a-124">-Filter</span></span>
<span data-ttu-id="9ab8a-125">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="9ab8a-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="9ab8a-126">-Skip</span></span>
<span data-ttu-id="9ab8a-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9ab8a-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="9ab8a-128">-Top</span></span>
<span data-ttu-id="9ab8a-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9ab8a-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9ab8a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab8a-131">CommonParameters</span></span>
<span data-ttu-id="9ab8a-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab8a-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ab8a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab8a-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9ab8a-134">INPUTS</span></span>

## <span data-ttu-id="9ab8a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ab8a-135">OUTPUTS</span></span>

### <span data-ttu-id="9ab8a-136">Microsoft. AzureStack. Management. Fabric. admin. Models. SlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="9ab8a-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.SlbMuxInstance</span></span>

## <span data-ttu-id="9ab8a-137">Note</span><span class="sxs-lookup"><span data-stu-id="9ab8a-137">NOTES</span></span>

## <span data-ttu-id="9ab8a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ab8a-138">RELATED LINKS</span></span>
