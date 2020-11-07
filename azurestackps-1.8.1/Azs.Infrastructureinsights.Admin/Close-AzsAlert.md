---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14885871139eaed1c901312b9540a90d385795e5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859921"
---
# <span data-ttu-id="bbe98-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="bbe98-101">Close-AzsAlert</span></span>

## <span data-ttu-id="bbe98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bbe98-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe98-103">Chiude l'avviso indicato.</span><span class="sxs-lookup"><span data-stu-id="bbe98-103">Closes the given alert.</span></span>

## <span data-ttu-id="bbe98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbe98-104">SYNTAX</span></span>

### <span data-ttu-id="bbe98-105">Chiudi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bbe98-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbe98-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bbe98-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbe98-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbe98-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbe98-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbe98-108">DESCRIPTION</span></span>
<span data-ttu-id="bbe98-109">Chiude l'avviso indicato.</span><span class="sxs-lookup"><span data-stu-id="bbe98-109">Closes the given alert.</span></span>

## <span data-ttu-id="bbe98-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbe98-110">EXAMPLES</span></span>

### <span data-ttu-id="bbe98-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="bbe98-111">EXAMPLE 1</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="bbe98-112">Chiudere un avviso per nome.</span><span class="sxs-lookup"><span data-stu-id="bbe98-112">Close an alert by Name.</span></span>

### <span data-ttu-id="bbe98-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="bbe98-113">EXAMPLE 2</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="bbe98-114">Chiudere un avviso tramite piping.</span><span class="sxs-lookup"><span data-stu-id="bbe98-114">Close an alert through piping.</span></span>

## <span data-ttu-id="bbe98-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bbe98-115">PARAMETERS</span></span>

### <span data-ttu-id="bbe98-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbe98-116">-Name</span></span>
<span data-ttu-id="bbe98-117">Identificatore avviso.</span><span class="sxs-lookup"><span data-stu-id="bbe98-117">The alert identifier.</span></span>

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

### <span data-ttu-id="bbe98-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bbe98-118">-Location</span></span>
<span data-ttu-id="bbe98-119">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="bbe98-119">Name of the location.</span></span>

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

### <span data-ttu-id="bbe98-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbe98-120">-ResourceGroupName</span></span>
<span data-ttu-id="bbe98-121">Nome del gruppo di risorse dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="bbe98-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="bbe98-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbe98-122">-InputObject</span></span>
<span data-ttu-id="bbe98-123">Un avviso restituito da Get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="bbe98-123">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="bbe98-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbe98-124">-ResourceId</span></span>
<span data-ttu-id="bbe98-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="bbe98-125">The resource id.</span></span>

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

### <span data-ttu-id="bbe98-126">-Force</span><span class="sxs-lookup"><span data-stu-id="bbe98-126">-Force</span></span>
<span data-ttu-id="bbe98-127">Parametro switch per non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="bbe98-127">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="bbe98-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbe98-128">-WhatIf</span></span>
<span data-ttu-id="bbe98-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbe98-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbe98-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbe98-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbe98-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bbe98-131">-Confirm</span></span>
<span data-ttu-id="bbe98-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbe98-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbe98-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe98-133">CommonParameters</span></span>
<span data-ttu-id="bbe98-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbe98-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe98-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbe98-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe98-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bbe98-136">INPUTS</span></span>

## <span data-ttu-id="bbe98-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbe98-137">OUTPUTS</span></span>

### <span data-ttu-id="bbe98-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="bbe98-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="bbe98-139">Note</span><span class="sxs-lookup"><span data-stu-id="bbe98-139">NOTES</span></span>

## <span data-ttu-id="bbe98-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbe98-140">RELATED LINKS</span></span>
