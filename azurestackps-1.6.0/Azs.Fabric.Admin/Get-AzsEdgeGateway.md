---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a81fcf688e1c269aabd64250e9b0694730edc8f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490717"
---
# <span data-ttu-id="ad2d2-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="ad2d2-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="ad2d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad2d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2d2-103">Restituisce l'elenco di tutti i gateway di Edge in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="ad2d2-103">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="ad2d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad2d2-104">SYNTAX</span></span>

### <span data-ttu-id="ad2d2-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad2d2-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ad2d2-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="ad2d2-106">Get</span></span>
```
Get-AzsEdgeGateway [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ad2d2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad2d2-107">ResourceId</span></span>
```
Get-AzsEdgeGateway -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ad2d2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad2d2-108">DESCRIPTION</span></span>
<span data-ttu-id="ad2d2-109">Restituisce l'elenco di tutti i gateway di Edge in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="ad2d2-109">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="ad2d2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad2d2-110">EXAMPLES</span></span>

### <span data-ttu-id="ad2d2-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ad2d2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsEdgeGateway
```

<span data-ttu-id="ad2d2-112">Ottenere un elenco di tutti i gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="ad2d2-112">Get a list of all edge gateways.</span></span>

### <span data-ttu-id="ad2d2-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ad2d2-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsEdgeGateway -Name "AzS-Gwy01"
```

<span data-ttu-id="ad2d2-114">Ottenere un gateway Edge specifico.</span><span class="sxs-lookup"><span data-stu-id="ad2d2-114">Get a specific edge gateway.</span></span>

## <span data-ttu-id="ad2d2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad2d2-115">PARAMETERS</span></span>

### <span data-ttu-id="ad2d2-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="ad2d2-116">-Filter</span></span>
<span data-ttu-id="ad2d2-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="ad2d2-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="ad2d2-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ad2d2-118">-Location</span></span>
<span data-ttu-id="ad2d2-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ad2d2-119">Location of the resource.</span></span>

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

### <span data-ttu-id="ad2d2-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad2d2-120">-Name</span></span>
<span data-ttu-id="ad2d2-121">Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="ad2d2-121">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="ad2d2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad2d2-122">-ResourceGroupName</span></span>
<span data-ttu-id="ad2d2-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad2d2-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ad2d2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad2d2-124">-ResourceId</span></span>
<span data-ttu-id="ad2d2-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="ad2d2-125">The resource id.</span></span>

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

### <span data-ttu-id="ad2d2-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="ad2d2-126">-Skip</span></span>
<span data-ttu-id="ad2d2-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="ad2d2-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ad2d2-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="ad2d2-128">-Top</span></span>
<span data-ttu-id="ad2d2-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="ad2d2-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ad2d2-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="ad2d2-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ad2d2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2d2-131">CommonParameters</span></span>
<span data-ttu-id="ad2d2-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad2d2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad2d2-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad2d2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2d2-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad2d2-134">INPUTS</span></span>

## <span data-ttu-id="ad2d2-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad2d2-135">OUTPUTS</span></span>

### <span data-ttu-id="ad2d2-136">Microsoft. AzureStack. Management. Fabric. admin. Models. EdgeGateway</span><span class="sxs-lookup"><span data-stu-id="ad2d2-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGateway</span></span>

## <span data-ttu-id="ad2d2-137">Note</span><span class="sxs-lookup"><span data-stu-id="ad2d2-137">NOTES</span></span>

## <span data-ttu-id="ad2d2-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad2d2-138">RELATED LINKS</span></span>

