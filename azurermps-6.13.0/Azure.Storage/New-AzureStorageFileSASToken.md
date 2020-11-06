---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
ms.openlocfilehash: 66c89b70b80cf56471e5d12aec975e4e568d5a1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517775"
---
# <span data-ttu-id="83321-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="83321-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="83321-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83321-102">SYNOPSIS</span></span>
<span data-ttu-id="83321-103">Genera un token della firma di accesso condiviso per un file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="83321-103">Generates a shared access signature token for a Storage file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83321-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83321-104">SYNTAX</span></span>

### <span data-ttu-id="83321-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="83321-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83321-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="83321-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83321-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="83321-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83321-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="83321-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83321-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83321-109">DESCRIPTION</span></span>
<span data-ttu-id="83321-110">Il cmdlet **New-AzureStorageFileSASToken** genera un token della firma di accesso condiviso per un file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="83321-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="83321-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83321-111">EXAMPLES</span></span>

### <span data-ttu-id="83321-112">Esempio 1: generare un token della firma di accesso condiviso con autorizzazioni di file completo</span><span class="sxs-lookup"><span data-stu-id="83321-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="83321-113">Questo comando genera un token della firma di accesso condiviso con le autorizzazioni complete per il file denominato FilePath.</span><span class="sxs-lookup"><span data-stu-id="83321-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="83321-114">Esempio 2: generare un token della firma di accesso condiviso con un limite di tempo</span><span class="sxs-lookup"><span data-stu-id="83321-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="83321-115">Il primo comando crea un oggetto **DateTime** usando il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="83321-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="83321-116">Il comando Archivia l'ora corrente nella variabile $StartTime.</span><span class="sxs-lookup"><span data-stu-id="83321-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="83321-117">Il secondo comando aggiunge due ore all'oggetto in $StartTime e quindi archivia il risultato nella variabile $EndTime.</span><span class="sxs-lookup"><span data-stu-id="83321-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="83321-118">Questo oggetto è un tempo di due ore nel futuro.</span><span class="sxs-lookup"><span data-stu-id="83321-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="83321-119">Il terzo comando genera un token della firma di accesso condiviso con le autorizzazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="83321-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="83321-120">Questo token diventa valido in corrispondenza dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="83321-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="83321-121">Il token rimane valido fino a quando non viene archiviato il tempo in $EndTime.</span><span class="sxs-lookup"><span data-stu-id="83321-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="83321-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83321-122">PARAMETERS</span></span>

### <span data-ttu-id="83321-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="83321-123">-Context</span></span>
<span data-ttu-id="83321-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="83321-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="83321-125">Per ottenere un contesto, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="83321-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83321-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83321-126">-DefaultProfile</span></span>
<span data-ttu-id="83321-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83321-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83321-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="83321-128">-ExpiryTime</span></span>
<span data-ttu-id="83321-129">Specifica il momento in cui la firma di accesso condiviso diventa non valida.</span><span class="sxs-lookup"><span data-stu-id="83321-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="83321-130">-File</span><span class="sxs-lookup"><span data-stu-id="83321-130">-File</span></span>
<span data-ttu-id="83321-131">Specifica un oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="83321-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="83321-132">È possibile creare un file cloud o ottenerne uno usando il cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="83321-132">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83321-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="83321-133">-FullUri</span></span>
<span data-ttu-id="83321-134">Indica che questo cmdlet restituisce l'URI BLOB completo e il token della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="83321-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="83321-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="83321-135">-IPAddressOrRange</span></span>
<span data-ttu-id="83321-136">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="83321-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="83321-137">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="83321-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="83321-138">-Path</span><span class="sxs-lookup"><span data-stu-id="83321-138">-Path</span></span>
<span data-ttu-id="83321-139">Specifica il percorso del file relativo a una condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="83321-139">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83321-140">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="83321-140">-Permission</span></span>
<span data-ttu-id="83321-141">Specifica le autorizzazioni per un file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="83321-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="83321-142">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="83321-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83321-143">-Policy</span><span class="sxs-lookup"><span data-stu-id="83321-143">-Policy</span></span>
<span data-ttu-id="83321-144">Specifica i criteri di accesso archiviati per un file.</span><span class="sxs-lookup"><span data-stu-id="83321-144">Specifies the stored access policy for a file.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83321-145">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="83321-145">-Protocol</span></span>
<span data-ttu-id="83321-146">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="83321-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="83321-147">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="83321-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="83321-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="83321-148">HttpsOnly</span></span>
* <span data-ttu-id="83321-149">HttpsOrHttp il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="83321-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="83321-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="83321-150">-ShareName</span></span>
<span data-ttu-id="83321-151">Specifica il nome della condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="83321-151">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83321-152">-StartTime</span><span class="sxs-lookup"><span data-stu-id="83321-152">-StartTime</span></span>
<span data-ttu-id="83321-153">Specifica il momento in cui la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="83321-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="83321-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83321-154">CommonParameters</span></span>
<span data-ttu-id="83321-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83321-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83321-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83321-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83321-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83321-157">INPUTS</span></span>

### <span data-ttu-id="83321-158">System. String</span><span class="sxs-lookup"><span data-stu-id="83321-158">System.String</span></span>

### <span data-ttu-id="83321-159">Microsoft. WindowsAzure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="83321-159">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="83321-160">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="83321-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>
<span data-ttu-id="83321-161">Parameters: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="83321-161">Parameters: Context (ByValue)</span></span>

## <span data-ttu-id="83321-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83321-162">OUTPUTS</span></span>

### <span data-ttu-id="83321-163">System. String</span><span class="sxs-lookup"><span data-stu-id="83321-163">System.String</span></span>

## <span data-ttu-id="83321-164">Note</span><span class="sxs-lookup"><span data-stu-id="83321-164">NOTES</span></span>

## <span data-ttu-id="83321-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83321-165">RELATED LINKS</span></span>

[<span data-ttu-id="83321-166">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="83321-166">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="83321-167">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="83321-167">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
