---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25243539ef01a7476b6b0befb2d5cb29595001ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491194"
---
# <span data-ttu-id="c6c52-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="c6c52-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="c6c52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6c52-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c52-103">Restituisce un elenco di tutti i pool di archiviazione per una posizione.</span><span class="sxs-lookup"><span data-stu-id="c6c52-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="c6c52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6c52-104">SYNTAX</span></span>

### <span data-ttu-id="c6c52-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6c52-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c6c52-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="c6c52-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6c52-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6c52-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c6c52-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6c52-108">DESCRIPTION</span></span>
<span data-ttu-id="c6c52-109">Restituisce un elenco di tutti i pool di archiviazione per una posizione.</span><span class="sxs-lookup"><span data-stu-id="c6c52-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="c6c52-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6c52-110">EXAMPLES</span></span>

### <span data-ttu-id="c6c52-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c6c52-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStoragePool -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="c6c52-112">Ottenere tutti i pool di archiviazione in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="c6c52-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="c6c52-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c6c52-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStoragePool -StorageSubSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="c6c52-114">Ottenere un pool di archiviazione in una determinata posizione in base a un nome di pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c6c52-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="c6c52-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6c52-115">PARAMETERS</span></span>

### <span data-ttu-id="c6c52-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="c6c52-116">-Filter</span></span>
<span data-ttu-id="c6c52-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="c6c52-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="c6c52-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c6c52-118">-Location</span></span>
<span data-ttu-id="c6c52-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c6c52-119">Location of the resource.</span></span>

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

### <span data-ttu-id="c6c52-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6c52-120">-Name</span></span>
<span data-ttu-id="c6c52-121">Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c6c52-121">Storage pool name.</span></span>

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

### <span data-ttu-id="c6c52-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6c52-122">-ResourceGroupName</span></span>
<span data-ttu-id="c6c52-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="c6c52-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c6c52-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6c52-124">-ResourceId</span></span>
<span data-ttu-id="c6c52-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c6c52-125">The resource id.</span></span>

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

### <span data-ttu-id="c6c52-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="c6c52-126">-Skip</span></span>
<span data-ttu-id="c6c52-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="c6c52-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c6c52-128">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="c6c52-128">-StorageSystem</span></span>
<span data-ttu-id="c6c52-129">Sistema di archiviazione in cui si trova il pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c6c52-129">Storage system in which the storage pool is located.</span></span>

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

### <span data-ttu-id="c6c52-130">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="c6c52-130">-Top</span></span>
<span data-ttu-id="c6c52-131">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="c6c52-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c6c52-132">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="c6c52-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c6c52-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c52-133">CommonParameters</span></span>
<span data-ttu-id="c6c52-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6c52-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c52-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6c52-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c52-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6c52-136">INPUTS</span></span>

## <span data-ttu-id="c6c52-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6c52-137">OUTPUTS</span></span>

### <span data-ttu-id="c6c52-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="c6c52-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="c6c52-139">Note</span><span class="sxs-lookup"><span data-stu-id="c6c52-139">NOTES</span></span>

## <span data-ttu-id="c6c52-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6c52-140">RELATED LINKS</span></span>

