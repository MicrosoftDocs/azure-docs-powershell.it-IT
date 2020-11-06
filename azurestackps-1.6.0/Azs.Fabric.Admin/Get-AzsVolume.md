---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67835cc0ae5191f50aefb79f76148752c68508bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491586"
---
# <span data-ttu-id="e39b0-101">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="e39b0-101">Get-AzsVolume</span></span>

## <span data-ttu-id="e39b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e39b0-102">SYNOPSIS</span></span>
<span data-ttu-id="e39b0-103">Restituisce un elenco di tutti i volumi di archiviazione in una posizione.</span><span class="sxs-lookup"><span data-stu-id="e39b0-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="e39b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e39b0-104">SYNTAX</span></span>

### <span data-ttu-id="e39b0-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e39b0-105">List (Default)</span></span>
```
Get-AzsVolume -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e39b0-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="e39b0-106">Get</span></span>
```
Get-AzsVolume -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e39b0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e39b0-107">ResourceId</span></span>
```
Get-AzsVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e39b0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e39b0-108">DESCRIPTION</span></span>
<span data-ttu-id="e39b0-109">Restituisce un elenco di tutti i volumi di archiviazione in una posizione.</span><span class="sxs-lookup"><span data-stu-id="e39b0-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="e39b0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e39b0-110">EXAMPLES</span></span>

### <span data-ttu-id="e39b0-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e39b0-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="e39b0-112">Ottenere un elenco di tutti i volumi di archiviazione in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="e39b0-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="e39b0-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e39b0-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="e39b0-114">Ottenere un volume di archiviazione per nome in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="e39b0-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="e39b0-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e39b0-115">PARAMETERS</span></span>

### <span data-ttu-id="e39b0-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="e39b0-116">-Filter</span></span>
<span data-ttu-id="e39b0-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="e39b0-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="e39b0-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e39b0-118">-Location</span></span>
<span data-ttu-id="e39b0-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e39b0-119">Location of the resource.</span></span>

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

### <span data-ttu-id="e39b0-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e39b0-120">-Name</span></span>
<span data-ttu-id="e39b0-121">Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e39b0-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="e39b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e39b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="e39b0-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="e39b0-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e39b0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e39b0-124">-ResourceId</span></span>
<span data-ttu-id="e39b0-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e39b0-125">The resource id.</span></span>

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

### <span data-ttu-id="e39b0-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="e39b0-126">-ScaleUnit</span></span>
<span data-ttu-id="e39b0-127">Nome dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="e39b0-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="e39b0-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="e39b0-128">-StorageSubSystem</span></span>
<span data-ttu-id="e39b0-129">Sottosistema di archiviazione in cui si trova il volume.</span><span class="sxs-lookup"><span data-stu-id="e39b0-129">Storage subsystem in which the volume is located.</span></span>

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

### <span data-ttu-id="e39b0-130">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="e39b0-130">-Top</span></span>
<span data-ttu-id="e39b0-131">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="e39b0-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e39b0-132">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="e39b0-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e39b0-133">-Skip</span><span class="sxs-lookup"><span data-stu-id="e39b0-133">-Skip</span></span>
<span data-ttu-id="e39b0-134">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="e39b0-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e39b0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e39b0-135">CommonParameters</span></span>
<span data-ttu-id="e39b0-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e39b0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e39b0-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e39b0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e39b0-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e39b0-138">INPUTS</span></span>

## <span data-ttu-id="e39b0-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e39b0-139">OUTPUTS</span></span>

### <span data-ttu-id="e39b0-140">Microsoft. AzureStack. Management. Fabric. admin. Models. volume</span><span class="sxs-lookup"><span data-stu-id="e39b0-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>
## <span data-ttu-id="e39b0-141">Note</span><span class="sxs-lookup"><span data-stu-id="e39b0-141">NOTES</span></span>

## <span data-ttu-id="e39b0-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e39b0-142">RELATED LINKS</span></span>
