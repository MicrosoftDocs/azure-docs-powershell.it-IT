---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04b011279d88f294e1caf95519e29a8368b08546
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93860038"
---
# <span data-ttu-id="c0699-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="c0699-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="c0699-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0699-102">SYNOPSIS</span></span>
<span data-ttu-id="c0699-103">Arrestare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="c0699-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="c0699-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0699-104">SYNTAX</span></span>

### <span data-ttu-id="c0699-105">Arresto (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c0699-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0699-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0699-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0699-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0699-107">DESCRIPTION</span></span>
<span data-ttu-id="c0699-108">Arrestare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="c0699-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="c0699-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0699-109">EXAMPLES</span></span>

### <span data-ttu-id="c0699-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="c0699-110">EXAMPLE 1</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="c0699-111">Arrestare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="c0699-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="c0699-112">In caso di errore viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="c0699-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="c0699-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0699-113">PARAMETERS</span></span>

### <span data-ttu-id="c0699-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0699-114">-Name</span></span>
<span data-ttu-id="c0699-115">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="c0699-115">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="c0699-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c0699-116">-Location</span></span>
<span data-ttu-id="c0699-117">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c0699-117">Location of the resource.</span></span>

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

### <span data-ttu-id="c0699-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0699-118">-ResourceGroupName</span></span>
<span data-ttu-id="c0699-119">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="c0699-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c0699-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0699-120">-ResourceId</span></span>
<span data-ttu-id="c0699-121">ID risorsa istanza ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="c0699-121">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="c0699-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0699-122">-AsJob</span></span>
<span data-ttu-id="c0699-123">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="c0699-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c0699-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c0699-124">-Force</span></span>
<span data-ttu-id="c0699-125">Non chiedere conferma</span><span class="sxs-lookup"><span data-stu-id="c0699-125">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="c0699-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0699-126">-WhatIf</span></span>
<span data-ttu-id="c0699-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0699-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0699-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0699-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0699-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c0699-129">-Confirm</span></span>
<span data-ttu-id="c0699-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0699-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0699-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0699-131">CommonParameters</span></span>
<span data-ttu-id="c0699-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0699-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0699-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0699-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0699-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0699-134">INPUTS</span></span>

## <span data-ttu-id="c0699-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0699-135">OUTPUTS</span></span>

## <span data-ttu-id="c0699-136">Note</span><span class="sxs-lookup"><span data-stu-id="c0699-136">NOTES</span></span>

## <span data-ttu-id="c0699-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0699-137">RELATED LINKS</span></span>
