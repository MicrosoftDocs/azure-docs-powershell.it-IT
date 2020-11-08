---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A6964C80-1991-46FC-84C8-5B00616386BE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e43f841fea77626c18edbda541fa011e95faceb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029598"
---
# <span data-ttu-id="90db2-101">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="90db2-101">Remove-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="90db2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90db2-102">SYNOPSIS</span></span>
<span data-ttu-id="90db2-103">Rimuove l'associazione dall'indirizzo IP riservato al servizio VM o cloud.</span><span class="sxs-lookup"><span data-stu-id="90db2-103">Removes the association from the reserved IP address to the VM or cloud service.</span></span>

## <span data-ttu-id="90db2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90db2-104">SYNTAX</span></span>

```
Remove-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="90db2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90db2-105">DESCRIPTION</span></span>
<span data-ttu-id="90db2-106">Il cmdlet **Remove-AzureReservedIPAssociation** Annulla l'associazione di un indirizzo IP riservato da una macchina virtuale (VM) o da un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="90db2-106">The **Remove-AzureReservedIPAssociation** cmdlet disassociates a reserved IP address from a virtual machine (VM) or Cloud Service.</span></span>
<span data-ttu-id="90db2-107">Al termine dell'operazione, l'indirizzo IP riservato è gratuito e la VM/VIP ottiene un indirizzo IP pubblico dinamico dall'inventario di Azure.</span><span class="sxs-lookup"><span data-stu-id="90db2-107">When the operation completes, the reserved IP address is free and the VM/VIP gets a dynamic public IP Address from the Azure Inventory.</span></span>

## <span data-ttu-id="90db2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90db2-108">EXAMPLES</span></span>

### <span data-ttu-id="90db2-109">Esempio 1: rimuovere un'associazione IP riservata</span><span class="sxs-lookup"><span data-stu-id="90db2-109">Example 1: Remove a reserved IP association</span></span>
```
PS C:\> Remove-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="90db2-110">Questo comando Dissocia l'indirizzo IP riservato denominato ResIp14 dal servizio denominato PipTestWestEurope.</span><span class="sxs-lookup"><span data-stu-id="90db2-110">This command disassociates the reserved IP address named ResIp14 from the service named PipTestWestEurope.</span></span>
<span data-ttu-id="90db2-111">A PipTestWestEurope verrà assegnato un nuovo VIP dinamico.</span><span class="sxs-lookup"><span data-stu-id="90db2-111">PipTestWestEurope will be assigned a new dynamic VIP.</span></span>

## <span data-ttu-id="90db2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90db2-112">PARAMETERS</span></span>

### <span data-ttu-id="90db2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="90db2-113">-Force</span></span>
<span data-ttu-id="90db2-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="90db2-114">Forces the command to run without asking for user confirmation.</span></span>

<span data-ttu-id="90db2-115">Usa questo contrassegno per ignorare i messaggi di avviso durante la rimozione dell'associazione riservata IP.</span><span class="sxs-lookup"><span data-stu-id="90db2-115">Use this flag to bypass warning messages when removing the reserved IP association.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90db2-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="90db2-116">-InformationAction</span></span>
<span data-ttu-id="90db2-117">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="90db2-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="90db2-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="90db2-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="90db2-119">Continuare</span><span class="sxs-lookup"><span data-stu-id="90db2-119">Continue</span></span>
- <span data-ttu-id="90db2-120">Ignora</span><span class="sxs-lookup"><span data-stu-id="90db2-120">Ignore</span></span>
- <span data-ttu-id="90db2-121">Informarsi</span><span class="sxs-lookup"><span data-stu-id="90db2-121">Inquire</span></span>
- <span data-ttu-id="90db2-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="90db2-122">SilentlyContinue</span></span>
- <span data-ttu-id="90db2-123">Stop</span><span class="sxs-lookup"><span data-stu-id="90db2-123">Stop</span></span>
- <span data-ttu-id="90db2-124">Sospensione</span><span class="sxs-lookup"><span data-stu-id="90db2-124">Suspend</span></span>

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

### <span data-ttu-id="90db2-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="90db2-125">-InformationVariable</span></span>
<span data-ttu-id="90db2-126">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="90db2-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="90db2-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="90db2-127">-Profile</span></span>
<span data-ttu-id="90db2-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90db2-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="90db2-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="90db2-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="90db2-130">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="90db2-130">-ReservedIPName</span></span>
<span data-ttu-id="90db2-131">Specifica il nome dell'indirizzo IP riservato.</span><span class="sxs-lookup"><span data-stu-id="90db2-131">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="90db2-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="90db2-132">-ServiceName</span></span>
<span data-ttu-id="90db2-133">Specifica il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="90db2-133">Specifies the  name of the service.</span></span>

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

### <span data-ttu-id="90db2-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="90db2-134">-Slot</span></span>
<span data-ttu-id="90db2-135">Specifica l'ambiente di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="90db2-135">Specifies the deployment environment.</span></span>
<span data-ttu-id="90db2-136">I valori accettabili per questo parametro sono: produzione, staging.</span><span class="sxs-lookup"><span data-stu-id="90db2-136">The acceptable values for this parameter are: Production, Staging.</span></span>

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

### <span data-ttu-id="90db2-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="90db2-137">-VirtualIPName</span></span>
<span data-ttu-id="90db2-138">Specifica un indirizzo IP virtuale da cui rimuovere l'associazione con un servizio o una VM.</span><span class="sxs-lookup"><span data-stu-id="90db2-138">Specifies a virtual IP address from which to remove the association with a service or VM.</span></span>

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

### <span data-ttu-id="90db2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90db2-139">CommonParameters</span></span>
<span data-ttu-id="90db2-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90db2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90db2-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90db2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90db2-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90db2-142">INPUTS</span></span>

## <span data-ttu-id="90db2-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90db2-143">OUTPUTS</span></span>

### <span data-ttu-id="90db2-144">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="90db2-144">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="90db2-145">Note</span><span class="sxs-lookup"><span data-stu-id="90db2-145">NOTES</span></span>

## <span data-ttu-id="90db2-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90db2-146">RELATED LINKS</span></span>

[<span data-ttu-id="90db2-147">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="90db2-147">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


