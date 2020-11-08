---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 781b920bf955a84554b9152f54c9847a00a8b160
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030198"
---
# <span data-ttu-id="ed6a7-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="ed6a7-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="ed6a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed6a7-102">SYNOPSIS</span></span>
<span data-ttu-id="ed6a7-103">Riavvia il ruolo dell'infrastruttura richiedente.</span><span class="sxs-lookup"><span data-stu-id="ed6a7-103">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="ed6a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed6a7-104">SYNTAX</span></span>

### <span data-ttu-id="ed6a7-105">Restart (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ed6a7-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed6a7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed6a7-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed6a7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed6a7-107">DESCRIPTION</span></span>
<span data-ttu-id="ed6a7-108">Riavvia il ruolo dell'infrastruttura richiedente.</span><span class="sxs-lookup"><span data-stu-id="ed6a7-108">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="ed6a7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed6a7-109">EXAMPLES</span></span>

### <span data-ttu-id="ed6a7-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="ed6a7-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="ed6a7-111">Riavviare un ruolo di infrastruttura che si è arrestato.</span><span class="sxs-lookup"><span data-stu-id="ed6a7-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="ed6a7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed6a7-112">PARAMETERS</span></span>

### <span data-ttu-id="ed6a7-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed6a7-113">-Name</span></span>
<span data-ttu-id="ed6a7-114">Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="ed6a7-114">Infrastructure role name.</span></span>

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

### <span data-ttu-id="ed6a7-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ed6a7-115">-Location</span></span>
<span data-ttu-id="ed6a7-116">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ed6a7-116">Location of the resource.</span></span>

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

### <span data-ttu-id="ed6a7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed6a7-117">-ResourceGroupName</span></span>
<span data-ttu-id="ed6a7-118">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="ed6a7-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ed6a7-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed6a7-119">-ResourceId</span></span>
<span data-ttu-id="ed6a7-120">ID risorsa ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="ed6a7-120">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="ed6a7-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed6a7-121">-AsJob</span></span>
<span data-ttu-id="ed6a7-122">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="ed6a7-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="ed6a7-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ed6a7-123">-Force</span></span>
<span data-ttu-id="ed6a7-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ed6a7-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ed6a7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed6a7-125">-WhatIf</span></span>
<span data-ttu-id="ed6a7-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed6a7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed6a7-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed6a7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed6a7-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ed6a7-128">-Confirm</span></span>
<span data-ttu-id="ed6a7-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed6a7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed6a7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed6a7-130">CommonParameters</span></span>
<span data-ttu-id="ed6a7-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed6a7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed6a7-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed6a7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed6a7-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed6a7-133">INPUTS</span></span>

## <span data-ttu-id="ed6a7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed6a7-134">OUTPUTS</span></span>

## <span data-ttu-id="ed6a7-135">Note</span><span class="sxs-lookup"><span data-stu-id="ed6a7-135">NOTES</span></span>

## <span data-ttu-id="ed6a7-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed6a7-136">RELATED LINKS</span></span>
