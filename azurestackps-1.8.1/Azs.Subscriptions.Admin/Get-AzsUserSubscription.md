---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859550"
---
# <span data-ttu-id="8313e-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="8313e-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="8313e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8313e-102">SYNOPSIS</span></span>
<span data-ttu-id="8313e-103">Ottenere l'elenco degli abbonamenti agli utenti come amministratore.</span><span class="sxs-lookup"><span data-stu-id="8313e-103">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="8313e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8313e-104">SYNTAX</span></span>

### <span data-ttu-id="8313e-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8313e-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="8313e-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="8313e-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="8313e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8313e-107">DESCRIPTION</span></span>
<span data-ttu-id="8313e-108">Ottenere l'elenco degli abbonamenti agli utenti come amministratore.</span><span class="sxs-lookup"><span data-stu-id="8313e-108">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="8313e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8313e-109">EXAMPLES</span></span>

### <span data-ttu-id="8313e-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8313e-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="8313e-111">Ottenere l'elenco degli abbonamenti agli utenti come amministratore.</span><span class="sxs-lookup"><span data-stu-id="8313e-111">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="8313e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8313e-112">PARAMETERS</span></span>

### <span data-ttu-id="8313e-113">-Filtro</span><span class="sxs-lookup"><span data-stu-id="8313e-113">-Filter</span></span>
<span data-ttu-id="8313e-114">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="8313e-114">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8313e-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8313e-115">-SubscriptionId</span></span>
<span data-ttu-id="8313e-116">Parametro ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8313e-116">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8313e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8313e-117">CommonParameters</span></span>
<span data-ttu-id="8313e-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8313e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8313e-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8313e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8313e-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8313e-120">INPUTS</span></span>

## <span data-ttu-id="8313e-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8313e-121">OUTPUTS</span></span>

### <span data-ttu-id="8313e-122">Microsoft. AzureStack. Management. abbonamenti. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="8313e-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="8313e-123">Note</span><span class="sxs-lookup"><span data-stu-id="8313e-123">NOTES</span></span>

## <span data-ttu-id="8313e-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8313e-124">RELATED LINKS</span></span>

