---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 70ee408b65839e46e408256780a6d705c9881bde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507107"
---
# <span data-ttu-id="47da8-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="47da8-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="47da8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47da8-102">SYNOPSIS</span></span>
<span data-ttu-id="47da8-103">Avviare la modalità di manutenzione per un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="47da8-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="47da8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47da8-104">SYNTAX</span></span>

### <span data-ttu-id="47da8-105">Disable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="47da8-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47da8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="47da8-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47da8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47da8-107">DESCRIPTION</span></span>
<span data-ttu-id="47da8-108">Avviare la modalità di manutenzione per un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="47da8-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="47da8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47da8-109">EXAMPLES</span></span>

### <span data-ttu-id="47da8-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="47da8-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="47da8-111">Abilitare la modalità di manutenzione per un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="47da8-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="47da8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47da8-112">PARAMETERS</span></span>

### <span data-ttu-id="47da8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47da8-113">-AsJob</span></span>
<span data-ttu-id="47da8-114">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="47da8-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="47da8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="47da8-115">-Force</span></span>
<span data-ttu-id="47da8-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="47da8-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="47da8-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="47da8-117">-Location</span></span>
<span data-ttu-id="47da8-118">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="47da8-118">Location of the resource.</span></span>

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

### <span data-ttu-id="47da8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="47da8-119">-Name</span></span>
<span data-ttu-id="47da8-120">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="47da8-120">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="47da8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47da8-121">-ResourceGroupName</span></span>
<span data-ttu-id="47da8-122">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="47da8-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="47da8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47da8-123">-ResourceId</span></span>
<span data-ttu-id="47da8-124">ID risorsa del nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="47da8-124">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="47da8-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="47da8-125">-Confirm</span></span>
<span data-ttu-id="47da8-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47da8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47da8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47da8-127">-WhatIf</span></span>
<span data-ttu-id="47da8-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47da8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47da8-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47da8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47da8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47da8-130">CommonParameters</span></span>
<span data-ttu-id="47da8-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47da8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47da8-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47da8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47da8-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47da8-133">INPUTS</span></span>

## <span data-ttu-id="47da8-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47da8-134">OUTPUTS</span></span>

## <span data-ttu-id="47da8-135">Note</span><span class="sxs-lookup"><span data-stu-id="47da8-135">NOTES</span></span>

## <span data-ttu-id="47da8-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47da8-136">RELATED LINKS</span></span>

