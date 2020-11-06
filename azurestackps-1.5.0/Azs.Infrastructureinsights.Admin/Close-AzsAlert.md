---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ce97fe1fc7e21f166b1bb86db52bc8ad6e29e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491133"
---
# <span data-ttu-id="63f71-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="63f71-101">Close-AzsAlert</span></span>

## <span data-ttu-id="63f71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63f71-102">SYNOPSIS</span></span>
<span data-ttu-id="63f71-103">Chiude l'avviso indicato.</span><span class="sxs-lookup"><span data-stu-id="63f71-103">Closes the given alert.</span></span>

## <span data-ttu-id="63f71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63f71-104">SYNTAX</span></span>

### <span data-ttu-id="63f71-105">Chiudi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="63f71-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63f71-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="63f71-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63f71-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="63f71-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63f71-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63f71-108">DESCRIPTION</span></span>
<span data-ttu-id="63f71-109">Chiude l'avviso indicato.</span><span class="sxs-lookup"><span data-stu-id="63f71-109">Closes the given alert.</span></span>

## <span data-ttu-id="63f71-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63f71-110">EXAMPLES</span></span>

### <span data-ttu-id="63f71-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="63f71-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="63f71-112">Chiudere un avviso per nome.</span><span class="sxs-lookup"><span data-stu-id="63f71-112">Close an alert by Name.</span></span>

### <span data-ttu-id="63f71-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="63f71-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="63f71-114">Chiudere un avviso tramite piping.</span><span class="sxs-lookup"><span data-stu-id="63f71-114">Close an alert through piping.</span></span>

## <span data-ttu-id="63f71-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63f71-115">PARAMETERS</span></span>

### <span data-ttu-id="63f71-116">-Force</span><span class="sxs-lookup"><span data-stu-id="63f71-116">-Force</span></span>
<span data-ttu-id="63f71-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="63f71-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="63f71-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63f71-118">-InputObject</span></span>
<span data-ttu-id="63f71-119">Un avviso restituito da Get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="63f71-119">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="63f71-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="63f71-120">-Location</span></span>
<span data-ttu-id="63f71-121">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="63f71-121">Name of the location.</span></span>

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

### <span data-ttu-id="63f71-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="63f71-122">-Name</span></span>
<span data-ttu-id="63f71-123">Identificatore avviso.</span><span class="sxs-lookup"><span data-stu-id="63f71-123">The alert identifier.</span></span>

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

### <span data-ttu-id="63f71-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63f71-124">-ResourceGroupName</span></span>
<span data-ttu-id="63f71-125">Nome del gruppo di risorse che la risorsa risiede.</span><span class="sxs-lookup"><span data-stu-id="63f71-125">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="63f71-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63f71-126">-ResourceId</span></span>
<span data-ttu-id="63f71-127">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="63f71-127">The resource id.</span></span>

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

### <span data-ttu-id="63f71-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="63f71-128">-Confirm</span></span>
<span data-ttu-id="63f71-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63f71-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63f71-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63f71-130">-WhatIf</span></span>
<span data-ttu-id="63f71-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63f71-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63f71-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63f71-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63f71-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f71-133">CommonParameters</span></span>
<span data-ttu-id="63f71-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f71-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f71-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63f71-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f71-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63f71-136">INPUTS</span></span>

## <span data-ttu-id="63f71-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63f71-137">OUTPUTS</span></span>

### <span data-ttu-id="63f71-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="63f71-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="63f71-139">Note</span><span class="sxs-lookup"><span data-stu-id="63f71-139">NOTES</span></span>

## <span data-ttu-id="63f71-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63f71-140">RELATED LINKS</span></span>

