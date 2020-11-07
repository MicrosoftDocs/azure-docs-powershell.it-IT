---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c5de84b66283d683d121c99c0cf2e0ea27a4a66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858633"
---
# <span data-ttu-id="f4289-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="f4289-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="f4289-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4289-102">SYNOPSIS</span></span>
<span data-ttu-id="f4289-103">Accendere un nodo di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="f4289-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="f4289-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4289-104">SYNTAX</span></span>

### <span data-ttu-id="f4289-105">PowerOn (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4289-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4289-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4289-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4289-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4289-107">DESCRIPTION</span></span>
<span data-ttu-id="f4289-108">Accendere un nodo di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="f4289-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="f4289-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4289-109">EXAMPLES</span></span>

### <span data-ttu-id="f4289-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f4289-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="f4289-111">ProvisioningState: riuscito</span><span class="sxs-lookup"><span data-stu-id="f4289-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="f4289-112">Accendere un nodo di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="f4289-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="f4289-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4289-113">PARAMETERS</span></span>

### <span data-ttu-id="f4289-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4289-114">-AsJob</span></span>
<span data-ttu-id="f4289-115">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="f4289-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f4289-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f4289-116">-Force</span></span>
<span data-ttu-id="f4289-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="f4289-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f4289-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f4289-118">-Location</span></span>
<span data-ttu-id="f4289-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f4289-119">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4289-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4289-120">-Name</span></span>
<span data-ttu-id="f4289-121">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="f4289-121">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4289-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4289-122">-ResourceGroupName</span></span>
<span data-ttu-id="f4289-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="f4289-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4289-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4289-124">-ResourceId</span></span>
<span data-ttu-id="f4289-125">ID risorsa del nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="f4289-125">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="f4289-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f4289-126">-Confirm</span></span>
<span data-ttu-id="f4289-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4289-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4289-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4289-128">-WhatIf</span></span>
<span data-ttu-id="f4289-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4289-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4289-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4289-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4289-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4289-131">CommonParameters</span></span>
<span data-ttu-id="f4289-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4289-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4289-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4289-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4289-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4289-134">INPUTS</span></span>

## <span data-ttu-id="f4289-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4289-135">OUTPUTS</span></span>

## <span data-ttu-id="f4289-136">Note</span><span class="sxs-lookup"><span data-stu-id="f4289-136">NOTES</span></span>

## <span data-ttu-id="f4289-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4289-137">RELATED LINKS</span></span>

