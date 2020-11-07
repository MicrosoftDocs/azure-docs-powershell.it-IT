---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 869cd48507ba9384026f8e58b9cd7853179b844f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858262"
---
# <span data-ttu-id="de9bd-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="de9bd-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="de9bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de9bd-102">SYNOPSIS</span></span>
<span data-ttu-id="de9bd-103">Restituisce un elenco di tutte le unità di misura in una posizione.</span><span class="sxs-lookup"><span data-stu-id="de9bd-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="de9bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de9bd-104">SYNTAX</span></span>

### <span data-ttu-id="de9bd-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de9bd-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="de9bd-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="de9bd-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="de9bd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="de9bd-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="de9bd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de9bd-108">DESCRIPTION</span></span>
<span data-ttu-id="de9bd-109">Restituisce un elenco di tutte le unità di misura in una posizione.</span><span class="sxs-lookup"><span data-stu-id="de9bd-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="de9bd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de9bd-110">EXAMPLES</span></span>

### <span data-ttu-id="de9bd-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="de9bd-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="de9bd-112">Restituisce un elenco di informazioni sulle unità di misura.</span><span class="sxs-lookup"><span data-stu-id="de9bd-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="de9bd-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="de9bd-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="de9bd-114">Restituire informazioni su un'unità di misura specifica.</span><span class="sxs-lookup"><span data-stu-id="de9bd-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="de9bd-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de9bd-115">PARAMETERS</span></span>

### <span data-ttu-id="de9bd-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="de9bd-116">-Filter</span></span>
<span data-ttu-id="de9bd-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="de9bd-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="de9bd-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="de9bd-118">-Location</span></span>
<span data-ttu-id="de9bd-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="de9bd-119">Location of the resource.</span></span>

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

### <span data-ttu-id="de9bd-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="de9bd-120">-Name</span></span>
<span data-ttu-id="de9bd-121">Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="de9bd-121">Name of the scale units.</span></span>

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

### <span data-ttu-id="de9bd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de9bd-122">-ResourceGroupName</span></span>
<span data-ttu-id="de9bd-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="de9bd-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="de9bd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de9bd-124">-ResourceId</span></span>
<span data-ttu-id="de9bd-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="de9bd-125">The resource id.</span></span>

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

### <span data-ttu-id="de9bd-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="de9bd-126">-Skip</span></span>
<span data-ttu-id="de9bd-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="de9bd-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="de9bd-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="de9bd-128">-Top</span></span>
<span data-ttu-id="de9bd-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="de9bd-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="de9bd-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="de9bd-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="de9bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de9bd-131">CommonParameters</span></span>
<span data-ttu-id="de9bd-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de9bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de9bd-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de9bd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de9bd-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de9bd-134">INPUTS</span></span>

## <span data-ttu-id="de9bd-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de9bd-135">OUTPUTS</span></span>

### <span data-ttu-id="de9bd-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="de9bd-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="de9bd-137">Note</span><span class="sxs-lookup"><span data-stu-id="de9bd-137">NOTES</span></span>

## <span data-ttu-id="de9bd-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de9bd-138">RELATED LINKS</span></span>

