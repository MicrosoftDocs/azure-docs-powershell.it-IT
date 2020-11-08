---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F956CC89-A2CA-4D73-8014-C36778C51927
online version: ''
schema: 2.0.0
ms.openlocfilehash: eba992b183795d016108419834c38bcf64a82d41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029630"
---
# <span data-ttu-id="eca47-101">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="eca47-101">Remove-AzureAvailabilitySet</span></span>

## <span data-ttu-id="eca47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eca47-102">SYNOPSIS</span></span>
<span data-ttu-id="eca47-103">Rimuove un set di disponibilità da una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="eca47-103">Removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="eca47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eca47-104">SYNTAX</span></span>

```
Remove-AzureAvailabilitySet -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="eca47-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eca47-105">DESCRIPTION</span></span>
<span data-ttu-id="eca47-106">Il cmdlet **Remove-AzureAvailabilitySet** rimuove un set di disponibilità da una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="eca47-106">The **Remove-AzureAvailabilitySet** cmdlet removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="eca47-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eca47-107">EXAMPLES</span></span>

### <span data-ttu-id="eca47-108">1:</span><span class="sxs-lookup"><span data-stu-id="eca47-108">1:</span></span>
```

```

## <span data-ttu-id="eca47-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eca47-109">PARAMETERS</span></span>

### <span data-ttu-id="eca47-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="eca47-110">-InformationAction</span></span>
<span data-ttu-id="eca47-111">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="eca47-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="eca47-112">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="eca47-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eca47-113">Continuare</span><span class="sxs-lookup"><span data-stu-id="eca47-113">Continue</span></span>
- <span data-ttu-id="eca47-114">Ignora</span><span class="sxs-lookup"><span data-stu-id="eca47-114">Ignore</span></span>
- <span data-ttu-id="eca47-115">Informarsi</span><span class="sxs-lookup"><span data-stu-id="eca47-115">Inquire</span></span>
- <span data-ttu-id="eca47-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="eca47-116">SilentlyContinue</span></span>
- <span data-ttu-id="eca47-117">Stop</span><span class="sxs-lookup"><span data-stu-id="eca47-117">Stop</span></span>
- <span data-ttu-id="eca47-118">Sospensione</span><span class="sxs-lookup"><span data-stu-id="eca47-118">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eca47-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="eca47-119">-InformationVariable</span></span>
<span data-ttu-id="eca47-120">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="eca47-120">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eca47-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="eca47-121">-Profile</span></span>
<span data-ttu-id="eca47-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eca47-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eca47-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="eca47-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eca47-124">-VM</span><span class="sxs-lookup"><span data-stu-id="eca47-124">-VM</span></span>
<span data-ttu-id="eca47-125">Specifica la macchina virtuale da cui questo cmdlet rimuove un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="eca47-125">Specifies the virtual machine from which this cmdlet removes an availability set.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eca47-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca47-126">CommonParameters</span></span>
<span data-ttu-id="eca47-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eca47-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca47-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eca47-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca47-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eca47-129">INPUTS</span></span>

## <span data-ttu-id="eca47-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eca47-130">OUTPUTS</span></span>

## <span data-ttu-id="eca47-131">Note</span><span class="sxs-lookup"><span data-stu-id="eca47-131">NOTES</span></span>

## <span data-ttu-id="eca47-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eca47-132">RELATED LINKS</span></span>

[<span data-ttu-id="eca47-133">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="eca47-133">Set-AzureAvailabilitySet</span></span>](./Set-AzureAvailabilitySet.md)


