---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9C22F5D7-1FD0-4699-83D7-1D72C5234DEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d09173c43de9c01056055f714217db5eb4c58225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023951"
---
# <span data-ttu-id="e451b-101">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="e451b-101">New-AzureReservedIP</span></span>

## <span data-ttu-id="e451b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e451b-102">SYNOPSIS</span></span>
<span data-ttu-id="e451b-103">Crea un indirizzo IP riservato.</span><span class="sxs-lookup"><span data-stu-id="e451b-103">Creates a reserved IP address.</span></span>

## <span data-ttu-id="e451b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e451b-104">SYNTAX</span></span>

### <span data-ttu-id="e451b-105">CreateNewReservedIP (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e451b-105">CreateNewReservedIP (Default)</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e451b-106">CreateInUseReservedIPUsingSlot</span><span class="sxs-lookup"><span data-stu-id="e451b-106">CreateInUseReservedIPUsingSlot</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e451b-107">CreateInUseReservedIP</span><span class="sxs-lookup"><span data-stu-id="e451b-107">CreateInUseReservedIP</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e451b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e451b-108">DESCRIPTION</span></span>
<span data-ttu-id="e451b-109">Il cmdlet **New-AzureReservedIP** crea un indirizzo IP riservato.</span><span class="sxs-lookup"><span data-stu-id="e451b-109">The **New-AzureReservedIP** cmdlet creates a reserved IP address.</span></span>

## <span data-ttu-id="e451b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e451b-110">EXAMPLES</span></span>

### <span data-ttu-id="e451b-111">Esempio 1: creare un nuovo IP riservato</span><span class="sxs-lookup"><span data-stu-id="e451b-111">Example 1: Create a new reserved IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName $Name -Label $Label -Location $Location
```

<span data-ttu-id="e451b-112">Questo comando crea un nuovo indirizzo IP riservato nell'abbonamento, che può essere usato per creare servizi cloud che includono computer Web, Worker e Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="e451b-112">This command creates a new reserved IP address in the subscription, which can be used for creating cloud services that include Web, Worker, and Virtual Machines.</span></span>

### <span data-ttu-id="e451b-113">Esempio 2: creare un IP riservato basato su un IP esistente</span><span class="sxs-lookup"><span data-stu-id="e451b-113">Example 2: Create a reserved IP based on an existing IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName resip14 -Location "West Europe" -ServiceName piptestwesteurope
```

<span data-ttu-id="e451b-114">Questo comando crea un VIP esistente (IP virtuale) nel servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="e451b-114">This command creates an existing VIP (Virtual IP) on the specified service.</span></span>

## <span data-ttu-id="e451b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e451b-115">PARAMETERS</span></span>

### <span data-ttu-id="e451b-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e451b-116">-InformationAction</span></span>
<span data-ttu-id="e451b-117">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="e451b-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e451b-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e451b-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e451b-119">Continuare</span><span class="sxs-lookup"><span data-stu-id="e451b-119">Continue</span></span>
- <span data-ttu-id="e451b-120">Ignora</span><span class="sxs-lookup"><span data-stu-id="e451b-120">Ignore</span></span>
- <span data-ttu-id="e451b-121">Informarsi</span><span class="sxs-lookup"><span data-stu-id="e451b-121">Inquire</span></span>
- <span data-ttu-id="e451b-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e451b-122">SilentlyContinue</span></span>
- <span data-ttu-id="e451b-123">Stop</span><span class="sxs-lookup"><span data-stu-id="e451b-123">Stop</span></span>
- <span data-ttu-id="e451b-124">Sospensione</span><span class="sxs-lookup"><span data-stu-id="e451b-124">Suspend</span></span>

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

### <span data-ttu-id="e451b-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e451b-125">-InformationVariable</span></span>
<span data-ttu-id="e451b-126">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="e451b-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e451b-127">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="e451b-127">-Label</span></span>
<span data-ttu-id="e451b-128">Specifica un'etichetta per l'indirizzo IP riservato.</span><span class="sxs-lookup"><span data-stu-id="e451b-128">Specifies a label for the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e451b-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e451b-129">-Location</span></span>
<span data-ttu-id="e451b-130">Specifica una posizione in cui creare l'indirizzo IP riservato.</span><span class="sxs-lookup"><span data-stu-id="e451b-130">Specifies a location at which to create the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e451b-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="e451b-131">-Profile</span></span>
<span data-ttu-id="e451b-132">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e451b-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e451b-133">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e451b-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e451b-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="e451b-134">-ReservedIPName</span></span>
<span data-ttu-id="e451b-135">Specifica il nome dell'indirizzo IP riservato.</span><span class="sxs-lookup"><span data-stu-id="e451b-135">Specifies the reserved IP address name.</span></span>

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

### <span data-ttu-id="e451b-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e451b-136">-ServiceName</span></span>
<span data-ttu-id="e451b-137">Specifica un nome di servizio.</span><span class="sxs-lookup"><span data-stu-id="e451b-137">Specifies a service name.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e451b-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="e451b-138">-Slot</span></span>
<span data-ttu-id="e451b-139">Specifica lo slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="e451b-139">Specifies the deployment slot.</span></span>
<span data-ttu-id="e451b-140">I valori accettabili per questo parametro sono: staging, Production.</span><span class="sxs-lookup"><span data-stu-id="e451b-140">The acceptable values for this parameter are: Staging, Production.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e451b-141">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="e451b-141">-VirtualIPName</span></span>
<span data-ttu-id="e451b-142">Specifica che questo cmdlet usa il parametro **VirtualIPName** per prenotare un indirizzo IP virtuale (VIP) esistente nella distribuzione.</span><span class="sxs-lookup"><span data-stu-id="e451b-142">Specifies that this cmdlet uses the **VirtualIPName** parameter to reserve an existing virtual IP address (VIP) in your deployment.</span></span>
<span data-ttu-id="e451b-143">Se questo parametro non viene specificato, questo cmdlet riserva un nuovo VIP.</span><span class="sxs-lookup"><span data-stu-id="e451b-143">If this parameter is not specified, this cmdlet reserves a new VIP.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e451b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e451b-144">CommonParameters</span></span>
<span data-ttu-id="e451b-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e451b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e451b-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e451b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e451b-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e451b-147">INPUTS</span></span>

## <span data-ttu-id="e451b-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e451b-148">OUTPUTS</span></span>

## <span data-ttu-id="e451b-149">Note</span><span class="sxs-lookup"><span data-stu-id="e451b-149">NOTES</span></span>

## <span data-ttu-id="e451b-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e451b-150">RELATED LINKS</span></span>

[<span data-ttu-id="e451b-151">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="e451b-151">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="e451b-152">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="e451b-152">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


