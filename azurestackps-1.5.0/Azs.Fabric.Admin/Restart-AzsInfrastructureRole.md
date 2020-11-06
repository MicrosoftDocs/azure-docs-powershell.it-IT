---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: da781ee77cb94e7bc442b72ad0655041cf23b546
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490894"
---
# <span data-ttu-id="d49d9-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="d49d9-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="d49d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d49d9-102">SYNOPSIS</span></span>
<span data-ttu-id="d49d9-103">Riavvia il ruolo dell'infrastruttura richiesto.</span><span class="sxs-lookup"><span data-stu-id="d49d9-103">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="d49d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d49d9-104">SYNTAX</span></span>

### <span data-ttu-id="d49d9-105">Restart (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d49d9-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d49d9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d49d9-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d49d9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d49d9-107">DESCRIPTION</span></span>
<span data-ttu-id="d49d9-108">Riavvia il ruolo dell'infrastruttura richiesto.</span><span class="sxs-lookup"><span data-stu-id="d49d9-108">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="d49d9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d49d9-109">EXAMPLES</span></span>

### <span data-ttu-id="d49d9-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d49d9-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restart-AzsInfrastructureRole -Name "Compute Controller"
```

<span data-ttu-id="d49d9-111">Riavviare un ruolo di infrastruttura che si è arrestato.</span><span class="sxs-lookup"><span data-stu-id="d49d9-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="d49d9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d49d9-112">PARAMETERS</span></span>

### <span data-ttu-id="d49d9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d49d9-113">-AsJob</span></span>
<span data-ttu-id="d49d9-114">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="d49d9-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d49d9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d49d9-115">-Force</span></span>
<span data-ttu-id="d49d9-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d49d9-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d49d9-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d49d9-117">-Location</span></span>
<span data-ttu-id="d49d9-118">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d49d9-118">Location of the resource.</span></span>

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

### <span data-ttu-id="d49d9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d49d9-119">-Name</span></span>
<span data-ttu-id="d49d9-120">Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="d49d9-120">Infrastructure role name.</span></span>

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

### <span data-ttu-id="d49d9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d49d9-121">-ResourceGroupName</span></span>
<span data-ttu-id="d49d9-122">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="d49d9-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="d49d9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d49d9-123">-ResourceId</span></span>
<span data-ttu-id="d49d9-124">ID risorsa ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="d49d9-124">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="d49d9-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d49d9-125">-Confirm</span></span>
<span data-ttu-id="d49d9-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d49d9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d49d9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d49d9-127">-WhatIf</span></span>
<span data-ttu-id="d49d9-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d49d9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d49d9-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d49d9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d49d9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d49d9-130">CommonParameters</span></span>
<span data-ttu-id="d49d9-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d49d9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d49d9-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d49d9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d49d9-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d49d9-133">INPUTS</span></span>

## <span data-ttu-id="d49d9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d49d9-134">OUTPUTS</span></span>

## <span data-ttu-id="d49d9-135">Note</span><span class="sxs-lookup"><span data-stu-id="d49d9-135">NOTES</span></span>

## <span data-ttu-id="d49d9-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d49d9-136">RELATED LINKS</span></span>

