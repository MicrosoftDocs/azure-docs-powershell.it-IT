---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: fdceee36319d1c9ea950dbf5573b4ba0e3c614ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858769"
---
# <span data-ttu-id="55899-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="55899-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="55899-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55899-102">SYNOPSIS</span></span>
<span data-ttu-id="55899-103">Eliminare l'abbonamento a specificato.</span><span class="sxs-lookup"><span data-stu-id="55899-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="55899-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55899-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55899-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55899-105">DESCRIPTION</span></span>
<span data-ttu-id="55899-106">Eliminare l'abbonamento a specificato.</span><span class="sxs-lookup"><span data-stu-id="55899-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="55899-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55899-107">EXAMPLES</span></span>

### <span data-ttu-id="55899-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="55899-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="55899-109">Eliminare l'abbonamento a specificato.</span><span class="sxs-lookup"><span data-stu-id="55899-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="55899-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55899-110">PARAMETERS</span></span>

### <span data-ttu-id="55899-111">-Force</span><span class="sxs-lookup"><span data-stu-id="55899-111">-Force</span></span>
<span data-ttu-id="55899-112">Rimuovere l'abbonamento senza richiedere conferma</span><span class="sxs-lookup"><span data-stu-id="55899-112">Remove subscription without prompting</span></span>

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

### <span data-ttu-id="55899-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55899-113">-SubscriptionId</span></span>
<span data-ttu-id="55899-114">ID dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="55899-114">Id of the subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55899-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="55899-115">-Confirm</span></span>
<span data-ttu-id="55899-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55899-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55899-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55899-117">-WhatIf</span></span>
<span data-ttu-id="55899-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55899-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55899-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55899-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55899-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55899-120">CommonParameters</span></span>
<span data-ttu-id="55899-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55899-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55899-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55899-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55899-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55899-123">INPUTS</span></span>

## <span data-ttu-id="55899-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55899-124">OUTPUTS</span></span>

## <span data-ttu-id="55899-125">Note</span><span class="sxs-lookup"><span data-stu-id="55899-125">NOTES</span></span>

## <span data-ttu-id="55899-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55899-126">RELATED LINKS</span></span>

