---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03dfddb3ec666df5096184c5e00692862e091626
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030142"
---
# <span data-ttu-id="1a841-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="1a841-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="1a841-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a841-102">SYNOPSIS</span></span>
<span data-ttu-id="1a841-103">Riavviare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="1a841-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="1a841-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a841-104">SYNTAX</span></span>

### <span data-ttu-id="1a841-105">Restart (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1a841-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a841-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a841-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a841-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a841-107">DESCRIPTION</span></span>
<span data-ttu-id="1a841-108">Riavviare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="1a841-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="1a841-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a841-109">EXAMPLES</span></span>

### <span data-ttu-id="1a841-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="1a841-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="1a841-111">Riavviare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="1a841-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="1a841-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a841-112">PARAMETERS</span></span>

### <span data-ttu-id="1a841-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a841-113">-Name</span></span>
<span data-ttu-id="1a841-114">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="1a841-114">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="1a841-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1a841-115">-Location</span></span>
<span data-ttu-id="1a841-116">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1a841-116">Location of the resource.</span></span>

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

### <span data-ttu-id="1a841-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a841-117">-ResourceGroupName</span></span>
<span data-ttu-id="1a841-118">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="1a841-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1a841-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a841-119">-ResourceId</span></span>
<span data-ttu-id="1a841-120">ID risorsa istanza ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="1a841-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="1a841-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a841-121">-AsJob</span></span>
<span data-ttu-id="1a841-122">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="1a841-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="1a841-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1a841-123">-Force</span></span>
<span data-ttu-id="1a841-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="1a841-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1a841-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a841-125">-WhatIf</span></span>
<span data-ttu-id="1a841-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a841-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a841-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a841-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a841-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1a841-128">-Confirm</span></span>
<span data-ttu-id="1a841-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a841-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a841-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a841-130">CommonParameters</span></span>
<span data-ttu-id="1a841-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a841-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a841-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a841-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a841-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a841-133">INPUTS</span></span>

## <span data-ttu-id="1a841-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a841-134">OUTPUTS</span></span>

## <span data-ttu-id="1a841-135">Note</span><span class="sxs-lookup"><span data-stu-id="1a841-135">NOTES</span></span>

## <span data-ttu-id="1a841-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a841-136">RELATED LINKS</span></span>
