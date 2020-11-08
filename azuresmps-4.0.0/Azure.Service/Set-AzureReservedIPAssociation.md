---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3249E908-B1D9-4707-844D-168274F1A466
online version: ''
schema: 2.0.0
ms.openlocfilehash: ae16609adf70b2e5a0edcd05c36b30860a3920cf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023783"
---
# <span data-ttu-id="b151a-101">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="b151a-101">Set-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="b151a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b151a-102">SYNOPSIS</span></span>
<span data-ttu-id="b151a-103">Associa un indirizzo IP riservato a una macchina virtuale o un servizio cloud esistente.</span><span class="sxs-lookup"><span data-stu-id="b151a-103">Associates a reserved IP address with an existing virtual machine or cloud service.</span></span>

## <span data-ttu-id="b151a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b151a-104">SYNTAX</span></span>

```
Set-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String> [[-VirtualIPName] <String>]
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b151a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b151a-105">DESCRIPTION</span></span>
<span data-ttu-id="b151a-106">Il cmdlet **set-AzureReservedIPAssociation** associa un indirizzo IP riservato con l'indirizzo IP virtuale (VIP) di una macchina virtuale in uso o di un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b151a-106">The **Set-AzureReservedIPAssociation** cmdlet associates a reserved IP address with the Virtual IP address (VIP) of a running virtual machine or cloud service.</span></span>
<span data-ttu-id="b151a-107">L'indirizzo IP riservato non deve essere in uso al momento della chiamata di questo cmdlet e deve trovarsi nella stessa area geografica della macchina virtuale o del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b151a-107">The reserved IP address must not be in use at the time of invocation of this cmdlet, and must be in the same region as the virtual machine or cloud service.</span></span>

<span data-ttu-id="b151a-108">Il completamento dell'operazione dura circa 30 secondi, dopodiché la macchina virtuale o il servizio è accessibile usando l'indirizzo IP riservato.</span><span class="sxs-lookup"><span data-stu-id="b151a-108">The operation takes about 30 seconds to complete, after which the virtual machine or service is accessible using the reserved IP address.</span></span>

## <span data-ttu-id="b151a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b151a-109">EXAMPLES</span></span>

### <span data-ttu-id="b151a-110">Esempio 1: impostare un'associazione IP riservata</span><span class="sxs-lookup"><span data-stu-id="b151a-110">Example 1: Set a reserved IP association</span></span>
```
PS C:\> Set-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="b151a-111">Questo comando assegna l'indirizzo IP riservato denominato ResIp14 al servizio PipTestWestEurope.</span><span class="sxs-lookup"><span data-stu-id="b151a-111">This command assigns the reserved IP address named ResIp14 to the service PipTestWestEurope.</span></span>
<span data-ttu-id="b151a-112">ResIp14 è un IP riservato nell'area dell'Europa occidentale.</span><span class="sxs-lookup"><span data-stu-id="b151a-112">ResIp14 is a reserved IP in the West Europe region.</span></span>

## <span data-ttu-id="b151a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b151a-113">PARAMETERS</span></span>

### <span data-ttu-id="b151a-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b151a-114">-InformationAction</span></span>
<span data-ttu-id="b151a-115">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="b151a-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b151a-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b151a-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b151a-117">Continuare</span><span class="sxs-lookup"><span data-stu-id="b151a-117">Continue</span></span>
- <span data-ttu-id="b151a-118">Ignora</span><span class="sxs-lookup"><span data-stu-id="b151a-118">Ignore</span></span>
- <span data-ttu-id="b151a-119">Informarsi</span><span class="sxs-lookup"><span data-stu-id="b151a-119">Inquire</span></span>
- <span data-ttu-id="b151a-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b151a-120">SilentlyContinue</span></span>
- <span data-ttu-id="b151a-121">Stop</span><span class="sxs-lookup"><span data-stu-id="b151a-121">Stop</span></span>
- <span data-ttu-id="b151a-122">Sospensione</span><span class="sxs-lookup"><span data-stu-id="b151a-122">Suspend</span></span>

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

### <span data-ttu-id="b151a-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b151a-123">-InformationVariable</span></span>
<span data-ttu-id="b151a-124">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="b151a-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b151a-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="b151a-125">-Profile</span></span>
<span data-ttu-id="b151a-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b151a-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b151a-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b151a-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b151a-128">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="b151a-128">-ReservedIPName</span></span>
<span data-ttu-id="b151a-129">Specifica il nome dell'indirizzo IP riservato da associare a una macchina virtuale o a un servizio.</span><span class="sxs-lookup"><span data-stu-id="b151a-129">Specifies the name of the reserved IP address to associate with a virtual machine or service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151a-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b151a-130">-ServiceName</span></span>
<span data-ttu-id="b151a-131">Specifica il nome del servizio con la distribuzione con cui associare l'indirizzo IP riservato.</span><span class="sxs-lookup"><span data-stu-id="b151a-131">Specifies the name of the service that has the deployment with which to associate the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151a-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="b151a-132">-Slot</span></span>
<span data-ttu-id="b151a-133">Specifica lo slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b151a-133">Specifies the deployment slot.</span></span>
<span data-ttu-id="b151a-134">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b151a-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b151a-135">Gestione temporanea</span><span class="sxs-lookup"><span data-stu-id="b151a-135">Staging</span></span>
- <span data-ttu-id="b151a-136">Produzione</span><span class="sxs-lookup"><span data-stu-id="b151a-136">Production</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151a-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="b151a-137">-VirtualIPName</span></span>
<span data-ttu-id="b151a-138">Specifica il nome di un VIP esistente da associare a un IP riservato.</span><span class="sxs-lookup"><span data-stu-id="b151a-138">Specifies the name of an existing VIP to associate with a reserved IP.</span></span>
<span data-ttu-id="b151a-139">Vedere Add-AzureVirtualIP per aggiungere VIP al servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b151a-139">See Add-AzureVirtualIP to add VIPs to your cloud service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b151a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b151a-140">CommonParameters</span></span>
<span data-ttu-id="b151a-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b151a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b151a-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b151a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b151a-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b151a-143">INPUTS</span></span>

## <span data-ttu-id="b151a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b151a-144">OUTPUTS</span></span>

### <span data-ttu-id="b151a-145">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="b151a-145">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="b151a-146">Note</span><span class="sxs-lookup"><span data-stu-id="b151a-146">NOTES</span></span>

## <span data-ttu-id="b151a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b151a-147">RELATED LINKS</span></span>

[<span data-ttu-id="b151a-148">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="b151a-148">Remove-AzureReservedIPAssociation</span></span>](./Remove-AzureReservedIPAssociation.md)


