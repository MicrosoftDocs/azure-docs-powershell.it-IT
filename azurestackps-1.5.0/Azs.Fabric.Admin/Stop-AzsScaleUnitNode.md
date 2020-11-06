---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6de990526330cdd192cd99707aacc1e06ad49c5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507140"
---
# <span data-ttu-id="3052d-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="3052d-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="3052d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3052d-102">SYNOPSIS</span></span>
<span data-ttu-id="3052d-103">Spegnere un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="3052d-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="3052d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3052d-104">SYNTAX</span></span>

### <span data-ttu-id="3052d-105">Interrompi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3052d-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3052d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3052d-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3052d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3052d-107">DESCRIPTION</span></span>
<span data-ttu-id="3052d-108">Spegnere un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="3052d-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="3052d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3052d-109">EXAMPLES</span></span>

### <span data-ttu-id="3052d-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3052d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="3052d-111">Arrestare un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="3052d-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="3052d-112">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3052d-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="3052d-113">Spegnere un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="3052d-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="3052d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3052d-114">PARAMETERS</span></span>

### <span data-ttu-id="3052d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3052d-115">-AsJob</span></span>
<span data-ttu-id="3052d-116">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="3052d-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="3052d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3052d-117">-Force</span></span>
<span data-ttu-id="3052d-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="3052d-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3052d-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3052d-119">-Location</span></span>
<span data-ttu-id="3052d-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3052d-120">Location of the resource.</span></span>

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

### <span data-ttu-id="3052d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3052d-121">-Name</span></span>
<span data-ttu-id="3052d-122">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="3052d-122">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="3052d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3052d-123">-ResourceGroupName</span></span>
<span data-ttu-id="3052d-124">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="3052d-124">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="3052d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3052d-125">-ResourceId</span></span>
<span data-ttu-id="3052d-126">ID risorsa del nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="3052d-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="3052d-127">-Arresto</span><span class="sxs-lookup"><span data-stu-id="3052d-127">-Shutdown</span></span>
<span data-ttu-id="3052d-128">Se impostato con garbo, arrestare il nodo dell'unità di scala; in caso contrario, è difficile spegnere il nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="3052d-128">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="3052d-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3052d-129">-Confirm</span></span>
<span data-ttu-id="3052d-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3052d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3052d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3052d-131">-WhatIf</span></span>
<span data-ttu-id="3052d-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3052d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3052d-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3052d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3052d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3052d-134">CommonParameters</span></span>
<span data-ttu-id="3052d-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3052d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3052d-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3052d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3052d-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3052d-137">INPUTS</span></span>

## <span data-ttu-id="3052d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3052d-138">OUTPUTS</span></span>

## <span data-ttu-id="3052d-139">Note</span><span class="sxs-lookup"><span data-stu-id="3052d-139">NOTES</span></span>

## <span data-ttu-id="3052d-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3052d-140">RELATED LINKS</span></span>

