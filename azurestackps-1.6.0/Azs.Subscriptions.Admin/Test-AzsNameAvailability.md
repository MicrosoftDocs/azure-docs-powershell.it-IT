---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 267a5bf4c3f864c987c0bc747eefce9dd3ffe6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491206"
---
# <span data-ttu-id="1f781-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="1f781-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="1f781-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f781-102">SYNOPSIS</span></span>
<span data-ttu-id="1f781-103">Restituisce il avaialbility del tipo e del nome della risorsa di sottoscrizione specificati</span><span class="sxs-lookup"><span data-stu-id="1f781-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="1f781-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f781-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="1f781-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f781-105">DESCRIPTION</span></span>
<span data-ttu-id="1f781-106">Restituisce il avaialbility del tipo e del nome della risorsa di sottoscrizione specificati</span><span class="sxs-lookup"><span data-stu-id="1f781-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="1f781-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f781-107">EXAMPLES</span></span>

### <span data-ttu-id="1f781-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1f781-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="1f781-109">Restituisce il avaialbility del tipo e del nome della risorsa di sottoscrizione specificati</span><span class="sxs-lookup"><span data-stu-id="1f781-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="1f781-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f781-110">PARAMETERS</span></span>

### <span data-ttu-id="1f781-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f781-111">-Name</span></span>
<span data-ttu-id="1f781-112">Il nome della risorsa da verificare.</span><span class="sxs-lookup"><span data-stu-id="1f781-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="1f781-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="1f781-113">-ResourceType</span></span>
<span data-ttu-id="1f781-114">Tipo di risorsa da verificare.</span><span class="sxs-lookup"><span data-stu-id="1f781-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="1f781-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f781-115">CommonParameters</span></span>
<span data-ttu-id="1f781-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f781-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f781-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f781-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f781-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f781-118">INPUTS</span></span>

## <span data-ttu-id="1f781-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f781-119">OUTPUTS</span></span>

### <span data-ttu-id="1f781-120">Microsoft. AzureStack. Management. subscriptions. admin. Models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1f781-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="1f781-121">Note</span><span class="sxs-lookup"><span data-stu-id="1f781-121">NOTES</span></span>

## <span data-ttu-id="1f781-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f781-122">RELATED LINKS</span></span>

