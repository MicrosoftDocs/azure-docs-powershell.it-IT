---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa4bd73f9300daf8ca17e3a11d884e06e9852234
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857950"
---
# <span data-ttu-id="c5bae-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="c5bae-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="c5bae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5bae-102">SYNOPSIS</span></span>
<span data-ttu-id="c5bae-103">Rimuove il piano specificato</span><span class="sxs-lookup"><span data-stu-id="c5bae-103">Removes the specified plan</span></span>

## <span data-ttu-id="c5bae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5bae-104">SYNTAX</span></span>

### <span data-ttu-id="c5bae-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5bae-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5bae-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5bae-106">ResourceId</span></span>
```
Remove-AzsPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5bae-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5bae-107">DESCRIPTION</span></span>
<span data-ttu-id="c5bae-108">Rimuove il piano specificato</span><span class="sxs-lookup"><span data-stu-id="c5bae-108">Removes the specified plan</span></span>

## <span data-ttu-id="c5bae-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5bae-109">EXAMPLES</span></span>

### <span data-ttu-id="c5bae-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c5bae-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlan -Name plan1 -ResourceGroupName "rg1"
```

<span data-ttu-id="c5bae-111">Rimuove il piano specificato</span><span class="sxs-lookup"><span data-stu-id="c5bae-111">Removes the specified plan</span></span>

## <span data-ttu-id="c5bae-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5bae-112">PARAMETERS</span></span>

### <span data-ttu-id="c5bae-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c5bae-113">-Force</span></span>
<span data-ttu-id="c5bae-114">Contrassegna per rimuovere l'elemento senza conferma.</span><span class="sxs-lookup"><span data-stu-id="c5bae-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="c5bae-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5bae-115">-Name</span></span>
<span data-ttu-id="c5bae-116">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="c5bae-116">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5bae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5bae-117">-ResourceGroupName</span></span>
<span data-ttu-id="c5bae-118">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c5bae-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5bae-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5bae-119">-ResourceId</span></span>
<span data-ttu-id="c5bae-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c5bae-120">The resource id.</span></span>

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

### <span data-ttu-id="c5bae-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c5bae-121">-Confirm</span></span>
<span data-ttu-id="c5bae-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5bae-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5bae-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5bae-123">-WhatIf</span></span>
<span data-ttu-id="c5bae-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5bae-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5bae-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5bae-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5bae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5bae-126">CommonParameters</span></span>
<span data-ttu-id="c5bae-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5bae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5bae-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5bae-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5bae-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5bae-129">INPUTS</span></span>

## <span data-ttu-id="c5bae-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5bae-130">OUTPUTS</span></span>

## <span data-ttu-id="c5bae-131">Note</span><span class="sxs-lookup"><span data-stu-id="c5bae-131">NOTES</span></span>

## <span data-ttu-id="c5bae-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5bae-132">RELATED LINKS</span></span>

