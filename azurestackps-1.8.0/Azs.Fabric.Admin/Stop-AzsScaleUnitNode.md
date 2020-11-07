---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1a26c22b5714fc7db448935b31b0af685301217
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859138"
---
# <span data-ttu-id="840b7-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="840b7-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="840b7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="840b7-102">SYNOPSIS</span></span>
<span data-ttu-id="840b7-103">Spegnere un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="840b7-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="840b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="840b7-104">SYNTAX</span></span>

### <span data-ttu-id="840b7-105">Interrompi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="840b7-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="840b7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="840b7-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="840b7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="840b7-107">DESCRIPTION</span></span>
<span data-ttu-id="840b7-108">Spegnere un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="840b7-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="840b7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="840b7-109">EXAMPLES</span></span>

### <span data-ttu-id="840b7-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="840b7-110">EXAMPLE 1</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="840b7-111">Arrestare un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="840b7-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="840b7-112">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="840b7-112">EXAMPLE 2</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="840b7-113">Spegnere un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="840b7-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="840b7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="840b7-114">PARAMETERS</span></span>

### <span data-ttu-id="840b7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="840b7-115">-Name</span></span>
<span data-ttu-id="840b7-116">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="840b7-116">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="840b7-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="840b7-117">-Location</span></span>
<span data-ttu-id="840b7-118">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="840b7-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="840b7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="840b7-119">-ResourceGroupName</span></span>
<span data-ttu-id="840b7-120">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="840b7-120">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="840b7-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="840b7-121">-ResourceId</span></span>
<span data-ttu-id="840b7-122">ID risorsa del nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="840b7-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="840b7-123">-Arresto</span><span class="sxs-lookup"><span data-stu-id="840b7-123">-Shutdown</span></span>
<span data-ttu-id="840b7-124">Se impostato con garbo, arrestare il nodo dell'unità di scala; in caso contrario, è difficile spegnere il nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="840b7-124">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="840b7-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="840b7-125">-AsJob</span></span>
<span data-ttu-id="840b7-126">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="840b7-126">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="840b7-127">-Force</span><span class="sxs-lookup"><span data-stu-id="840b7-127">-Force</span></span>
<span data-ttu-id="840b7-128">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="840b7-128">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="840b7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="840b7-129">-WhatIf</span></span>
<span data-ttu-id="840b7-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="840b7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="840b7-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="840b7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="840b7-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="840b7-132">-Confirm</span></span>
<span data-ttu-id="840b7-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="840b7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="840b7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="840b7-134">CommonParameters</span></span>
<span data-ttu-id="840b7-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="840b7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="840b7-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="840b7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="840b7-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="840b7-137">INPUTS</span></span>

## <span data-ttu-id="840b7-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="840b7-138">OUTPUTS</span></span>

## <span data-ttu-id="840b7-139">Note</span><span class="sxs-lookup"><span data-stu-id="840b7-139">NOTES</span></span>

## <span data-ttu-id="840b7-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="840b7-140">RELATED LINKS</span></span>
