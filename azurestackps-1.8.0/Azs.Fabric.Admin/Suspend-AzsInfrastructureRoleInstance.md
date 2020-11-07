---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04b011279d88f294e1caf95519e29a8368b08546
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859141"
---
# <span data-ttu-id="38abe-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="38abe-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="38abe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38abe-102">SYNOPSIS</span></span>
<span data-ttu-id="38abe-103">Arrestare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="38abe-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="38abe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38abe-104">SYNTAX</span></span>

### <span data-ttu-id="38abe-105">Arresto (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38abe-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38abe-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="38abe-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38abe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38abe-107">DESCRIPTION</span></span>
<span data-ttu-id="38abe-108">Arrestare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="38abe-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="38abe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38abe-109">EXAMPLES</span></span>

### <span data-ttu-id="38abe-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="38abe-110">EXAMPLE 1</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="38abe-111">Arrestare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="38abe-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="38abe-112">In caso di errore viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="38abe-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="38abe-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38abe-113">PARAMETERS</span></span>

### <span data-ttu-id="38abe-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="38abe-114">-Name</span></span>
<span data-ttu-id="38abe-115">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="38abe-115">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38abe-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="38abe-116">-Location</span></span>
<span data-ttu-id="38abe-117">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="38abe-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38abe-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38abe-118">-ResourceGroupName</span></span>
<span data-ttu-id="38abe-119">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="38abe-119">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38abe-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38abe-120">-ResourceId</span></span>
<span data-ttu-id="38abe-121">ID risorsa istanza ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="38abe-121">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="38abe-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38abe-122">-AsJob</span></span>
<span data-ttu-id="38abe-123">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="38abe-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="38abe-124">-Force</span><span class="sxs-lookup"><span data-stu-id="38abe-124">-Force</span></span>
<span data-ttu-id="38abe-125">Non chiedere conferma</span><span class="sxs-lookup"><span data-stu-id="38abe-125">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="38abe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38abe-126">-WhatIf</span></span>
<span data-ttu-id="38abe-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38abe-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38abe-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38abe-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38abe-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="38abe-129">-Confirm</span></span>
<span data-ttu-id="38abe-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38abe-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38abe-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38abe-131">CommonParameters</span></span>
<span data-ttu-id="38abe-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38abe-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38abe-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38abe-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38abe-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38abe-134">INPUTS</span></span>

## <span data-ttu-id="38abe-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38abe-135">OUTPUTS</span></span>

## <span data-ttu-id="38abe-136">Note</span><span class="sxs-lookup"><span data-stu-id="38abe-136">NOTES</span></span>

## <span data-ttu-id="38abe-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38abe-137">RELATED LINKS</span></span>
