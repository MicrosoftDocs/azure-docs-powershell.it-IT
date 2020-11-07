---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3760ecd9c0bc9fd62e49ee8163dfe24ae190985e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93858933"
---
# <span data-ttu-id="3f203-101">Get-AzsStorageSystem</span><span class="sxs-lookup"><span data-stu-id="3f203-101">Get-AzsStorageSystem</span></span>

## <span data-ttu-id="3f203-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f203-102">SYNOPSIS</span></span>
<span data-ttu-id="3f203-103">Restituisce un elenco di tutti i sottosistemi di archiviazione per una posizione.</span><span class="sxs-lookup"><span data-stu-id="3f203-103">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="3f203-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f203-104">SYNTAX</span></span>

### <span data-ttu-id="3f203-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3f203-105">List (Default)</span></span>
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3f203-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="3f203-106">Get</span></span>
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3f203-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f203-107">ResourceId</span></span>
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3f203-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f203-108">DESCRIPTION</span></span>
<span data-ttu-id="3f203-109">Restituisce un elenco di tutti i sottosistemi di archiviazione per una posizione.</span><span class="sxs-lookup"><span data-stu-id="3f203-109">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="3f203-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f203-110">EXAMPLES</span></span>

### <span data-ttu-id="3f203-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="3f203-111">EXAMPLE 1</span></span>
```
Get-AzsStorageSystem
```

<span data-ttu-id="3f203-112">Ottenere tutti i sottosistemi di archiviazione da una posizione.</span><span class="sxs-lookup"><span data-stu-id="3f203-112">Get all storage subsystems from a location.</span></span>

### <span data-ttu-id="3f203-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="3f203-113">EXAMPLE 2</span></span>
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

<span data-ttu-id="3f203-114">Ottenere un sottosistema di archiviazione assegnato un percorso e un nome.</span><span class="sxs-lookup"><span data-stu-id="3f203-114">Get a storage subsystem given a location and name.</span></span>

## <span data-ttu-id="3f203-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f203-115">PARAMETERS</span></span>

### <span data-ttu-id="3f203-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f203-116">-Name</span></span>
<span data-ttu-id="3f203-117">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="3f203-117">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="3f203-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3f203-118">-Location</span></span>
<span data-ttu-id="3f203-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3f203-119">Location of the resource.</span></span>

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

### <span data-ttu-id="3f203-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f203-120">-ResourceGroupName</span></span>
<span data-ttu-id="3f203-121">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="3f203-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="3f203-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f203-122">-ResourceId</span></span>
<span data-ttu-id="3f203-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="3f203-123">The resource id.</span></span>

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

### <span data-ttu-id="3f203-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="3f203-124">-Filter</span></span>
<span data-ttu-id="3f203-125">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="3f203-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="3f203-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="3f203-126">-Skip</span></span>
<span data-ttu-id="3f203-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="3f203-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3f203-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="3f203-128">-Top</span></span>
<span data-ttu-id="3f203-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="3f203-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3f203-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="3f203-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3f203-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f203-131">CommonParameters</span></span>
<span data-ttu-id="3f203-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f203-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f203-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f203-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f203-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f203-134">INPUTS</span></span>

## <span data-ttu-id="3f203-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f203-135">OUTPUTS</span></span>

### <span data-ttu-id="3f203-136">Microsoft. AzureStack. Management. Fabric. admin. Models. StorageSystem</span><span class="sxs-lookup"><span data-stu-id="3f203-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSystem</span></span>

## <span data-ttu-id="3f203-137">Note</span><span class="sxs-lookup"><span data-stu-id="3f203-137">NOTES</span></span>

## <span data-ttu-id="3f203-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f203-138">RELATED LINKS</span></span>
