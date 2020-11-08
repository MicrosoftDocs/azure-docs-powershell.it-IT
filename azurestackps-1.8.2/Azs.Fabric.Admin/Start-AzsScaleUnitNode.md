---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030301"
---
# <span data-ttu-id="0d337-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="0d337-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="0d337-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d337-102">SYNOPSIS</span></span>
<span data-ttu-id="0d337-103">Accendere un nodo di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="0d337-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="0d337-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d337-104">SYNTAX</span></span>

### <span data-ttu-id="0d337-105">PowerOn (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0d337-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d337-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d337-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d337-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d337-107">DESCRIPTION</span></span>
<span data-ttu-id="0d337-108">Accendere un nodo di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="0d337-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="0d337-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d337-109">EXAMPLES</span></span>

### <span data-ttu-id="0d337-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="0d337-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="0d337-111">ProvisioningState: riuscito</span><span class="sxs-lookup"><span data-stu-id="0d337-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="0d337-112">Accendere un nodo di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="0d337-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="0d337-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d337-113">PARAMETERS</span></span>

### <span data-ttu-id="0d337-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d337-114">-Name</span></span>
<span data-ttu-id="0d337-115">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="0d337-115">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="0d337-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0d337-116">-Location</span></span>
<span data-ttu-id="0d337-117">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0d337-117">Location of the resource.</span></span>

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

### <span data-ttu-id="0d337-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d337-118">-ResourceGroupName</span></span>
<span data-ttu-id="0d337-119">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="0d337-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="0d337-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d337-120">-ResourceId</span></span>
<span data-ttu-id="0d337-121">ID risorsa del nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="0d337-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="0d337-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d337-122">-AsJob</span></span>
<span data-ttu-id="0d337-123">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="0d337-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="0d337-124">-Force</span><span class="sxs-lookup"><span data-stu-id="0d337-124">-Force</span></span>
<span data-ttu-id="0d337-125">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="0d337-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0d337-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d337-126">-WhatIf</span></span>
<span data-ttu-id="0d337-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d337-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d337-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d337-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d337-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0d337-129">-Confirm</span></span>
<span data-ttu-id="0d337-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d337-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d337-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d337-131">CommonParameters</span></span>
<span data-ttu-id="0d337-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d337-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d337-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d337-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d337-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d337-134">INPUTS</span></span>

## <span data-ttu-id="0d337-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d337-135">OUTPUTS</span></span>

## <span data-ttu-id="0d337-136">Note</span><span class="sxs-lookup"><span data-stu-id="0d337-136">NOTES</span></span>

## <span data-ttu-id="0d337-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d337-137">RELATED LINKS</span></span>
