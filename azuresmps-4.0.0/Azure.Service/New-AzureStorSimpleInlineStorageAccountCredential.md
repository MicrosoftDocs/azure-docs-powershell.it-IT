---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BC68C60C-86E3-4857-95AE-1A915A841F7D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 803bc4006e5be8582183248c22115fcd51862d13
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023475"
---
# <span data-ttu-id="f9430-101">New-AzureStorSimpleInlineStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="f9430-101">New-AzureStorSimpleInlineStorageAccountCredential</span></span>

## <span data-ttu-id="f9430-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9430-102">SYNOPSIS</span></span>
<span data-ttu-id="f9430-103">Crea una credenziale dell'account di archiviazione inline.</span><span class="sxs-lookup"><span data-stu-id="f9430-103">Creates an inline storage account credential.</span></span>

## <span data-ttu-id="f9430-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9430-104">SYNTAX</span></span>

```
New-AzureStorSimpleInlineStorageAccountCredential -StorageAccountName <String> -StorageAccountKey <String>
 [-Endpoint <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f9430-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9430-105">DESCRIPTION</span></span>
<span data-ttu-id="f9430-106">Il cmdlet **New-AzureStorSimpleInlineStorageAccountCredential** crea un oggetto credenziale dell'account di archiviazione di Azure inline.</span><span class="sxs-lookup"><span data-stu-id="f9430-106">The **New-AzureStorSimpleInlineStorageAccountCredential** cmdlet creates an inline Azure storage account credential object.</span></span>
<span data-ttu-id="f9430-107">Questo cmdlet crea un oggetto credenziali fittizio.</span><span class="sxs-lookup"><span data-stu-id="f9430-107">This cmdlet creates a dummy credential object.</span></span>
<span data-ttu-id="f9430-108">Puoi usare il cmdlet **New-AzureStorSimpleDeviceVolumeContainer** e il cmdlet Current nello stesso comando usando la pipeline di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f9430-108">You can use the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet and the current cmdlet in the same command by using the Windows PowerShell pipeline.</span></span>
<span data-ttu-id="f9430-109">L'oggetto credenziale dell'account di archiviazione effettivo viene creato come parte della creazione del contenitore del volume.</span><span class="sxs-lookup"><span data-stu-id="f9430-109">The actual storage account credential object is created as part of creation of the volume container.</span></span>

## <span data-ttu-id="f9430-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9430-110">EXAMPLES</span></span>

### <span data-ttu-id="f9430-111">Esempio 1: creare una credenziale dell'account di archiviazione in linea</span><span class="sxs-lookup"><span data-stu-id="f9430-111">Example 1: Create a storage account credential inline</span></span>
```
PS C:\>New-AzureStorSimpleInlineStorageAccountCredential -Name "contoso76" -Key x6o/tpZh8Coo8Tteo0NHLksTOKr/P9Vufo0LZNGdPGVTSUu00/p6ta1w9gRbVBNjzN8aa504kH2zkEsfUme+kw== | New-AzureStorSimpleDeviceVolumeContainer -Name "VolumeContainer_06" -DeviceName Contoso_App3 -BandWidthRate 256 -EncryptionEnabled $True -EncryptionKey "Key22" -WaitForComplete
VERBOSE: ClientRequestId: 535d24d5-1ed8-4759-92b2-dd492f94e23e_PS
VERBOSE: ClientRequestId: f32fc069-96c9-4fd9-a71a-0e62d81f25d8_PS
VERBOSE: ClientRequestId: 4376a931-89f5-448f-92bd-b2f7234244c9_PS
VERBOSE: ClientRequestId: 980109d4-7d76-40d0-ae3c-db539e2cb486_PS
VERBOSE: Encryption in progress... 
VERBOSE: Creating StorageAccountCredential inline
VERBOSE: Found storage account with name : contoso76
VERBOSE: Storage credential verification succeeded. 
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: d4f8a5de-bf81-4773-b6e6-edb034284cf4_PS


JobId        : 2dec64d3-b30d-4d35-adb3-12689b235b79
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: abd4082a-2eda-42ad-8cb3-5864dd2f7d1f_PS
BandwidthRate                   : 256
EncryptionKey                   : SK23I39L7GvoLce7u63TMT/A/V/TW8JXe+PoXKEKzwsr3t/h7tdqV1EpfaK0DGO/qo5b2PLCagFHAxnZEiejg
                                  jtF9TcyK+aLyzEnkqtM+eNRJmgANzJ9C/5L6Ubp+eSWiy+U/pyZygxPrb37e0yFg+qbHV9R9Qi+afBpHD9Gsi
                                  rhURuOc/idWG29eaEifuRzn/zEjvwJ2pEyYLcsuL+ftfRYZom69XO+cRDv5yT3xdNI/dAod/5YUaf1IhJl8wR
                                  cWjqyr00NxlCI03hTgH2sFyTFZWc07S2KI5K5n3rmCL6vGT76SRgNFeUxGz3v06/VoBhdmv9vDfrEz5UkW04d
                                  Qw==
InstanceId                      : a72bf4bb-0f0a-4ec2-a8b1-c4548825f522
IsDefault                       : False
IsEncryptionEnabled             : True
Name                            : VolumneContainer_06
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 0
```

<span data-ttu-id="f9430-112">Questo comando crea una credenziale dell'account di archiviazione in linea e la passa al cmdlet **New-AzureStorSimpleDeviceVolumeContainer** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="f9430-112">This command creates a storage account credential inline, and then passes it to the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f9430-113">Questo contenitore usa le credenziali fittizie per creare un contenitore di volumi.</span><span class="sxs-lookup"><span data-stu-id="f9430-113">That container uses the dummy credential to create a volume container.</span></span>

## <span data-ttu-id="f9430-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9430-114">PARAMETERS</span></span>

### <span data-ttu-id="f9430-115">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="f9430-115">-Endpoint</span></span>
<span data-ttu-id="f9430-116">Specifica l'endpoint di archiviazione di Azure per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f9430-116">Specifies the Azure storage endpoint for the storage account.</span></span>

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

### <span data-ttu-id="f9430-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="f9430-117">-Profile</span></span>
<span data-ttu-id="f9430-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9430-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f9430-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f9430-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f9430-120">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f9430-120">-StorageAccountKey</span></span>
<span data-ttu-id="f9430-121">Specifica la chiave dell'account di archiviazione in formato testo normale.</span><span class="sxs-lookup"><span data-stu-id="f9430-121">Specifies the account key of the storage account in plain text.</span></span>
<span data-ttu-id="f9430-122">La chiave viene trasferita in formato crittografato.</span><span class="sxs-lookup"><span data-stu-id="f9430-122">The key is transferred in encrypted format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9430-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f9430-123">-StorageAccountName</span></span>
<span data-ttu-id="f9430-124">Specifica il nome di un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="f9430-124">Specifies the name of an existing storage account.</span></span>

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

### <span data-ttu-id="f9430-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9430-125">CommonParameters</span></span>
<span data-ttu-id="f9430-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9430-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9430-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9430-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9430-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9430-128">INPUTS</span></span>

### <span data-ttu-id="f9430-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f9430-129">None</span></span>

## <span data-ttu-id="f9430-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9430-130">OUTPUTS</span></span>

### <span data-ttu-id="f9430-131">StorageAccountCredentialResponse</span><span class="sxs-lookup"><span data-stu-id="f9430-131">StorageAccountCredentialResponse</span></span>
<span data-ttu-id="f9430-132">Questo cmdlet restituisce un oggetto **CloudType** , che contiene i campi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f9430-132">This cmdlet returns a **CloudType** object, which contains the following fields:</span></span> 

- <span data-ttu-id="f9430-133">**Hostname**.</span><span class="sxs-lookup"><span data-stu-id="f9430-133">**Hostname**.</span></span>
<span data-ttu-id="f9430-134">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="f9430-134">**String**.</span></span> 
- <span data-ttu-id="f9430-135">**InstanceID**.</span><span class="sxs-lookup"><span data-stu-id="f9430-135">**InstanceId**.</span></span>
<span data-ttu-id="f9430-136">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="f9430-136">**String**.</span></span> 
- <span data-ttu-id="f9430-137">**Impostazione predefinita**.</span><span class="sxs-lookup"><span data-stu-id="f9430-137">**IsDefault**.</span></span>
<span data-ttu-id="f9430-138">**Valore booleano**.</span><span class="sxs-lookup"><span data-stu-id="f9430-138">**Boolean**.</span></span> 
- <span data-ttu-id="f9430-139">**Posizione**.</span><span class="sxs-lookup"><span data-stu-id="f9430-139">**Location**.</span></span>
<span data-ttu-id="f9430-140">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="f9430-140">**String**.</span></span> 
- <span data-ttu-id="f9430-141">**Login**.</span><span class="sxs-lookup"><span data-stu-id="f9430-141">**Login**.</span></span>
<span data-ttu-id="f9430-142">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="f9430-142">**String**.</span></span> 
- <span data-ttu-id="f9430-143">**Nome**.</span><span class="sxs-lookup"><span data-stu-id="f9430-143">**Name**.</span></span>
<span data-ttu-id="f9430-144">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="f9430-144">**String**.</span></span> 
- <span data-ttu-id="f9430-145">**OperationInProgress**.</span><span class="sxs-lookup"><span data-stu-id="f9430-145">**OperationInProgress**.</span></span>
<span data-ttu-id="f9430-146">**OperationInProgress**.</span><span class="sxs-lookup"><span data-stu-id="f9430-146">**OperationInProgress**.</span></span> 
- <span data-ttu-id="f9430-147">**Password**.</span><span class="sxs-lookup"><span data-stu-id="f9430-147">**Password**.</span></span>
<span data-ttu-id="f9430-148">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="f9430-148">**String**.</span></span> 
- <span data-ttu-id="f9430-149">**PasswordEncryptionCertThumbprint**.</span><span class="sxs-lookup"><span data-stu-id="f9430-149">**PasswordEncryptionCertThumbprint**.</span></span>
<span data-ttu-id="f9430-150">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="f9430-150">**String**.</span></span> 
- <span data-ttu-id="f9430-151">**UseSSL**.</span><span class="sxs-lookup"><span data-stu-id="f9430-151">**UseSSL**.</span></span>
<span data-ttu-id="f9430-152">**Valore booleano**.</span><span class="sxs-lookup"><span data-stu-id="f9430-152">**Boolean**.</span></span> 
- <span data-ttu-id="f9430-153">**VolumeCount**.</span><span class="sxs-lookup"><span data-stu-id="f9430-153">**VolumeCount**.</span></span>
<span data-ttu-id="f9430-154">**Numero intero**.</span><span class="sxs-lookup"><span data-stu-id="f9430-154">**Integer**.</span></span>

## <span data-ttu-id="f9430-155">Note</span><span class="sxs-lookup"><span data-stu-id="f9430-155">NOTES</span></span>

## <span data-ttu-id="f9430-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9430-156">RELATED LINKS</span></span>

[<span data-ttu-id="f9430-157">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="f9430-157">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="f9430-158">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="f9430-158">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


