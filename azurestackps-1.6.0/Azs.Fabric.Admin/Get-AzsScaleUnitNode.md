---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d5870624b6d39b3e821ed6a7fb76d87c8422ab2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685192"
---
# <span data-ttu-id="de55c-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="de55c-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="de55c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de55c-102">SYNOPSIS</span></span>
<span data-ttu-id="de55c-103">Restituisce un elenco di tutti i nodi di unità di scala in una posizione.</span><span class="sxs-lookup"><span data-stu-id="de55c-103">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="de55c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de55c-104">SYNTAX</span></span>

### <span data-ttu-id="de55c-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de55c-105">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="de55c-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="de55c-106">Get</span></span>
```
Get-AzsScaleUnitNode [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="de55c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="de55c-107">ResourceId</span></span>
```
Get-AzsScaleUnitNode -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="de55c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de55c-108">DESCRIPTION</span></span>
<span data-ttu-id="de55c-109">Restituisce un elenco di tutti i nodi di unità di scala in una posizione.</span><span class="sxs-lookup"><span data-stu-id="de55c-109">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="de55c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de55c-110">EXAMPLES</span></span>

### <span data-ttu-id="de55c-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="de55c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsScaleUnitNode
```

<span data-ttu-id="de55c-112">Ottenere tutti i nodi delle unità di scala in una posizione.</span><span class="sxs-lookup"><span data-stu-id="de55c-112">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="de55c-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="de55c-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsScaleUnitNode -Name "HC1n25r2231"
```

<span data-ttu-id="de55c-114">Ottenere un nodo specifico dell'unità di scala in una posizione assegnata un nome.</span><span class="sxs-lookup"><span data-stu-id="de55c-114">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="de55c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de55c-115">PARAMETERS</span></span>

### <span data-ttu-id="de55c-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="de55c-116">-Filter</span></span>
<span data-ttu-id="de55c-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="de55c-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="de55c-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="de55c-118">-Location</span></span>
<span data-ttu-id="de55c-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="de55c-119">Location of the resource.</span></span>

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

### <span data-ttu-id="de55c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="de55c-120">-Name</span></span>
<span data-ttu-id="de55c-121">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="de55c-121">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="de55c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de55c-122">-ResourceGroupName</span></span>
<span data-ttu-id="de55c-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="de55c-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="de55c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de55c-124">-ResourceId</span></span>
<span data-ttu-id="de55c-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="de55c-125">The resource id.</span></span>

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

### <span data-ttu-id="de55c-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="de55c-126">-Skip</span></span>
<span data-ttu-id="de55c-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="de55c-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="de55c-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="de55c-128">-Top</span></span>
<span data-ttu-id="de55c-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="de55c-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="de55c-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="de55c-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="de55c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de55c-131">CommonParameters</span></span>
<span data-ttu-id="de55c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de55c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de55c-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de55c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de55c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de55c-134">INPUTS</span></span>

## <span data-ttu-id="de55c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de55c-135">OUTPUTS</span></span>

### <span data-ttu-id="de55c-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="de55c-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnitNode</span></span>

## <span data-ttu-id="de55c-137">Note</span><span class="sxs-lookup"><span data-stu-id="de55c-137">NOTES</span></span>

## <span data-ttu-id="de55c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de55c-138">RELATED LINKS</span></span>

