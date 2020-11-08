---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5605F11E-EEA0-4C32-8445-2E001D56BC47
online version: ''
schema: 2.0.0
ms.openlocfilehash: e364692858cf190b48b61f4d38fbf483d229ffb7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023478"
---
# <span data-ttu-id="e821f-101">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="e821f-101">New-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="e821f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e821f-102">SYNOPSIS</span></span>
<span data-ttu-id="e821f-103">Crea un contenitore di volumi.</span><span class="sxs-lookup"><span data-stu-id="e821f-103">Creates a volume container.</span></span>

## <span data-ttu-id="e821f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e821f-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainerName <String>
 -PrimaryStorageAccountCredential <StorageAccountCredentialResponse> -BandWidthRateInMbps <Int32>
 [-EncryptionEnabled <Boolean>] [-EncryptionKey <String>] [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e821f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e821f-105">DESCRIPTION</span></span>
<span data-ttu-id="e821f-106">Il cmdlet **New-AzureStorSimpleDeviceVolumeContainer** crea un contenitore di volumi.</span><span class="sxs-lookup"><span data-stu-id="e821f-106">The **New-AzureStorSimpleDeviceVolumeContainer** cmdlet creates a volume container.</span></span>
<span data-ttu-id="e821f-107">È necessario associare una credenziale dell'account di archiviazione al nuovo contenitore di volumi.</span><span class="sxs-lookup"><span data-stu-id="e821f-107">You must associate a storage account credential with the new volume container.</span></span>
<span data-ttu-id="e821f-108">Per ottenere una credenziale dell'account di archiviazione, usare il cmdlet **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="e821f-108">To obtain a storage account credential, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

## <span data-ttu-id="e821f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e821f-109">EXAMPLES</span></span>

### <span data-ttu-id="e821f-110">Esempio 1: creare un contenitore</span><span class="sxs-lookup"><span data-stu-id="e821f-110">Example 1: Create a container</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount" | New-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" -BandWidthRateInMbps 256
VERBOSE: ClientRequestId: 96a4ccd4-f2a9-4820-8bc8-e6b7b56dce0d_PS
VERBOSE: ClientRequestId: 90be20db-098a-4f2b-a6da-9da6f533a846_PS
VERBOSE: ClientRequestId: 410fd33a-8fa3-4ae5-a1bf-1b6da9b34ffc_PS
VERBOSE: Storage Access Credential with name ContosoAccount found! 
VERBOSE: ClientRequestId: 0a6d1008-ba1f-43b2-a424-9c86be2fb83b_PS
VERBOSE: ClientRequestId: 08f0d657-a130-4a25-8090-270c58b479dc_PS
VERBOSE: ClientRequestId: 0f3e894a-b031-467c-a258-41b74c89cf18_PS
5b192120-9df0-40ed-b75e-b4e728bd37ef
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
5b192120-9df0-40ed-b75e-b4e728bd37ef for tracking the task's status
```

<span data-ttu-id="e821f-111">Questo comando ottiene le credenziali dell'account di archiviazione per l'account denominato ContosoAccount usando il cmdlet **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="e821f-111">This command gets the storage account credential for the account named ContosoAccount by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>
<span data-ttu-id="e821f-112">Il comando passa le credenziali al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="e821f-112">The command passes the credential to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e821f-113">Questo cmdlet usa le credenziali di tale cmdlet per creare il contenitore denominato Container08 nel dispositivo denominato Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="e821f-113">This cmdlet uses the credential from that cmdlet to create the container named Container08 on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="e821f-114">Questo comando avvia il processo e quindi restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="e821f-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="e821f-115">Per visualizzare lo stato del processo, usare il cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="e821f-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="e821f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e821f-116">PARAMETERS</span></span>

### <span data-ttu-id="e821f-117">-BandWidthRateInMbps</span><span class="sxs-lookup"><span data-stu-id="e821f-117">-BandWidthRateInMbps</span></span>
<span data-ttu-id="e821f-118">Specifica la frequenza della larghezza di banda in megabit al secondo (Mbps).</span><span class="sxs-lookup"><span data-stu-id="e821f-118">Specifies the bandwidth rate in megabits per second (Mbps).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CloudBandwidthInMbps

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e821f-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e821f-119">-DeviceName</span></span>
<span data-ttu-id="e821f-120">Specifica il nome del dispositivo StorSimple in cui creare il contenitore del volume.</span><span class="sxs-lookup"><span data-stu-id="e821f-120">Specifies the name of the StorSimple device on which to create the volume container.</span></span>

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

### <span data-ttu-id="e821f-121">-EncryptionEnabled</span><span class="sxs-lookup"><span data-stu-id="e821f-121">-EncryptionEnabled</span></span>
<span data-ttu-id="e821f-122">Indica se abilitare la crittografia.</span><span class="sxs-lookup"><span data-stu-id="e821f-122">Indicates whether to enable encryption.</span></span>

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

### <span data-ttu-id="e821f-123">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e821f-123">-EncryptionKey</span></span>
<span data-ttu-id="e821f-124">Specifica la chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e821f-124">Specifies the encryption key.</span></span>

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

### <span data-ttu-id="e821f-125">-PrimaryStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e821f-125">-PrimaryStorageAccountCredential</span></span>
<span data-ttu-id="e821f-126">Specifica le credenziali, come oggetto **StorageAccountCredential** , da associare al nuovo contenitore di volumi.</span><span class="sxs-lookup"><span data-stu-id="e821f-126">Specifies the credential, as a **StorageAccountCredential** object, to associate with the new volume container.</span></span>
<span data-ttu-id="e821f-127">Per ottenere un oggetto **StorageAccountCredential** , usa il cmdlet **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="e821f-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: (All)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e821f-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="e821f-128">-Profile</span></span>
<span data-ttu-id="e821f-129">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="e821f-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="e821f-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="e821f-130">-VolumeContainerName</span></span>
<span data-ttu-id="e821f-131">Specifica il nome del contenitore di volumi da creare.</span><span class="sxs-lookup"><span data-stu-id="e821f-131">Specifies the name of the volume container to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e821f-132">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="e821f-132">-WaitForComplete</span></span>
<span data-ttu-id="e821f-133">Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e821f-133">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="e821f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e821f-134">CommonParameters</span></span>
<span data-ttu-id="e821f-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e821f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e821f-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e821f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e821f-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e821f-137">INPUTS</span></span>

### <span data-ttu-id="e821f-138">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e821f-138">StorageAccountCredential</span></span>
<span data-ttu-id="e821f-139">Questo cmdlet accetta un oggetto **PrimaryStorageAccountCredential** da associare al contenitore del volume.</span><span class="sxs-lookup"><span data-stu-id="e821f-139">This cmdlet accepts a **PrimaryStorageAccountCredential** object to associate with the volume container.</span></span>

## <span data-ttu-id="e821f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e821f-140">OUTPUTS</span></span>

### <span data-ttu-id="e821f-141">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="e821f-141">TaskStatusInfo</span></span>
<span data-ttu-id="e821f-142">Questo cmdlet restituisce un oggetto **TaskStatusInfo** , se specifichi il parametro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="e821f-142">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="e821f-143">Note</span><span class="sxs-lookup"><span data-stu-id="e821f-143">NOTES</span></span>

## <span data-ttu-id="e821f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e821f-144">RELATED LINKS</span></span>

[<span data-ttu-id="e821f-145">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="e821f-145">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="e821f-146">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="e821f-146">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="e821f-147">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e821f-147">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="e821f-148">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="e821f-148">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


