---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FBED8515-4216-4AB6-B34E-D14A6063A3A7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2f145ec51bc6744d877661554e3d8e475d722fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023671"
---
# <span data-ttu-id="8be3e-101">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="8be3e-101">Add-AzureVirtualIP</span></span>

## <span data-ttu-id="8be3e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8be3e-102">SYNOPSIS</span></span>
<span data-ttu-id="8be3e-103">Aggiunge un IP virtuale a un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="8be3e-103">Adds a virtual IP to a cloud service.</span></span>

## <span data-ttu-id="8be3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8be3e-104">SYNTAX</span></span>

```
Add-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8be3e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8be3e-105">DESCRIPTION</span></span>
<span data-ttu-id="8be3e-106">Il cmdlet **Add-AzureVirtualIP** aggiunge un nuovo IP virtuale (VIP) al servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="8be3e-106">The **Add-AzureVirtualIP** cmdlet adds a new virtual IP (VIP) to your Azure service.</span></span>
<span data-ttu-id="8be3e-107">Il nuovo IP virtuale ha un nome ma non è assegnato un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="8be3e-107">The new virtual IP has a name but is not allocated an IP address.</span></span>

<span data-ttu-id="8be3e-108">L'indirizzo IP viene allocato solo quando si associa un endpoint al VIP.</span><span class="sxs-lookup"><span data-stu-id="8be3e-108">The IP address is allocated only when you associate an endpoint to the VIP.</span></span>
<span data-ttu-id="8be3e-109">Per altre informazioni, vedere Add-AzureEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8be3e-109">See Add-AzureEndpoint for more details.</span></span>

<span data-ttu-id="8be3e-110">L'abbonamento viene addebitato per i VIP aggiuntivi solo dopo che sono stati associati a un endpoint.</span><span class="sxs-lookup"><span data-stu-id="8be3e-110">Your subscription is charged for extra VIPs only once they are associated with an endpoint.</span></span>

## <span data-ttu-id="8be3e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8be3e-111">EXAMPLES</span></span>

### <span data-ttu-id="8be3e-112">Esempio 1: aggiungere un IP virtuale a un servizio</span><span class="sxs-lookup"><span data-stu-id="8be3e-112">Example 1: Add a virtual IP to a service</span></span>
```
PS C:\> Add-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
OperationDescription OperationId                          OperationStatus
-------------------- -----------                          ---------------
Add-AzureVirtualIP   4bd7b638-d2e7-216f-ba38-5221233d70ce Succeeded
```

<span data-ttu-id="8be3e-113">Questo comando aggiunge un indirizzo IP virtuale a un servizio.</span><span class="sxs-lookup"><span data-stu-id="8be3e-113">This command adds a virtual IP address to a service.</span></span>

## <span data-ttu-id="8be3e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8be3e-114">PARAMETERS</span></span>

### <span data-ttu-id="8be3e-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8be3e-115">-InformationAction</span></span>
<span data-ttu-id="8be3e-116">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="8be3e-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8be3e-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8be3e-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8be3e-118">Continuare</span><span class="sxs-lookup"><span data-stu-id="8be3e-118">Continue</span></span>
- <span data-ttu-id="8be3e-119">Ignora</span><span class="sxs-lookup"><span data-stu-id="8be3e-119">Ignore</span></span>
- <span data-ttu-id="8be3e-120">Informarsi</span><span class="sxs-lookup"><span data-stu-id="8be3e-120">Inquire</span></span>
- <span data-ttu-id="8be3e-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8be3e-121">SilentlyContinue</span></span>
- <span data-ttu-id="8be3e-122">Stop</span><span class="sxs-lookup"><span data-stu-id="8be3e-122">Stop</span></span>
- <span data-ttu-id="8be3e-123">Sospensione</span><span class="sxs-lookup"><span data-stu-id="8be3e-123">Suspend</span></span>

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

### <span data-ttu-id="8be3e-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8be3e-124">-InformationVariable</span></span>
<span data-ttu-id="8be3e-125">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="8be3e-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8be3e-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="8be3e-126">-Profile</span></span>
<span data-ttu-id="8be3e-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8be3e-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8be3e-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8be3e-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8be3e-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8be3e-129">-ServiceName</span></span>
<span data-ttu-id="8be3e-130">Specifica il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="8be3e-130">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be3e-131">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="8be3e-131">-VirtualIPName</span></span>
<span data-ttu-id="8be3e-132">Specifica il nome dell'indirizzo IP virtuale.</span><span class="sxs-lookup"><span data-stu-id="8be3e-132">Specifies the name of the virtual IP address.</span></span>

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

### <span data-ttu-id="8be3e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be3e-133">CommonParameters</span></span>
<span data-ttu-id="8be3e-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be3e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be3e-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be3e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be3e-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8be3e-136">INPUTS</span></span>

## <span data-ttu-id="8be3e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8be3e-137">OUTPUTS</span></span>

### <span data-ttu-id="8be3e-138">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="8be3e-138">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="8be3e-139">Note</span><span class="sxs-lookup"><span data-stu-id="8be3e-139">NOTES</span></span>

## <span data-ttu-id="8be3e-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8be3e-140">RELATED LINKS</span></span>

[<span data-ttu-id="8be3e-141">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="8be3e-141">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="8be3e-142">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="8be3e-142">Remove-AzureVirtualIP</span></span>](./Remove-AzureVirtualIP.md)


