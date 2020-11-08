---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C60F78AE-3803-4D9F-A4F3-EAA42052C0E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a0708ca37cdb2b700772da2fe9cb684b8b29a30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023729"
---
# <span data-ttu-id="f4358-101">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f4358-101">Start-AzureVM</span></span>

## <span data-ttu-id="f4358-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4358-102">SYNOPSIS</span></span>
<span data-ttu-id="f4358-103">Avvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4358-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="f4358-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4358-104">SYNTAX</span></span>

### <span data-ttu-id="f4358-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4358-105">ByName (Default)</span></span>
```
Start-AzureVM [-Name] <String[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f4358-106">Input</span><span class="sxs-lookup"><span data-stu-id="f4358-106">Input</span></span>
```
Start-AzureVM -VM <IPersistentVM[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f4358-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4358-107">DESCRIPTION</span></span>
<span data-ttu-id="f4358-108">Il cmdlet **Start-AzureVM** richiede l'inizio di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4358-108">The **Start-AzureVM** cmdlet requests the start of an Azure virtual machine.</span></span>

## <span data-ttu-id="f4358-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4358-109">EXAMPLES</span></span>

### <span data-ttu-id="f4358-110">Esempio 1: avviare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="f4358-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04"
```

<span data-ttu-id="f4358-111">Questo comando avvia la macchina virtuale denominata VirtualMachine04 che viene eseguita nel servizio Azure denominato ContosoService03.</span><span class="sxs-lookup"><span data-stu-id="f4358-111">This command starts the virtual machine named VirtualMachine04 that runs in the Azure service named ContosoService03.</span></span>

### <span data-ttu-id="f4358-112">Esempio 2: avviare una macchina virtuale usando un oggetto macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="f4358-112">Example 2: Start a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "DatabaseServer" | Start-AzureVM
```

<span data-ttu-id="f4358-113">Questo comando Recupera l'oggetto macchina virtuale per la macchina virtuale il cui nome è DatabaseServer e quindi le richieste per avviarlo.</span><span class="sxs-lookup"><span data-stu-id="f4358-113">This command retrieves the virtual machine object for the virtual machine whose name is DatabaseServer, and then requests to start it.</span></span>

## <span data-ttu-id="f4358-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4358-114">PARAMETERS</span></span>

### <span data-ttu-id="f4358-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f4358-115">-InformationAction</span></span>
<span data-ttu-id="f4358-116">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="f4358-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f4358-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4358-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f4358-118">Continuare</span><span class="sxs-lookup"><span data-stu-id="f4358-118">Continue</span></span>
- <span data-ttu-id="f4358-119">Ignora</span><span class="sxs-lookup"><span data-stu-id="f4358-119">Ignore</span></span>
- <span data-ttu-id="f4358-120">Informarsi</span><span class="sxs-lookup"><span data-stu-id="f4358-120">Inquire</span></span>
- <span data-ttu-id="f4358-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f4358-121">SilentlyContinue</span></span>
- <span data-ttu-id="f4358-122">Stop</span><span class="sxs-lookup"><span data-stu-id="f4358-122">Stop</span></span>
- <span data-ttu-id="f4358-123">Sospensione</span><span class="sxs-lookup"><span data-stu-id="f4358-123">Suspend</span></span>

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

### <span data-ttu-id="f4358-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f4358-124">-InformationVariable</span></span>
<span data-ttu-id="f4358-125">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="f4358-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f4358-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4358-126">-Name</span></span>
<span data-ttu-id="f4358-127">Specifica il nome della macchina virtuale da avviare.</span><span class="sxs-lookup"><span data-stu-id="f4358-127">Specifies the name of the virtual machine to start.</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4358-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="f4358-128">-Profile</span></span>
<span data-ttu-id="f4358-129">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4358-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f4358-130">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f4358-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f4358-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f4358-131">-ServiceName</span></span>
<span data-ttu-id="f4358-132">Specifica il nome del servizio Azure che contiene la macchina virtuale da avviare.</span><span class="sxs-lookup"><span data-stu-id="f4358-132">Specifies the name of the Azure service that contains the virtual machine to start.</span></span>

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

### <span data-ttu-id="f4358-133">-VM</span><span class="sxs-lookup"><span data-stu-id="f4358-133">-VM</span></span>
<span data-ttu-id="f4358-134">Specifica un oggetto macchina virtuale che identifica la macchina virtuale da avviare.</span><span class="sxs-lookup"><span data-stu-id="f4358-134">Specifies a virtual machine object that identifies the virtual machine to start.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4358-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4358-135">CommonParameters</span></span>
<span data-ttu-id="f4358-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4358-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4358-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4358-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4358-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4358-138">INPUTS</span></span>

## <span data-ttu-id="f4358-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4358-139">OUTPUTS</span></span>

## <span data-ttu-id="f4358-140">Note</span><span class="sxs-lookup"><span data-stu-id="f4358-140">NOTES</span></span>

## <span data-ttu-id="f4358-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4358-141">RELATED LINKS</span></span>

[<span data-ttu-id="f4358-142">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f4358-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="f4358-143">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f4358-143">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="f4358-144">Riavviare-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f4358-144">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="f4358-145">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f4358-145">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="f4358-146">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f4358-146">Update-AzureVM</span></span>](./Update-AzureVM.md)


