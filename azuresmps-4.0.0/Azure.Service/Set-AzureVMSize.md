---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 437889D1-F24F-4BBE-8C56-7C3E48CEA517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86dd38ce7fa55507be3362c1494b88df491a1067
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023749"
---
# <span data-ttu-id="c9adf-101">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="c9adf-101">Set-AzureVMSize</span></span>

## <span data-ttu-id="c9adf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9adf-102">SYNOPSIS</span></span>
<span data-ttu-id="c9adf-103">Imposta le dimensioni di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9adf-103">Sets the size of an Azure virtual machine.</span></span>

## <span data-ttu-id="c9adf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9adf-104">SYNTAX</span></span>

```
Set-AzureVMSize [-InstanceSize] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c9adf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9adf-105">DESCRIPTION</span></span>
<span data-ttu-id="c9adf-106">Il cmdlet **set-AzureVMSize** aggiorna le dimensioni di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c9adf-106">The **Set-AzureVMSize** cmdlet updates the size of a virtual machine.</span></span>
<span data-ttu-id="c9adf-107">Ha due parametri: *InstanceSize* , che è la nuova dimensione della macchina virtuale e *VM* , un oggetto macchina virtuale recuperato usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="c9adf-107">It has two parameters: *InstanceSize* , which is the new size of the virtual machine, and *VM* , which is a virtual machine object retrieved by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="c9adf-108">Il risultato di **set-AzureVMSize** può essere inviato tramite pipe al cmdlet **Update-AzureVM** o archiviato in una variabile per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="c9adf-108">The result of **Set-AzureVMSize** can be piped to the **Update-AzureVM** cmdlet or stored in a variable for later use.</span></span>
<span data-ttu-id="c9adf-109">Non viene eseguita alcuna modifica effettiva finché non viene eseguito **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="c9adf-109">No actual change is made until **Update-AzureVM** is executed.</span></span>

<span data-ttu-id="c9adf-110">Nota: questo cmdlet richiede che la macchina virtuale venga revisionata e potrebbe ottenere un nuovo indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="c9adf-110">Note: This cmdlet will require the virtual machine to be re-provisioned and it might get a new IP address.</span></span>

## <span data-ttu-id="c9adf-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9adf-111">EXAMPLES</span></span>

### <span data-ttu-id="c9adf-112">Esempio 1: impostare le dimensioni di una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="c9adf-112">Example 1: Set the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MySvc1" -Name "MyVM3" | Set-AzureVMSize "Small" | Update-AzureVM
```

<span data-ttu-id="c9adf-113">Questo comando aggiorna una macchina virtuale in dimensioni "piccole".</span><span class="sxs-lookup"><span data-stu-id="c9adf-113">This command updates a virtual machine to size "Small".</span></span>

## <span data-ttu-id="c9adf-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9adf-114">PARAMETERS</span></span>

### <span data-ttu-id="c9adf-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c9adf-115">-InformationAction</span></span>
<span data-ttu-id="c9adf-116">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c9adf-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c9adf-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9adf-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9adf-118">Continuare</span><span class="sxs-lookup"><span data-stu-id="c9adf-118">Continue</span></span>
- <span data-ttu-id="c9adf-119">Ignora</span><span class="sxs-lookup"><span data-stu-id="c9adf-119">Ignore</span></span>
- <span data-ttu-id="c9adf-120">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c9adf-120">Inquire</span></span>
- <span data-ttu-id="c9adf-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c9adf-121">SilentlyContinue</span></span>
- <span data-ttu-id="c9adf-122">Stop</span><span class="sxs-lookup"><span data-stu-id="c9adf-122">Stop</span></span>
- <span data-ttu-id="c9adf-123">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c9adf-123">Suspend</span></span>

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

### <span data-ttu-id="c9adf-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c9adf-124">-InformationVariable</span></span>
<span data-ttu-id="c9adf-125">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c9adf-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c9adf-126">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="c9adf-126">-InstanceSize</span></span>
<span data-ttu-id="c9adf-127">Specifica le dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c9adf-127">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="c9adf-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9adf-128">The acceptable values for this parameter are:</span></span>

<span data-ttu-id="c9adf-129">--Piccolo--medio--grande---------------------------a6</span><span class="sxs-lookup"><span data-stu-id="c9adf-129">--ExtraSmall --Small --Medium --Large --ExtraLarge --A5 --A6 --A7</span></span>

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

### <span data-ttu-id="c9adf-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="c9adf-130">-Profile</span></span>
<span data-ttu-id="c9adf-131">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9adf-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c9adf-132">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c9adf-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c9adf-133">-VM</span><span class="sxs-lookup"><span data-stu-id="c9adf-133">-VM</span></span>
<span data-ttu-id="c9adf-134">Specifica l'oggetto macchina virtuale persistente a cui questo cmdlet imposta le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="c9adf-134">Specifies the persistent virtual machine object that this cmdlet sets the size of.</span></span>

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

### <span data-ttu-id="c9adf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9adf-135">CommonParameters</span></span>
<span data-ttu-id="c9adf-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9adf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9adf-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9adf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9adf-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9adf-138">INPUTS</span></span>

## <span data-ttu-id="c9adf-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9adf-139">OUTPUTS</span></span>

## <span data-ttu-id="c9adf-140">Note</span><span class="sxs-lookup"><span data-stu-id="c9adf-140">NOTES</span></span>

## <span data-ttu-id="c9adf-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9adf-141">RELATED LINKS</span></span>

[<span data-ttu-id="c9adf-142">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c9adf-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="c9adf-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c9adf-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


