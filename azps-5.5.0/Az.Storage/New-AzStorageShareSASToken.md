---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: 8dbb6f79a61d388aec033030de471092fa16ba77
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207778"
---
# <span data-ttu-id="2afe0-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="2afe0-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="2afe0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2afe0-102">SYNOPSIS</span></span>
<span data-ttu-id="2afe0-103">Generare il token della firma di accesso condiviso per la condivisione di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2afe0-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="2afe0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2afe0-104">SYNTAX</span></span>

### <span data-ttu-id="2afe0-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="2afe0-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2afe0-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="2afe0-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2afe0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2afe0-107">DESCRIPTION</span></span>
<span data-ttu-id="2afe0-108">Il cmdlet **New-AzStorageShareSASToken genera** un token di firma di accesso condiviso per una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2afe0-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="2afe0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2afe0-109">EXAMPLES</span></span>

### <span data-ttu-id="2afe0-110">Esempio 1: Generare un token di firma di accesso condiviso per una condivisione</span><span class="sxs-lookup"><span data-stu-id="2afe0-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="2afe0-111">Questo comando crea un token di firma di accesso condiviso per la condivisione denominata ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="2afe0-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="2afe0-112">Esempio 2: Generare più token di firma di accesso condiviso tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="2afe0-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="2afe0-113">Questo comando recupera tutte le condivisioni di archiviazione che corrispondono al test del prefisso.</span><span class="sxs-lookup"><span data-stu-id="2afe0-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="2afe0-114">Il comando li passa al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="2afe0-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2afe0-115">Il cmdlet corrente crea un token di accesso condiviso per ogni condivisione di archiviazione che ha le autorizzazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="2afe0-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="2afe0-116">Esempio 3: Generare un token di firma di accesso condiviso che usa criteri di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="2afe0-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="2afe0-117">Questo comando crea un token di firma di accesso condiviso per la condivisione di archiviazione denominata ContosoShare il cui criterio è denominato ContosoPolicy03.</span><span class="sxs-lookup"><span data-stu-id="2afe0-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="2afe0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2afe0-118">PARAMETERS</span></span>

### <span data-ttu-id="2afe0-119">-Context</span><span class="sxs-lookup"><span data-stu-id="2afe0-119">-Context</span></span>
<span data-ttu-id="2afe0-120">Specifica un contesto di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2afe0-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="2afe0-121">Per ottenere un contesto, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2afe0-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2afe0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2afe0-122">-DefaultProfile</span></span>
<span data-ttu-id="2afe0-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2afe0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2afe0-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2afe0-124">-ExpiryTime</span></span>
<span data-ttu-id="2afe0-125">Specifica l'ora in cui la firma di accesso condiviso diventa non valida.</span><span class="sxs-lookup"><span data-stu-id="2afe0-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="2afe0-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="2afe0-126">-FullUri</span></span>
<span data-ttu-id="2afe0-127">Indica che questo cmdlet restituisce l'URI BLOB completo e il token di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="2afe0-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="2afe0-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="2afe0-128">-IPAddressOrRange</span></span>
<span data-ttu-id="2afe0-129">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="2afe0-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="2afe0-130">L'intervallo è inclusivo.</span><span class="sxs-lookup"><span data-stu-id="2afe0-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="2afe0-131">-Permission</span><span class="sxs-lookup"><span data-stu-id="2afe0-131">-Permission</span></span>
<span data-ttu-id="2afe0-132">Specifica le autorizzazioni nel token per accedere alla condivisione e ai file nella condivisione.</span><span class="sxs-lookup"><span data-stu-id="2afe0-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="2afe0-133">È importante notare che si tratta di una stringa, ad esempio `rwd` (per Lettura, Scrittura ed Elimina).</span><span class="sxs-lookup"><span data-stu-id="2afe0-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="2afe0-134">-Policy</span><span class="sxs-lookup"><span data-stu-id="2afe0-134">-Policy</span></span>
<span data-ttu-id="2afe0-135">Specifica i criteri di accesso archiviati per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="2afe0-135">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="2afe0-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="2afe0-136">-Protocol</span></span>
<span data-ttu-id="2afe0-137">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="2afe0-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="2afe0-138">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="2afe0-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="2afe0-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="2afe0-139">HttpsOnly</span></span>
* <span data-ttu-id="2afe0-140">HttpsOrHttp Il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="2afe0-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="2afe0-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2afe0-141">-ShareName</span></span>
<span data-ttu-id="2afe0-142">Specifica il nome della condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2afe0-142">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="2afe0-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2afe0-143">-StartTime</span></span>
<span data-ttu-id="2afe0-144">Specifica l'ora in cui la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="2afe0-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="2afe0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2afe0-145">CommonParameters</span></span>
<span data-ttu-id="2afe0-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2afe0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2afe0-147">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2afe0-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2afe0-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="2afe0-148">INPUTS</span></span>

### <span data-ttu-id="2afe0-149">System.String</span><span class="sxs-lookup"><span data-stu-id="2afe0-149">System.String</span></span>

### <span data-ttu-id="2afe0-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2afe0-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2afe0-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2afe0-151">OUTPUTS</span></span>

### <span data-ttu-id="2afe0-152">System.String</span><span class="sxs-lookup"><span data-stu-id="2afe0-152">System.String</span></span>

## <span data-ttu-id="2afe0-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="2afe0-153">NOTES</span></span>
* <span data-ttu-id="2afe0-154">Parole chiave: comuni, azure, servizi, dati, archiviazione, BLOB, coda, tabella</span><span class="sxs-lookup"><span data-stu-id="2afe0-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="2afe0-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2afe0-155">RELATED LINKS</span></span>

[<span data-ttu-id="2afe0-156">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="2afe0-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="2afe0-157">New-azStorageFilesASToken</span><span class="sxs-lookup"><span data-stu-id="2afe0-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
