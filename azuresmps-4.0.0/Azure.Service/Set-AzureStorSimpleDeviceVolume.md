---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 39E9BB88-6AD8-4B05-9498-35393E22BA30
online version: ''
schema: 2.0.0
ms.openlocfilehash: 234b1f7fa2719cc1b34e6bcd0b8e8fd340acc4af
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029880"
---
# <span data-ttu-id="7501c-101">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="7501c-101">Set-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="7501c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7501c-102">SYNOPSIS</span></span>
<span data-ttu-id="7501c-103">Aggiorna le proprietà di un volume esistente.</span><span class="sxs-lookup"><span data-stu-id="7501c-103">Updates the properties of an existing volume.</span></span>

## <span data-ttu-id="7501c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7501c-104">SYNTAX</span></span>

### <span data-ttu-id="7501c-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="7501c-105">IdentifyByName</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7501c-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="7501c-106">IdentifyByObject</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7501c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7501c-107">DESCRIPTION</span></span>
<span data-ttu-id="7501c-108">Il cmdlet **set-AzureStorSimpleDeviceVolume** aggiorna le proprietà di un volume esistente.</span><span class="sxs-lookup"><span data-stu-id="7501c-108">The **Set-AzureStorSimpleDeviceVolume** cmdlet updates the properties of an existing volume.</span></span>
<span data-ttu-id="7501c-109">Questo cmdlet associa un volume a uno o più record di controllo di Access.</span><span class="sxs-lookup"><span data-stu-id="7501c-109">This cmdlet associates a volume with one or more access control records.</span></span>
<span data-ttu-id="7501c-110">Per ottenere oggetti **AccessControlRecord** , usa il cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="7501c-110">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="7501c-111">Aggiornare le dimensioni o il tipo per il volume.</span><span class="sxs-lookup"><span data-stu-id="7501c-111">Update the size or type for the volume.</span></span>
<span data-ttu-id="7501c-112">Aggiornare inoltre se creare il volume online.</span><span class="sxs-lookup"><span data-stu-id="7501c-112">Also, update whether to create the volume online.</span></span>

## <span data-ttu-id="7501c-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7501c-113">EXAMPLES</span></span>

### <span data-ttu-id="7501c-114">Esempio 1: aggiornare il valore online per un volume</span><span class="sxs-lookup"><span data-stu-id="7501c-114">Example 1: Update online value for a volume</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $False
VERBOSE: ClientRequestId: f2869570-ea47-4be7-801e-9c0f22f2600d_PS
VERBOSE: ClientRequestId: c70bb86a-51d3-4390-be17-4d0847641dc3_PS
VERBOSE: ClientRequestId: d20cb5b2-6b3c-4e06-af99-cada28c5e50a_PS
VERBOSE: ClientRequestId: ab6d533e-b55b-4cfb-9c58-9153295e0547_PS
de7000f1-29c7-4102-a375-b52432f9e67e
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
de7000f1-29c7-4102-a375-b52432f9e67e for tracking the task's status
```

<span data-ttu-id="7501c-115">Questo comando Aggiorna il volume denominato Volume18 per avere un valore online di $False.</span><span class="sxs-lookup"><span data-stu-id="7501c-115">This command updates the volume named Volume18 to have an online value of $False.</span></span>
<span data-ttu-id="7501c-116">Questo comando avvia l'attività e quindi restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="7501c-116">This command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="7501c-117">Per visualizzare lo stato dell'attività, usa il cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="7501c-117">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="7501c-118">Esempio 2: modificare il valore e il tipo online</span><span class="sxs-lookup"><span data-stu-id="7501c-118">Example 2: Modify online value and type</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $True -VolumeAppType ArchiveVolume 
VERBOSE: ClientRequestId: af42b02a-645e-4801-a2d7-4197511c68cf_PS
VERBOSE: ClientRequestId: 7cb4f3b4-548e-42dc-a38c-0df0911c5206_PS
VERBOSE: ClientRequestId: 7cc706ad-a58f-4939-8e78-cabae8379a51_PS
VERBOSE: ClientRequestId: 6bed21d5-12fc-4a12-a89c-120bdb5636b1_PS
aa977225-af78-4c93-b754-72704afc928f
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
aa977225-af78-4c93-b754-72704afc928f for tracking the task's status
```

<span data-ttu-id="7501c-119">Questo comando Aggiorna il volume denominato Volume18.</span><span class="sxs-lookup"><span data-stu-id="7501c-119">This command updates the volume named Volume18.</span></span>
<span data-ttu-id="7501c-120">Modifica il tipo e modifica il valore del parametro *online* in $true.</span><span class="sxs-lookup"><span data-stu-id="7501c-120">It modifies the type and changes the value of the *Online* parameter to $True.</span></span>

## <span data-ttu-id="7501c-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7501c-121">PARAMETERS</span></span>

### <span data-ttu-id="7501c-122">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="7501c-122">-AccessControlRecords</span></span>
<span data-ttu-id="7501c-123">Specifica un elenco di record di controllo di Access da associare al volume.</span><span class="sxs-lookup"><span data-stu-id="7501c-123">Specifies a list of access control records to associate with the volume.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7501c-124">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7501c-124">-DeviceName</span></span>
<span data-ttu-id="7501c-125">Specifica il nome del dispositivo StorSimple in cui aggiornare il volume.</span><span class="sxs-lookup"><span data-stu-id="7501c-125">Specifies the name of the StorSimple device on which to update the volume exists.</span></span>

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

### <span data-ttu-id="7501c-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7501c-126">-InformationAction</span></span>
<span data-ttu-id="7501c-127">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="7501c-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7501c-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7501c-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7501c-129">Continuare</span><span class="sxs-lookup"><span data-stu-id="7501c-129">Continue</span></span>
- <span data-ttu-id="7501c-130">Ignora</span><span class="sxs-lookup"><span data-stu-id="7501c-130">Ignore</span></span>
- <span data-ttu-id="7501c-131">Informarsi</span><span class="sxs-lookup"><span data-stu-id="7501c-131">Inquire</span></span>
- <span data-ttu-id="7501c-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7501c-132">SilentlyContinue</span></span>
- <span data-ttu-id="7501c-133">Stop</span><span class="sxs-lookup"><span data-stu-id="7501c-133">Stop</span></span>
- <span data-ttu-id="7501c-134">Sospensione</span><span class="sxs-lookup"><span data-stu-id="7501c-134">Suspend</span></span>

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

### <span data-ttu-id="7501c-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7501c-135">-InformationVariable</span></span>
<span data-ttu-id="7501c-136">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="7501c-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7501c-137">-NewName</span><span class="sxs-lookup"><span data-stu-id="7501c-137">-NewName</span></span>
<span data-ttu-id="7501c-138">Specifica un nuovo nome per il dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="7501c-138">Specifies a new name for the StorSimple device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7501c-139">-Online</span><span class="sxs-lookup"><span data-stu-id="7501c-139">-Online</span></span>
<span data-ttu-id="7501c-140">Specifica se il volume è online.</span><span class="sxs-lookup"><span data-stu-id="7501c-140">Specifies whether the volume is online.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7501c-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="7501c-141">-Profile</span></span>
<span data-ttu-id="7501c-142">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="7501c-142">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="7501c-143">-Volume</span><span class="sxs-lookup"><span data-stu-id="7501c-143">-Volume</span></span>
<span data-ttu-id="7501c-144">Specifica il nome del volume da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="7501c-144">Specifies the name of the volume to update.</span></span>

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

### <span data-ttu-id="7501c-145">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="7501c-145">-VolumeAppType</span></span>
<span data-ttu-id="7501c-146">Specifica se aggiornare il volume per essere un volume principale o di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7501c-146">Specifies whether to update the volume to be a primary or archive volume.</span></span>
<span data-ttu-id="7501c-147">I valori validi sono: PrimaryVolume e ArchiveVolume.</span><span class="sxs-lookup"><span data-stu-id="7501c-147">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7501c-148">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="7501c-148">-VolumeName</span></span>
<span data-ttu-id="7501c-149">Specifica il nome del volume da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="7501c-149">Specifies the name of the volume to update.</span></span>

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

### <span data-ttu-id="7501c-150">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="7501c-150">-VolumeSizeInBytes</span></span>
<span data-ttu-id="7501c-151">Specifica la dimensione aggiornata, in byte, per il volume.</span><span class="sxs-lookup"><span data-stu-id="7501c-151">Specifies the updated size, in bytes, for the volume.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7501c-152">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="7501c-152">-WaitForComplete</span></span>
<span data-ttu-id="7501c-153">Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7501c-153">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="7501c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7501c-154">CommonParameters</span></span>
<span data-ttu-id="7501c-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7501c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7501c-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7501c-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7501c-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7501c-157">INPUTS</span></span>

### <span data-ttu-id="7501c-158">Elenco\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="7501c-158">List\<AccessControlRecord\></span></span>
<span data-ttu-id="7501c-159">Questo cmdlet accetta un elenco di oggetti **AccessControlRecord** da associare a un volume.</span><span class="sxs-lookup"><span data-stu-id="7501c-159">This cmdlet accepts a list of **AccessControlRecord** objects to associate to a volume.</span></span>

## <span data-ttu-id="7501c-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7501c-160">OUTPUTS</span></span>

### <span data-ttu-id="7501c-161">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="7501c-161">TaskStatusInfo</span></span>
<span data-ttu-id="7501c-162">Questo cmdlet restituisce un oggetto **TaskStatusInfo** , se specifichi il parametro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="7501c-162">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="7501c-163">Note</span><span class="sxs-lookup"><span data-stu-id="7501c-163">NOTES</span></span>

## <span data-ttu-id="7501c-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7501c-164">RELATED LINKS</span></span>

[<span data-ttu-id="7501c-165">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="7501c-165">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="7501c-166">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="7501c-166">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="7501c-167">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="7501c-167">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="7501c-168">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="7501c-168">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="7501c-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="7501c-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


