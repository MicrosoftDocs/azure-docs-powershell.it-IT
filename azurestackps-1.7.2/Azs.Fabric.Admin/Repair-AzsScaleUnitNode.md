---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ad784757210273cd2e456069c8d3a759e973a0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857914"
---
# <span data-ttu-id="e85a6-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="e85a6-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="e85a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e85a6-102">SYNOPSIS</span></span>
<span data-ttu-id="e85a6-103">Ripristina un nodo del cluster.</span><span class="sxs-lookup"><span data-stu-id="e85a6-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="e85a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e85a6-104">SYNTAX</span></span>

### <span data-ttu-id="e85a6-105">Ripristino (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e85a6-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e85a6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e85a6-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e85a6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e85a6-107">DESCRIPTION</span></span>
<span data-ttu-id="e85a6-108">Ripristina un nodo del cluster.</span><span class="sxs-lookup"><span data-stu-id="e85a6-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="e85a6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e85a6-109">EXAMPLES</span></span>

### <span data-ttu-id="e85a6-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e85a6-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="e85a6-111">Ripristinare un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="e85a6-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="e85a6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e85a6-112">PARAMETERS</span></span>

### <span data-ttu-id="e85a6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e85a6-113">-AsJob</span></span>
<span data-ttu-id="e85a6-114">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="e85a6-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="e85a6-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="e85a6-115">-BMCIPv4Address</span></span>
<span data-ttu-id="e85a6-116">Indirizzo BMC del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="e85a6-116">BMC address of the physical machine.</span></span>

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

### <span data-ttu-id="e85a6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e85a6-117">-Force</span></span>
<span data-ttu-id="e85a6-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="e85a6-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e85a6-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e85a6-119">-Location</span></span>
<span data-ttu-id="e85a6-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e85a6-120">Location of the resource.</span></span>

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

### <span data-ttu-id="e85a6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e85a6-121">-Name</span></span>
<span data-ttu-id="e85a6-122">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="e85a6-122">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="e85a6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e85a6-123">-ResourceGroupName</span></span>
<span data-ttu-id="e85a6-124">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="e85a6-124">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e85a6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e85a6-125">-ResourceId</span></span>
<span data-ttu-id="e85a6-126">ID risorsa del nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="e85a6-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="e85a6-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e85a6-127">-Confirm</span></span>
<span data-ttu-id="e85a6-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e85a6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e85a6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e85a6-129">-WhatIf</span></span>
<span data-ttu-id="e85a6-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e85a6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e85a6-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e85a6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e85a6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e85a6-132">CommonParameters</span></span>
<span data-ttu-id="e85a6-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e85a6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e85a6-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e85a6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e85a6-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e85a6-135">INPUTS</span></span>

## <span data-ttu-id="e85a6-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e85a6-136">OUTPUTS</span></span>

## <span data-ttu-id="e85a6-137">Note</span><span class="sxs-lookup"><span data-stu-id="e85a6-137">NOTES</span></span>

## <span data-ttu-id="e85a6-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e85a6-138">RELATED LINKS</span></span>

