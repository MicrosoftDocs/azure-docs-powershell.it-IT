---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: fb349f2c5c8d394fb7af31190f58ea2ee10425ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200635"
---
# <span data-ttu-id="07a12-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="07a12-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="07a12-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07a12-102">SYNOPSIS</span></span>
<span data-ttu-id="07a12-103">Genera un token SAS per un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="07a12-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="07a12-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07a12-104">SYNTAX</span></span>

### <span data-ttu-id="07a12-105">BlobNameWithPermission (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="07a12-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a12-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="07a12-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a12-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="07a12-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a12-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="07a12-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07a12-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07a12-109">DESCRIPTION</span></span>
<span data-ttu-id="07a12-110">Il cmdlet **New-AzStorageBlobSASToken** genera un token SAS (Shared Access Signature) per un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="07a12-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="07a12-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07a12-111">EXAMPLES</span></span>

### <span data-ttu-id="07a12-112">Esempio 1: generare un token SAS BLOB con l'autorizzazione BLOB completo</span><span class="sxs-lookup"><span data-stu-id="07a12-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="07a12-113">Questo esempio genera un token SAS BLOB con l'autorizzazione BLOB completo.</span><span class="sxs-lookup"><span data-stu-id="07a12-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="07a12-114">Esempio 2: generare un token SAS BLOB con durata</span><span class="sxs-lookup"><span data-stu-id="07a12-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="07a12-115">Questo esempio genera un token SAS BLOB con la durata.</span><span class="sxs-lookup"><span data-stu-id="07a12-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="07a12-116">Esempio 3: generare un token SAS di identità utente con il contesto di archiviazione basato sull'autenticazione OAuth</span><span class="sxs-lookup"><span data-stu-id="07a12-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="07a12-117">Questo esempio genera un token SAS BLOB di identità utente con il contesto di archiviazione basato sull'autenticazione OAuth</span><span class="sxs-lookup"><span data-stu-id="07a12-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="07a12-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07a12-118">PARAMETERS</span></span>

### <span data-ttu-id="07a12-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="07a12-119">-Blob</span></span>
<span data-ttu-id="07a12-120">Specifica il nome BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="07a12-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="07a12-121">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="07a12-121">-BlobBaseClient</span></span>
<span data-ttu-id="07a12-122">Oggetto BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="07a12-122">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a12-123">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="07a12-123">-CloudBlob</span></span>
<span data-ttu-id="07a12-124">Specifica l'oggetto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="07a12-124">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="07a12-125">Per ottenere un oggetto **CloudBlob** , usa il cmdlet [Get-AzStorageBlob](./Get-AzStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="07a12-125">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a12-126">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="07a12-126">-Container</span></span>
<span data-ttu-id="07a12-127">Specifica il nome del contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="07a12-127">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="07a12-128">-Contesto</span><span class="sxs-lookup"><span data-stu-id="07a12-128">-Context</span></span>
<span data-ttu-id="07a12-129">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="07a12-129">Specifies the storage context.</span></span>
<span data-ttu-id="07a12-130">Quando il contesto di archiviazione si basa sull'autenticazione OAuth, verrà generato un token SAS BLOB di identità utente.</span><span class="sxs-lookup"><span data-stu-id="07a12-130">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="07a12-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a12-131">-DefaultProfile</span></span>
<span data-ttu-id="07a12-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07a12-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a12-133">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="07a12-133">-ExpiryTime</span></span>
<span data-ttu-id="07a12-134">Specifica quando scade la firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="07a12-134">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="07a12-135">Quando il contesto di archiviazione si basa sull'autenticazione OAuth, il tempo di scadenza deve essere in 7 giorni dall'ora corrente e non deve essere precedente all'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="07a12-135">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="07a12-136">-FullUri</span><span class="sxs-lookup"><span data-stu-id="07a12-136">-FullUri</span></span>
<span data-ttu-id="07a12-137">Indica che questo cmdlet restituisce l'URI BLOB completo e il token della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="07a12-137">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="07a12-138">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="07a12-138">-IPAddressOrRange</span></span>
<span data-ttu-id="07a12-139">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="07a12-139">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="07a12-140">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="07a12-140">The range is inclusive.</span></span>

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

### <span data-ttu-id="07a12-141">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="07a12-141">-Permission</span></span>
<span data-ttu-id="07a12-142">Specifica le autorizzazioni per un BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="07a12-142">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="07a12-143">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="07a12-143">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="07a12-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="07a12-144">-Policy</span></span>
<span data-ttu-id="07a12-145">Specifica un criterio di accesso archiviato in Azure.</span><span class="sxs-lookup"><span data-stu-id="07a12-145">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="07a12-146">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="07a12-146">-Protocol</span></span>
<span data-ttu-id="07a12-147">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="07a12-147">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="07a12-148">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="07a12-148">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="07a12-149">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="07a12-149">HttpsOnly</span></span>
* <span data-ttu-id="07a12-150">HttpsOrHttp il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="07a12-150">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a12-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="07a12-151">-StartTime</span></span>
<span data-ttu-id="07a12-152">Specifica il momento in cui la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="07a12-152">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="07a12-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07a12-153">-Confirm</span></span>
<span data-ttu-id="07a12-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07a12-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a12-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07a12-155">-WhatIf</span></span>
<span data-ttu-id="07a12-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07a12-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07a12-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07a12-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a12-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a12-158">CommonParameters</span></span>
<span data-ttu-id="07a12-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07a12-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a12-160">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a12-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a12-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07a12-161">INPUTS</span></span>

### <span data-ttu-id="07a12-162">Microsoft. Azure. storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="07a12-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="07a12-163">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="07a12-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="07a12-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07a12-164">OUTPUTS</span></span>

### <span data-ttu-id="07a12-165">System. String</span><span class="sxs-lookup"><span data-stu-id="07a12-165">System.String</span></span>

## <span data-ttu-id="07a12-166">Note</span><span class="sxs-lookup"><span data-stu-id="07a12-166">NOTES</span></span>

## <span data-ttu-id="07a12-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07a12-167">RELATED LINKS</span></span>

[<span data-ttu-id="07a12-168">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="07a12-168">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="07a12-169">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="07a12-169">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
