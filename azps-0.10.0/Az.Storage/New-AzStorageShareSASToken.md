---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: 3def59e143627b57e6a9f403283082a315584aa2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862129"
---
# <span data-ttu-id="8fea5-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="8fea5-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="8fea5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8fea5-102">SYNOPSIS</span></span>
<span data-ttu-id="8fea5-103">Genera il token della firma di accesso condiviso per la condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8fea5-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="8fea5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8fea5-104">SYNTAX</span></span>

### <span data-ttu-id="8fea5-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="8fea5-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fea5-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="8fea5-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fea5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fea5-107">DESCRIPTION</span></span>
<span data-ttu-id="8fea5-108">Il cmdlet **New-AzStorageShareSASToken** genera un token della firma di accesso condiviso per una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8fea5-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="8fea5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8fea5-109">EXAMPLES</span></span>

### <span data-ttu-id="8fea5-110">Esempio 1: generare un token della firma di accesso condiviso per una condivisione</span><span class="sxs-lookup"><span data-stu-id="8fea5-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="8fea5-111">Questo comando crea un token della firma di accesso condiviso per la condivisione denominata ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="8fea5-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="8fea5-112">Esempio 2: generare più token della firma di accesso condiviso tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="8fea5-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="8fea5-113">Questo comando consente di ottenere tutte le condivisioni di archiviazione corrispondenti al test del prefisso.</span><span class="sxs-lookup"><span data-stu-id="8fea5-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="8fea5-114">Il comando li passa al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="8fea5-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8fea5-115">Il cmdlet Current crea un token di accesso condiviso per ogni condivisione di archiviazione con le autorizzazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="8fea5-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="8fea5-116">Esempio 3: generare un token della firma di accesso condiviso che usa un criterio di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="8fea5-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="8fea5-117">Questo comando crea un token della firma di accesso condiviso per la condivisione di archiviazione denominata ContosoShare con il criterio denominato ContosoPolicy03.</span><span class="sxs-lookup"><span data-stu-id="8fea5-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="8fea5-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8fea5-118">PARAMETERS</span></span>

### <span data-ttu-id="8fea5-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="8fea5-119">-Context</span></span>
<span data-ttu-id="8fea5-120">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8fea5-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="8fea5-121">Per ottenere un contesto, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="8fea5-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8fea5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fea5-122">-DefaultProfile</span></span>
<span data-ttu-id="8fea5-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8fea5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fea5-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8fea5-124">-ExpiryTime</span></span>
<span data-ttu-id="8fea5-125">Specifica il momento in cui la firma di accesso condiviso diventa non valida.</span><span class="sxs-lookup"><span data-stu-id="8fea5-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="8fea5-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="8fea5-126">-FullUri</span></span>
<span data-ttu-id="8fea5-127">Indica che questo cmdlet restituisce l'URI BLOB completo e il token della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="8fea5-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="8fea5-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="8fea5-128">-IPAddressOrRange</span></span>
<span data-ttu-id="8fea5-129">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="8fea5-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="8fea5-130">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="8fea5-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="8fea5-131">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="8fea5-131">-Permission</span></span>
<span data-ttu-id="8fea5-132">Specifica le autorizzazioni nel token per accedere alla condivisione e ai file sotto la condivisione.</span><span class="sxs-lookup"><span data-stu-id="8fea5-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="8fea5-133">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="8fea5-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="8fea5-134">-Policy</span><span class="sxs-lookup"><span data-stu-id="8fea5-134">-Policy</span></span>
<span data-ttu-id="8fea5-135">Specifica i criteri di accesso archiviati per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="8fea5-135">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="8fea5-136">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="8fea5-136">-Protocol</span></span>
<span data-ttu-id="8fea5-137">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="8fea5-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="8fea5-138">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8fea5-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="8fea5-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8fea5-139">HttpsOnly</span></span>
* <span data-ttu-id="8fea5-140">HttpsOrHttp il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="8fea5-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAz.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fea5-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8fea5-141">-ShareName</span></span>
<span data-ttu-id="8fea5-142">Specifica il nome della condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8fea5-142">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fea5-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8fea5-143">-StartTime</span></span>
<span data-ttu-id="8fea5-144">Specifica il momento in cui la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="8fea5-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="8fea5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fea5-145">CommonParameters</span></span>
<span data-ttu-id="8fea5-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fea5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fea5-147">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fea5-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fea5-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8fea5-148">INPUTS</span></span>

### <span data-ttu-id="8fea5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="8fea5-149">System.String</span></span>

### <span data-ttu-id="8fea5-150">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8fea5-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8fea5-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8fea5-151">OUTPUTS</span></span>

### <span data-ttu-id="8fea5-152">System. String</span><span class="sxs-lookup"><span data-stu-id="8fea5-152">System.String</span></span>

## <span data-ttu-id="8fea5-153">Note</span><span class="sxs-lookup"><span data-stu-id="8fea5-153">NOTES</span></span>
* <span data-ttu-id="8fea5-154">Parole chiave: comuni, Azure, servizi, dati, archiviazione, BLOB, coda, tabella</span><span class="sxs-lookup"><span data-stu-id="8fea5-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="8fea5-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8fea5-155">RELATED LINKS</span></span>

[<span data-ttu-id="8fea5-156">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="8fea5-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="8fea5-157">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="8fea5-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
