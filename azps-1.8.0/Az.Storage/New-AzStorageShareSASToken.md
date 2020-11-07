---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: 0fc159773b54e8eba39fc3fe5ca45a2559c1521c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676558"
---
# <span data-ttu-id="31128-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="31128-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="31128-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31128-102">SYNOPSIS</span></span>
<span data-ttu-id="31128-103">Genera il token della firma di accesso condiviso per la condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="31128-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="31128-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31128-104">SYNTAX</span></span>

### <span data-ttu-id="31128-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="31128-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31128-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="31128-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31128-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31128-107">DESCRIPTION</span></span>
<span data-ttu-id="31128-108">Il cmdlet **New-AzStorageShareSASToken** genera un token della firma di accesso condiviso per una condivisione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="31128-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="31128-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31128-109">EXAMPLES</span></span>

### <span data-ttu-id="31128-110">Esempio 1: generare un token della firma di accesso condiviso per una condivisione</span><span class="sxs-lookup"><span data-stu-id="31128-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="31128-111">Questo comando crea un token della firma di accesso condiviso per la condivisione denominata ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="31128-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="31128-112">Esempio 2: generare più token della firma di accesso condiviso tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="31128-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="31128-113">Questo comando consente di ottenere tutte le condivisioni di archiviazione corrispondenti al test del prefisso.</span><span class="sxs-lookup"><span data-stu-id="31128-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="31128-114">Il comando li passa al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="31128-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="31128-115">Il cmdlet Current crea un token di accesso condiviso per ogni condivisione di archiviazione con le autorizzazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="31128-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="31128-116">Esempio 3: generare un token della firma di accesso condiviso che usa un criterio di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="31128-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="31128-117">Questo comando crea un token della firma di accesso condiviso per la condivisione di archiviazione denominata ContosoShare con il criterio denominato ContosoPolicy03.</span><span class="sxs-lookup"><span data-stu-id="31128-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="31128-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31128-118">PARAMETERS</span></span>

### <span data-ttu-id="31128-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="31128-119">-Context</span></span>
<span data-ttu-id="31128-120">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="31128-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="31128-121">Per ottenere un contesto, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="31128-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="31128-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31128-122">-DefaultProfile</span></span>
<span data-ttu-id="31128-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31128-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31128-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="31128-124">-ExpiryTime</span></span>
<span data-ttu-id="31128-125">Specifica il momento in cui la firma di accesso condiviso diventa non valida.</span><span class="sxs-lookup"><span data-stu-id="31128-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="31128-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="31128-126">-FullUri</span></span>
<span data-ttu-id="31128-127">Indica che questo cmdlet restituisce l'URI BLOB completo e il token della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="31128-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="31128-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="31128-128">-IPAddressOrRange</span></span>
<span data-ttu-id="31128-129">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="31128-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="31128-130">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="31128-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="31128-131">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="31128-131">-Permission</span></span>
<span data-ttu-id="31128-132">Specifica le autorizzazioni nel token per accedere alla condivisione e ai file sotto la condivisione.</span><span class="sxs-lookup"><span data-stu-id="31128-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="31128-133">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="31128-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="31128-134">-Policy</span><span class="sxs-lookup"><span data-stu-id="31128-134">-Policy</span></span>
<span data-ttu-id="31128-135">Specifica i criteri di accesso archiviati per una condivisione.</span><span class="sxs-lookup"><span data-stu-id="31128-135">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="31128-136">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="31128-136">-Protocol</span></span>
<span data-ttu-id="31128-137">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="31128-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="31128-138">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="31128-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="31128-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="31128-139">HttpsOnly</span></span>
* <span data-ttu-id="31128-140">HttpsOrHttp il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="31128-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="31128-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="31128-141">-ShareName</span></span>
<span data-ttu-id="31128-142">Specifica il nome della condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="31128-142">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="31128-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="31128-143">-StartTime</span></span>
<span data-ttu-id="31128-144">Specifica il momento in cui la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="31128-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="31128-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31128-145">CommonParameters</span></span>
<span data-ttu-id="31128-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31128-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31128-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31128-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31128-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31128-148">INPUTS</span></span>

### <span data-ttu-id="31128-149">System. String</span><span class="sxs-lookup"><span data-stu-id="31128-149">System.String</span></span>

### <span data-ttu-id="31128-150">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="31128-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="31128-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31128-151">OUTPUTS</span></span>

### <span data-ttu-id="31128-152">System. String</span><span class="sxs-lookup"><span data-stu-id="31128-152">System.String</span></span>

## <span data-ttu-id="31128-153">Note</span><span class="sxs-lookup"><span data-stu-id="31128-153">NOTES</span></span>
* <span data-ttu-id="31128-154">Parole chiave: comuni, Azure, servizi, dati, archiviazione, BLOB, coda, tabella</span><span class="sxs-lookup"><span data-stu-id="31128-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="31128-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31128-155">RELATED LINKS</span></span>

[<span data-ttu-id="31128-156">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="31128-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="31128-157">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="31128-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
