---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94609250696a99a337153e9e0d3a1d092e380c40
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859294"
---
# <span data-ttu-id="fbe6a-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="fbe6a-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="fbe6a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fbe6a-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe6a-103">Eliminare una quota per nome.</span><span class="sxs-lookup"><span data-stu-id="fbe6a-103">Delete a quota by name.</span></span>

## <span data-ttu-id="fbe6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbe6a-104">SYNTAX</span></span>

### <span data-ttu-id="fbe6a-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fbe6a-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fbe6a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbe6a-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbe6a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbe6a-107">DESCRIPTION</span></span>
<span data-ttu-id="fbe6a-108">Eliminare una quota per nome.</span><span class="sxs-lookup"><span data-stu-id="fbe6a-108">Delete a quota by name.</span></span>

## <span data-ttu-id="fbe6a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbe6a-109">EXAMPLES</span></span>

### <span data-ttu-id="fbe6a-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="fbe6a-110">EXAMPLE 1</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="fbe6a-111">Rimuovere una quota di rete per nome.</span><span class="sxs-lookup"><span data-stu-id="fbe6a-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="fbe6a-112">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="fbe6a-112">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="fbe6a-113">Rimuovere una quota di rete usando una pipe.</span><span class="sxs-lookup"><span data-stu-id="fbe6a-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="fbe6a-114">ESEMPIO 3</span><span class="sxs-lookup"><span data-stu-id="fbe6a-114">EXAMPLE 3</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="fbe6a-115">Rimuovere una quota di rete.</span><span class="sxs-lookup"><span data-stu-id="fbe6a-115">Remove a network quota.</span></span>

## <span data-ttu-id="fbe6a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fbe6a-116">PARAMETERS</span></span>

### <span data-ttu-id="fbe6a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="fbe6a-117">-Name</span></span>
<span data-ttu-id="fbe6a-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fbe6a-118">Name of the resource.</span></span>

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

### <span data-ttu-id="fbe6a-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fbe6a-119">-Location</span></span>
<span data-ttu-id="fbe6a-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fbe6a-120">Location of the resource.</span></span>

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

### <span data-ttu-id="fbe6a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbe6a-121">-ResourceId</span></span>
<span data-ttu-id="fbe6a-122">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="fbe6a-122">The resource id.</span></span>

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

### <span data-ttu-id="fbe6a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbe6a-123">-AsJob</span></span>
<span data-ttu-id="fbe6a-124">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="fbe6a-124">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="fbe6a-125">-Force</span><span class="sxs-lookup"><span data-stu-id="fbe6a-125">-Force</span></span>
<span data-ttu-id="fbe6a-126">Parametro switch per non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="fbe6a-126">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="fbe6a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe6a-127">-WhatIf</span></span>
<span data-ttu-id="fbe6a-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbe6a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbe6a-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbe6a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbe6a-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fbe6a-130">-Confirm</span></span>
<span data-ttu-id="fbe6a-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbe6a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbe6a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe6a-132">CommonParameters</span></span>
<span data-ttu-id="fbe6a-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe6a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe6a-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe6a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe6a-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fbe6a-135">INPUTS</span></span>

## <span data-ttu-id="fbe6a-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbe6a-136">OUTPUTS</span></span>

## <span data-ttu-id="fbe6a-137">Note</span><span class="sxs-lookup"><span data-stu-id="fbe6a-137">NOTES</span></span>

## <span data-ttu-id="fbe6a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbe6a-138">RELATED LINKS</span></span>
