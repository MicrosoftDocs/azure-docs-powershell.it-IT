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
ms.locfileid: "93685206"
---
# <span data-ttu-id="03569-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="03569-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="03569-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03569-102">SYNOPSIS</span></span>
<span data-ttu-id="03569-103">Restituisce il avaialbility del tipo e del nome della risorsa di sottoscrizione specificati</span><span class="sxs-lookup"><span data-stu-id="03569-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="03569-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03569-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="03569-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03569-105">DESCRIPTION</span></span>
<span data-ttu-id="03569-106">Restituisce il avaialbility del tipo e del nome della risorsa di sottoscrizione specificati</span><span class="sxs-lookup"><span data-stu-id="03569-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="03569-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03569-107">EXAMPLES</span></span>

### <span data-ttu-id="03569-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="03569-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="03569-109">Restituisce il avaialbility del tipo e del nome della risorsa di sottoscrizione specificati</span><span class="sxs-lookup"><span data-stu-id="03569-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="03569-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03569-110">PARAMETERS</span></span>

### <span data-ttu-id="03569-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="03569-111">-Name</span></span>
<span data-ttu-id="03569-112">Il nome della risorsa da verificare.</span><span class="sxs-lookup"><span data-stu-id="03569-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="03569-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="03569-113">-ResourceType</span></span>
<span data-ttu-id="03569-114">Tipo di risorsa da verificare.</span><span class="sxs-lookup"><span data-stu-id="03569-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="03569-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03569-115">CommonParameters</span></span>
<span data-ttu-id="03569-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03569-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03569-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03569-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03569-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03569-118">INPUTS</span></span>

## <span data-ttu-id="03569-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03569-119">OUTPUTS</span></span>

### <span data-ttu-id="03569-120">Microsoft. AzureStack. Management. subscriptions. admin. Models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="03569-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="03569-121">Note</span><span class="sxs-lookup"><span data-stu-id="03569-121">NOTES</span></span>

## <span data-ttu-id="03569-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03569-122">RELATED LINKS</span></span>

