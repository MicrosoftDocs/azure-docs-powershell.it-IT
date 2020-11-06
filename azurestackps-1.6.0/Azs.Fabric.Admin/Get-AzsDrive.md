---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cab0b994648a414aa164b746a02e3fe1fb848e9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490721"
---
# <span data-ttu-id="c4e02-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="c4e02-101">Get-AzsDrive</span></span>

## <span data-ttu-id="c4e02-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4e02-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e02-103">Restituisce un elenco di tutte le unità di archiviazione per un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="c4e02-103">Returns a list of all storage drives for a given cluster.</span></span>

## <span data-ttu-id="c4e02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4e02-104">SYNTAX</span></span>

### <span data-ttu-id="c4e02-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4e02-105">List (Default)</span></span>
```
Get-AzsDrive -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c4e02-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="c4e02-106">Get</span></span>
```
Get-AzsDrive -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c4e02-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4e02-107">ResourceId</span></span>
```
Get-AzsDrive -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c4e02-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4e02-108">DESCRIPTION</span></span>
<span data-ttu-id="c4e02-109">Restituisce un elenco di tutte le unità di archiviazione per un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="c4e02-109">Returns a list of all storage drives for a given cluster.</span></span>

## <span data-ttu-id="c4e02-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4e02-110">EXAMPLES</span></span>

### <span data-ttu-id="c4e02-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c4e02-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="c4e02-112">Ottenere un elenco di tutte le unità di archiviazione per un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="c4e02-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="c4e02-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c4e02-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a654528c-60bb-18e1-457c-51b7cdb7e14a
```

<span data-ttu-id="c4e02-114">Ottenere un'unità di archiviazione per nome per un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="c4e02-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="c4e02-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4e02-115">PARAMETERS</span></span>

### <span data-ttu-id="c4e02-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="c4e02-116">-Filter</span></span>
<span data-ttu-id="c4e02-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="c4e02-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="c4e02-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c4e02-118">-Location</span></span>
<span data-ttu-id="c4e02-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c4e02-119">Location of the resource.</span></span>

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

### <span data-ttu-id="c4e02-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4e02-120">-Name</span></span>
<span data-ttu-id="c4e02-121">Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c4e02-121">Name of the storage drive.</span></span>

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

### <span data-ttu-id="c4e02-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4e02-122">-ResourceGroupName</span></span>
<span data-ttu-id="c4e02-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="c4e02-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c4e02-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4e02-124">-ResourceId</span></span>
<span data-ttu-id="c4e02-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c4e02-125">The resource id.</span></span>

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

### <span data-ttu-id="c4e02-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c4e02-126">-ScaleUnit</span></span>
<span data-ttu-id="c4e02-127">Nome dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="c4e02-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="c4e02-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="c4e02-128">-StorageSubSystem</span></span>
<span data-ttu-id="c4e02-129">Sottosistema di archiviazione in cui si trova l'unità.</span><span class="sxs-lookup"><span data-stu-id="c4e02-129">Storage subsystem in which the drive is located.</span></span>

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

### <span data-ttu-id="c4e02-130">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="c4e02-130">-Top</span></span>
<span data-ttu-id="c4e02-131">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="c4e02-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c4e02-132">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="c4e02-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c4e02-133">-Skip</span><span class="sxs-lookup"><span data-stu-id="c4e02-133">-Skip</span></span>
<span data-ttu-id="c4e02-134">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="c4e02-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c4e02-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e02-135">CommonParameters</span></span>
<span data-ttu-id="c4e02-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4e02-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e02-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4e02-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e02-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4e02-138">INPUTS</span></span>

## <span data-ttu-id="c4e02-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4e02-139">OUTPUTS</span></span>

### <span data-ttu-id="c4e02-140">Microsoft. AzureStack. Management. Fabric. admin. Models. Drive</span><span class="sxs-lookup"><span data-stu-id="c4e02-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Drive</span></span>
## <span data-ttu-id="c4e02-141">Note</span><span class="sxs-lookup"><span data-stu-id="c4e02-141">NOTES</span></span>

## <span data-ttu-id="c4e02-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4e02-142">RELATED LINKS</span></span>
