---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 498374f19f83befc5697395eb58bb191555b10ca
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859490"
---
# <span data-ttu-id="d0183-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="d0183-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="d0183-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0183-102">SYNOPSIS</span></span>
<span data-ttu-id="d0183-103">Ripristina un nodo del cluster.</span><span class="sxs-lookup"><span data-stu-id="d0183-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="d0183-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0183-104">SYNTAX</span></span>

### <span data-ttu-id="d0183-105">Ripristino (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0183-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0183-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0183-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0183-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0183-107">DESCRIPTION</span></span>
<span data-ttu-id="d0183-108">Ripristina un nodo del cluster.</span><span class="sxs-lookup"><span data-stu-id="d0183-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="d0183-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0183-109">EXAMPLES</span></span>

### <span data-ttu-id="d0183-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="d0183-110">EXAMPLE 1</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="d0183-111">Ripristinare un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="d0183-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="d0183-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0183-112">PARAMETERS</span></span>

### <span data-ttu-id="d0183-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0183-113">-Name</span></span>
<span data-ttu-id="d0183-114">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="d0183-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0183-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="d0183-115">-BMCIPv4Address</span></span>
<span data-ttu-id="d0183-116">Indirizzo BMC del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="d0183-116">BMC address of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0183-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d0183-117">-Location</span></span>
<span data-ttu-id="d0183-118">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d0183-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0183-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0183-119">-ResourceGroupName</span></span>
<span data-ttu-id="d0183-120">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="d0183-120">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0183-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0183-121">-ResourceId</span></span>
<span data-ttu-id="d0183-122">ID risorsa del nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="d0183-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="d0183-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0183-123">-AsJob</span></span>
<span data-ttu-id="d0183-124">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="d0183-124">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0183-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d0183-125">-Force</span></span>
<span data-ttu-id="d0183-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d0183-126">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0183-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0183-127">-WhatIf</span></span>
<span data-ttu-id="d0183-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0183-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0183-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0183-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0183-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d0183-130">-Confirm</span></span>
<span data-ttu-id="d0183-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0183-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0183-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0183-132">CommonParameters</span></span>
<span data-ttu-id="d0183-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0183-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0183-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0183-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0183-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0183-135">INPUTS</span></span>

## <span data-ttu-id="d0183-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0183-136">OUTPUTS</span></span>

## <span data-ttu-id="d0183-137">Note</span><span class="sxs-lookup"><span data-stu-id="d0183-137">NOTES</span></span>

## <span data-ttu-id="d0183-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0183-138">RELATED LINKS</span></span>
