---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88d9fc8456c86f0806313bb0234e145b7f4d727a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93858965"
---
# <span data-ttu-id="f3ef8-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="f3ef8-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="f3ef8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3ef8-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ef8-103">Restituisce un elenco di tutte le reti logiche in una posizione.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-103">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="f3ef8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3ef8-104">SYNTAX</span></span>

### <span data-ttu-id="f3ef8-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f3ef8-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f3ef8-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="f3ef8-106">Get</span></span>
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="f3ef8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3ef8-107">ResourceId</span></span>
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f3ef8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3ef8-108">DESCRIPTION</span></span>
<span data-ttu-id="f3ef8-109">Restituisce un elenco di tutte le reti logiche in una posizione.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-109">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="f3ef8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3ef8-110">EXAMPLES</span></span>

### <span data-ttu-id="f3ef8-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="f3ef8-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalNetwork
```

<span data-ttu-id="f3ef8-112">Ottenere tutte le reti logiche in una posizione.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="f3ef8-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="f3ef8-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

<span data-ttu-id="f3ef8-114">Ottenere una rete logica specifica in una posizione basata su un nome.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="f3ef8-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3ef8-115">PARAMETERS</span></span>

### <span data-ttu-id="f3ef8-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3ef8-116">-Name</span></span>
<span data-ttu-id="f3ef8-117">Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-117">Name of the logical network.</span></span>

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

### <span data-ttu-id="f3ef8-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f3ef8-118">-Location</span></span>
<span data-ttu-id="f3ef8-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-119">Location of the resource.</span></span>

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

### <span data-ttu-id="f3ef8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3ef8-120">-ResourceGroupName</span></span>
<span data-ttu-id="f3ef8-121">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="f3ef8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3ef8-122">-ResourceId</span></span>
<span data-ttu-id="f3ef8-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-123">The resource id.</span></span>

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

### <span data-ttu-id="f3ef8-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="f3ef8-124">-Filter</span></span>
<span data-ttu-id="f3ef8-125">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="f3ef8-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="f3ef8-126">-Skip</span></span>
<span data-ttu-id="f3ef8-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f3ef8-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="f3ef8-128">-Top</span></span>
<span data-ttu-id="f3ef8-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f3ef8-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f3ef8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ef8-131">CommonParameters</span></span>
<span data-ttu-id="f3ef8-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ef8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ef8-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3ef8-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ef8-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3ef8-134">INPUTS</span></span>

## <span data-ttu-id="f3ef8-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3ef8-135">OUTPUTS</span></span>

### <span data-ttu-id="f3ef8-136">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="f3ef8-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalNetwork</span></span>

## <span data-ttu-id="f3ef8-137">Note</span><span class="sxs-lookup"><span data-stu-id="f3ef8-137">NOTES</span></span>

## <span data-ttu-id="f3ef8-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3ef8-138">RELATED LINKS</span></span>
