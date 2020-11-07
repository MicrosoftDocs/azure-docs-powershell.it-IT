---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 199d9fb2ce88c149965d488b55bce669f364a615
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859518"
---
# <span data-ttu-id="b6bbe-101">New-PlanAcquisitionPropertiesObject</span><span class="sxs-lookup"><span data-stu-id="b6bbe-101">New-PlanAcquisitionPropertiesObject</span></span>

## <span data-ttu-id="b6bbe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6bbe-102">SYNOPSIS</span></span>
<span data-ttu-id="b6bbe-103">Rappresenta l'acquisizione di un piano di componente aggiuntivo per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b6bbe-103">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="b6bbe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6bbe-104">SYNTAX</span></span>

```
New-PlanAcquisitionPropertiesObject [[-ProvisioningState] <String>] [[-AcquisitionTime] <String>]
 [[-Id] <String>] [[-PlanId] <String>] [[-AcquisitionId] <String>] [[-ExternalReferenceId] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6bbe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6bbe-105">DESCRIPTION</span></span>
<span data-ttu-id="b6bbe-106">Rappresenta l'acquisizione di un piano di componente aggiuntivo per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b6bbe-106">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="b6bbe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6bbe-107">EXAMPLES</span></span>

### <span data-ttu-id="b6bbe-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b6bbe-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b6bbe-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="b6bbe-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b6bbe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6bbe-110">PARAMETERS</span></span>

### <span data-ttu-id="b6bbe-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="b6bbe-111">-AcquisitionId</span></span>
<span data-ttu-id="b6bbe-112">Identificatore di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="b6bbe-112">Acquisition identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6bbe-113">-AcquisitionTime</span><span class="sxs-lookup"><span data-stu-id="b6bbe-113">-AcquisitionTime</span></span>
<span data-ttu-id="b6bbe-114">Tempo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="b6bbe-114">Acquisition time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6bbe-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="b6bbe-115">-ExternalReferenceId</span></span>
<span data-ttu-id="b6bbe-116">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="b6bbe-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6bbe-117">-ID</span><span class="sxs-lookup"><span data-stu-id="b6bbe-117">-Id</span></span>
<span data-ttu-id="b6bbe-118">Identificatore nel contesto della sottoscrizione tenant.</span><span class="sxs-lookup"><span data-stu-id="b6bbe-118">Identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6bbe-119">-PlanId</span><span class="sxs-lookup"><span data-stu-id="b6bbe-119">-PlanId</span></span>
<span data-ttu-id="b6bbe-120">Identificatore piano nel contesto dell'abbonamento tenant.</span><span class="sxs-lookup"><span data-stu-id="b6bbe-120">Plan identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6bbe-121">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="b6bbe-121">-ProvisioningState</span></span>
<span data-ttu-id="b6bbe-122">Stato del provisioning.</span><span class="sxs-lookup"><span data-stu-id="b6bbe-122">State of the provisioning.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6bbe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6bbe-123">CommonParameters</span></span>
<span data-ttu-id="b6bbe-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6bbe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6bbe-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6bbe-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6bbe-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6bbe-126">INPUTS</span></span>

## <span data-ttu-id="b6bbe-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6bbe-127">OUTPUTS</span></span>

## <span data-ttu-id="b6bbe-128">Note</span><span class="sxs-lookup"><span data-stu-id="b6bbe-128">NOTES</span></span>

## <span data-ttu-id="b6bbe-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6bbe-129">RELATED LINKS</span></span>

