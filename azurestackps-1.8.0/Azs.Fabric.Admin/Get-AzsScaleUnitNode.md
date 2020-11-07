---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07cb5e675003eccc9fad54e723e80a0ddb73ff9a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93858949"
---
# <span data-ttu-id="9586a-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="9586a-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="9586a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9586a-102">SYNOPSIS</span></span>
<span data-ttu-id="9586a-103">Restituisce un elenco di tutti i nodi di unità di scala in una posizione.</span><span class="sxs-lookup"><span data-stu-id="9586a-103">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="9586a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9586a-104">SYNTAX</span></span>

### <span data-ttu-id="9586a-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9586a-105">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9586a-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="9586a-106">Get</span></span>
```
Get-AzsScaleUnitNode [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="9586a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9586a-107">ResourceId</span></span>
```
Get-AzsScaleUnitNode -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="9586a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9586a-108">DESCRIPTION</span></span>
<span data-ttu-id="9586a-109">Restituisce un elenco di tutti i nodi di unità di scala in una posizione.</span><span class="sxs-lookup"><span data-stu-id="9586a-109">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="9586a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9586a-110">EXAMPLES</span></span>

### <span data-ttu-id="9586a-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="9586a-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnitNode
```

<span data-ttu-id="9586a-112">Ottenere tutti i nodi delle unità di scala in una posizione.</span><span class="sxs-lookup"><span data-stu-id="9586a-112">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="9586a-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="9586a-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnitNode -Name "HC1n25r2231"
```

<span data-ttu-id="9586a-114">Ottenere un nodo specifico dell'unità di scala in una posizione assegnata un nome.</span><span class="sxs-lookup"><span data-stu-id="9586a-114">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="9586a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9586a-115">PARAMETERS</span></span>

### <span data-ttu-id="9586a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9586a-116">-Name</span></span>
<span data-ttu-id="9586a-117">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="9586a-117">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="9586a-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9586a-118">-Location</span></span>
<span data-ttu-id="9586a-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9586a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="9586a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9586a-120">-ResourceGroupName</span></span>
<span data-ttu-id="9586a-121">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="9586a-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="9586a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9586a-122">-ResourceId</span></span>
<span data-ttu-id="9586a-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9586a-123">The resource id.</span></span>

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

### <span data-ttu-id="9586a-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="9586a-124">-Filter</span></span>
<span data-ttu-id="9586a-125">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="9586a-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="9586a-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="9586a-126">-Skip</span></span>
<span data-ttu-id="9586a-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="9586a-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9586a-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="9586a-128">-Top</span></span>
<span data-ttu-id="9586a-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="9586a-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9586a-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="9586a-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9586a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9586a-131">CommonParameters</span></span>
<span data-ttu-id="9586a-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9586a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9586a-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9586a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9586a-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9586a-134">INPUTS</span></span>

## <span data-ttu-id="9586a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9586a-135">OUTPUTS</span></span>

### <span data-ttu-id="9586a-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="9586a-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnitNode</span></span>

## <span data-ttu-id="9586a-137">Note</span><span class="sxs-lookup"><span data-stu-id="9586a-137">NOTES</span></span>

## <span data-ttu-id="9586a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9586a-138">RELATED LINKS</span></span>
