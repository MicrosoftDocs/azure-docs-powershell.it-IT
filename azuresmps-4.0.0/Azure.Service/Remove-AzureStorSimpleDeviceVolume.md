---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A62D1A9D-C0EF-4305-B1F9-3AE68A79222D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a5023abffae6bbc2b70b7400e604ffabb1d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029922"
---
# <span data-ttu-id="df6df-101">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="df6df-101">Remove-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="df6df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df6df-102">SYNOPSIS</span></span>
<span data-ttu-id="df6df-103">Rimuove un volume da un dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="df6df-103">Removes a volume from a StorSimple device.</span></span>

## <span data-ttu-id="df6df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df6df-104">SYNTAX</span></span>

### <span data-ttu-id="df6df-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="df6df-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="df6df-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="df6df-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="df6df-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df6df-107">DESCRIPTION</span></span>
<span data-ttu-id="df6df-108">Il cmdlet **Remove-AzureStorSimpleDeviceVolume** rimuove un volume da un dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="df6df-108">The **Remove-AzureStorSimpleDeviceVolume** cmdlet removes a volume from a StorSimple device.</span></span>
<span data-ttu-id="df6df-109">Questo cmdlet richiede la conferma a meno che non specifichi il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="df6df-109">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="df6df-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df6df-110">EXAMPLES</span></span>

### <span data-ttu-id="df6df-111">Esempio 1: rimuovere un volume usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="df6df-111">Example 1: Remove a volume by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" | Remove-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: 2933e24d-9564-42b5-9053-5f0bc4f59ea8_PS
VERBOSE: ClientRequestId: 7c2d854b-537a-4253-bb0c-c15bc8aa2b49_PS
VERBOSE: ClientRequestId: 4bf749ac-517c-49e7-8027-a8f62e272014_PS
VERBOSE: ClientRequestId: 7d9ec87a-616d-4ca9-bfb8-158859174d59_PS

Confirm
Are you sure you want to remove the volume? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 67a38e28-a015-44b1-8159-c1a6604f4d81_PS
VERBOSE: About to run a job to remove your volume! 
VERBOSE: ClientRequestId: 56101c10-07ca-40f4-8f19-c6fdd895e3a5_PS
32925451-4451-4478-89f7-d8930505d3fb
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
32925451-4451-4478-89f7-d8930505d3fb for tracking the task's status
VERBOSE: Volume with name: Volume18 is found.
```

<span data-ttu-id="df6df-112">Questo comando ottiene il volume denominato Volume18 nel dispositivo denominato Contoso63-AppVm e quindi passa tale volume al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="df6df-112">This command gets the volume named Volume18 on the device named Contoso63-AppVm, and then passes that volume to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="df6df-113">Il cmdlet corrente avvia l'attività che rimuove il volume e quindi restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="df6df-113">The current cmdlet starts the task that removes the volume, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="df6df-114">Per visualizzare lo stato dell'attività, usa il cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="df6df-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="df6df-115">Il comando non specifica il parametro *Force* , quindi il cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="df6df-115">The command does not specify the *Force* parameter, so the cmdlet prompts you for confirmation.</span></span>

### <span data-ttu-id="df6df-116">Esempio 2: rimuovere un volume senza conferma</span><span class="sxs-lookup"><span data-stu-id="df6df-116">Example 2: Remove a volume without confirmation</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Force
VERBOSE: ClientRequestId: 72f13290-41eb-4ac4-9535-da1a42d0fa0b_PS
VERBOSE: ClientRequestId: ae0c1d99-1a66-4a69-9260-f2c8c12546bd_PS
VERBOSE: ClientRequestId: 9610744f-d031-488f-87e6-3ecddb305e13_PS
VERBOSE: About to run a job to remove your volume! 
VERBOSE: ClientRequestId: d33525d8-7276-4d2a-942d-d10f8078f1f7_PS
483f8cb4-ebc3-46a9-a9e6-0989e25738a0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
483f8cb4-ebc3-46a9-a9e6-0989e25738a0 for tracking the task's status
```

<span data-ttu-id="df6df-117">Questo comando rimuove il volume denominato Volume18 dal dispositivo denominato Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="df6df-117">This command removes the volume named Volume18 from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="df6df-118">Il comando specifica il parametro *Force* , quindi il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="df6df-118">The command specifies the *Force* parameter, so the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="df6df-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df6df-119">PARAMETERS</span></span>

### <span data-ttu-id="df6df-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="df6df-120">-DeviceName</span></span>
<span data-ttu-id="df6df-121">Specifica il nome del dispositivo StorSimple in cui il volume da rimuovere esiste.</span><span class="sxs-lookup"><span data-stu-id="df6df-121">Specifies the name of the StorSimple device on which to the volume to remove exists.</span></span>

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

### <span data-ttu-id="df6df-122">-Force</span><span class="sxs-lookup"><span data-stu-id="df6df-122">-Force</span></span>
<span data-ttu-id="df6df-123">Indica che questo cmdlet non richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="df6df-123">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6df-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="df6df-124">-Profile</span></span>
<span data-ttu-id="df6df-125">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="df6df-125">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="df6df-126">-Volume</span><span class="sxs-lookup"><span data-stu-id="df6df-126">-Volume</span></span>
<span data-ttu-id="df6df-127">Specifica il volume da rimuovere, come oggetto **VirtualDisk** .</span><span class="sxs-lookup"><span data-stu-id="df6df-127">Specifies the volume to remove, as a **VirtualDisk** object.</span></span>
<span data-ttu-id="df6df-128">Per ottenere un oggetto **VirtualDisk** , usa il cmdlet **Get-AzureStorSimpleDeviceVolume** .</span><span class="sxs-lookup"><span data-stu-id="df6df-128">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolume** cmdlet.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df6df-129">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="df6df-129">-VolumeName</span></span>
<span data-ttu-id="df6df-130">Specifica il nome del volume da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="df6df-130">Specifies the name of the volume to remove.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6df-131">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="df6df-131">-WaitForComplete</span></span>
<span data-ttu-id="df6df-132">Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="df6df-132">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6df-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df6df-133">CommonParameters</span></span>
<span data-ttu-id="df6df-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df6df-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df6df-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df6df-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df6df-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df6df-136">INPUTS</span></span>

### <span data-ttu-id="df6df-137">VirtualDisk</span><span class="sxs-lookup"><span data-stu-id="df6df-137">VirtualDisk</span></span>
<span data-ttu-id="df6df-138">Questo cmdlet accetta l'oggetto **VirtualDisk** da eliminare o il nome del volume di **VirtualDisk** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="df6df-138">This cmdlet accepts either the **VirtualDisk** object to delete or the volume name of the **VirtualDisk** to delete.</span></span>

## <span data-ttu-id="df6df-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df6df-139">OUTPUTS</span></span>

### <span data-ttu-id="df6df-140">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="df6df-140">TaskStatusInfo</span></span>
<span data-ttu-id="df6df-141">Questo cmdlet restituisce un oggetto **TaskStatusInfo** , se specifichi il parametro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="df6df-141">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="df6df-142">Note</span><span class="sxs-lookup"><span data-stu-id="df6df-142">NOTES</span></span>

## <span data-ttu-id="df6df-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df6df-143">RELATED LINKS</span></span>

[<span data-ttu-id="df6df-144">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="df6df-144">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="df6df-145">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="df6df-145">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="df6df-146">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="df6df-146">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="df6df-147">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="df6df-147">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


