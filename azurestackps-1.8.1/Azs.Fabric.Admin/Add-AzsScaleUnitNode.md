---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ced1207f07360c0a18674d6f8ae4170be9b87beb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93860065"
---
# <span data-ttu-id="46768-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="46768-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="46768-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="46768-102">SYNOPSIS</span></span>
<span data-ttu-id="46768-103">Aggiungere una nuova unità di scala.</span><span class="sxs-lookup"><span data-stu-id="46768-103">Add a new scale unit.</span></span>

## <span data-ttu-id="46768-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46768-104">SYNTAX</span></span>

### <span data-ttu-id="46768-105">Scalabilità (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="46768-105">ScaleOut (Default)</span></span>
```
Add-AzsScaleUnitNode -Name <String> -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence]
 [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46768-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="46768-106">ResourceId</span></span>
```
Add-AzsScaleUnitNode -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence] -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46768-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46768-107">DESCRIPTION</span></span>
<span data-ttu-id="46768-108">Aggiungere una nuova unità di scala.</span><span class="sxs-lookup"><span data-stu-id="46768-108">Add a new scale unit.</span></span>

## <span data-ttu-id="46768-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46768-109">EXAMPLES</span></span>

### <span data-ttu-id="46768-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="46768-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -ScaleUnitName "Azs-ERC03" -NodeList $nodeList
```

<span data-ttu-id="46768-111">Aggiungere un nuovo nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="46768-111">Add a new scale unit node.</span></span>

## <span data-ttu-id="46768-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="46768-112">PARAMETERS</span></span>

### <span data-ttu-id="46768-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46768-113">-AsJob</span></span>
<span data-ttu-id="46768-114">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="46768-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="46768-115">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="46768-115">-AwaitStorageConvergence</span></span>
<span data-ttu-id="46768-116">Il contrassegno indica se l'operazione deve attendere lo spazio di archiviazione per confluire prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="46768-116">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="46768-117">-Force</span><span class="sxs-lookup"><span data-stu-id="46768-117">-Force</span></span>
<span data-ttu-id="46768-118">Non chiedere conferma</span><span class="sxs-lookup"><span data-stu-id="46768-118">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="46768-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="46768-119">-Location</span></span>
<span data-ttu-id="46768-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="46768-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46768-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="46768-121">-Name</span></span>
<span data-ttu-id="46768-122">{{Fill Name Description}}</span><span class="sxs-lookup"><span data-stu-id="46768-122">{{Fill Name Description}}</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46768-123">-NodeList</span><span class="sxs-lookup"><span data-stu-id="46768-123">-NodeList</span></span>
<span data-ttu-id="46768-124">Elenco di nodi nell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="46768-124">List of nodes in the scale unit.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46768-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46768-125">-ResourceGroupName</span></span>
<span data-ttu-id="46768-126">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="46768-126">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46768-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46768-127">-ResourceId</span></span>
<span data-ttu-id="46768-128">ID risorsa del nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="46768-128">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="46768-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="46768-129">-Confirm</span></span>
<span data-ttu-id="46768-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46768-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46768-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46768-131">-WhatIf</span></span>
<span data-ttu-id="46768-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46768-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46768-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46768-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46768-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46768-134">CommonParameters</span></span>
<span data-ttu-id="46768-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46768-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46768-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46768-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46768-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="46768-137">INPUTS</span></span>

## <span data-ttu-id="46768-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46768-138">OUTPUTS</span></span>

## <span data-ttu-id="46768-139">Note</span><span class="sxs-lookup"><span data-stu-id="46768-139">NOTES</span></span>

## <span data-ttu-id="46768-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46768-140">RELATED LINKS</span></span>

