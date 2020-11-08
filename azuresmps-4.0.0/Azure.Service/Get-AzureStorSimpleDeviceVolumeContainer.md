---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7EF20FC0-3E2A-4AFC-AC02-9B11C8952DB8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22263501f2a79a36c1ace1915ee6898c4833b52b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023521"
---
# <span data-ttu-id="260a9-101">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="260a9-101">Get-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="260a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="260a9-102">SYNOPSIS</span></span>
<span data-ttu-id="260a9-103">Ottiene i contenitori del volume in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="260a9-103">Gets volume containers on a device.</span></span>

## <span data-ttu-id="260a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="260a9-104">SYNTAX</span></span>

```
Get-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> [-VolumeContainerName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="260a9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="260a9-105">DESCRIPTION</span></span>
<span data-ttu-id="260a9-106">Il cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** ottiene un elenco di contenitori di volumi in un dispositivo o un contenitore di volumi con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="260a9-106">The **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet gets a list of volume containers on a device, or volume container that has the specified name.</span></span>
<span data-ttu-id="260a9-107">L'oggetto restituito contiene le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="260a9-107">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="260a9-108">**BandwidthRate**</span><span class="sxs-lookup"><span data-stu-id="260a9-108">**BandwidthRate**</span></span>
- <span data-ttu-id="260a9-109">**EncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="260a9-109">**EncryptionKey**</span></span>
- <span data-ttu-id="260a9-110">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="260a9-110">**InstanceId**</span></span>
- <span data-ttu-id="260a9-111">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="260a9-111">**IsDefault**</span></span>
- <span data-ttu-id="260a9-112">**IsEncryptionEnabled**</span><span class="sxs-lookup"><span data-stu-id="260a9-112">**IsEncryptionEnabled**</span></span>
- <span data-ttu-id="260a9-113">**Nome**</span><span class="sxs-lookup"><span data-stu-id="260a9-113">**Name**</span></span>
- <span data-ttu-id="260a9-114">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="260a9-114">**OperationInProgress**</span></span>
- <span data-ttu-id="260a9-115">**Proprietà**</span><span class="sxs-lookup"><span data-stu-id="260a9-115">**Owned**</span></span>
- <span data-ttu-id="260a9-116">**PrimaryStorageAccountCredential**</span><span class="sxs-lookup"><span data-stu-id="260a9-116">**PrimaryStorageAccountCredential**</span></span>
- <span data-ttu-id="260a9-117">**SecretsEncryptionThumbprint**</span><span class="sxs-lookup"><span data-stu-id="260a9-117">**SecretsEncryptionThumbprint**</span></span>
- <span data-ttu-id="260a9-118">**VolumeCount**</span><span class="sxs-lookup"><span data-stu-id="260a9-118">**VolumeCount**</span></span>

## <span data-ttu-id="260a9-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="260a9-119">EXAMPLES</span></span>

### <span data-ttu-id="260a9-120">Esempio 1: ottenere tutti i contenitori in un dispositivo</span><span class="sxs-lookup"><span data-stu-id="260a9-120">Example 1: Get all the containers on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "8600-Bravo 001"
InstanceId                           Name                                             IsEncryptionEnabled  Owned BandwidthRate                                    PrimaryStorageAccountCredential                 VolumeCount                                    
----------                           ----                                             -------------------  ----- -------------                                    -------------------------------                 -----------                                    
127135b6-92de-4f53-850d-70e1f9a38cbe Test_Container                                   False                True  0                                                Test_Account                                    6
```

<span data-ttu-id="260a9-121">Questo comando consente di ottenere un elenco dei contenitori del volume nel dispositivo denominato 8600-bravo 001.</span><span class="sxs-lookup"><span data-stu-id="260a9-121">This command gets a list of the volume containers on the device named 8600-Bravo 001.</span></span>

### <span data-ttu-id="260a9-122">Esempio 2: ottenere un contenitore usando il relativo nome</span><span class="sxs-lookup"><span data-stu-id="260a9-122">Example 2: Get a container by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08"
VERBOSE: ClientRequestId: 8027c66a-869b-4ea3-97a2-e17d98ec751c_PS
VERBOSE: ClientRequestId: 344f9be5-0887-4d37-98ef-e45c557774f1_PS
VERBOSE: ClientRequestId: 14919be5-d6f5-4f81-b7f1-d7fafff2238c_PS


BandwidthRate                   : 256
EncryptionKey                   : 
InstanceId                      : 04ea9aad-7a56-4a50-b195-86061b0a810a
IsDefault                       : False
IsEncryptionEnabled             : False
Name                            : Container03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 5

VERBOSE: Volume container with name: Container03 is found.
```

<span data-ttu-id="260a9-123">Questo comando consente di ottenere il contenitore del volume denominato Container08 nel dispositivo denominato Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="260a9-123">This command gets the volume container named Container08 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="260a9-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="260a9-124">PARAMETERS</span></span>

### <span data-ttu-id="260a9-125">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="260a9-125">-DeviceName</span></span>
<span data-ttu-id="260a9-126">Specifica il nome di un dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="260a9-126">Specifies the name of a StorSimple device.</span></span>
<span data-ttu-id="260a9-127">Questo cmdlet ottiene i contenitori del volume dal dispositivo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="260a9-127">This cmdlet gets volume containers from the device that this parameter specifies.</span></span>

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

### <span data-ttu-id="260a9-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="260a9-128">-Profile</span></span>
<span data-ttu-id="260a9-129">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="260a9-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="260a9-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="260a9-130">-VolumeContainerName</span></span>
<span data-ttu-id="260a9-131">Specifica il nome del contenitore di volumi da ottenere.</span><span class="sxs-lookup"><span data-stu-id="260a9-131">Specifies the name of the volume container to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260a9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="260a9-132">CommonParameters</span></span>
<span data-ttu-id="260a9-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="260a9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="260a9-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="260a9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="260a9-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="260a9-135">INPUTS</span></span>

### <span data-ttu-id="260a9-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="260a9-136">None</span></span>

## <span data-ttu-id="260a9-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="260a9-137">OUTPUTS</span></span>

### <span data-ttu-id="260a9-138">DataContainer, IList\<DataContainer\></span><span class="sxs-lookup"><span data-stu-id="260a9-138">DataContainer, IList\<DataContainer\></span></span>
<span data-ttu-id="260a9-139">Questo cmdlet restituisce un oggetto **DataContainer** , se specifichi il parametro *VolumeContainerName* .</span><span class="sxs-lookup"><span data-stu-id="260a9-139">This cmdlet returns a **DataContainer** object, if you specify the *VolumeContainerName* parameter.</span></span>
<span data-ttu-id="260a9-140">Se non specifichi questo parametro, questo cmdlet restituisce un oggetto **IList \<DataContainer\>** .</span><span class="sxs-lookup"><span data-stu-id="260a9-140">If you do not specify that parameter, this cmdlet returns an **IList\<DataContainer\>** object.</span></span>

## <span data-ttu-id="260a9-141">Note</span><span class="sxs-lookup"><span data-stu-id="260a9-141">NOTES</span></span>

## <span data-ttu-id="260a9-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="260a9-142">RELATED LINKS</span></span>

[<span data-ttu-id="260a9-143">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="260a9-143">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="260a9-144">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="260a9-144">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)


