---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 6d399c7ed7c074cd5adaf0579097c0706f46192d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002606"
---
# <span data-ttu-id="ea664-101">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="ea664-101">New-AzStorageAccountSASToken</span></span>

## <span data-ttu-id="ea664-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea664-102">SYNOPSIS</span></span>
<span data-ttu-id="ea664-103">Crea un token di firma di accesso condiviso a livello di account.</span><span class="sxs-lookup"><span data-stu-id="ea664-103">Creates an account-level SAS token.</span></span>

## <span data-ttu-id="ea664-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea664-104">SYNTAX</span></span>

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea664-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ea664-105">DESCRIPTION</span></span>
<span data-ttu-id="ea664-106">Il cmdlet **New-AzStorageSASToken** crea un token di firma di accesso condiviso (SAS) a livello di account per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ea664-106">The **New-AzStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="ea664-107">È possibile usare il token di firma di accesso condiviso per delegare le autorizzazioni per più servizi o per delegare autorizzazioni per i servizi non disponibili con un token di firma di accesso condiviso a livello di oggetto.</span><span class="sxs-lookup"><span data-stu-id="ea664-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="ea664-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea664-108">EXAMPLES</span></span>

### <span data-ttu-id="ea664-109">Esempio 1: Creare un token di firma di accesso condiviso a livello di account con autorizzazione completa</span><span class="sxs-lookup"><span data-stu-id="ea664-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="ea664-110">Questo comando crea un token di firma di accesso condiviso a livello di account con autorizzazioni complete.</span><span class="sxs-lookup"><span data-stu-id="ea664-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="ea664-111">Esempio 2: Creare un token di firma di accesso condiviso a livello di account per un intervallo di indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="ea664-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="ea664-112">Questo comando crea un token di firma di accesso condiviso a livello di account per le richieste solo HTTPS dall'intervallo specificato di indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="ea664-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="ea664-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea664-113">PARAMETERS</span></span>

### <span data-ttu-id="ea664-114">-Context</span><span class="sxs-lookup"><span data-stu-id="ea664-114">-Context</span></span>
<span data-ttu-id="ea664-115">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ea664-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ea664-116">È possibile usare il cmdlet New-AzStorageContext per ottenere un **oggetto AzureStorageContext.**</span><span class="sxs-lookup"><span data-stu-id="ea664-116">You can use the New-AzStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="ea664-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea664-117">-DefaultProfile</span></span>
<span data-ttu-id="ea664-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea664-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea664-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ea664-119">-ExpiryTime</span></span>
<span data-ttu-id="ea664-120">Specifica l'ora in cui la firma di accesso condiviso diventa non valida.</span><span class="sxs-lookup"><span data-stu-id="ea664-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="ea664-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ea664-121">-IPAddressOrRange</span></span>
<span data-ttu-id="ea664-122">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="ea664-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="ea664-123">L'intervallo è inclusivo.</span><span class="sxs-lookup"><span data-stu-id="ea664-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="ea664-124">-Permission</span><span class="sxs-lookup"><span data-stu-id="ea664-124">-Permission</span></span>
<span data-ttu-id="ea664-125">Specifica le autorizzazioni per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ea664-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="ea664-126">Le autorizzazioni sono valide solo se corrispondono al tipo di risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="ea664-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="ea664-127">È importante notare che si tratta di una stringa, ad esempio `rwd` (per Lettura, Scrittura ed Elimina).</span><span class="sxs-lookup"><span data-stu-id="ea664-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="ea664-128">Per altre informazioni sui valori di autorizzazione accettabili, vedere Creazione di una firma di accesso condiviso per un account http://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="ea664-128">For more information about acceptable permission values, see Constructing an Account SAS http://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="ea664-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ea664-129">-Protocol</span></span>
<span data-ttu-id="ea664-130">Specifica il protocollo consentito per una richiesta effettuata con la firma di accesso condiviso dell'account.</span><span class="sxs-lookup"><span data-stu-id="ea664-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="ea664-131">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="ea664-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ea664-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ea664-132">HttpsOnly</span></span>
- <span data-ttu-id="ea664-133">HttpsOrHttp Il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="ea664-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="ea664-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ea664-134">-ResourceType</span></span>
<span data-ttu-id="ea664-135">Specifica i tipi di risorse disponibili con il token di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="ea664-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="ea664-136">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="ea664-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ea664-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ea664-137">None</span></span>
- <span data-ttu-id="ea664-138">Servizio</span><span class="sxs-lookup"><span data-stu-id="ea664-138">Service</span></span>
- <span data-ttu-id="ea664-139">Contenitore</span><span class="sxs-lookup"><span data-stu-id="ea664-139">Container</span></span>
- <span data-ttu-id="ea664-140">Oggetto</span><span class="sxs-lookup"><span data-stu-id="ea664-140">Object</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea664-141">-Service</span><span class="sxs-lookup"><span data-stu-id="ea664-141">-Service</span></span>
<span data-ttu-id="ea664-142">Specifica il servizio.</span><span class="sxs-lookup"><span data-stu-id="ea664-142">Specifies the service.</span></span>
<span data-ttu-id="ea664-143">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="ea664-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ea664-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ea664-144">None</span></span>
- <span data-ttu-id="ea664-145">BLOB</span><span class="sxs-lookup"><span data-stu-id="ea664-145">Blob</span></span>
- <span data-ttu-id="ea664-146">File</span><span class="sxs-lookup"><span data-stu-id="ea664-146">File</span></span>
- <span data-ttu-id="ea664-147">Coda</span><span class="sxs-lookup"><span data-stu-id="ea664-147">Queue</span></span>
- <span data-ttu-id="ea664-148">tavolo</span><span class="sxs-lookup"><span data-stu-id="ea664-148">Table</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea664-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ea664-149">-StartTime</span></span>
<span data-ttu-id="ea664-150">Specifica l'ora, come oggetto **DateTime,** in cui la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="ea664-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="ea664-151">Per ottenere un **oggetto DateTime,** usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="ea664-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="ea664-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea664-152">CommonParameters</span></span>
<span data-ttu-id="ea664-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea664-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea664-154">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea664-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea664-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="ea664-155">INPUTS</span></span>

### <span data-ttu-id="ea664-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ea664-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ea664-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea664-157">OUTPUTS</span></span>

### <span data-ttu-id="ea664-158">System.String</span><span class="sxs-lookup"><span data-stu-id="ea664-158">System.String</span></span>

## <span data-ttu-id="ea664-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="ea664-159">NOTES</span></span>

## <span data-ttu-id="ea664-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea664-160">RELATED LINKS</span></span>

[<span data-ttu-id="ea664-161">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ea664-161">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)

[<span data-ttu-id="ea664-162">New-azStorageContainersASToken</span><span class="sxs-lookup"><span data-stu-id="ea664-162">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)

[<span data-ttu-id="ea664-163">New-azStorageFilesASToken</span><span class="sxs-lookup"><span data-stu-id="ea664-163">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)

[<span data-ttu-id="ea664-164">New-azStorageQueuesASToken</span><span class="sxs-lookup"><span data-stu-id="ea664-164">New-AzStorageQueueSASToken</span></span>](./New-AzStorageQueueSASToken.md)

[<span data-ttu-id="ea664-165">New-azStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="ea664-165">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)

[<span data-ttu-id="ea664-166">New-azStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="ea664-166">New-AzStorageTableSASToken</span></span>](./New-AzStorageTableSASToken.md)


