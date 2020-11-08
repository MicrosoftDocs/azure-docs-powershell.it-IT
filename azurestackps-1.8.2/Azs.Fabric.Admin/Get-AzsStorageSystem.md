---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3760ecd9c0bc9fd62e49ee8163dfe24ae190985e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030226"
---
# <span data-ttu-id="79522-101">Get-AzsStorageSystem</span><span class="sxs-lookup"><span data-stu-id="79522-101">Get-AzsStorageSystem</span></span>

## <span data-ttu-id="79522-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79522-102">SYNOPSIS</span></span>
<span data-ttu-id="79522-103">Restituisce un elenco di tutti i sottosistemi di archiviazione per una posizione.</span><span class="sxs-lookup"><span data-stu-id="79522-103">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="79522-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79522-104">SYNTAX</span></span>

### <span data-ttu-id="79522-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="79522-105">List (Default)</span></span>
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="79522-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="79522-106">Get</span></span>
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="79522-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="79522-107">ResourceId</span></span>
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="79522-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79522-108">DESCRIPTION</span></span>
<span data-ttu-id="79522-109">Restituisce un elenco di tutti i sottosistemi di archiviazione per una posizione.</span><span class="sxs-lookup"><span data-stu-id="79522-109">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="79522-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79522-110">EXAMPLES</span></span>

### <span data-ttu-id="79522-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="79522-111">EXAMPLE 1</span></span>
```
Get-AzsStorageSystem
```

<span data-ttu-id="79522-112">Ottenere tutti i sottosistemi di archiviazione da una posizione.</span><span class="sxs-lookup"><span data-stu-id="79522-112">Get all storage subsystems from a location.</span></span>

### <span data-ttu-id="79522-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="79522-113">EXAMPLE 2</span></span>
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

<span data-ttu-id="79522-114">Ottenere un sottosistema di archiviazione assegnato un percorso e un nome.</span><span class="sxs-lookup"><span data-stu-id="79522-114">Get a storage subsystem given a location and name.</span></span>

## <span data-ttu-id="79522-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79522-115">PARAMETERS</span></span>

### <span data-ttu-id="79522-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="79522-116">-Name</span></span>
<span data-ttu-id="79522-117">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="79522-117">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="79522-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="79522-118">-Location</span></span>
<span data-ttu-id="79522-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="79522-119">Location of the resource.</span></span>

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

### <span data-ttu-id="79522-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79522-120">-ResourceGroupName</span></span>
<span data-ttu-id="79522-121">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="79522-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="79522-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79522-122">-ResourceId</span></span>
<span data-ttu-id="79522-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="79522-123">The resource id.</span></span>

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

### <span data-ttu-id="79522-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="79522-124">-Filter</span></span>
<span data-ttu-id="79522-125">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="79522-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="79522-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="79522-126">-Skip</span></span>
<span data-ttu-id="79522-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="79522-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="79522-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="79522-128">-Top</span></span>
<span data-ttu-id="79522-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="79522-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="79522-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="79522-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="79522-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79522-131">CommonParameters</span></span>
<span data-ttu-id="79522-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79522-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79522-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79522-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79522-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79522-134">INPUTS</span></span>

## <span data-ttu-id="79522-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79522-135">OUTPUTS</span></span>

### <span data-ttu-id="79522-136">Microsoft. AzureStack. Management. Fabric. admin. Models. StorageSystem</span><span class="sxs-lookup"><span data-stu-id="79522-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSystem</span></span>

## <span data-ttu-id="79522-137">Note</span><span class="sxs-lookup"><span data-stu-id="79522-137">NOTES</span></span>

## <span data-ttu-id="79522-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79522-138">RELATED LINKS</span></span>
