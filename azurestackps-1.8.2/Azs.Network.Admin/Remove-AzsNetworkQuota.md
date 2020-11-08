---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94609250696a99a337153e9e0d3a1d092e380c40
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030632"
---
# <span data-ttu-id="0f32e-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="0f32e-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="0f32e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f32e-102">SYNOPSIS</span></span>
<span data-ttu-id="0f32e-103">Eliminare una quota per nome.</span><span class="sxs-lookup"><span data-stu-id="0f32e-103">Delete a quota by name.</span></span>

## <span data-ttu-id="0f32e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f32e-104">SYNTAX</span></span>

### <span data-ttu-id="0f32e-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f32e-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f32e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f32e-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f32e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f32e-107">DESCRIPTION</span></span>
<span data-ttu-id="0f32e-108">Eliminare una quota per nome.</span><span class="sxs-lookup"><span data-stu-id="0f32e-108">Delete a quota by name.</span></span>

## <span data-ttu-id="0f32e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f32e-109">EXAMPLES</span></span>

### <span data-ttu-id="0f32e-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="0f32e-110">EXAMPLE 1</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="0f32e-111">Rimuovere una quota di rete per nome.</span><span class="sxs-lookup"><span data-stu-id="0f32e-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="0f32e-112">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="0f32e-112">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="0f32e-113">Rimuovere una quota di rete usando una pipe.</span><span class="sxs-lookup"><span data-stu-id="0f32e-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="0f32e-114">ESEMPIO 3</span><span class="sxs-lookup"><span data-stu-id="0f32e-114">EXAMPLE 3</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="0f32e-115">Rimuovere una quota di rete.</span><span class="sxs-lookup"><span data-stu-id="0f32e-115">Remove a network quota.</span></span>

## <span data-ttu-id="0f32e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f32e-116">PARAMETERS</span></span>

### <span data-ttu-id="0f32e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f32e-117">-Name</span></span>
<span data-ttu-id="0f32e-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f32e-118">Name of the resource.</span></span>

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

### <span data-ttu-id="0f32e-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0f32e-119">-Location</span></span>
<span data-ttu-id="0f32e-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f32e-120">Location of the resource.</span></span>

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

### <span data-ttu-id="0f32e-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f32e-121">-ResourceId</span></span>
<span data-ttu-id="0f32e-122">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f32e-122">The resource id.</span></span>

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

### <span data-ttu-id="0f32e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f32e-123">-AsJob</span></span>
<span data-ttu-id="0f32e-124">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="0f32e-124">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="0f32e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="0f32e-125">-Force</span></span>
<span data-ttu-id="0f32e-126">Parametro switch per non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="0f32e-126">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="0f32e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f32e-127">-WhatIf</span></span>
<span data-ttu-id="0f32e-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f32e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f32e-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f32e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f32e-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0f32e-130">-Confirm</span></span>
<span data-ttu-id="0f32e-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f32e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f32e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f32e-132">CommonParameters</span></span>
<span data-ttu-id="0f32e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f32e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f32e-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f32e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f32e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f32e-135">INPUTS</span></span>

## <span data-ttu-id="0f32e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f32e-136">OUTPUTS</span></span>

## <span data-ttu-id="0f32e-137">Note</span><span class="sxs-lookup"><span data-stu-id="0f32e-137">NOTES</span></span>

## <span data-ttu-id="0f32e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f32e-138">RELATED LINKS</span></span>
