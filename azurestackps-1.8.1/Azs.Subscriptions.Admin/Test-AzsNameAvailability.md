---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859985"
---
# <span data-ttu-id="9d44b-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="9d44b-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="9d44b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d44b-102">SYNOPSIS</span></span>
<span data-ttu-id="9d44b-103">Restituisce il avaialbility del tipo e del nome della risorsa di sottoscrizione specificati</span><span class="sxs-lookup"><span data-stu-id="9d44b-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="9d44b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d44b-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="9d44b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d44b-105">DESCRIPTION</span></span>
<span data-ttu-id="9d44b-106">Restituisce il avaialbility del tipo e del nome della risorsa di sottoscrizione specificati</span><span class="sxs-lookup"><span data-stu-id="9d44b-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="9d44b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d44b-107">EXAMPLES</span></span>

### <span data-ttu-id="9d44b-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9d44b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="9d44b-109">Restituisce il avaialbility del tipo e del nome della risorsa di sottoscrizione specificati</span><span class="sxs-lookup"><span data-stu-id="9d44b-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="9d44b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d44b-110">PARAMETERS</span></span>

### <span data-ttu-id="9d44b-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d44b-111">-Name</span></span>
<span data-ttu-id="9d44b-112">Il nome della risorsa da verificare.</span><span class="sxs-lookup"><span data-stu-id="9d44b-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="9d44b-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9d44b-113">-ResourceType</span></span>
<span data-ttu-id="9d44b-114">Tipo di risorsa da verificare.</span><span class="sxs-lookup"><span data-stu-id="9d44b-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="9d44b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d44b-115">CommonParameters</span></span>
<span data-ttu-id="9d44b-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d44b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d44b-117">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d44b-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d44b-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d44b-118">INPUTS</span></span>

## <span data-ttu-id="9d44b-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d44b-119">OUTPUTS</span></span>

### <span data-ttu-id="9d44b-120">Microsoft. AzureStack. Management. subscriptions. admin. Models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="9d44b-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="9d44b-121">Note</span><span class="sxs-lookup"><span data-stu-id="9d44b-121">NOTES</span></span>

## <span data-ttu-id="9d44b-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d44b-122">RELATED LINKS</span></span>

