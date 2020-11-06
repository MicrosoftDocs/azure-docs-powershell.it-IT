---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f5a52ebfe2d59a200add1c8f763f7a3cafa59c18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507003"
---
# <span data-ttu-id="59aa4-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="59aa4-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="59aa4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="59aa4-103">Alimentazione in un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="59aa4-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="59aa4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59aa4-104">SYNTAX</span></span>

### <span data-ttu-id="59aa4-105">PowerOn (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59aa4-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59aa4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="59aa4-106">ResourceId</span></span>
```
Start-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59aa4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59aa4-107">DESCRIPTION</span></span>
<span data-ttu-id="59aa4-108">Alimentazione in un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="59aa4-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="59aa4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59aa4-109">EXAMPLES</span></span>

### <span data-ttu-id="59aa4-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="59aa4-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="59aa4-111">Alimentazione in un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="59aa4-111">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="59aa4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59aa4-112">PARAMETERS</span></span>

### <span data-ttu-id="59aa4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59aa4-113">-AsJob</span></span>
<span data-ttu-id="59aa4-114">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="59aa4-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="59aa4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="59aa4-115">-Force</span></span>
<span data-ttu-id="59aa4-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="59aa4-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="59aa4-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="59aa4-117">-Location</span></span>
<span data-ttu-id="59aa4-118">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="59aa4-118">Location of the resource.</span></span>

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

### <span data-ttu-id="59aa4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="59aa4-119">-Name</span></span>
<span data-ttu-id="59aa4-120">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="59aa4-120">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="59aa4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59aa4-121">-ResourceGroupName</span></span>
<span data-ttu-id="59aa4-122">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="59aa4-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="59aa4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59aa4-123">-ResourceId</span></span>
<span data-ttu-id="59aa4-124">ID risorsa istanza ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="59aa4-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="59aa4-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="59aa4-125">-Confirm</span></span>
<span data-ttu-id="59aa4-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59aa4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59aa4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59aa4-127">-WhatIf</span></span>
<span data-ttu-id="59aa4-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59aa4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59aa4-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59aa4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59aa4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59aa4-130">CommonParameters</span></span>
<span data-ttu-id="59aa4-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59aa4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59aa4-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59aa4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59aa4-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59aa4-133">INPUTS</span></span>

## <span data-ttu-id="59aa4-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59aa4-134">OUTPUTS</span></span>

## <span data-ttu-id="59aa4-135">Note</span><span class="sxs-lookup"><span data-stu-id="59aa4-135">NOTES</span></span>

## <span data-ttu-id="59aa4-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59aa4-136">RELATED LINKS</span></span>

