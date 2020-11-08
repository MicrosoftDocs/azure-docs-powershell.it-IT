---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BDCD6FD8-F4D5-4897-BF91-C78773DD3546
online version: ''
schema: 2.0.0
ms.openlocfilehash: f414f480328d508f0178d2536d144dceda3baab6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023471"
---
# <span data-ttu-id="7a9d3-101">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7a9d3-101">New-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="7a9d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="7a9d3-103">Aggiunge una credenziale di accesso di Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-103">Adds an Azure storage access credential.</span></span>

## <span data-ttu-id="7a9d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a9d3-104">SYNTAX</span></span>

```
New-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> -StorageAccountKey <String>
 -UseSSL <Boolean> [-Endpoint <String>] [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7a9d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a9d3-105">DESCRIPTION</span></span>
<span data-ttu-id="7a9d3-106">Il cmdlet **New-AzureStorSimpleStorageAccountCredential** aggiunge una credenziale di accesso di Azure storage a StorSimple Manager per l'uso da parte dei cmdlet di StorSimple OneSDK.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-106">The **New-AzureStorSimpleStorageAccountCredential** cmdlet adds an Azure storage access credential to StorSimple manager for use by StorSimple OneSDK cmdlets.</span></span>
<span data-ttu-id="7a9d3-107">La maggior parte dei cmdlet di StorSimple OneSDK tratta le entità che sono legate a un account di archiviazione specifico, ad esempio volumi, contenitori di volumi, backup e criteri di backup.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-107">Most of the StorSimple OneSDK cmdlets deal with entities that are eventually tied to a specific storage account, such as volumes, volume containers, backups, and backup policies.</span></span>
<span data-ttu-id="7a9d3-108">Per alcuni cmdlet, è necessario specificare le credenziali dell'account di archiviazione in uso.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-108">For some cmdlets, you must provide the credentials of the storage account in use.</span></span>
<span data-ttu-id="7a9d3-109">Una credenziale dell'account di archiviazione è un oggetto di Access creato in OneSDK che punta a un account di archiviazione di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-109">A storage account credential is an access object created in OneSDK that points to an existing Azure storage account.</span></span>
<span data-ttu-id="7a9d3-110">Fornisci il nome e il codice di accesso di un account di archiviazione esistente per creare una credenziale dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-110">You provide the name and access key of an existing storage account to create a storage account credential.</span></span>
<span data-ttu-id="7a9d3-111">Puoi quindi usare l'oggetto credenziale con altri cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-111">You can then use that credential object with other cmdlets.</span></span>

<span data-ttu-id="7a9d3-112">Questo cmdlet usa la chiave di registrazione che fornisci quando selezioni la risorsa usando il cmdlet **Select-AzureStorSimpleResource** .</span><span class="sxs-lookup"><span data-stu-id="7a9d3-112">This cmdlet uses the registration key that you provide when you select the resource by using the **Select-AzureStorSimpleResource** cmdlet.</span></span>
<span data-ttu-id="7a9d3-113">Verificare che il valore sia corretto per evitare errori di crittografia.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-113">Be sure that value is correct to avoid encryption failure.</span></span>
<span data-ttu-id="7a9d3-114">Per modificare la chiave di registrazione in un valore corretto, usare **Select-AzureStorSimpleResource**.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-114">To modify the registration key to a correct value, use **Select-AzureStorSimpleResource**.</span></span>

## <span data-ttu-id="7a9d3-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a9d3-115">EXAMPLES</span></span>

### <span data-ttu-id="7a9d3-116">Esempio 1: creare una credenziale</span><span class="sxs-lookup"><span data-stu-id="7a9d3-116">Example 1: Create a credential</span></span>
```
PS C:\>New-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount07" -StorageAccountKey "L/eVcHtvqKjPWm5SaAJXtDlc0d69yVs0ICoZ2XIV1x0r9TqUyQyLUNS8lHvTvRmzdvQhJelav3fYyX7wyAu/SA==" -UseSSL $False -WaitForComplete
VERBOSE: ClientRequestId: f363cda4-54aa-4ee8-a3fa-00651ac86ffb_PS
VERBOSE: Found storage account with name : ContosoAccount07
VERBOSE: Storage credential verification succeeded. 
VERBOSE: ClientRequestId: 716ce6df-62b3-4d48-8e0e-b0c94eec6934_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: 19aa4ef7-2789-4817-980c-19e33d257650_PS

JobId        : 84f74c25-b742-452c-973c-43c7446e9f49
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 72bcdf37-bf06-4dac-adc9-31bb8d06475a_PS
CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : b9986714-cef4-4c3f-a719-7acfc9559320
IsDefault                        : False
Location                         : West Europe
Login                            : ContosoAccount07
Name                             : ContosoAccount07
OperationInProgress              : None

Password                         : G1sBQ6/qAN1gyRGRZVarpi7o6ToJl61sGugfeJ75yx7cwyaGLQHjrSEEwhxThbDJkxso2emAOarTe920Uufy
                                   0AmJ9NpBI5hNyIFfwS4Ff+z2WmfKOzApyeofW5Zy7GPufehe/2ondq0XG4pGt3qxHFXNVUuiaPSU6TVWEKSh
                                   hWDaksSXYMGij3DJdZDW1MA49e6Q7OY+rFujbYvi9P2OjVj8T+FbiMtMB5NnQEqE+t3k74RqPIDKU+d3h9x4
                                   rYbAksGPfMvSa0fUipwYJ+Y5/NABA6j/MfB2pNDJbvqDoa1JCX6SKiwL81wmTh78/KnDY5ST3Said5DzKEbR
                                   iYMQZg==
PasswordEncryptionCertThumbprint : 
UseSSL                           : False
VolumeCount                      : 0
```

<span data-ttu-id="7a9d3-117">Questo comando crea una credenziale di accesso dello spazio di archiviazione per l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-117">This command creates a storage access credential for the specified storage account.</span></span>
<span data-ttu-id="7a9d3-118">Questo comando specifica il parametro *WaitForComplete* e, quindi, il cmdlet attende finché l'attività non viene completata per restituire il controllo alla console.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-118">This command specifies the *WaitForComplete* parameter, and, so, the cmdlet waits until the task finishes to return control to the console.</span></span>

### <span data-ttu-id="7a9d3-119">Esempio 2: creare una credenziale ed eseguire query sullo stato dell'attività</span><span class="sxs-lookup"><span data-stu-id="7a9d3-119">Example 2: Create a credential and query that status of the task</span></span>
```
PS C:\>New-AzureStorSimpleStorageAccountCredential -Name "ContosoAccount08" -Key "6BlMpSVrCQVQy3iOpkxiyY8uk/e3PiHIhadxV4qpPlKInr/eRFrGcWKDrfNC1IHj6oh0If/h3rALdZ0zuaf9cQ==" -UseSSL $True
PS C:\> Get-AzureStorSimpleTask -InstanceId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: 6104a834-ea57-4687-8e0b-1d97dc1c038b_PS
VERBOSE: Found storage account with name : ContosoAccount08
VERBOSE: Storage credential verification succeeded. 
VERBOSE: ClientRequestId: 1f686fa4-5afc-43c3-87b6-f2da7bf9e65f_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: 8acb3770-bd72-43e6-9622-481002ad40b0_PS
53816d8d-a8b5-4c1d-a177-e59007608d6d
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
53816d8d-a8b5-4c1d-a177-e59007608d6d for tracking the task's status
```

<span data-ttu-id="7a9d3-120">Il primo comando crea una credenziale di accesso dello spazio di archiviazione per l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-120">The first command creates a storage access credential for the specified storage account.</span></span>
<span data-ttu-id="7a9d3-121">Il comando restituisce un ID attività.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-121">The command returns a task ID.</span></span>

<span data-ttu-id="7a9d3-122">Il secondo comando esegue una query sullo stato dell'attività usando il cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="7a9d3-122">The second command queries the status of the task by using the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="7a9d3-123">Il comando specifica l'ID attività dal primo comando.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-123">The command specifies the task ID from the first command.</span></span>

### <span data-ttu-id="7a9d3-124">Esempio 3: creare una credenziale da usare con un altro cmdlet</span><span class="sxs-lookup"><span data-stu-id="7a9d3-124">Example 3: Create a credential to use with another cmdlet</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -Name "ContosoAccount09" | New-AzureStorSimpleDeviceVolumeContainer -Name "VC03" -DeviceName "Contoso63-AppVm" -BandWidthRate 256 -EncryptionEnabled $True -EncryptionKey "<your encryption key>" -WaitForComplete
VERBOSE: ClientRequestId: b1d1e637-cd72-4a1e-95a8-4db1d0b921a7_PS
VERBOSE: ClientRequestId: 71f56ca0-1f0b-4655-9331-4849e096345a_PS
VERBOSE: ClientRequestId: fbdd5a96-c95f-4547-9bcd-376d05543348_PS
VERBOSE: Storage Access Credential with name ContosoAccount09 found! 
VERBOSE: ClientRequestId: b44e0363-9979-4e97-aeb1-d9eb4073a337_PS
VERBOSE: ClientRequestId: a6047943-b01e-44e4-a91d-5103aa80ce57_PS
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: ac2dfd8b-922f-4e4d-8c8d-df1e2f87806c_PS


JobId        : 1cf2db5d-624f-46c4-97b9-c36451ba144e
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 9558414b-0883-4cf6-8a02-40efc7edd80d_PS
BandwidthRate                   : 256
EncryptionKey                   : g53NTgCF3SBVZzzk+9yUz5nZopvZpNr3th92ol7WRO7ZUKhodPm7WNjjHEKB0/V+JY6P68tdaF4JxF5jH58e/
                                  mCtTvnPNpOxykYFdY9GKGd9gnf+36sUPqiLFP+ONO5nN/N/zFmOeyuySsaa3gJsZG8eIiFc821yfe9m5QPbF
                                  bx/Qyu8qLl1R1LrKU7k+46IXfwQYSyclztydyuzvFUUic9kaJuR3944VLvrjvxJIbnLrYy7hsn+Gfq7ds9NFq
                                  AUILBH0+bk2uWgUlofAcE8fJ/rzDAHr8nFGWxOTJSrqAo0J3st8BN39+BcrY+zOWsMc/vKfc+Ss5PsGVGDT1r
                                  eQ==
InstanceId                      : 60c34706-ef0c-4c6f-ad90-7249f42648f7
IsDefault                       : False
IsEncryptionEnabled             : True
Name                            : VC03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 0
```

<span data-ttu-id="7a9d3-125">Questo comando crea una credenziale dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-125">This command creates a storage account credential.</span></span>
<span data-ttu-id="7a9d3-126">Il comando passa quindi tale credenziale al cmdlet **New-AzureStorSimpleDeviceVolumeContainer** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-126">The command then passes that credential to the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7a9d3-127">Questo cmdlet crea un nuovo contenitore di volumi usando le credenziali.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-127">That cmdlet creates a new volume container by using the credential.</span></span>

## <span data-ttu-id="7a9d3-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a9d3-128">PARAMETERS</span></span>

### <span data-ttu-id="7a9d3-129">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="7a9d3-129">-Endpoint</span></span>
<span data-ttu-id="7a9d3-130">Specifica l'endpoint di archiviazione di Azure per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-130">Specifies the Azure storage endpoint for the storage account.</span></span>

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

### <span data-ttu-id="7a9d3-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="7a9d3-131">-Profile</span></span>
<span data-ttu-id="7a9d3-132">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-132">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="7a9d3-133">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7a9d3-133">-StorageAccountKey</span></span>
<span data-ttu-id="7a9d3-134">Specifica il codice di accesso dell'account di archiviazione in formato testo normale.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-134">Specifies the access key of the storage account in plain text.</span></span>

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

### <span data-ttu-id="7a9d3-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7a9d3-135">-StorageAccountName</span></span>
<span data-ttu-id="7a9d3-136">Specifica il nome di un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-136">Specifies the name of an existing storage account.</span></span>

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

### <span data-ttu-id="7a9d3-137">-UseSSL</span><span class="sxs-lookup"><span data-stu-id="7a9d3-137">-UseSSL</span></span>
<span data-ttu-id="7a9d3-138">Indica se usare SSL per la connessione quando si usa la nuova credenziale dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-138">Indicates whether to use SSL for the connection when using the new storage account credential.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a9d3-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="7a9d3-139">-WaitForComplete</span></span>
<span data-ttu-id="7a9d3-140">Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-140">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="7a9d3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a9d3-141">CommonParameters</span></span>
<span data-ttu-id="7a9d3-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a9d3-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a9d3-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a9d3-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a9d3-144">INPUTS</span></span>

### <span data-ttu-id="7a9d3-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7a9d3-145">None</span></span>

## <span data-ttu-id="7a9d3-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a9d3-146">OUTPUTS</span></span>

### <span data-ttu-id="7a9d3-147">IEnumerable \<StorageAccountCredentialResponse\> , TaskResponse</span><span class="sxs-lookup"><span data-stu-id="7a9d3-147">IEnumerable\<StorageAccountCredentialResponse\>, TaskResponse</span></span>
<span data-ttu-id="7a9d3-148">Questo cmdlet restituisce un elenco di oggetti **StorageAccountCredentialResponse** , se specifichi il parametro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="7a9d3-148">This cmdlet returns a list of **StorageAccountCredentialResponse** objects, if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="7a9d3-149">Se non specifichi tale parametro, il cmdlet restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="7a9d3-149">If you do not specify that parameter, the cmdlet returns a **TaskResponse** object.</span></span>
<span data-ttu-id="7a9d3-150">Un **StorageAccountCredentialResponse** contiene le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="7a9d3-150">A **StorageAccountCredentialResponse** contains the following properties:</span></span> 

- <span data-ttu-id="7a9d3-151">**CloudType** ( **CloudType** )</span><span class="sxs-lookup"><span data-stu-id="7a9d3-151">**CloudType** ( **CloudType** )</span></span>
- <span data-ttu-id="7a9d3-152">**Hostname** ( **stringa** )</span><span class="sxs-lookup"><span data-stu-id="7a9d3-152">**Hostname** ( **String** )</span></span>
- <span data-ttu-id="7a9d3-153">**InstanceID** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="7a9d3-153">**InstanceId** ( **String** )</span></span>
- <span data-ttu-id="7a9d3-154">**IsDefault** ( **booleano** )</span><span class="sxs-lookup"><span data-stu-id="7a9d3-154">**IsDefault** ( **Boolean** )</span></span>
- <span data-ttu-id="7a9d3-155">**Location** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="7a9d3-155">**Location** ( **String** )</span></span>
- <span data-ttu-id="7a9d3-156">**Login** ( **stringa** )</span><span class="sxs-lookup"><span data-stu-id="7a9d3-156">**Login** ( **String** )</span></span>
- <span data-ttu-id="7a9d3-157">**Nome** ( **stringa** )</span><span class="sxs-lookup"><span data-stu-id="7a9d3-157">**Name** ( **String** )</span></span>
- <span data-ttu-id="7a9d3-158">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="7a9d3-158">**OperationInProgress** ( **OperationInProgress** )</span></span>
- <span data-ttu-id="7a9d3-159">**Password** ( **stringa** )</span><span class="sxs-lookup"><span data-stu-id="7a9d3-159">**Password** ( **String** )</span></span>
- <span data-ttu-id="7a9d3-160">**PasswordEncryptionCertThumbprint** ( **stringa** )</span><span class="sxs-lookup"><span data-stu-id="7a9d3-160">**PasswordEncryptionCertThumbprint** ( **String** )</span></span>
- <span data-ttu-id="7a9d3-161">**UseSSL** ( **booleano** )</span><span class="sxs-lookup"><span data-stu-id="7a9d3-161">**UseSSL** ( **Boolean** )</span></span>
- <span data-ttu-id="7a9d3-162">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="7a9d3-162">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="7a9d3-163">Note</span><span class="sxs-lookup"><span data-stu-id="7a9d3-163">NOTES</span></span>

## <span data-ttu-id="7a9d3-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a9d3-164">RELATED LINKS</span></span>

[<span data-ttu-id="7a9d3-165">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7a9d3-165">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="7a9d3-166">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7a9d3-166">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="7a9d3-167">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7a9d3-167">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="7a9d3-168">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="7a9d3-168">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="7a9d3-169">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="7a9d3-169">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


