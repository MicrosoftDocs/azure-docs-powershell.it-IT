---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 17efee05b4d10ce87d327d8b7de26063bfc0cac5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685542"
---
# <span data-ttu-id="28dbd-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="28dbd-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="28dbd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="28dbd-103">Genera un token SAS per un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="28dbd-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28dbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28dbd-104">SYNTAX</span></span>

### <span data-ttu-id="28dbd-105">BlobNameWithPermission (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="28dbd-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="28dbd-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="28dbd-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="28dbd-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="28dbd-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="28dbd-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="28dbd-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="28dbd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28dbd-109">DESCRIPTION</span></span>
<span data-ttu-id="28dbd-110">Il cmdlet **New-AzureStorageBlobSASToken** genera un token SAS (Shared Access Signature) per un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="28dbd-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="28dbd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28dbd-111">EXAMPLES</span></span>

### <span data-ttu-id="28dbd-112">Esempio 1: generare un token SAS BLOB con l'autorizzazione BLOB completo</span><span class="sxs-lookup"><span data-stu-id="28dbd-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="28dbd-113">Questo esempio genera un token SAS BLOB con l'autorizzazione BLOB completo.</span><span class="sxs-lookup"><span data-stu-id="28dbd-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="28dbd-114">Esempio 2: generare un token SAS BLOB con durata</span><span class="sxs-lookup"><span data-stu-id="28dbd-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="28dbd-115">Questo esempio genera un token SAS BLOB con la durata.</span><span class="sxs-lookup"><span data-stu-id="28dbd-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="28dbd-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28dbd-116">PARAMETERS</span></span>

### <span data-ttu-id="28dbd-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="28dbd-117">-Blob</span></span>
<span data-ttu-id="28dbd-118">Specifica il nome BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="28dbd-118">Specifies the storage blob name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28dbd-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="28dbd-119">-CloudBlob</span></span>
<span data-ttu-id="28dbd-120">Specifica l'oggetto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="28dbd-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="28dbd-121">Per ottenere un oggetto **CloudBlob** , usa il cmdlet [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="28dbd-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28dbd-122">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="28dbd-122">-Container</span></span>
<span data-ttu-id="28dbd-123">Specifica il nome del contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="28dbd-123">Specifies the storage container name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28dbd-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="28dbd-124">-Context</span></span>
<span data-ttu-id="28dbd-125">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="28dbd-125">Specifies the storage context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28dbd-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="28dbd-126">-ExpiryTime</span></span>
<span data-ttu-id="28dbd-127">Specifica quando scade la firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="28dbd-127">Specifies when the shared access signature expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28dbd-128">-FullUri</span><span class="sxs-lookup"><span data-stu-id="28dbd-128">-FullUri</span></span>
<span data-ttu-id="28dbd-129">Indica che questo cmdlet restituisce l'URI BLOB completo e il token della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="28dbd-129">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="28dbd-130">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="28dbd-130">-IPAddressOrRange</span></span>
<span data-ttu-id="28dbd-131">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="28dbd-131">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="28dbd-132">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="28dbd-132">The range is inclusive.</span></span>

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

### <span data-ttu-id="28dbd-133">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="28dbd-133">-Permission</span></span>
<span data-ttu-id="28dbd-134">Specifica le autorizzazioni per un BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="28dbd-134">Specifies the permissions for a storage blob.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28dbd-135">-Policy</span><span class="sxs-lookup"><span data-stu-id="28dbd-135">-Policy</span></span>
<span data-ttu-id="28dbd-136">Specifica un criterio di accesso archiviato in Azure.</span><span class="sxs-lookup"><span data-stu-id="28dbd-136">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28dbd-137">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="28dbd-137">-Protocol</span></span>
<span data-ttu-id="28dbd-138">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="28dbd-138">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="28dbd-139">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="28dbd-139">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="28dbd-140">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="28dbd-140">HttpsOnly</span></span>
* <span data-ttu-id="28dbd-141">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="28dbd-141">HttpsOrHttp</span></span>

<span data-ttu-id="28dbd-142">Il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="28dbd-142">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28dbd-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="28dbd-143">-StartTime</span></span>
<span data-ttu-id="28dbd-144">Specifica il momento in cui la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="28dbd-144">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28dbd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28dbd-145">CommonParameters</span></span>
<span data-ttu-id="28dbd-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28dbd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28dbd-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28dbd-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28dbd-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28dbd-148">INPUTS</span></span>

### <span data-ttu-id="28dbd-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="28dbd-149">IStorageContext</span></span>

<span data-ttu-id="28dbd-150">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="28dbd-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="28dbd-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28dbd-151">OUTPUTS</span></span>

### <span data-ttu-id="28dbd-152">System. String</span><span class="sxs-lookup"><span data-stu-id="28dbd-152">System.String</span></span>

## <span data-ttu-id="28dbd-153">Note</span><span class="sxs-lookup"><span data-stu-id="28dbd-153">NOTES</span></span>

## <span data-ttu-id="28dbd-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28dbd-154">RELATED LINKS</span></span>

[<span data-ttu-id="28dbd-155">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="28dbd-155">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="28dbd-156">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="28dbd-156">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
