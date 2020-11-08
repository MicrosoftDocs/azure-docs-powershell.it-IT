---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E0590AD4-F67B-48EF-8657-8890A2204CB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 607cd288bcc9c86209a3ae0af569e964205f5cb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029529"
---
# <span data-ttu-id="23d91-101">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="23d91-101">Set-AzureAvailabilitySet</span></span>

## <span data-ttu-id="23d91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23d91-102">SYNOPSIS</span></span>
<span data-ttu-id="23d91-103">Imposta il nome del set di disponibilità in una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="23d91-103">Sets the name of the availability set on an Azure virtual machine.</span></span>

## <span data-ttu-id="23d91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23d91-104">SYNTAX</span></span>

```
Set-AzureAvailabilitySet [-AvailabilitySetName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="23d91-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23d91-105">DESCRIPTION</span></span>
<span data-ttu-id="23d91-106">Il cmdlet **set-AzureAvailabilitySet** imposta il nome del set di disponibilità in una macchina virtuale di Azure dopo la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="23d91-106">The **Set-AzureAvailabilitySet** cmdlet sets the name of the availability set on an Azure virtual machine after deployment.</span></span>

## <span data-ttu-id="23d91-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23d91-107">EXAMPLES</span></span>

### <span data-ttu-id="23d91-108">Esempio 1: modificare il nome di un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="23d91-108">Example 1: Modify the name of an availability set</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine24" | Set-AzureAvailabilitySet -AvailabilitySetName "AvailabilitySet14" | Update-AzureVM
```

<span data-ttu-id="23d91-109">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 nel servizio denominato ContosoService usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="23d91-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="23d91-110">Il comando passa l'oggetto al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="23d91-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="23d91-111">Questo cmdlet modifica il nome del set di disponibilità per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="23d91-111">That cmdlet modifies the name of the availability set for that virtual machine.</span></span>
<span data-ttu-id="23d91-112">Il comando Aggiorna la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="23d91-112">The command updates the virtual machine.</span></span>

## <span data-ttu-id="23d91-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23d91-113">PARAMETERS</span></span>

### <span data-ttu-id="23d91-114">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="23d91-114">-AvailabilitySetName</span></span>
<span data-ttu-id="23d91-115">Specifica il nome del set di disponibilità a cui appartiene la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="23d91-115">Specifies the name of the availability set to which the virtual machine belongs.</span></span>

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

### <span data-ttu-id="23d91-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="23d91-116">-InformationAction</span></span>
<span data-ttu-id="23d91-117">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="23d91-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="23d91-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="23d91-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23d91-119">Continuare</span><span class="sxs-lookup"><span data-stu-id="23d91-119">Continue</span></span>
- <span data-ttu-id="23d91-120">Ignora</span><span class="sxs-lookup"><span data-stu-id="23d91-120">Ignore</span></span>
- <span data-ttu-id="23d91-121">Informarsi</span><span class="sxs-lookup"><span data-stu-id="23d91-121">Inquire</span></span>
- <span data-ttu-id="23d91-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="23d91-122">SilentlyContinue</span></span>
- <span data-ttu-id="23d91-123">Stop</span><span class="sxs-lookup"><span data-stu-id="23d91-123">Stop</span></span>
- <span data-ttu-id="23d91-124">Sospensione</span><span class="sxs-lookup"><span data-stu-id="23d91-124">Suspend</span></span>

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

### <span data-ttu-id="23d91-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="23d91-125">-InformationVariable</span></span>
<span data-ttu-id="23d91-126">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="23d91-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="23d91-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="23d91-127">-Profile</span></span>
<span data-ttu-id="23d91-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23d91-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="23d91-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="23d91-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23d91-130">-VM</span><span class="sxs-lookup"><span data-stu-id="23d91-130">-VM</span></span>
<span data-ttu-id="23d91-131">Specifica la configurazione della macchina virtuale che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="23d91-131">Specifies the virtual machine configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="23d91-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d91-132">CommonParameters</span></span>
<span data-ttu-id="23d91-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23d91-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d91-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23d91-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d91-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23d91-135">INPUTS</span></span>

## <span data-ttu-id="23d91-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23d91-136">OUTPUTS</span></span>

## <span data-ttu-id="23d91-137">Note</span><span class="sxs-lookup"><span data-stu-id="23d91-137">NOTES</span></span>

## <span data-ttu-id="23d91-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23d91-138">RELATED LINKS</span></span>

[<span data-ttu-id="23d91-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="23d91-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="23d91-140">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="23d91-140">Remove-AzureAvailabilitySet</span></span>](./Remove-AzureAvailabilitySet.md)


