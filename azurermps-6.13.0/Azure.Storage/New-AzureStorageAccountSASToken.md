---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
ms.openlocfilehash: 8b0eb67808bf4148d93006b24273d55b737adfea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517800"
---
# <span data-ttu-id="0b295-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="0b295-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="0b295-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b295-102">SYNOPSIS</span></span>
<span data-ttu-id="0b295-103">Crea un token SAS a livello di account.</span><span class="sxs-lookup"><span data-stu-id="0b295-103">Creates an account-level SAS token.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b295-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b295-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b295-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b295-105">DESCRIPTION</span></span>
<span data-ttu-id="0b295-106">Il cmdlet **New-AzureStorageSASToken** crea un token SAS (Shared Access Signature) a livello di account per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0b295-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="0b295-107">Puoi usare il token SAS per delegare le autorizzazioni per più servizi o per delegare le autorizzazioni per i servizi non disponibili con un token SAS a livello di oggetto.</span><span class="sxs-lookup"><span data-stu-id="0b295-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="0b295-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b295-108">EXAMPLES</span></span>

### <span data-ttu-id="0b295-109">Esempio 1: creare un token SAS a livello di account con l'autorizzazione completa</span><span class="sxs-lookup"><span data-stu-id="0b295-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="0b295-110">Questo comando crea un token SAS a livello di account con l'autorizzazione completa.</span><span class="sxs-lookup"><span data-stu-id="0b295-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="0b295-111">Esempio 2: creare un token SAS a livello di account per un intervallo di indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="0b295-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="0b295-112">Questo comando crea un token SAS a livello di account per le richieste solo HTTPS dall'intervallo di indirizzi IP specificato.</span><span class="sxs-lookup"><span data-stu-id="0b295-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="0b295-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b295-113">PARAMETERS</span></span>

### <span data-ttu-id="0b295-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0b295-114">-Context</span></span>
<span data-ttu-id="0b295-115">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0b295-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="0b295-116">Puoi usare il cmdlet New-AzureStorageContext per ottenere un oggetto **AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="0b295-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="0b295-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b295-117">-DefaultProfile</span></span>
<span data-ttu-id="0b295-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b295-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b295-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0b295-119">-ExpiryTime</span></span>
<span data-ttu-id="0b295-120">Specifica il momento in cui la firma di accesso condiviso diventa non valida.</span><span class="sxs-lookup"><span data-stu-id="0b295-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="0b295-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="0b295-121">-IPAddressOrRange</span></span>
<span data-ttu-id="0b295-122">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="0b295-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="0b295-123">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="0b295-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="0b295-124">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="0b295-124">-Permission</span></span>
<span data-ttu-id="0b295-125">Specifica le autorizzazioni per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0b295-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="0b295-126">Le autorizzazioni sono valide solo se corrispondono al tipo di risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="0b295-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="0b295-127">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="0b295-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="0b295-128">Per altre informazioni sui valori di autorizzazione accettabili, vedere Creazione di un account SAS https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="0b295-128">For more information about acceptable permission values, see Constructing an Account SAS https://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="0b295-129">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="0b295-129">-Protocol</span></span>
<span data-ttu-id="0b295-130">Specifica il protocollo consentito per una richiesta effettuata con l'account SAS.</span><span class="sxs-lookup"><span data-stu-id="0b295-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="0b295-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b295-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b295-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="0b295-132">HttpsOnly</span></span>
- <span data-ttu-id="0b295-133">HttpsOrHttp il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="0b295-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="0b295-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0b295-134">-ResourceType</span></span>
<span data-ttu-id="0b295-135">Specifica i tipi di risorsa disponibili con il token SAS.</span><span class="sxs-lookup"><span data-stu-id="0b295-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="0b295-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b295-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b295-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0b295-137">None</span></span>
- <span data-ttu-id="0b295-138">Servizio</span><span class="sxs-lookup"><span data-stu-id="0b295-138">Service</span></span>
- <span data-ttu-id="0b295-139">Contenitore</span><span class="sxs-lookup"><span data-stu-id="0b295-139">Container</span></span>
- <span data-ttu-id="0b295-140">Oggetto</span><span class="sxs-lookup"><span data-stu-id="0b295-140">Object</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b295-141">-Servizio</span><span class="sxs-lookup"><span data-stu-id="0b295-141">-Service</span></span>
<span data-ttu-id="0b295-142">Specifica il servizio.</span><span class="sxs-lookup"><span data-stu-id="0b295-142">Specifies the service.</span></span>
<span data-ttu-id="0b295-143">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b295-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b295-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0b295-144">None</span></span>
- <span data-ttu-id="0b295-145">BLOB</span><span class="sxs-lookup"><span data-stu-id="0b295-145">Blob</span></span>
- <span data-ttu-id="0b295-146">File</span><span class="sxs-lookup"><span data-stu-id="0b295-146">File</span></span>
- <span data-ttu-id="0b295-147">Coda</span><span class="sxs-lookup"><span data-stu-id="0b295-147">Queue</span></span>
- <span data-ttu-id="0b295-148">tavolo</span><span class="sxs-lookup"><span data-stu-id="0b295-148">Table</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b295-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0b295-149">-StartTime</span></span>
<span data-ttu-id="0b295-150">Specifica il tempo, come oggetto **DateTime** , in corrispondenza del quale il SAS diventa valido.</span><span class="sxs-lookup"><span data-stu-id="0b295-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="0b295-151">Per ottenere un oggetto **DateTime** , usa il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="0b295-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="0b295-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b295-152">CommonParameters</span></span>
<span data-ttu-id="0b295-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b295-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b295-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b295-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b295-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b295-155">INPUTS</span></span>

### <span data-ttu-id="0b295-156">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0b295-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0b295-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b295-157">OUTPUTS</span></span>

### <span data-ttu-id="0b295-158">System. String</span><span class="sxs-lookup"><span data-stu-id="0b295-158">System.String</span></span>

## <span data-ttu-id="0b295-159">Note</span><span class="sxs-lookup"><span data-stu-id="0b295-159">NOTES</span></span>

## <span data-ttu-id="0b295-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b295-160">RELATED LINKS</span></span>

[<span data-ttu-id="0b295-161">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0b295-161">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="0b295-162">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="0b295-162">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="0b295-163">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="0b295-163">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="0b295-164">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="0b295-164">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="0b295-165">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="0b295-165">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="0b295-166">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="0b295-166">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


