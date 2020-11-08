---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030174"
---
# <span data-ttu-id="0dea3-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="0dea3-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="0dea3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0dea3-102">SYNOPSIS</span></span>
<span data-ttu-id="0dea3-103">Restituisce il avaialbility del tipo e del nome della risorsa di sottoscrizione specificati</span><span class="sxs-lookup"><span data-stu-id="0dea3-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="0dea3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0dea3-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="0dea3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0dea3-105">DESCRIPTION</span></span>
<span data-ttu-id="0dea3-106">Restituisce il avaialbility del tipo e del nome della risorsa di sottoscrizione specificati</span><span class="sxs-lookup"><span data-stu-id="0dea3-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="0dea3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0dea3-107">EXAMPLES</span></span>

### <span data-ttu-id="0dea3-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0dea3-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="0dea3-109">Restituisce il avaialbility del tipo e del nome della risorsa di sottoscrizione specificati</span><span class="sxs-lookup"><span data-stu-id="0dea3-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="0dea3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0dea3-110">PARAMETERS</span></span>

### <span data-ttu-id="0dea3-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="0dea3-111">-Name</span></span>
<span data-ttu-id="0dea3-112">Il nome della risorsa da verificare.</span><span class="sxs-lookup"><span data-stu-id="0dea3-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="0dea3-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0dea3-113">-ResourceType</span></span>
<span data-ttu-id="0dea3-114">Tipo di risorsa da verificare.</span><span class="sxs-lookup"><span data-stu-id="0dea3-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="0dea3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dea3-115">CommonParameters</span></span>
<span data-ttu-id="0dea3-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dea3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dea3-117">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dea3-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dea3-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0dea3-118">INPUTS</span></span>

## <span data-ttu-id="0dea3-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0dea3-119">OUTPUTS</span></span>

### <span data-ttu-id="0dea3-120">Microsoft. AzureStack. Management. subscriptions. admin. Models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="0dea3-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="0dea3-121">Note</span><span class="sxs-lookup"><span data-stu-id="0dea3-121">NOTES</span></span>

## <span data-ttu-id="0dea3-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0dea3-122">RELATED LINKS</span></span>

