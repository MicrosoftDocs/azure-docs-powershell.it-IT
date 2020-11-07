---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348582b008d50371bc937961cd76edbf1ba13762
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858625"
---
# <span data-ttu-id="0a8ad-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="0a8ad-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="0a8ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a8ad-102">SYNOPSIS</span></span>
<span data-ttu-id="0a8ad-103">Arrestare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="0a8ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a8ad-104">SYNTAX</span></span>

### <span data-ttu-id="0a8ad-105">Arresto (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0a8ad-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8ad-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a8ad-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a8ad-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a8ad-107">DESCRIPTION</span></span>
<span data-ttu-id="0a8ad-108">Arrestare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="0a8ad-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a8ad-109">EXAMPLES</span></span>

### <span data-ttu-id="0a8ad-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0a8ad-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="0a8ad-111">Arrestare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="0a8ad-112">In caso di errore viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="0a8ad-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a8ad-113">PARAMETERS</span></span>

### <span data-ttu-id="0a8ad-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a8ad-114">-AsJob</span></span>
<span data-ttu-id="0a8ad-115">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="0a8ad-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0a8ad-116">-Force</span></span>
<span data-ttu-id="0a8ad-117">Non chiedere conferma</span><span class="sxs-lookup"><span data-stu-id="0a8ad-117">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="0a8ad-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0a8ad-118">-Location</span></span>
<span data-ttu-id="0a8ad-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-119">Location of the resource.</span></span>

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

### <span data-ttu-id="0a8ad-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a8ad-120">-Name</span></span>
<span data-ttu-id="0a8ad-121">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="0a8ad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a8ad-122">-ResourceGroupName</span></span>
<span data-ttu-id="0a8ad-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="0a8ad-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a8ad-124">-ResourceId</span></span>
<span data-ttu-id="0a8ad-125">ID risorsa istanza ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-125">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="0a8ad-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0a8ad-126">-Confirm</span></span>
<span data-ttu-id="0a8ad-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a8ad-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a8ad-128">-WhatIf</span></span>
<span data-ttu-id="0a8ad-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a8ad-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a8ad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a8ad-131">CommonParameters</span></span>
<span data-ttu-id="0a8ad-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a8ad-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a8ad-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a8ad-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a8ad-134">INPUTS</span></span>

## <span data-ttu-id="0a8ad-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a8ad-135">OUTPUTS</span></span>

## <span data-ttu-id="0a8ad-136">Note</span><span class="sxs-lookup"><span data-stu-id="0a8ad-136">NOTES</span></span>

## <span data-ttu-id="0a8ad-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a8ad-137">RELATED LINKS</span></span>

