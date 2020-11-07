---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47e4c38d3ccd98350721d358cb98eec55341ba97
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859942"
---
# <span data-ttu-id="7bd04-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="7bd04-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="7bd04-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7bd04-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd04-103">Spegnere un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="7bd04-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="7bd04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7bd04-104">SYNTAX</span></span>

### <span data-ttu-id="7bd04-105">PowerOff (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7bd04-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bd04-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bd04-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bd04-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bd04-107">DESCRIPTION</span></span>
<span data-ttu-id="7bd04-108">Spegnere un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="7bd04-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="7bd04-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7bd04-109">EXAMPLES</span></span>

### <span data-ttu-id="7bd04-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="7bd04-110">EXAMPLE 1</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="7bd04-111">Spegnere un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="7bd04-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="7bd04-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7bd04-112">PARAMETERS</span></span>

### <span data-ttu-id="7bd04-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7bd04-113">-Name</span></span>
<span data-ttu-id="7bd04-114">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="7bd04-114">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="7bd04-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7bd04-115">-Location</span></span>
<span data-ttu-id="7bd04-116">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7bd04-116">Location of the resource.</span></span>

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

### <span data-ttu-id="7bd04-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd04-117">-ResourceGroupName</span></span>
<span data-ttu-id="7bd04-118">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="7bd04-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="7bd04-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bd04-119">-ResourceId</span></span>
<span data-ttu-id="7bd04-120">ID risorsa istanza ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="7bd04-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="7bd04-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bd04-121">-AsJob</span></span>
<span data-ttu-id="7bd04-122">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="7bd04-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="7bd04-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7bd04-123">-Force</span></span>
<span data-ttu-id="7bd04-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="7bd04-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="7bd04-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bd04-125">-WhatIf</span></span>
<span data-ttu-id="7bd04-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bd04-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bd04-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bd04-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bd04-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7bd04-128">-Confirm</span></span>
<span data-ttu-id="7bd04-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bd04-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bd04-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd04-130">CommonParameters</span></span>
<span data-ttu-id="7bd04-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd04-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd04-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bd04-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd04-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7bd04-133">INPUTS</span></span>

## <span data-ttu-id="7bd04-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7bd04-134">OUTPUTS</span></span>

## <span data-ttu-id="7bd04-135">Note</span><span class="sxs-lookup"><span data-stu-id="7bd04-135">NOTES</span></span>

## <span data-ttu-id="7bd04-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7bd04-136">RELATED LINKS</span></span>
