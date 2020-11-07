---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcc4dbfdd4634c53835c588947a77c4c2e773af4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93858938"
---
# <span data-ttu-id="256f2-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="256f2-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="256f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="256f2-102">SYNOPSIS</span></span>
<span data-ttu-id="256f2-103">Restituisce un elenco di tutti i pool di archiviazione per una posizione.</span><span class="sxs-lookup"><span data-stu-id="256f2-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="256f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="256f2-104">SYNTAX</span></span>

### <span data-ttu-id="256f2-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="256f2-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="256f2-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="256f2-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="256f2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="256f2-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="256f2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="256f2-108">DESCRIPTION</span></span>
<span data-ttu-id="256f2-109">Restituisce un elenco di tutti i pool di archiviazione per una posizione.</span><span class="sxs-lookup"><span data-stu-id="256f2-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="256f2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="256f2-110">EXAMPLES</span></span>

### <span data-ttu-id="256f2-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="256f2-111">EXAMPLE 1</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="256f2-112">Ottenere tutti i pool di archiviazione in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="256f2-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="256f2-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="256f2-113">EXAMPLE 2</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="256f2-114">Ottenere un pool di archiviazione in una determinata posizione in base a un nome di pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="256f2-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="256f2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="256f2-115">PARAMETERS</span></span>

### <span data-ttu-id="256f2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="256f2-116">-Name</span></span>
<span data-ttu-id="256f2-117">Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="256f2-117">Storage pool name.</span></span>

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

### <span data-ttu-id="256f2-118">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="256f2-118">-StorageSystem</span></span>
<span data-ttu-id="256f2-119">Nome del sistema secondario di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="256f2-119">Name of the Storage Sub System.</span></span>

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

### <span data-ttu-id="256f2-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="256f2-120">-Location</span></span>
<span data-ttu-id="256f2-121">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="256f2-121">Location of the resource.</span></span>

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

### <span data-ttu-id="256f2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="256f2-122">-ResourceGroupName</span></span>
<span data-ttu-id="256f2-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="256f2-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="256f2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="256f2-124">-ResourceId</span></span>
<span data-ttu-id="256f2-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="256f2-125">The resource id.</span></span>

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

### <span data-ttu-id="256f2-126">-Filtro</span><span class="sxs-lookup"><span data-stu-id="256f2-126">-Filter</span></span>
<span data-ttu-id="256f2-127">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="256f2-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="256f2-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="256f2-128">-Skip</span></span>
<span data-ttu-id="256f2-129">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="256f2-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="256f2-130">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="256f2-130">-Top</span></span>
<span data-ttu-id="256f2-131">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="256f2-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="256f2-132">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="256f2-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="256f2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="256f2-133">CommonParameters</span></span>
<span data-ttu-id="256f2-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="256f2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="256f2-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="256f2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="256f2-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="256f2-136">INPUTS</span></span>

## <span data-ttu-id="256f2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="256f2-137">OUTPUTS</span></span>

### <span data-ttu-id="256f2-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="256f2-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="256f2-139">Note</span><span class="sxs-lookup"><span data-stu-id="256f2-139">NOTES</span></span>

## <span data-ttu-id="256f2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="256f2-140">RELATED LINKS</span></span>
