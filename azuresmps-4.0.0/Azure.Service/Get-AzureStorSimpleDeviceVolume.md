---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 79EE846E-D5BE-4808-BC6F-E3B16A308AB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9d0cd7ef0eacc7ff3e38c4619b60a0bd61f24f1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023524"
---
# <span data-ttu-id="7e850-101">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="7e850-101">Get-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="7e850-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e850-102">SYNOPSIS</span></span>
<span data-ttu-id="7e850-103">Ottiene i volumi in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e850-103">Gets volumes on a device.</span></span>

## <span data-ttu-id="7e850-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e850-104">SYNTAX</span></span>

### <span data-ttu-id="7e850-105">IdentifyByParentObject</span><span class="sxs-lookup"><span data-stu-id="7e850-105">IdentifyByParentObject</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7e850-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="7e850-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e850-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e850-107">DESCRIPTION</span></span>
<span data-ttu-id="7e850-108">Il cmdlet **Get-AzureStorSimpleDeviceVolume** ottiene un elenco di volumi per un contenitore di volumi specificato o un volume con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="7e850-108">The **Get-AzureStorSimpleDeviceVolume** cmdlet gets a list of volumes for a specified volume container, or volume that has the specified name.</span></span>
<span data-ttu-id="7e850-109">L'oggetto restituito contiene le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="7e850-109">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="7e850-110">**AccessType**</span><span class="sxs-lookup"><span data-stu-id="7e850-110">**AccessType**</span></span>
- <span data-ttu-id="7e850-111">**AcrList**</span><span class="sxs-lookup"><span data-stu-id="7e850-111">**AcrList**</span></span>
- <span data-ttu-id="7e850-112">**AppType**</span><span class="sxs-lookup"><span data-stu-id="7e850-112">**AppType**</span></span>
- <span data-ttu-id="7e850-113">**DataContainer**</span><span class="sxs-lookup"><span data-stu-id="7e850-113">**DataContainer**</span></span>
- <span data-ttu-id="7e850-114">**DataContainerId**</span><span class="sxs-lookup"><span data-stu-id="7e850-114">**DataContainerId**</span></span>
- <span data-ttu-id="7e850-115">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="7e850-115">**InstanceId**</span></span>
- <span data-ttu-id="7e850-116">**IsBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="7e850-116">**IsBackupEnabled**</span></span>
- <span data-ttu-id="7e850-117">**IsDefaultBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="7e850-117">**IsDefaultBackupEnabled**</span></span>
- <span data-ttu-id="7e850-118">**IsMonitoringEnabled**</span><span class="sxs-lookup"><span data-stu-id="7e850-118">**IsMonitoringEnabled**</span></span>
- <span data-ttu-id="7e850-119">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7e850-119">**Name**</span></span>
- <span data-ttu-id="7e850-120">**Online**</span><span class="sxs-lookup"><span data-stu-id="7e850-120">**Online**</span></span>
- <span data-ttu-id="7e850-121">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="7e850-121">**OperationInProgress**</span></span>
- <span data-ttu-id="7e850-122">**SizeInBytes**</span><span class="sxs-lookup"><span data-stu-id="7e850-122">**SizeInBytes**</span></span>
- <span data-ttu-id="7e850-123">**VSN**</span><span class="sxs-lookup"><span data-stu-id="7e850-123">**VSN**</span></span>

## <span data-ttu-id="7e850-124">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e850-124">EXAMPLES</span></span>

### <span data-ttu-id="7e850-125">Esempio 1: ottenere volumi in un contenitore specificato</span><span class="sxs-lookup"><span data-stu-id="7e850-125">Example 1: Get volumes in a specified container</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container03" | Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
InstanceId             : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c
Name                   : Volume 1 Clone
Online                 : True
SizeInBytes            : 3298534883328
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c

InstanceId             : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe
Name                   : Volume 3 Clone
Online                 : True
SizeInBytes            : 1717986918400
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe

InstanceId             : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
Name                   : Volume 4
Online                 : True
SizeInBytes            : 1610612736000
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
```

<span data-ttu-id="7e850-126">Questo comando ottiene il contenitore del volume denominato Container03 nel dispositivo denominato Contoso63-AppVm usando il cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="7e850-126">This command gets the volume container named Container03 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="7e850-127">Il comando usa l'operatore pipeline per passare tale contenitore al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="7e850-127">The command uses the pipeline operator to pass that container to the current cmdlet.</span></span>
<span data-ttu-id="7e850-128">Questo cmdlet recupera tutti i volumi in tale contenitore per il dispositivo denominato Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="7e850-128">That cmdlet gets all the volumes in that container for the device named Contoso63-AppVm.</span></span>

### <span data-ttu-id="7e850-129">Esempio 2: ottenere un volume usando il relativo nome</span><span class="sxs-lookup"><span data-stu-id="7e850-129">Example 2: Get a volume by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18"
InstanceId             : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
Name                   : Volume18
Online                 : True
SizeInBytes            : 2748779069440
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
```

<span data-ttu-id="7e850-130">Questo comando ottiene il volume denominato Volume18 nel dispositivo denominato Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="7e850-130">This command gets the volume named Volume18 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="7e850-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e850-131">PARAMETERS</span></span>

### <span data-ttu-id="7e850-132">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7e850-132">-DeviceName</span></span>
<span data-ttu-id="7e850-133">Specifica il nome del dispositivo StorSimple da cui ottenere volumi.</span><span class="sxs-lookup"><span data-stu-id="7e850-133">Specifies the name of the StorSimple device from which to get volumes.</span></span>

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

### <span data-ttu-id="7e850-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="7e850-134">-Profile</span></span>
<span data-ttu-id="7e850-135">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="7e850-135">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="7e850-136">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="7e850-136">-VolumeContainer</span></span>
<span data-ttu-id="7e850-137">Specifica il contenitore del volume, come oggetto **DataContainer** , che include i volumi da ottenere.</span><span class="sxs-lookup"><span data-stu-id="7e850-137">Specifies the volume container, as a **DataContainer** object, that includes the volumes to get.</span></span>
<span data-ttu-id="7e850-138">Per ottenere un **DataContainer** , usare il cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="7e850-138">To obtain a **DataContainer** , use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: IdentifyByParentObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e850-139">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="7e850-139">-VolumeName</span></span>
<span data-ttu-id="7e850-140">Specifica il nome del volume da ottenere.</span><span class="sxs-lookup"><span data-stu-id="7e850-140">Specifies the name of the volume to get.</span></span>

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

### <span data-ttu-id="7e850-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e850-141">CommonParameters</span></span>
<span data-ttu-id="7e850-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e850-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e850-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e850-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e850-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e850-144">INPUTS</span></span>

### <span data-ttu-id="7e850-145">DataContainer</span><span class="sxs-lookup"><span data-stu-id="7e850-145">DataContainer</span></span>
<span data-ttu-id="7e850-146">Questo cmdlet accetta un oggetto **DataContainer** che contiene il volume da ottenere.</span><span class="sxs-lookup"><span data-stu-id="7e850-146">This cmdlet accepts a **DataContainer** object that contains the volume to get.</span></span>

## <span data-ttu-id="7e850-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e850-147">OUTPUTS</span></span>

### <span data-ttu-id="7e850-148">VirtualDisk, IList\<VirtualDisk\></span><span class="sxs-lookup"><span data-stu-id="7e850-148">VirtualDisk, IList\<VirtualDisk\></span></span>
<span data-ttu-id="7e850-149">Questo cmdlet restituisce un oggetto **VirtualDisk** se specifichi il parametro *VolumeName* .</span><span class="sxs-lookup"><span data-stu-id="7e850-149">This cmdlet returns a **VirtualDisk** object if you specify the *VolumeName* parameter.</span></span>
<span data-ttu-id="7e850-150">Se specifichi *VolumeContainer* , questo cmdlet restituisce un oggetto **IList \<VirtualDisk\>** .</span><span class="sxs-lookup"><span data-stu-id="7e850-150">If you specify the *VolumeContainer* , this cmdlet returns an **IList\<VirtualDisk\>** object.</span></span>

## <span data-ttu-id="7e850-151">Note</span><span class="sxs-lookup"><span data-stu-id="7e850-151">NOTES</span></span>

## <span data-ttu-id="7e850-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e850-152">RELATED LINKS</span></span>

[<span data-ttu-id="7e850-153">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="7e850-153">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="7e850-154">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="7e850-154">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="7e850-155">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="7e850-155">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="7e850-156">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="7e850-156">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


