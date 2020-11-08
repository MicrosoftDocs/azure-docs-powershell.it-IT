---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14885871139eaed1c901312b9540a90d385795e5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030384"
---
# <span data-ttu-id="83f3d-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="83f3d-101">Close-AzsAlert</span></span>

## <span data-ttu-id="83f3d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="83f3d-103">Chiude l'avviso indicato.</span><span class="sxs-lookup"><span data-stu-id="83f3d-103">Closes the given alert.</span></span>

## <span data-ttu-id="83f3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83f3d-104">SYNTAX</span></span>

### <span data-ttu-id="83f3d-105">Chiudi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="83f3d-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83f3d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="83f3d-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83f3d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="83f3d-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83f3d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83f3d-108">DESCRIPTION</span></span>
<span data-ttu-id="83f3d-109">Chiude l'avviso indicato.</span><span class="sxs-lookup"><span data-stu-id="83f3d-109">Closes the given alert.</span></span>

## <span data-ttu-id="83f3d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83f3d-110">EXAMPLES</span></span>

### <span data-ttu-id="83f3d-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="83f3d-111">EXAMPLE 1</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="83f3d-112">Chiudere un avviso per nome.</span><span class="sxs-lookup"><span data-stu-id="83f3d-112">Close an alert by Name.</span></span>

### <span data-ttu-id="83f3d-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="83f3d-113">EXAMPLE 2</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="83f3d-114">Chiudere un avviso tramite piping.</span><span class="sxs-lookup"><span data-stu-id="83f3d-114">Close an alert through piping.</span></span>

## <span data-ttu-id="83f3d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83f3d-115">PARAMETERS</span></span>

### <span data-ttu-id="83f3d-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="83f3d-116">-Name</span></span>
<span data-ttu-id="83f3d-117">Identificatore avviso.</span><span class="sxs-lookup"><span data-stu-id="83f3d-117">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f3d-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="83f3d-118">-Location</span></span>
<span data-ttu-id="83f3d-119">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="83f3d-119">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f3d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83f3d-120">-ResourceGroupName</span></span>
<span data-ttu-id="83f3d-121">Nome del gruppo di risorse dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="83f3d-121">Resource group name of the alert.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f3d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83f3d-122">-InputObject</span></span>
<span data-ttu-id="83f3d-123">Un avviso restituito da Get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="83f3d-123">An alert returned from Get-AzsAlert.</span></span>

```yaml
Type: Alert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83f3d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83f3d-124">-ResourceId</span></span>
<span data-ttu-id="83f3d-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="83f3d-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83f3d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="83f3d-126">-Force</span></span>
<span data-ttu-id="83f3d-127">Parametro switch per non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="83f3d-127">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="83f3d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83f3d-128">-WhatIf</span></span>
<span data-ttu-id="83f3d-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83f3d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83f3d-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83f3d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83f3d-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="83f3d-131">-Confirm</span></span>
<span data-ttu-id="83f3d-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83f3d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83f3d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f3d-133">CommonParameters</span></span>
<span data-ttu-id="83f3d-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83f3d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f3d-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83f3d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f3d-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83f3d-136">INPUTS</span></span>

## <span data-ttu-id="83f3d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83f3d-137">OUTPUTS</span></span>

### <span data-ttu-id="83f3d-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="83f3d-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="83f3d-139">Note</span><span class="sxs-lookup"><span data-stu-id="83f3d-139">NOTES</span></span>

## <span data-ttu-id="83f3d-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83f3d-140">RELATED LINKS</span></span>
