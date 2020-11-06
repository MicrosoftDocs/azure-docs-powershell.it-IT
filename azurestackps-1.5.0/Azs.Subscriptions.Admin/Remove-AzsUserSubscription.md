---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d76356e99419ff345e2eccc025c91637417de1a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491022"
---
# <span data-ttu-id="75eb1-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="75eb1-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="75eb1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="75eb1-103">Rimuove l'abbonamento al tenant specificato.</span><span class="sxs-lookup"><span data-stu-id="75eb1-103">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="75eb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75eb1-104">SYNTAX</span></span>

```
Remove-AzsUserSubscription [-SubscriptionId] <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75eb1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75eb1-105">DESCRIPTION</span></span>
<span data-ttu-id="75eb1-106">Rimuove l'abbonamento al tenant specificato.</span><span class="sxs-lookup"><span data-stu-id="75eb1-106">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="75eb1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75eb1-107">EXAMPLES</span></span>

### <span data-ttu-id="75eb1-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="75eb1-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="75eb1-109">Rimuovere l'abbonamento del tenant specificato.</span><span class="sxs-lookup"><span data-stu-id="75eb1-109">Remove the specified tenant subscription.</span></span>

## <span data-ttu-id="75eb1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75eb1-110">PARAMETERS</span></span>

### <span data-ttu-id="75eb1-111">-Force</span><span class="sxs-lookup"><span data-stu-id="75eb1-111">-Force</span></span>
<span data-ttu-id="75eb1-112">Contrassegna per rimuovere l'elemento senza conferma.</span><span class="sxs-lookup"><span data-stu-id="75eb1-112">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="75eb1-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75eb1-113">-SubscriptionId</span></span>
<span data-ttu-id="75eb1-114">Parametro ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="75eb1-114">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75eb1-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="75eb1-115">-Confirm</span></span>
<span data-ttu-id="75eb1-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75eb1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75eb1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75eb1-117">-WhatIf</span></span>
<span data-ttu-id="75eb1-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75eb1-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75eb1-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75eb1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75eb1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75eb1-120">CommonParameters</span></span>
<span data-ttu-id="75eb1-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75eb1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75eb1-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75eb1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75eb1-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75eb1-123">INPUTS</span></span>

## <span data-ttu-id="75eb1-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75eb1-124">OUTPUTS</span></span>

## <span data-ttu-id="75eb1-125">Note</span><span class="sxs-lookup"><span data-stu-id="75eb1-125">NOTES</span></span>

## <span data-ttu-id="75eb1-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75eb1-126">RELATED LINKS</span></span>

