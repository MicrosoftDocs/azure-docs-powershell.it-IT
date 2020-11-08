---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d77229892da63973513dd8870a949ff296f5538
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030111"
---
# <span data-ttu-id="52d31-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="52d31-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="52d31-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52d31-102">SYNOPSIS</span></span>
<span data-ttu-id="52d31-103">Interrompere la modalità di manutenzione per un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="52d31-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="52d31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52d31-104">SYNTAX</span></span>

### <span data-ttu-id="52d31-105">Enable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="52d31-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52d31-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="52d31-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52d31-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52d31-107">DESCRIPTION</span></span>
<span data-ttu-id="52d31-108">Interrompere la modalità di manutenzione per un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="52d31-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="52d31-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52d31-109">EXAMPLES</span></span>

### <span data-ttu-id="52d31-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="52d31-110">EXAMPLE 1</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="52d31-111">Interrompere la modalità di manutenzione in un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="52d31-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="52d31-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52d31-112">PARAMETERS</span></span>

### <span data-ttu-id="52d31-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="52d31-113">-Name</span></span>
<span data-ttu-id="52d31-114">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="52d31-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d31-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="52d31-115">-Location</span></span>
<span data-ttu-id="52d31-116">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="52d31-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d31-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52d31-117">-ResourceGroupName</span></span>
<span data-ttu-id="52d31-118">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="52d31-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d31-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52d31-119">-ResourceId</span></span>
<span data-ttu-id="52d31-120">ID risorsa del nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="52d31-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="52d31-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52d31-121">-AsJob</span></span>
<span data-ttu-id="52d31-122">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="52d31-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="52d31-123">-Force</span><span class="sxs-lookup"><span data-stu-id="52d31-123">-Force</span></span>
<span data-ttu-id="52d31-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="52d31-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="52d31-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52d31-125">-WhatIf</span></span>
<span data-ttu-id="52d31-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52d31-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52d31-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52d31-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52d31-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="52d31-128">-Confirm</span></span>
<span data-ttu-id="52d31-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52d31-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52d31-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d31-130">CommonParameters</span></span>
<span data-ttu-id="52d31-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52d31-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d31-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52d31-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d31-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52d31-133">INPUTS</span></span>

## <span data-ttu-id="52d31-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52d31-134">OUTPUTS</span></span>

## <span data-ttu-id="52d31-135">Note</span><span class="sxs-lookup"><span data-stu-id="52d31-135">NOTES</span></span>

## <span data-ttu-id="52d31-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52d31-136">RELATED LINKS</span></span>
