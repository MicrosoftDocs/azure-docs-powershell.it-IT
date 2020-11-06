---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8d84b310a16a73456bcd519332fa76ad1a6566
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507027"
---
# <span data-ttu-id="bd776-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="bd776-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="bd776-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd776-102">SYNOPSIS</span></span>
<span data-ttu-id="bd776-103">Genera un token SAS per un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bd776-103">Generates an SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="bd776-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd776-104">SYNTAX</span></span>

### <span data-ttu-id="bd776-105">BlobNameWithPermission (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bd776-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="bd776-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="bd776-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="bd776-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="bd776-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="bd776-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="bd776-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="bd776-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd776-109">DESCRIPTION</span></span>
<span data-ttu-id="bd776-110">Il cmdlet **New-AzureStorageBlobSASToken** genera un token SAS (Shared Access Signature) per un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bd776-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="bd776-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd776-111">EXAMPLES</span></span>

### <span data-ttu-id="bd776-112">Esempio 1: generare un token SAS BLOB con l'autorizzazione BLOB completo</span><span class="sxs-lookup"><span data-stu-id="bd776-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="bd776-113">Questo esempio genera un token SAS BLOB con l'autorizzazione BLOB completo.</span><span class="sxs-lookup"><span data-stu-id="bd776-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="bd776-114">Esempio 2: generare un token SAS BLOB con durata</span><span class="sxs-lookup"><span data-stu-id="bd776-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="bd776-115">Questo esempio genera un token SAS BLOB con la durata.</span><span class="sxs-lookup"><span data-stu-id="bd776-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="bd776-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd776-116">PARAMETERS</span></span>

### <span data-ttu-id="bd776-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="bd776-117">-Blob</span></span>
<span data-ttu-id="bd776-118">Specifica il nome BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bd776-118">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="bd776-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="bd776-119">-CloudBlob</span></span>
<span data-ttu-id="bd776-120">Specifica l'oggetto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="bd776-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="bd776-121">Per ottenere un oggetto **CloudBlob** , usa il cmdlet [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="bd776-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="bd776-122">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="bd776-122">-Container</span></span>
<span data-ttu-id="bd776-123">Specifica il nome del contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bd776-123">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="bd776-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="bd776-124">-Context</span></span>
<span data-ttu-id="bd776-125">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bd776-125">Specifies the storage context.</span></span>

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

### <span data-ttu-id="bd776-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="bd776-126">-ExpiryTime</span></span>
<span data-ttu-id="bd776-127">Specifica quando scade la firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="bd776-127">Specifies when the shared access signature expires.</span></span>

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

### <span data-ttu-id="bd776-128">-FullUri</span><span class="sxs-lookup"><span data-stu-id="bd776-128">-FullUri</span></span>
<span data-ttu-id="bd776-129">Indica che questo cmdlet restituisce l'URI BLOB completo e il token della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="bd776-129">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="bd776-130">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="bd776-130">-IPAddressOrRange</span></span>
<span data-ttu-id="bd776-131">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="bd776-131">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="bd776-132">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="bd776-132">The range is inclusive.</span></span>

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

### <span data-ttu-id="bd776-133">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="bd776-133">-Permission</span></span>
<span data-ttu-id="bd776-134">Specifica le autorizzazioni per un BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bd776-134">Specifies the permissions for a storage blob.</span></span>

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

### <span data-ttu-id="bd776-135">-Policy</span><span class="sxs-lookup"><span data-stu-id="bd776-135">-Policy</span></span>
<span data-ttu-id="bd776-136">Specifica un criterio di accesso archiviato in Azure.</span><span class="sxs-lookup"><span data-stu-id="bd776-136">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="bd776-137">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="bd776-137">-Protocol</span></span>
<span data-ttu-id="bd776-138">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="bd776-138">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="bd776-139">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="bd776-139">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="bd776-140">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="bd776-140">HttpsOnly</span></span>
* <span data-ttu-id="bd776-141">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="bd776-141">HttpsOrHttp</span></span>

<span data-ttu-id="bd776-142">Il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="bd776-142">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="bd776-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bd776-143">-StartTime</span></span>
<span data-ttu-id="bd776-144">Specifica il momento in cui la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="bd776-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="bd776-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd776-145">CommonParameters</span></span>
<span data-ttu-id="bd776-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd776-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd776-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd776-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd776-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd776-148">INPUTS</span></span>

## <span data-ttu-id="bd776-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd776-149">OUTPUTS</span></span>

## <span data-ttu-id="bd776-150">Note</span><span class="sxs-lookup"><span data-stu-id="bd776-150">NOTES</span></span>

## <span data-ttu-id="bd776-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd776-151">RELATED LINKS</span></span>

[<span data-ttu-id="bd776-152">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="bd776-152">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="bd776-153">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="bd776-153">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
