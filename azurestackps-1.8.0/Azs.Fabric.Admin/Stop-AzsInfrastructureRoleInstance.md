---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47e4c38d3ccd98350721d358cb98eec55341ba97
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93858901"
---
# <span data-ttu-id="07a01-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="07a01-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="07a01-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07a01-102">SYNOPSIS</span></span>
<span data-ttu-id="07a01-103">Spegnere un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="07a01-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="07a01-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07a01-104">SYNTAX</span></span>

### <span data-ttu-id="07a01-105">PowerOff (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="07a01-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a01-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="07a01-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07a01-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07a01-107">DESCRIPTION</span></span>
<span data-ttu-id="07a01-108">Spegnere un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="07a01-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="07a01-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07a01-109">EXAMPLES</span></span>

### <span data-ttu-id="07a01-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="07a01-110">EXAMPLE 1</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="07a01-111">Spegnere un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="07a01-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="07a01-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07a01-112">PARAMETERS</span></span>

### <span data-ttu-id="07a01-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="07a01-113">-Name</span></span>
<span data-ttu-id="07a01-114">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="07a01-114">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a01-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="07a01-115">-Location</span></span>
<span data-ttu-id="07a01-116">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="07a01-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a01-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07a01-117">-ResourceGroupName</span></span>
<span data-ttu-id="07a01-118">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="07a01-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a01-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07a01-119">-ResourceId</span></span>
<span data-ttu-id="07a01-120">ID risorsa istanza ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="07a01-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="07a01-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07a01-121">-AsJob</span></span>
<span data-ttu-id="07a01-122">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="07a01-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="07a01-123">-Force</span><span class="sxs-lookup"><span data-stu-id="07a01-123">-Force</span></span>
<span data-ttu-id="07a01-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="07a01-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="07a01-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07a01-125">-WhatIf</span></span>
<span data-ttu-id="07a01-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07a01-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07a01-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07a01-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07a01-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07a01-128">-Confirm</span></span>
<span data-ttu-id="07a01-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07a01-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07a01-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a01-130">CommonParameters</span></span>
<span data-ttu-id="07a01-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07a01-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a01-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a01-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a01-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07a01-133">INPUTS</span></span>

## <span data-ttu-id="07a01-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07a01-134">OUTPUTS</span></span>

## <span data-ttu-id="07a01-135">Note</span><span class="sxs-lookup"><span data-stu-id="07a01-135">NOTES</span></span>

## <span data-ttu-id="07a01-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07a01-136">RELATED LINKS</span></span>
