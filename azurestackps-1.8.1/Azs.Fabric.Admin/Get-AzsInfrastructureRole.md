---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a20f0fbc5b059e878f0062569ffba2c16794204
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859674"
---
# <span data-ttu-id="0c9c9-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="0c9c9-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="0c9c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c9c9-102">SYNOPSIS</span></span>
<span data-ttu-id="0c9c9-103">Restituisce un elenco di tutti i ruoli dell'infrastruttura in una posizione.</span><span class="sxs-lookup"><span data-stu-id="0c9c9-103">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="0c9c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c9c9-104">SYNTAX</span></span>

### <span data-ttu-id="0c9c9-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c9c9-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0c9c9-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="0c9c9-106">Get</span></span>
```
Get-AzsInfrastructureRole [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c9c9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c9c9-107">ResourceId</span></span>
```
Get-AzsInfrastructureRole -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0c9c9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c9c9-108">DESCRIPTION</span></span>
<span data-ttu-id="0c9c9-109">Restituisce un elenco di tutti i ruoli dell'infrastruttura in una posizione.</span><span class="sxs-lookup"><span data-stu-id="0c9c9-109">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="0c9c9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c9c9-110">EXAMPLES</span></span>

### <span data-ttu-id="0c9c9-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="0c9c9-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRole
```

<span data-ttu-id="0c9c9-112">Ottenere un elenco di tutti i ruoli dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="0c9c9-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="0c9c9-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="0c9c9-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="0c9c9-114">Ottenere un ruolo di infrastruttura basato sul nome.</span><span class="sxs-lookup"><span data-stu-id="0c9c9-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="0c9c9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c9c9-115">PARAMETERS</span></span>

### <span data-ttu-id="0c9c9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c9c9-116">-Name</span></span>
<span data-ttu-id="0c9c9-117">Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="0c9c9-117">Infrastructure role name.</span></span>

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

### <span data-ttu-id="0c9c9-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0c9c9-118">-Location</span></span>
<span data-ttu-id="0c9c9-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0c9c9-119">Location of the resource.</span></span>

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

### <span data-ttu-id="0c9c9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c9c9-120">-ResourceGroupName</span></span>
<span data-ttu-id="0c9c9-121">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="0c9c9-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="0c9c9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c9c9-122">-ResourceId</span></span>
<span data-ttu-id="0c9c9-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="0c9c9-123">The resource id.</span></span>

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

### <span data-ttu-id="0c9c9-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="0c9c9-124">-Filter</span></span>
<span data-ttu-id="0c9c9-125">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="0c9c9-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="0c9c9-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="0c9c9-126">-Skip</span></span>
<span data-ttu-id="0c9c9-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="0c9c9-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="0c9c9-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="0c9c9-128">-Top</span></span>
<span data-ttu-id="0c9c9-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="0c9c9-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0c9c9-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="0c9c9-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="0c9c9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c9c9-131">CommonParameters</span></span>
<span data-ttu-id="0c9c9-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c9c9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c9c9-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c9c9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c9c9-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c9c9-134">INPUTS</span></span>

## <span data-ttu-id="0c9c9-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c9c9-135">OUTPUTS</span></span>

### <span data-ttu-id="0c9c9-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRole</span><span class="sxs-lookup"><span data-stu-id="0c9c9-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRole</span></span>

## <span data-ttu-id="0c9c9-137">Note</span><span class="sxs-lookup"><span data-stu-id="0c9c9-137">NOTES</span></span>

## <span data-ttu-id="0c9c9-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c9c9-138">RELATED LINKS</span></span>
