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
ms.locfileid: "93491389"
---
# <span data-ttu-id="a77df-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="a77df-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="a77df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a77df-102">SYNOPSIS</span></span>
<span data-ttu-id="a77df-103">Arrestare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="a77df-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="a77df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a77df-104">SYNTAX</span></span>

### <span data-ttu-id="a77df-105">Arresto (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a77df-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a77df-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a77df-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a77df-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a77df-107">DESCRIPTION</span></span>
<span data-ttu-id="a77df-108">Arrestare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="a77df-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="a77df-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a77df-109">EXAMPLES</span></span>

### <span data-ttu-id="a77df-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a77df-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="a77df-111">Arrestare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="a77df-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="a77df-112">In caso di errore viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="a77df-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="a77df-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a77df-113">PARAMETERS</span></span>

### <span data-ttu-id="a77df-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a77df-114">-AsJob</span></span>
<span data-ttu-id="a77df-115">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="a77df-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="a77df-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a77df-116">-Force</span></span>
<span data-ttu-id="a77df-117">Non chiedere conferma</span><span class="sxs-lookup"><span data-stu-id="a77df-117">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="a77df-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a77df-118">-Location</span></span>
<span data-ttu-id="a77df-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a77df-119">Location of the resource.</span></span>

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

### <span data-ttu-id="a77df-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a77df-120">-Name</span></span>
<span data-ttu-id="a77df-121">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="a77df-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="a77df-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a77df-122">-ResourceGroupName</span></span>
<span data-ttu-id="a77df-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="a77df-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a77df-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a77df-124">-ResourceId</span></span>
<span data-ttu-id="a77df-125">ID risorsa istanza ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="a77df-125">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="a77df-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a77df-126">-Confirm</span></span>
<span data-ttu-id="a77df-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a77df-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a77df-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a77df-128">-WhatIf</span></span>
<span data-ttu-id="a77df-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a77df-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a77df-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a77df-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a77df-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a77df-131">CommonParameters</span></span>
<span data-ttu-id="a77df-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a77df-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a77df-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a77df-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a77df-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a77df-134">INPUTS</span></span>

## <span data-ttu-id="a77df-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a77df-135">OUTPUTS</span></span>

## <span data-ttu-id="a77df-136">Note</span><span class="sxs-lookup"><span data-stu-id="a77df-136">NOTES</span></span>

## <span data-ttu-id="a77df-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a77df-137">RELATED LINKS</span></span>

