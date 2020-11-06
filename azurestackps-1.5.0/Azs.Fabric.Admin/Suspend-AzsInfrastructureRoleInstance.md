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
ms.locfileid: "93507139"
---
# <span data-ttu-id="25242-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="25242-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="25242-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="25242-102">SYNOPSIS</span></span>
<span data-ttu-id="25242-103">Arrestare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="25242-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="25242-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25242-104">SYNTAX</span></span>

### <span data-ttu-id="25242-105">Arresto (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="25242-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25242-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="25242-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25242-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25242-107">DESCRIPTION</span></span>
<span data-ttu-id="25242-108">Arrestare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="25242-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="25242-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25242-109">EXAMPLES</span></span>

### <span data-ttu-id="25242-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="25242-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="25242-111">Arrestare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="25242-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="25242-112">In caso di errore viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="25242-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="25242-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="25242-113">PARAMETERS</span></span>

### <span data-ttu-id="25242-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25242-114">-AsJob</span></span>
<span data-ttu-id="25242-115">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="25242-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="25242-116">-Force</span><span class="sxs-lookup"><span data-stu-id="25242-116">-Force</span></span>
<span data-ttu-id="25242-117">Non chiedere conferma</span><span class="sxs-lookup"><span data-stu-id="25242-117">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="25242-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="25242-118">-Location</span></span>
<span data-ttu-id="25242-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="25242-119">Location of the resource.</span></span>

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

### <span data-ttu-id="25242-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="25242-120">-Name</span></span>
<span data-ttu-id="25242-121">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="25242-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="25242-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25242-122">-ResourceGroupName</span></span>
<span data-ttu-id="25242-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="25242-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="25242-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25242-124">-ResourceId</span></span>
<span data-ttu-id="25242-125">ID risorsa istanza ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="25242-125">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="25242-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="25242-126">-Confirm</span></span>
<span data-ttu-id="25242-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25242-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25242-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25242-128">-WhatIf</span></span>
<span data-ttu-id="25242-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25242-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25242-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25242-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25242-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25242-131">CommonParameters</span></span>
<span data-ttu-id="25242-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25242-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25242-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25242-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25242-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="25242-134">INPUTS</span></span>

## <span data-ttu-id="25242-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25242-135">OUTPUTS</span></span>

## <span data-ttu-id="25242-136">Note</span><span class="sxs-lookup"><span data-stu-id="25242-136">NOTES</span></span>

## <span data-ttu-id="25242-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25242-137">RELATED LINKS</span></span>

