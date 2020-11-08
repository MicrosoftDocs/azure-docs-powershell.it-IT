---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07cb5e675003eccc9fad54e723e80a0ddb73ff9a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030635"
---
# <span data-ttu-id="07f76-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="07f76-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="07f76-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07f76-102">SYNOPSIS</span></span>
<span data-ttu-id="07f76-103">Restituisce un elenco di tutti i nodi di unità di scala in una posizione.</span><span class="sxs-lookup"><span data-stu-id="07f76-103">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="07f76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07f76-104">SYNTAX</span></span>

### <span data-ttu-id="07f76-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="07f76-105">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="07f76-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="07f76-106">Get</span></span>
```
Get-AzsScaleUnitNode [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="07f76-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="07f76-107">ResourceId</span></span>
```
Get-AzsScaleUnitNode -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="07f76-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07f76-108">DESCRIPTION</span></span>
<span data-ttu-id="07f76-109">Restituisce un elenco di tutti i nodi di unità di scala in una posizione.</span><span class="sxs-lookup"><span data-stu-id="07f76-109">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="07f76-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07f76-110">EXAMPLES</span></span>

### <span data-ttu-id="07f76-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="07f76-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnitNode
```

<span data-ttu-id="07f76-112">Ottenere tutti i nodi delle unità di scala in una posizione.</span><span class="sxs-lookup"><span data-stu-id="07f76-112">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="07f76-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="07f76-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnitNode -Name "HC1n25r2231"
```

<span data-ttu-id="07f76-114">Ottenere un nodo specifico dell'unità di scala in una posizione assegnata un nome.</span><span class="sxs-lookup"><span data-stu-id="07f76-114">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="07f76-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07f76-115">PARAMETERS</span></span>

### <span data-ttu-id="07f76-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="07f76-116">-Name</span></span>
<span data-ttu-id="07f76-117">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="07f76-117">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="07f76-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="07f76-118">-Location</span></span>
<span data-ttu-id="07f76-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="07f76-119">Location of the resource.</span></span>

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

### <span data-ttu-id="07f76-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f76-120">-ResourceGroupName</span></span>
<span data-ttu-id="07f76-121">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="07f76-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="07f76-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07f76-122">-ResourceId</span></span>
<span data-ttu-id="07f76-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="07f76-123">The resource id.</span></span>

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

### <span data-ttu-id="07f76-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="07f76-124">-Filter</span></span>
<span data-ttu-id="07f76-125">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="07f76-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="07f76-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="07f76-126">-Skip</span></span>
<span data-ttu-id="07f76-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="07f76-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="07f76-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="07f76-128">-Top</span></span>
<span data-ttu-id="07f76-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="07f76-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="07f76-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="07f76-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="07f76-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f76-131">CommonParameters</span></span>
<span data-ttu-id="07f76-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f76-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f76-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07f76-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f76-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07f76-134">INPUTS</span></span>

## <span data-ttu-id="07f76-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07f76-135">OUTPUTS</span></span>

### <span data-ttu-id="07f76-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="07f76-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnitNode</span></span>

## <span data-ttu-id="07f76-137">Note</span><span class="sxs-lookup"><span data-stu-id="07f76-137">NOTES</span></span>

## <span data-ttu-id="07f76-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07f76-138">RELATED LINKS</span></span>
