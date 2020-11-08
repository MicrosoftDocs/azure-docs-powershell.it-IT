---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 4e265fab8df3abd897c27131e0673241ce37b946
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200633"
---
# <span data-ttu-id="d769f-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d769f-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="d769f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d769f-102">SYNOPSIS</span></span>
<span data-ttu-id="d769f-103">Genera un token SAS per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d769f-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="d769f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d769f-104">SYNTAX</span></span>

### <span data-ttu-id="d769f-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="d769f-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d769f-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="d769f-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d769f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d769f-107">DESCRIPTION</span></span>
<span data-ttu-id="d769f-108">Il cmdlet **New-AzStorageContainerSASToken** genera un token SAS (Shared Access Signature) per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d769f-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="d769f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d769f-109">EXAMPLES</span></span>

### <span data-ttu-id="d769f-110">Esempio 1: generare un token SAS contenitore con l'autorizzazione contenitore completo</span><span class="sxs-lookup"><span data-stu-id="d769f-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="d769f-111">Questo esempio genera un token SAS contenitore con l'autorizzazione contenitore completo.</span><span class="sxs-lookup"><span data-stu-id="d769f-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="d769f-112">Esempio 2: generare più token SAS contenitore tramite pipeline</span><span class="sxs-lookup"><span data-stu-id="d769f-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="d769f-113">Questo esempio genera più token SAS contenitore usando la pipeline.</span><span class="sxs-lookup"><span data-stu-id="d769f-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="d769f-114">Esempio 3: generare il token SAS contenitore con i criteri di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="d769f-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="d769f-115">Questo esempio genera un token SAS contenitore con criteri di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="d769f-115">This example generates a container SAS token with shared access policy.</span></span>

### <span data-ttu-id="d769f-116">Esempio 3: generare un token SAS contenitore di identità utente con il contesto di archiviazione basato sull'autenticazione OAuth</span><span class="sxs-lookup"><span data-stu-id="d769f-116">Example 3: Generate a User Identity container SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="d769f-117">Questo esempio genera un token SAS contenitore di identità utente con il contesto di archiviazione basato sull'autenticazione OAuth</span><span class="sxs-lookup"><span data-stu-id="d769f-117">This example generates a User Identity container SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="d769f-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d769f-118">PARAMETERS</span></span>

### <span data-ttu-id="d769f-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d769f-119">-Context</span></span>
<span data-ttu-id="d769f-120">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d769f-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d769f-121">Puoi crearlo usando il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d769f-121">You can create it by using the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="d769f-122">Quando il contesto di archiviazione si basa sull'autenticazione OAuth, verrà generato un token SAS contenitore di identità utente.</span><span class="sxs-lookup"><span data-stu-id="d769f-122">When the storage context is based on OAuth authentication, will generates a User Identity container SAS token.</span></span>

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

### <span data-ttu-id="d769f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d769f-123">-DefaultProfile</span></span>
<span data-ttu-id="d769f-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d769f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d769f-125">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d769f-125">-ExpiryTime</span></span>
<span data-ttu-id="d769f-126">Specifica il momento in cui la firma di accesso condiviso diventa non valida.</span><span class="sxs-lookup"><span data-stu-id="d769f-126">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="d769f-127">Se l'utente imposta l'ora di inizio ma non quella di scadenza, l'ora di scadenza viene impostata sull'ora di inizio più un'ora.</span><span class="sxs-lookup"><span data-stu-id="d769f-127">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="d769f-128">Se non viene specificato né l'ora di inizio né l'ora di scadenza, il tempo di scadenza viene impostato sull'ora corrente e su un orario.</span><span class="sxs-lookup"><span data-stu-id="d769f-128">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>
<span data-ttu-id="d769f-129">Quando il contesto di archiviazione si basa sull'autenticazione OAuth, il tempo di scadenza deve essere in 7 giorni dall'ora corrente e non deve essere precedente all'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="d769f-129">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="d769f-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="d769f-130">-FullUri</span></span>
<span data-ttu-id="d769f-131">Indica che questo cmdlet restituisce l'URI BLOB completo e il token della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="d769f-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="d769f-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d769f-132">-IPAddressOrRange</span></span>
<span data-ttu-id="d769f-133">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="d769f-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="d769f-134">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="d769f-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="d769f-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="d769f-135">-Name</span></span>
<span data-ttu-id="d769f-136">Specifica un nome di contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d769f-136">Specifies an Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d769f-137">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="d769f-137">-Permission</span></span>
<span data-ttu-id="d769f-138">Specifica le autorizzazioni per un contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d769f-138">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="d769f-139">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="d769f-139">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d769f-140">-Policy</span><span class="sxs-lookup"><span data-stu-id="d769f-140">-Policy</span></span>
<span data-ttu-id="d769f-141">Specifica un criterio di accesso archiviato in Azure.</span><span class="sxs-lookup"><span data-stu-id="d769f-141">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d769f-142">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="d769f-142">-Protocol</span></span>
<span data-ttu-id="d769f-143">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="d769f-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="d769f-144">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d769f-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="d769f-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d769f-145">HttpsOnly</span></span>
* <span data-ttu-id="d769f-146">HttpsOrHttp il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="d769f-146">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="d769f-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d769f-147">-StartTime</span></span>
<span data-ttu-id="d769f-148">Specifica il momento in cui la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="d769f-148">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="d769f-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d769f-149">-Confirm</span></span>
<span data-ttu-id="d769f-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d769f-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d769f-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d769f-151">-WhatIf</span></span>
<span data-ttu-id="d769f-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d769f-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d769f-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d769f-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d769f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d769f-154">CommonParameters</span></span>
<span data-ttu-id="d769f-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d769f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d769f-156">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d769f-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d769f-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d769f-157">INPUTS</span></span>

### <span data-ttu-id="d769f-158">System. String</span><span class="sxs-lookup"><span data-stu-id="d769f-158">System.String</span></span>

### <span data-ttu-id="d769f-159">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d769f-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d769f-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d769f-160">OUTPUTS</span></span>

### <span data-ttu-id="d769f-161">System. String</span><span class="sxs-lookup"><span data-stu-id="d769f-161">System.String</span></span>

## <span data-ttu-id="d769f-162">Note</span><span class="sxs-lookup"><span data-stu-id="d769f-162">NOTES</span></span>

## <span data-ttu-id="d769f-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d769f-163">RELATED LINKS</span></span>

[<span data-ttu-id="d769f-164">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d769f-164">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
