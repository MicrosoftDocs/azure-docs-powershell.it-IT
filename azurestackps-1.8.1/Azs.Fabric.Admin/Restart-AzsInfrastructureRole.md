---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 781b920bf955a84554b9152f54c9847a00a8b160
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859609"
---
# <span data-ttu-id="59292-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="59292-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="59292-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59292-102">SYNOPSIS</span></span>
<span data-ttu-id="59292-103">Riavvia il ruolo dell'infrastruttura richiedente.</span><span class="sxs-lookup"><span data-stu-id="59292-103">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="59292-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59292-104">SYNTAX</span></span>

### <span data-ttu-id="59292-105">Restart (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59292-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59292-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="59292-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59292-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59292-107">DESCRIPTION</span></span>
<span data-ttu-id="59292-108">Riavvia il ruolo dell'infrastruttura richiedente.</span><span class="sxs-lookup"><span data-stu-id="59292-108">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="59292-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59292-109">EXAMPLES</span></span>

### <span data-ttu-id="59292-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="59292-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="59292-111">Riavviare un ruolo di infrastruttura che si è arrestato.</span><span class="sxs-lookup"><span data-stu-id="59292-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="59292-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59292-112">PARAMETERS</span></span>

### <span data-ttu-id="59292-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="59292-113">-Name</span></span>
<span data-ttu-id="59292-114">Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="59292-114">Infrastructure role name.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59292-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="59292-115">-Location</span></span>
<span data-ttu-id="59292-116">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="59292-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59292-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59292-117">-ResourceGroupName</span></span>
<span data-ttu-id="59292-118">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="59292-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59292-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59292-119">-ResourceId</span></span>
<span data-ttu-id="59292-120">ID risorsa ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="59292-120">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="59292-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59292-121">-AsJob</span></span>
<span data-ttu-id="59292-122">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="59292-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="59292-123">-Force</span><span class="sxs-lookup"><span data-stu-id="59292-123">-Force</span></span>
<span data-ttu-id="59292-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="59292-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="59292-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59292-125">-WhatIf</span></span>
<span data-ttu-id="59292-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59292-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59292-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59292-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59292-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="59292-128">-Confirm</span></span>
<span data-ttu-id="59292-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59292-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59292-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59292-130">CommonParameters</span></span>
<span data-ttu-id="59292-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59292-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59292-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59292-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59292-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59292-133">INPUTS</span></span>

## <span data-ttu-id="59292-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59292-134">OUTPUTS</span></span>

## <span data-ttu-id="59292-135">Note</span><span class="sxs-lookup"><span data-stu-id="59292-135">NOTES</span></span>

## <span data-ttu-id="59292-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59292-136">RELATED LINKS</span></span>
