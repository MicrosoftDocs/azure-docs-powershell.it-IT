---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c60245b9e6b8d44d8c465427c41c69e5cd442bb0
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030112"
---
# <span data-ttu-id="4e9c2-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="4e9c2-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="4e9c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e9c2-102">SYNOPSIS</span></span>
<span data-ttu-id="4e9c2-103">Avviare la modalità di manutenzione per un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="4e9c2-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="4e9c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e9c2-104">SYNTAX</span></span>

### <span data-ttu-id="4e9c2-105">Disable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4e9c2-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e9c2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e9c2-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e9c2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e9c2-107">DESCRIPTION</span></span>
<span data-ttu-id="4e9c2-108">Avviare la modalità di manutenzione per un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="4e9c2-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="4e9c2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e9c2-109">EXAMPLES</span></span>

### <span data-ttu-id="4e9c2-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="4e9c2-110">EXAMPLE 1</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="4e9c2-111">Abilitare la modalità di manutenzione per un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="4e9c2-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="4e9c2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e9c2-112">PARAMETERS</span></span>

### <span data-ttu-id="4e9c2-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e9c2-113">-Name</span></span>
<span data-ttu-id="4e9c2-114">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="4e9c2-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="4e9c2-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4e9c2-115">-Location</span></span>
<span data-ttu-id="4e9c2-116">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4e9c2-116">Location of the resource.</span></span>

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

### <span data-ttu-id="4e9c2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e9c2-117">-ResourceGroupName</span></span>
<span data-ttu-id="4e9c2-118">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="4e9c2-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="4e9c2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e9c2-119">-ResourceId</span></span>
<span data-ttu-id="4e9c2-120">ID risorsa del nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="4e9c2-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="4e9c2-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e9c2-121">-AsJob</span></span>
<span data-ttu-id="4e9c2-122">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="4e9c2-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="4e9c2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4e9c2-123">-Force</span></span>
<span data-ttu-id="4e9c2-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="4e9c2-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4e9c2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e9c2-125">-WhatIf</span></span>
<span data-ttu-id="4e9c2-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e9c2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e9c2-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e9c2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e9c2-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4e9c2-128">-Confirm</span></span>
<span data-ttu-id="4e9c2-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e9c2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e9c2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e9c2-130">CommonParameters</span></span>
<span data-ttu-id="4e9c2-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e9c2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e9c2-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e9c2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e9c2-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e9c2-133">INPUTS</span></span>

## <span data-ttu-id="4e9c2-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e9c2-134">OUTPUTS</span></span>

## <span data-ttu-id="4e9c2-135">Note</span><span class="sxs-lookup"><span data-stu-id="4e9c2-135">NOTES</span></span>

## <span data-ttu-id="4e9c2-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e9c2-136">RELATED LINKS</span></span>
