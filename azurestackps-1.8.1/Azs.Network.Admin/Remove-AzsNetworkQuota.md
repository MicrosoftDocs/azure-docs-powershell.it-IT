---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94609250696a99a337153e9e0d3a1d092e380c40
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859874"
---
# <span data-ttu-id="a675d-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="a675d-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="a675d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a675d-102">SYNOPSIS</span></span>
<span data-ttu-id="a675d-103">Eliminare una quota per nome.</span><span class="sxs-lookup"><span data-stu-id="a675d-103">Delete a quota by name.</span></span>

## <span data-ttu-id="a675d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a675d-104">SYNTAX</span></span>

### <span data-ttu-id="a675d-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a675d-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a675d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a675d-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a675d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a675d-107">DESCRIPTION</span></span>
<span data-ttu-id="a675d-108">Eliminare una quota per nome.</span><span class="sxs-lookup"><span data-stu-id="a675d-108">Delete a quota by name.</span></span>

## <span data-ttu-id="a675d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a675d-109">EXAMPLES</span></span>

### <span data-ttu-id="a675d-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="a675d-110">EXAMPLE 1</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="a675d-111">Rimuovere una quota di rete per nome.</span><span class="sxs-lookup"><span data-stu-id="a675d-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="a675d-112">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="a675d-112">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="a675d-113">Rimuovere una quota di rete usando una pipe.</span><span class="sxs-lookup"><span data-stu-id="a675d-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="a675d-114">ESEMPIO 3</span><span class="sxs-lookup"><span data-stu-id="a675d-114">EXAMPLE 3</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="a675d-115">Rimuovere una quota di rete.</span><span class="sxs-lookup"><span data-stu-id="a675d-115">Remove a network quota.</span></span>

## <span data-ttu-id="a675d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a675d-116">PARAMETERS</span></span>

### <span data-ttu-id="a675d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a675d-117">-Name</span></span>
<span data-ttu-id="a675d-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a675d-118">Name of the resource.</span></span>

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

### <span data-ttu-id="a675d-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a675d-119">-Location</span></span>
<span data-ttu-id="a675d-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a675d-120">Location of the resource.</span></span>

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

### <span data-ttu-id="a675d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a675d-121">-ResourceId</span></span>
<span data-ttu-id="a675d-122">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a675d-122">The resource id.</span></span>

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

### <span data-ttu-id="a675d-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a675d-123">-AsJob</span></span>
<span data-ttu-id="a675d-124">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="a675d-124">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="a675d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a675d-125">-Force</span></span>
<span data-ttu-id="a675d-126">Parametro switch per non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="a675d-126">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="a675d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a675d-127">-WhatIf</span></span>
<span data-ttu-id="a675d-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a675d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a675d-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a675d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a675d-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a675d-130">-Confirm</span></span>
<span data-ttu-id="a675d-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a675d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a675d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a675d-132">CommonParameters</span></span>
<span data-ttu-id="a675d-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a675d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a675d-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a675d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a675d-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a675d-135">INPUTS</span></span>

## <span data-ttu-id="a675d-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a675d-136">OUTPUTS</span></span>

## <span data-ttu-id="a675d-137">Note</span><span class="sxs-lookup"><span data-stu-id="a675d-137">NOTES</span></span>

## <span data-ttu-id="a675d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a675d-138">RELATED LINKS</span></span>
