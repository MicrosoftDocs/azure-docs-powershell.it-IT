---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
ms.openlocfilehash: fb0565232410e840ef3e8adbad48e7f622a51d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519495"
---
# <span data-ttu-id="4701c-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="4701c-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="4701c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4701c-102">SYNOPSIS</span></span>
<span data-ttu-id="4701c-103">Crea un token SAS a livello di account.</span><span class="sxs-lookup"><span data-stu-id="4701c-103">Creates an account-level SAS token.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4701c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4701c-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="4701c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4701c-105">DESCRIPTION</span></span>
<span data-ttu-id="4701c-106">Il cmdlet **New-AzureStorageSASToken** crea un token SAS (Shared Access Signature) a livello di account per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4701c-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>

<span data-ttu-id="4701c-107">Puoi usare il token SAS per delegare le autorizzazioni per più servizi o per delegare le autorizzazioni per i servizi non disponibili con un token SAS a livello di oggetto.</span><span class="sxs-lookup"><span data-stu-id="4701c-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="4701c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4701c-108">EXAMPLES</span></span>

### <span data-ttu-id="4701c-109">Esempio 1: creare un token SAS a livello di account con l'autorizzazione completa</span><span class="sxs-lookup"><span data-stu-id="4701c-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="4701c-110">Questo comando crea un token SAS a livello di account con l'autorizzazione completa.</span><span class="sxs-lookup"><span data-stu-id="4701c-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="4701c-111">Esempio 2: creare un token SAS a livello di account per un intervallo di indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="4701c-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="4701c-112">Questo comando crea un token SAS a livello di account per le richieste solo HTTPS dall'intervallo di indirizzi IP specificato.</span><span class="sxs-lookup"><span data-stu-id="4701c-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="4701c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4701c-113">PARAMETERS</span></span>

### <span data-ttu-id="4701c-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4701c-114">-Context</span></span>
<span data-ttu-id="4701c-115">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4701c-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4701c-116">Puoi usare il cmdlet New-AzureStorageContext per ottenere un oggetto **AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="4701c-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="4701c-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4701c-117">-ExpiryTime</span></span>
<span data-ttu-id="4701c-118">Specifica il momento in cui la firma di accesso condiviso diventa non valida.</span><span class="sxs-lookup"><span data-stu-id="4701c-118">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="4701c-119">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="4701c-119">-IPAddressOrRange</span></span>
<span data-ttu-id="4701c-120">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="4701c-120">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="4701c-121">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="4701c-121">The range is inclusive.</span></span>

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

### <span data-ttu-id="4701c-122">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="4701c-122">-Permission</span></span>
<span data-ttu-id="4701c-123">Specifica le autorizzazioni per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4701c-123">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="4701c-124">Le autorizzazioni sono valide solo se corrispondono al tipo di risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="4701c-124">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="4701c-125">Per altre informazioni sui valori di autorizzazione accettabili, vedere Creazione di un account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="4701c-125">For more information about acceptable permission values, see Constructing an Account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="4701c-126">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="4701c-126">-Protocol</span></span>
<span data-ttu-id="4701c-127">Specifica il protocollo consentito per una richiesta effettuata con l'account SAS.</span><span class="sxs-lookup"><span data-stu-id="4701c-127">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="4701c-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4701c-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4701c-129">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="4701c-129">HttpsOnly</span></span>
- <span data-ttu-id="4701c-130">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="4701c-130">HttpsOrHttp</span></span>

<span data-ttu-id="4701c-131">Il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="4701c-131">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="4701c-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4701c-132">-ResourceType</span></span>
<span data-ttu-id="4701c-133">Specifica i tipi di risorsa disponibili con il token SAS.</span><span class="sxs-lookup"><span data-stu-id="4701c-133">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="4701c-134">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4701c-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4701c-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4701c-135">None</span></span>
- <span data-ttu-id="4701c-136">Servizio</span><span class="sxs-lookup"><span data-stu-id="4701c-136">Service</span></span>
- <span data-ttu-id="4701c-137">Contenitore</span><span class="sxs-lookup"><span data-stu-id="4701c-137">Container</span></span>
- <span data-ttu-id="4701c-138">Oggetto</span><span class="sxs-lookup"><span data-stu-id="4701c-138">Object</span></span>

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4701c-139">-Servizio</span><span class="sxs-lookup"><span data-stu-id="4701c-139">-Service</span></span>
<span data-ttu-id="4701c-140">Specifica il servizio.</span><span class="sxs-lookup"><span data-stu-id="4701c-140">Specifies the service.</span></span>
<span data-ttu-id="4701c-141">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4701c-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4701c-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4701c-142">None</span></span>
- <span data-ttu-id="4701c-143">BLOB</span><span class="sxs-lookup"><span data-stu-id="4701c-143">Blob</span></span>
- <span data-ttu-id="4701c-144">File</span><span class="sxs-lookup"><span data-stu-id="4701c-144">File</span></span>
- <span data-ttu-id="4701c-145">Coda</span><span class="sxs-lookup"><span data-stu-id="4701c-145">Queue</span></span>
- <span data-ttu-id="4701c-146">tavolo</span><span class="sxs-lookup"><span data-stu-id="4701c-146">Table</span></span>

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4701c-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4701c-147">-StartTime</span></span>
<span data-ttu-id="4701c-148">Specifica il tempo, come oggetto **DateTime** , in corrispondenza del quale il SAS diventa valido.</span><span class="sxs-lookup"><span data-stu-id="4701c-148">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="4701c-149">Per ottenere un oggetto **DateTime** , usa il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="4701c-149">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="4701c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4701c-150">CommonParameters</span></span>
<span data-ttu-id="4701c-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4701c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4701c-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4701c-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4701c-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4701c-153">INPUTS</span></span>

### <span data-ttu-id="4701c-154">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4701c-154">IStorageContext</span></span>

<span data-ttu-id="4701c-155">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="4701c-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="4701c-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4701c-156">OUTPUTS</span></span>

### <span data-ttu-id="4701c-157">System. String</span><span class="sxs-lookup"><span data-stu-id="4701c-157">System.String</span></span>

## <span data-ttu-id="4701c-158">Note</span><span class="sxs-lookup"><span data-stu-id="4701c-158">NOTES</span></span>

## <span data-ttu-id="4701c-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4701c-159">RELATED LINKS</span></span>

[<span data-ttu-id="4701c-160">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4701c-160">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="4701c-161">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="4701c-161">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="4701c-162">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="4701c-162">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="4701c-163">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="4701c-163">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="4701c-164">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="4701c-164">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="4701c-165">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="4701c-165">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)

