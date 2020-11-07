---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b06ae4189b427686f4237c1a6eae841fcaba5c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858786"
---
# <span data-ttu-id="ab083-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="ab083-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="ab083-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab083-102">SYNOPSIS</span></span>
<span data-ttu-id="ab083-103">Ripristina l'avviso indicato.</span><span class="sxs-lookup"><span data-stu-id="ab083-103">Repairs the given alert.</span></span>

## <span data-ttu-id="ab083-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab083-104">SYNTAX</span></span>

### <span data-ttu-id="ab083-105">Ripristino (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab083-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab083-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ab083-106">InputObject</span></span>
```
Repair-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab083-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab083-107">DESCRIPTION</span></span>
<span data-ttu-id="ab083-108">Ripristina l'avviso indicato.</span><span class="sxs-lookup"><span data-stu-id="ab083-108">Repairs the given alert.</span></span>

## <span data-ttu-id="ab083-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab083-109">EXAMPLES</span></span>

### <span data-ttu-id="ab083-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ab083-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="ab083-111">Ripristina un avviso per nome.</span><span class="sxs-lookup"><span data-stu-id="ab083-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="ab083-112">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ab083-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="ab083-113">Ripristina un avviso tramite piping.</span><span class="sxs-lookup"><span data-stu-id="ab083-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="ab083-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab083-114">PARAMETERS</span></span>

### <span data-ttu-id="ab083-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ab083-115">-Force</span></span>
<span data-ttu-id="ab083-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ab083-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ab083-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab083-117">-InputObject</span></span>
<span data-ttu-id="ab083-118">Un avviso restituito da Get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="ab083-118">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="ab083-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ab083-119">-Location</span></span>
<span data-ttu-id="ab083-120">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="ab083-120">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab083-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab083-121">-Name</span></span>
<span data-ttu-id="ab083-122">Identificatore avviso.</span><span class="sxs-lookup"><span data-stu-id="ab083-122">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab083-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab083-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab083-124">Nome del gruppo di risorse che la risorsa risiede.</span><span class="sxs-lookup"><span data-stu-id="ab083-124">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab083-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ab083-125">-Confirm</span></span>
<span data-ttu-id="ab083-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab083-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab083-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab083-127">-WhatIf</span></span>
<span data-ttu-id="ab083-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab083-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab083-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab083-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab083-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab083-130">CommonParameters</span></span>
<span data-ttu-id="ab083-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab083-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab083-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab083-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab083-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab083-133">INPUTS</span></span>

## <span data-ttu-id="ab083-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab083-134">OUTPUTS</span></span>

## <span data-ttu-id="ab083-135">Note</span><span class="sxs-lookup"><span data-stu-id="ab083-135">NOTES</span></span>

## <span data-ttu-id="ab083-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab083-136">RELATED LINKS</span></span>

