---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2abc9073b9e7bcbcd4644150ada4c19cd351f660
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490982"
---
# <span data-ttu-id="4dd82-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="4dd82-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="4dd82-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4dd82-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd82-103">Restituisce un elenco di tutti i sottosistemi di archiviazione per un'unità di misura.</span><span class="sxs-lookup"><span data-stu-id="4dd82-103">Returns a list of all storage subsystems for a scale unit.</span></span>

## <span data-ttu-id="4dd82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4dd82-104">SYNTAX</span></span>

### <span data-ttu-id="4dd82-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4dd82-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4dd82-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="4dd82-106">Get</span></span>
```
Get-AzsStorageSubSystem [-Name] <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dd82-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dd82-107">ResourceId</span></span>
```
Get-AzsStorageSubSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="4dd82-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4dd82-108">DESCRIPTION</span></span>
<span data-ttu-id="4dd82-109">Restituisce un elenco di tutti i sottosistemi di archiviazione per un'unità di misura.</span><span class="sxs-lookup"><span data-stu-id="4dd82-109">Returns a list of all storage subsystems for a scale unit.</span></span>

## <span data-ttu-id="4dd82-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4dd82-110">EXAMPLES</span></span>

### <span data-ttu-id="4dd82-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4dd82-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit S-Cluster
```

<span data-ttu-id="4dd82-112">Ottenere tutti i sottosistemi di archiviazione da un'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="4dd82-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="4dd82-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="4dd82-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit S-Cluster -Name S-Cluster.azurestack.local
```

<span data-ttu-id="4dd82-114">Ottenere un sottosistema di archiviazione assegnato un nome e un'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="4dd82-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="4dd82-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4dd82-115">PARAMETERS</span></span>

### <span data-ttu-id="4dd82-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="4dd82-116">-Filter</span></span>
<span data-ttu-id="4dd82-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="4dd82-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="4dd82-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4dd82-118">-Location</span></span>
<span data-ttu-id="4dd82-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4dd82-119">Location of the resource.</span></span>

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

### <span data-ttu-id="4dd82-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4dd82-120">-Name</span></span>
<span data-ttu-id="4dd82-121">Nome del sottosistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4dd82-121">Name of the storage subsystem.</span></span>

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

### <span data-ttu-id="4dd82-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dd82-122">-ResourceGroupName</span></span>
<span data-ttu-id="4dd82-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="4dd82-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="4dd82-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dd82-124">-ResourceId</span></span>
<span data-ttu-id="4dd82-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="4dd82-125">The resource id.</span></span>

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

### <span data-ttu-id="4dd82-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="4dd82-126">-ScaleUnit</span></span>
<span data-ttu-id="4dd82-127">Nome dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="4dd82-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="4dd82-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="4dd82-128">-Top</span></span>
<span data-ttu-id="4dd82-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="4dd82-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="4dd82-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="4dd82-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="4dd82-131">-Skip</span><span class="sxs-lookup"><span data-stu-id="4dd82-131">-Skip</span></span>
<span data-ttu-id="4dd82-132">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="4dd82-132">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="4dd82-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd82-133">CommonParameters</span></span>
<span data-ttu-id="4dd82-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dd82-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd82-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dd82-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd82-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4dd82-136">INPUTS</span></span>

## <span data-ttu-id="4dd82-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4dd82-137">OUTPUTS</span></span>

### <span data-ttu-id="4dd82-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="4dd82-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSubSystem</span></span>
## <span data-ttu-id="4dd82-139">Note</span><span class="sxs-lookup"><span data-stu-id="4dd82-139">NOTES</span></span>

## <span data-ttu-id="4dd82-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4dd82-140">RELATED LINKS</span></span>
