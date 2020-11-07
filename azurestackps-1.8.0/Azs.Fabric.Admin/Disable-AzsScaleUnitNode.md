---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c60245b9e6b8d44d8c465427c41c69e5cd442bb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859009"
---
# <span data-ttu-id="30348-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="30348-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="30348-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30348-102">SYNOPSIS</span></span>
<span data-ttu-id="30348-103">Avviare la modalità di manutenzione per un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="30348-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="30348-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30348-104">SYNTAX</span></span>

### <span data-ttu-id="30348-105">Disable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="30348-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30348-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="30348-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30348-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30348-107">DESCRIPTION</span></span>
<span data-ttu-id="30348-108">Avviare la modalità di manutenzione per un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="30348-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="30348-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30348-109">EXAMPLES</span></span>

### <span data-ttu-id="30348-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="30348-110">EXAMPLE 1</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="30348-111">Abilitare la modalità di manutenzione per un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="30348-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="30348-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30348-112">PARAMETERS</span></span>

### <span data-ttu-id="30348-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="30348-113">-Name</span></span>
<span data-ttu-id="30348-114">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="30348-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30348-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="30348-115">-Location</span></span>
<span data-ttu-id="30348-116">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="30348-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30348-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30348-117">-ResourceGroupName</span></span>
<span data-ttu-id="30348-118">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="30348-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30348-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30348-119">-ResourceId</span></span>
<span data-ttu-id="30348-120">ID risorsa del nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="30348-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="30348-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30348-121">-AsJob</span></span>
<span data-ttu-id="30348-122">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="30348-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="30348-123">-Force</span><span class="sxs-lookup"><span data-stu-id="30348-123">-Force</span></span>
<span data-ttu-id="30348-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="30348-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="30348-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30348-125">-WhatIf</span></span>
<span data-ttu-id="30348-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30348-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30348-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30348-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30348-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="30348-128">-Confirm</span></span>
<span data-ttu-id="30348-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30348-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30348-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30348-130">CommonParameters</span></span>
<span data-ttu-id="30348-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30348-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30348-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30348-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30348-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30348-133">INPUTS</span></span>

## <span data-ttu-id="30348-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30348-134">OUTPUTS</span></span>

## <span data-ttu-id="30348-135">Note</span><span class="sxs-lookup"><span data-stu-id="30348-135">NOTES</span></span>

## <span data-ttu-id="30348-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30348-136">RELATED LINKS</span></span>
