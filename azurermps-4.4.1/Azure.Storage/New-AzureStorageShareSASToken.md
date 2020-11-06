---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 84f280bf5e3297796bb8b56e5a5d42e513b79e79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510807"
---
# <span data-ttu-id="f8498-101">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="f8498-101">New-AzureStorageShareSASToken</span></span>

## <span data-ttu-id="f8498-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8498-102">SYNOPSIS</span></span>
<span data-ttu-id="f8498-103">Genera il token della firma di accesso condiviso per la condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f8498-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8498-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8498-104">SYNTAX</span></span>

### <span data-ttu-id="f8498-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="f8498-105">SasPolicy</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="f8498-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="f8498-106">SasPermission</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="f8498-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8498-107">DESCRIPTION</span></span>
<span data-ttu-id="f8498-108">Il cmdlet **New-AzureStorageShareSASToken** genera un token della firma di accesso condiviso per una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f8498-108">The **New-AzureStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="f8498-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8498-109">EXAMPLES</span></span>

### <span data-ttu-id="f8498-110">Esempio 1: generare un token della firma di accesso condiviso per una condivisione</span><span class="sxs-lookup"><span data-stu-id="f8498-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="f8498-111">Questo comando crea un token della firma di accesso condiviso per la condivisione denominata ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="f8498-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="f8498-112">Esempio 2: generare più token della firma di accesso condiviso tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="f8498-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="f8498-113">Questo comando consente di ottenere tutte le condivisioni di archiviazione corrispondenti al test del prefisso.</span><span class="sxs-lookup"><span data-stu-id="f8498-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="f8498-114">Il comando li passa al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="f8498-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f8498-115">Il cmdlet Current crea un token di accesso condiviso per ogni condivisione di archiviazione con le autorizzazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="f8498-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="f8498-116">Esempio 3: generare un token della firma di accesso condiviso che usa un criterio di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="f8498-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="f8498-117">Questo comando crea un token della firma di accesso condiviso per la condivisione di archiviazione denominata ContosoShare con il criterio denominato ContosoPolicy03.</span><span class="sxs-lookup"><span data-stu-id="f8498-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="f8498-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8498-118">PARAMETERS</span></span>

### <span data-ttu-id="f8498-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f8498-119">-Context</span></span>
<span data-ttu-id="f8498-120">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f8498-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="f8498-121">Per ottenere un contesto, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f8498-121">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f8498-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f8498-122">-ExpiryTime</span></span>
<span data-ttu-id="f8498-123">Specifica il momento in cui la firma di accesso condiviso diventa non valida.</span><span class="sxs-lookup"><span data-stu-id="f8498-123">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="f8498-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="f8498-124">-FullUri</span></span>
<span data-ttu-id="f8498-125">Indica che questo cmdlet restituisce l'URI BLOB completo e il token della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="f8498-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="f8498-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f8498-126">-IPAddressOrRange</span></span>
<span data-ttu-id="f8498-127">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="f8498-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="f8498-128">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="f8498-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="f8498-129">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="f8498-129">-Permission</span></span>
<span data-ttu-id="f8498-130">Specifica le autorizzazioni nel token per accedere alla condivisione e ai file sotto la condivisione.</span><span class="sxs-lookup"><span data-stu-id="f8498-130">Specifies the permissions in the token to access the share and files under the share.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8498-131">-Policy</span><span class="sxs-lookup"><span data-stu-id="f8498-131">-Policy</span></span>
<span data-ttu-id="f8498-132">Specifica i criteri di accesso archiviati per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="f8498-132">Specifies the stored access policy for a share.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8498-133">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="f8498-133">-Protocol</span></span>
<span data-ttu-id="f8498-134">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="f8498-134">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="f8498-135">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f8498-135">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="f8498-136">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="f8498-136">HttpsOnly</span></span>
* <span data-ttu-id="f8498-137">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="f8498-137">HttpsOrHttp</span></span>

<span data-ttu-id="f8498-138">Il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="f8498-138">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="f8498-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f8498-139">-ShareName</span></span>
<span data-ttu-id="f8498-140">Specifica il nome della condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f8498-140">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8498-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f8498-141">-StartTime</span></span>
<span data-ttu-id="f8498-142">Specifica il momento in cui la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="f8498-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="f8498-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8498-143">CommonParameters</span></span>
<span data-ttu-id="f8498-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8498-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8498-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8498-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8498-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8498-146">INPUTS</span></span>

### <span data-ttu-id="f8498-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f8498-147">IStorageContext</span></span>

<span data-ttu-id="f8498-148">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f8498-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="f8498-149">Stringa</span><span class="sxs-lookup"><span data-stu-id="f8498-149">String</span></span>

<span data-ttu-id="f8498-150">Il parametro "ShareName" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f8498-150">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f8498-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8498-151">OUTPUTS</span></span>

### <span data-ttu-id="f8498-152">System. String</span><span class="sxs-lookup"><span data-stu-id="f8498-152">System.String</span></span>

## <span data-ttu-id="f8498-153">Note</span><span class="sxs-lookup"><span data-stu-id="f8498-153">NOTES</span></span>
* <span data-ttu-id="f8498-154">Parole chiave: comuni, Azure, servizi, dati, archiviazione, BLOB, coda, tabella</span><span class="sxs-lookup"><span data-stu-id="f8498-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="f8498-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8498-155">RELATED LINKS</span></span>

[<span data-ttu-id="f8498-156">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="f8498-156">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="f8498-157">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="f8498-157">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)
