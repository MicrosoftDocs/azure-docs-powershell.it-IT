---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93858841"
---
# <span data-ttu-id="a6d4f-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="a6d4f-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="a6d4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d4f-103">Restituisce il avaialbility del tipo e del nome della risorsa di sottoscrizione specificati</span><span class="sxs-lookup"><span data-stu-id="a6d4f-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="a6d4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6d4f-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="a6d4f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6d4f-105">DESCRIPTION</span></span>
<span data-ttu-id="a6d4f-106">Restituisce il avaialbility del tipo e del nome della risorsa di sottoscrizione specificati</span><span class="sxs-lookup"><span data-stu-id="a6d4f-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="a6d4f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6d4f-107">EXAMPLES</span></span>

### <span data-ttu-id="a6d4f-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a6d4f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="a6d4f-109">Restituisce il avaialbility del tipo e del nome della risorsa di sottoscrizione specificati</span><span class="sxs-lookup"><span data-stu-id="a6d4f-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="a6d4f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6d4f-110">PARAMETERS</span></span>

### <span data-ttu-id="a6d4f-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6d4f-111">-Name</span></span>
<span data-ttu-id="a6d4f-112">Il nome della risorsa da verificare.</span><span class="sxs-lookup"><span data-stu-id="a6d4f-112">The resource name to verify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d4f-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a6d4f-113">-ResourceType</span></span>
<span data-ttu-id="a6d4f-114">Tipo di risorsa da verificare.</span><span class="sxs-lookup"><span data-stu-id="a6d4f-114">The resource type to verify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d4f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d4f-115">CommonParameters</span></span>
<span data-ttu-id="a6d4f-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6d4f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d4f-117">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6d4f-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d4f-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6d4f-118">INPUTS</span></span>

## <span data-ttu-id="a6d4f-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6d4f-119">OUTPUTS</span></span>

### <span data-ttu-id="a6d4f-120">Microsoft. AzureStack. Management. subscriptions. admin. Models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="a6d4f-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="a6d4f-121">Note</span><span class="sxs-lookup"><span data-stu-id="a6d4f-121">NOTES</span></span>

## <span data-ttu-id="a6d4f-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6d4f-122">RELATED LINKS</span></span>

