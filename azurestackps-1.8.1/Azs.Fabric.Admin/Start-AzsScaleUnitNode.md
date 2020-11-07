---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93860058"
---
# <span data-ttu-id="dee4e-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="dee4e-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="dee4e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dee4e-102">SYNOPSIS</span></span>
<span data-ttu-id="dee4e-103">Accendere un nodo di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="dee4e-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="dee4e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dee4e-104">SYNTAX</span></span>

### <span data-ttu-id="dee4e-105">PowerOn (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dee4e-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dee4e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dee4e-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dee4e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dee4e-107">DESCRIPTION</span></span>
<span data-ttu-id="dee4e-108">Accendere un nodo di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="dee4e-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="dee4e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dee4e-109">EXAMPLES</span></span>

### <span data-ttu-id="dee4e-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="dee4e-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="dee4e-111">ProvisioningState: riuscito</span><span class="sxs-lookup"><span data-stu-id="dee4e-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="dee4e-112">Accendere un nodo di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="dee4e-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="dee4e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dee4e-113">PARAMETERS</span></span>

### <span data-ttu-id="dee4e-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="dee4e-114">-Name</span></span>
<span data-ttu-id="dee4e-115">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="dee4e-115">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="dee4e-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="dee4e-116">-Location</span></span>
<span data-ttu-id="dee4e-117">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="dee4e-117">Location of the resource.</span></span>

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

### <span data-ttu-id="dee4e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dee4e-118">-ResourceGroupName</span></span>
<span data-ttu-id="dee4e-119">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="dee4e-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="dee4e-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dee4e-120">-ResourceId</span></span>
<span data-ttu-id="dee4e-121">ID risorsa del nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="dee4e-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="dee4e-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dee4e-122">-AsJob</span></span>
<span data-ttu-id="dee4e-123">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="dee4e-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="dee4e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="dee4e-124">-Force</span></span>
<span data-ttu-id="dee4e-125">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="dee4e-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="dee4e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dee4e-126">-WhatIf</span></span>
<span data-ttu-id="dee4e-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dee4e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dee4e-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dee4e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dee4e-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dee4e-129">-Confirm</span></span>
<span data-ttu-id="dee4e-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dee4e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dee4e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee4e-131">CommonParameters</span></span>
<span data-ttu-id="dee4e-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dee4e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee4e-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dee4e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee4e-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dee4e-134">INPUTS</span></span>

## <span data-ttu-id="dee4e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dee4e-135">OUTPUTS</span></span>

## <span data-ttu-id="dee4e-136">Note</span><span class="sxs-lookup"><span data-stu-id="dee4e-136">NOTES</span></span>

## <span data-ttu-id="dee4e-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dee4e-137">RELATED LINKS</span></span>
