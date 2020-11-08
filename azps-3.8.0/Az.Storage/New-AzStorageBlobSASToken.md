---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: 6bcb5163e31f2acbdd3e180cf76aef8fcfb33571
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021095"
---
# <span data-ttu-id="9099e-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="9099e-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="9099e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9099e-102">SYNOPSIS</span></span>
<span data-ttu-id="9099e-103">Genera un token SAS per un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9099e-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="9099e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9099e-104">SYNTAX</span></span>

### <span data-ttu-id="9099e-105">BlobNameWithPermission (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9099e-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9099e-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="9099e-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9099e-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="9099e-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9099e-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="9099e-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9099e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9099e-109">DESCRIPTION</span></span>
<span data-ttu-id="9099e-110">Il cmdlet **New-AzStorageBlobSASToken** genera un token SAS (Shared Access Signature) per un BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9099e-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="9099e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9099e-111">EXAMPLES</span></span>

### <span data-ttu-id="9099e-112">Esempio 1: generare un token SAS BLOB con l'autorizzazione BLOB completo</span><span class="sxs-lookup"><span data-stu-id="9099e-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="9099e-113">Questo esempio genera un token SAS BLOB con l'autorizzazione BLOB completo.</span><span class="sxs-lookup"><span data-stu-id="9099e-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="9099e-114">Esempio 2: generare un token SAS BLOB con durata</span><span class="sxs-lookup"><span data-stu-id="9099e-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="9099e-115">Questo esempio genera un token SAS BLOB con la durata.</span><span class="sxs-lookup"><span data-stu-id="9099e-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="9099e-116">Esempio 3: generare un token SAS di identità utente con il contesto di archiviazione basato sull'autenticazione OAuth</span><span class="sxs-lookup"><span data-stu-id="9099e-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="9099e-117">Questo esempio genera un token SAS BLOB di identità utente con il contesto di archiviazione basato sull'autenticazione OAuth</span><span class="sxs-lookup"><span data-stu-id="9099e-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="9099e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9099e-118">PARAMETERS</span></span>

### <span data-ttu-id="9099e-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="9099e-119">-Blob</span></span>
<span data-ttu-id="9099e-120">Specifica il nome BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9099e-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="9099e-121">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9099e-121">-CloudBlob</span></span>
<span data-ttu-id="9099e-122">Specifica l'oggetto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="9099e-122">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="9099e-123">Per ottenere un oggetto **CloudBlob** , usa il cmdlet [Get-AzStorageBlob](./Get-AzStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="9099e-123">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="9099e-124">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="9099e-124">-Container</span></span>
<span data-ttu-id="9099e-125">Specifica il nome del contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9099e-125">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="9099e-126">-Contesto</span><span class="sxs-lookup"><span data-stu-id="9099e-126">-Context</span></span>
<span data-ttu-id="9099e-127">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9099e-127">Specifies the storage context.</span></span>
<span data-ttu-id="9099e-128">Quando il contesto di archiviazione si basa sull'autenticazione OAuth, verrà generato un token SAS BLOB di identità utente.</span><span class="sxs-lookup"><span data-stu-id="9099e-128">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="9099e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9099e-129">-DefaultProfile</span></span>
<span data-ttu-id="9099e-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9099e-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9099e-131">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9099e-131">-ExpiryTime</span></span>
<span data-ttu-id="9099e-132">Specifica quando scade la firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="9099e-132">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="9099e-133">Quando il contesto di archiviazione si basa sull'autenticazione OAuth, il tempo di scadenza deve essere in 7 giorni dall'ora corrente e non deve essere precedente all'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="9099e-133">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="9099e-134">-FullUri</span><span class="sxs-lookup"><span data-stu-id="9099e-134">-FullUri</span></span>
<span data-ttu-id="9099e-135">Indica che questo cmdlet restituisce l'URI BLOB completo e il token della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="9099e-135">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="9099e-136">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="9099e-136">-IPAddressOrRange</span></span>
<span data-ttu-id="9099e-137">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="9099e-137">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="9099e-138">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="9099e-138">The range is inclusive.</span></span>

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

### <span data-ttu-id="9099e-139">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="9099e-139">-Permission</span></span>
<span data-ttu-id="9099e-140">Specifica le autorizzazioni per un BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9099e-140">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="9099e-141">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="9099e-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="9099e-142">-Policy</span><span class="sxs-lookup"><span data-stu-id="9099e-142">-Policy</span></span>
<span data-ttu-id="9099e-143">Specifica un criterio di accesso archiviato in Azure.</span><span class="sxs-lookup"><span data-stu-id="9099e-143">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="9099e-144">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="9099e-144">-Protocol</span></span>
<span data-ttu-id="9099e-145">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="9099e-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="9099e-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9099e-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="9099e-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="9099e-147">HttpsOnly</span></span>
* <span data-ttu-id="9099e-148">HttpsOrHttp il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="9099e-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="9099e-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9099e-149">-StartTime</span></span>
<span data-ttu-id="9099e-150">Specifica il momento in cui la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="9099e-150">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="9099e-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9099e-151">-Confirm</span></span>
<span data-ttu-id="9099e-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9099e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9099e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9099e-153">-WhatIf</span></span>
<span data-ttu-id="9099e-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9099e-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9099e-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9099e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9099e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9099e-156">CommonParameters</span></span>
<span data-ttu-id="9099e-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9099e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9099e-158">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9099e-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9099e-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9099e-159">INPUTS</span></span>

### <span data-ttu-id="9099e-160">Microsoft. Azure. storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9099e-160">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="9099e-161">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9099e-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9099e-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9099e-162">OUTPUTS</span></span>

### <span data-ttu-id="9099e-163">System. String</span><span class="sxs-lookup"><span data-stu-id="9099e-163">System.String</span></span>

## <span data-ttu-id="9099e-164">Note</span><span class="sxs-lookup"><span data-stu-id="9099e-164">NOTES</span></span>

## <span data-ttu-id="9099e-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9099e-165">RELATED LINKS</span></span>

[<span data-ttu-id="9099e-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9099e-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="9099e-167">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="9099e-167">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
