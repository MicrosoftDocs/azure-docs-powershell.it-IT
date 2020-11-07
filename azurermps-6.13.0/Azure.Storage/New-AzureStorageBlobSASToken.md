---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
ms.openlocfilehash: 60c93d851e173dd8ee8a5f33ff96bb4e2e12299b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517795"
---
# <span data-ttu-id="861bf-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="861bf-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="861bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="861bf-102">SYNOPSIS</span></span>
<span data-ttu-id="861bf-103">Genera un token SAS per un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="861bf-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="861bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="861bf-104">SYNTAX</span></span>

### <span data-ttu-id="861bf-105">BlobNameWithPermission (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="861bf-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="861bf-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="861bf-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="861bf-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="861bf-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="861bf-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="861bf-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="861bf-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="861bf-109">DESCRIPTION</span></span>
<span data-ttu-id="861bf-110">Il cmdlet **New-AzureStorageBlobSASToken** genera un token SAS (Shared Access Signature) per un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="861bf-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="861bf-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="861bf-111">EXAMPLES</span></span>

### <span data-ttu-id="861bf-112">Esempio 1: generare un token SAS BLOB con l'autorizzazione BLOB completo</span><span class="sxs-lookup"><span data-stu-id="861bf-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="861bf-113">Questo esempio genera un token SAS BLOB con l'autorizzazione BLOB completo.</span><span class="sxs-lookup"><span data-stu-id="861bf-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="861bf-114">Esempio 2: generare un token SAS BLOB con durata</span><span class="sxs-lookup"><span data-stu-id="861bf-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="861bf-115">Questo esempio genera un token SAS BLOB con la durata.</span><span class="sxs-lookup"><span data-stu-id="861bf-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="861bf-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="861bf-116">PARAMETERS</span></span>

### <span data-ttu-id="861bf-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="861bf-117">-Blob</span></span>
<span data-ttu-id="861bf-118">Specifica il nome BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="861bf-118">Specifies the storage blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861bf-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="861bf-119">-CloudBlob</span></span>
<span data-ttu-id="861bf-120">Specifica l'oggetto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="861bf-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="861bf-121">Per ottenere un oggetto **CloudBlob** , usa il cmdlet [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="861bf-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="861bf-122">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="861bf-122">-Container</span></span>
<span data-ttu-id="861bf-123">Specifica il nome del contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="861bf-123">Specifies the storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861bf-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="861bf-124">-Context</span></span>
<span data-ttu-id="861bf-125">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="861bf-125">Specifies the storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="861bf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="861bf-126">-DefaultProfile</span></span>
<span data-ttu-id="861bf-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="861bf-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861bf-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="861bf-128">-ExpiryTime</span></span>
<span data-ttu-id="861bf-129">Specifica quando scade la firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="861bf-129">Specifies when the shared access signature expires.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861bf-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="861bf-130">-FullUri</span></span>
<span data-ttu-id="861bf-131">Indica che questo cmdlet restituisce l'URI BLOB completo e il token della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="861bf-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861bf-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="861bf-132">-IPAddressOrRange</span></span>
<span data-ttu-id="861bf-133">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="861bf-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="861bf-134">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="861bf-134">The range is inclusive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861bf-135">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="861bf-135">-Permission</span></span>
<span data-ttu-id="861bf-136">Specifica le autorizzazioni per un BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="861bf-136">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="861bf-137">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="861bf-137">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861bf-138">-Policy</span><span class="sxs-lookup"><span data-stu-id="861bf-138">-Policy</span></span>
<span data-ttu-id="861bf-139">Specifica un criterio di accesso archiviato in Azure.</span><span class="sxs-lookup"><span data-stu-id="861bf-139">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861bf-140">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="861bf-140">-Protocol</span></span>
<span data-ttu-id="861bf-141">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="861bf-141">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="861bf-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="861bf-142">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="861bf-143">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="861bf-143">HttpsOnly</span></span>
* <span data-ttu-id="861bf-144">HttpsOrHttp il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="861bf-144">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861bf-145">-StartTime</span><span class="sxs-lookup"><span data-stu-id="861bf-145">-StartTime</span></span>
<span data-ttu-id="861bf-146">Specifica il momento in cui la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="861bf-146">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861bf-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="861bf-147">CommonParameters</span></span>
<span data-ttu-id="861bf-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="861bf-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="861bf-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="861bf-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="861bf-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="861bf-150">INPUTS</span></span>

### <span data-ttu-id="861bf-151">Microsoft. WindowsAzure. storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="861bf-151">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="861bf-152">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="861bf-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="861bf-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="861bf-153">OUTPUTS</span></span>

### <span data-ttu-id="861bf-154">System. String</span><span class="sxs-lookup"><span data-stu-id="861bf-154">System.String</span></span>

## <span data-ttu-id="861bf-155">Note</span><span class="sxs-lookup"><span data-stu-id="861bf-155">NOTES</span></span>

## <span data-ttu-id="861bf-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="861bf-156">RELATED LINKS</span></span>

[<span data-ttu-id="861bf-157">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="861bf-157">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="861bf-158">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="861bf-158">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)