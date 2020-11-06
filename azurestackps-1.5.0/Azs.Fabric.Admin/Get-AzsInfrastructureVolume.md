---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdb6542f9e7bfd594130374d5d72fed8b26596e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491470"
---
# <span data-ttu-id="1366a-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="1366a-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="1366a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1366a-102">SYNOPSIS</span></span>
<span data-ttu-id="1366a-103">Restituisce un elenco di tutti i volumi di archiviazione in una posizione.</span><span class="sxs-lookup"><span data-stu-id="1366a-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="1366a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1366a-104">SYNTAX</span></span>

### <span data-ttu-id="1366a-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1366a-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1366a-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="1366a-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1366a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1366a-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1366a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1366a-108">DESCRIPTION</span></span>
<span data-ttu-id="1366a-109">Restituisce un elenco di tutti i volumi di archiviazione in una posizione.</span><span class="sxs-lookup"><span data-stu-id="1366a-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="1366a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1366a-110">EXAMPLES</span></span>

### <span data-ttu-id="1366a-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1366a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="1366a-112">Ottenere un elenco di tutti i volumi di archiviazione in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="1366a-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="1366a-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1366a-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="1366a-114">Ottenere un volume di archiviazione per nome in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="1366a-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="1366a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1366a-115">PARAMETERS</span></span>

### <span data-ttu-id="1366a-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="1366a-116">-Filter</span></span>
<span data-ttu-id="1366a-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="1366a-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="1366a-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1366a-118">-Location</span></span>
<span data-ttu-id="1366a-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1366a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="1366a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1366a-120">-Name</span></span>
<span data-ttu-id="1366a-121">Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1366a-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="1366a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1366a-122">-ResourceGroupName</span></span>
<span data-ttu-id="1366a-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="1366a-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1366a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1366a-124">-ResourceId</span></span>
<span data-ttu-id="1366a-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="1366a-125">The resource id.</span></span>

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

### <span data-ttu-id="1366a-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="1366a-126">-Skip</span></span>
<span data-ttu-id="1366a-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="1366a-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1366a-128">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="1366a-128">-StoragePool</span></span>
<span data-ttu-id="1366a-129">Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1366a-129">Storage pool name.</span></span>

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

### <span data-ttu-id="1366a-130">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="1366a-130">-StorageSystem</span></span>
<span data-ttu-id="1366a-131">Sistema di archiviazione in cui si trova il volume dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="1366a-131">Storage system in which the infrastructure volume is located.</span></span>

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

### <span data-ttu-id="1366a-132">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="1366a-132">-Top</span></span>
<span data-ttu-id="1366a-133">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="1366a-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1366a-134">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="1366a-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1366a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1366a-135">CommonParameters</span></span>
<span data-ttu-id="1366a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1366a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1366a-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1366a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1366a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1366a-138">INPUTS</span></span>

## <span data-ttu-id="1366a-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1366a-139">OUTPUTS</span></span>

### <span data-ttu-id="1366a-140">Microsoft. AzureStack. Management. Fabric. admin. Models. volume</span><span class="sxs-lookup"><span data-stu-id="1366a-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="1366a-141">Note</span><span class="sxs-lookup"><span data-stu-id="1366a-141">NOTES</span></span>

## <span data-ttu-id="1366a-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1366a-142">RELATED LINKS</span></span>

