---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48f7fd6280596e70810d330f3fe69b37059e15cd
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859485"
---
# <span data-ttu-id="e66d3-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="e66d3-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="e66d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e66d3-102">SYNOPSIS</span></span>
<span data-ttu-id="e66d3-103">Alimentazione in un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="e66d3-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="e66d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e66d3-104">SYNTAX</span></span>

### <span data-ttu-id="e66d3-105">PowerOn (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e66d3-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e66d3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e66d3-106">ResourceId</span></span>
```
Start-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e66d3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e66d3-107">DESCRIPTION</span></span>
<span data-ttu-id="e66d3-108">Alimentazione in un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="e66d3-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="e66d3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e66d3-109">EXAMPLES</span></span>

### <span data-ttu-id="e66d3-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="e66d3-110">EXAMPLE 1</span></span>
```
Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="e66d3-111">Alimentazione in un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="e66d3-111">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="e66d3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e66d3-112">PARAMETERS</span></span>

### <span data-ttu-id="e66d3-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e66d3-113">-Name</span></span>
<span data-ttu-id="e66d3-114">Nome dell'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="e66d3-114">Name of the infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e66d3-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e66d3-115">-Location</span></span>
<span data-ttu-id="e66d3-116">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e66d3-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e66d3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e66d3-117">-ResourceGroupName</span></span>
<span data-ttu-id="e66d3-118">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="e66d3-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e66d3-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e66d3-119">-ResourceId</span></span>
<span data-ttu-id="e66d3-120">ID risorsa istanza ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="e66d3-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="e66d3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e66d3-121">-AsJob</span></span>
<span data-ttu-id="e66d3-122">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="e66d3-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="e66d3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e66d3-123">-Force</span></span>
<span data-ttu-id="e66d3-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="e66d3-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e66d3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e66d3-125">-WhatIf</span></span>
<span data-ttu-id="e66d3-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e66d3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e66d3-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e66d3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e66d3-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e66d3-128">-Confirm</span></span>
<span data-ttu-id="e66d3-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e66d3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e66d3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e66d3-130">CommonParameters</span></span>
<span data-ttu-id="e66d3-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e66d3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e66d3-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e66d3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e66d3-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e66d3-133">INPUTS</span></span>

## <span data-ttu-id="e66d3-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e66d3-134">OUTPUTS</span></span>

## <span data-ttu-id="e66d3-135">Note</span><span class="sxs-lookup"><span data-stu-id="e66d3-135">NOTES</span></span>

## <span data-ttu-id="e66d3-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e66d3-136">RELATED LINKS</span></span>
