---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 498374f19f83befc5697395eb58bb191555b10ca
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030225"
---
# <span data-ttu-id="11969-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="11969-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="11969-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11969-102">SYNOPSIS</span></span>
<span data-ttu-id="11969-103">Ripristina un nodo del cluster.</span><span class="sxs-lookup"><span data-stu-id="11969-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="11969-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11969-104">SYNTAX</span></span>

### <span data-ttu-id="11969-105">Ripristino (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="11969-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11969-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="11969-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11969-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11969-107">DESCRIPTION</span></span>
<span data-ttu-id="11969-108">Ripristina un nodo del cluster.</span><span class="sxs-lookup"><span data-stu-id="11969-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="11969-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11969-109">EXAMPLES</span></span>

### <span data-ttu-id="11969-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="11969-110">EXAMPLE 1</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="11969-111">Ripristinare un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="11969-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="11969-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11969-112">PARAMETERS</span></span>

### <span data-ttu-id="11969-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="11969-113">-Name</span></span>
<span data-ttu-id="11969-114">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="11969-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="11969-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="11969-115">-BMCIPv4Address</span></span>
<span data-ttu-id="11969-116">Indirizzo BMC del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="11969-116">BMC address of the physical machine.</span></span>

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

### <span data-ttu-id="11969-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="11969-117">-Location</span></span>
<span data-ttu-id="11969-118">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="11969-118">Location of the resource.</span></span>

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

### <span data-ttu-id="11969-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11969-119">-ResourceGroupName</span></span>
<span data-ttu-id="11969-120">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="11969-120">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="11969-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11969-121">-ResourceId</span></span>
<span data-ttu-id="11969-122">ID risorsa del nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="11969-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="11969-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11969-123">-AsJob</span></span>
<span data-ttu-id="11969-124">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="11969-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="11969-125">-Force</span><span class="sxs-lookup"><span data-stu-id="11969-125">-Force</span></span>
<span data-ttu-id="11969-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="11969-126">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="11969-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11969-127">-WhatIf</span></span>
<span data-ttu-id="11969-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11969-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11969-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11969-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11969-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="11969-130">-Confirm</span></span>
<span data-ttu-id="11969-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11969-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11969-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11969-132">CommonParameters</span></span>
<span data-ttu-id="11969-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11969-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11969-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11969-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11969-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11969-135">INPUTS</span></span>

## <span data-ttu-id="11969-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11969-136">OUTPUTS</span></span>

## <span data-ttu-id="11969-137">Note</span><span class="sxs-lookup"><span data-stu-id="11969-137">NOTES</span></span>

## <span data-ttu-id="11969-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11969-138">RELATED LINKS</span></span>
