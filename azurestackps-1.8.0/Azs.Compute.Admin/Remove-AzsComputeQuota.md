---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ebc1ebae40d6d1726ee6c23def6f82ff1efc8517
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859037"
---
# <span data-ttu-id="ae3d9-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="ae3d9-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="ae3d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae3d9-102">SYNOPSIS</span></span>
<span data-ttu-id="ae3d9-103">Elimina la quota di calcolo specificata.</span><span class="sxs-lookup"><span data-stu-id="ae3d9-103">Deletes specified compute quota.</span></span>

## <span data-ttu-id="ae3d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae3d9-104">SYNTAX</span></span>

### <span data-ttu-id="ae3d9-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ae3d9-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae3d9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae3d9-106">ResourceId</span></span>
```
Remove-AzsComputeQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae3d9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae3d9-107">DESCRIPTION</span></span>
<span data-ttu-id="ae3d9-108">Eliminare una quota esistente.</span><span class="sxs-lookup"><span data-stu-id="ae3d9-108">Delete an existing quota.</span></span>

## <span data-ttu-id="ae3d9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae3d9-109">EXAMPLES</span></span>

### <span data-ttu-id="ae3d9-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ae3d9-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsComputeQuota -Name ComputeQuota
```

<span data-ttu-id="ae3d9-111">Rimuovere una quota di calcolo in base a tutti i parametri.</span><span class="sxs-lookup"><span data-stu-id="ae3d9-111">Remove a compute quota given all the parameters.</span></span>

## <span data-ttu-id="ae3d9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae3d9-112">PARAMETERS</span></span>

### <span data-ttu-id="ae3d9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ae3d9-113">-Force</span></span>
<span data-ttu-id="ae3d9-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ae3d9-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ae3d9-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ae3d9-115">-Location</span></span>
<span data-ttu-id="ae3d9-116">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ae3d9-116">Location of the resource.</span></span> <span data-ttu-id="ae3d9-117">Se non viene assegnato l'impostazione predefinita è la posizione associata all'abbonamento di tenat.</span><span class="sxs-lookup"><span data-stu-id="ae3d9-117">If not given we default to the location bound to the tenat's subscription.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3d9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae3d9-118">-Name</span></span>
<span data-ttu-id="ae3d9-119">Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="ae3d9-119">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3d9-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae3d9-120">-ResourceId</span></span>
<span data-ttu-id="ae3d9-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="ae3d9-121">The resource id.</span></span>

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

### <span data-ttu-id="ae3d9-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae3d9-122">-Confirm</span></span>
<span data-ttu-id="ae3d9-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae3d9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae3d9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae3d9-124">-WhatIf</span></span>
<span data-ttu-id="ae3d9-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae3d9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae3d9-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae3d9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae3d9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae3d9-127">CommonParameters</span></span>
<span data-ttu-id="ae3d9-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae3d9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae3d9-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae3d9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae3d9-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae3d9-130">INPUTS</span></span>

## <span data-ttu-id="ae3d9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae3d9-131">OUTPUTS</span></span>

## <span data-ttu-id="ae3d9-132">Note</span><span class="sxs-lookup"><span data-stu-id="ae3d9-132">NOTES</span></span>

## <span data-ttu-id="ae3d9-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae3d9-133">RELATED LINKS</span></span>

