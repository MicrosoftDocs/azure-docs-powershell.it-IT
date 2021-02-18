---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
ms.openlocfilehash: fcd58edbb3d6e03becc8e6305f58555fedf36107
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190838"
---
# <span data-ttu-id="65ffa-101">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="65ffa-101">New-AzStorageFileSASToken</span></span>

## <span data-ttu-id="65ffa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="65ffa-103">Genera un token di firma di accesso condiviso per un file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="65ffa-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="65ffa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65ffa-104">SYNTAX</span></span>

### <span data-ttu-id="65ffa-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="65ffa-105">NameSasPermission</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65ffa-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="65ffa-106">NameSasPolicy</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65ffa-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="65ffa-107">FileSasPermission</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65ffa-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="65ffa-108">FileSasPolicy</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65ffa-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="65ffa-109">DESCRIPTION</span></span>
<span data-ttu-id="65ffa-110">Il cmdlet **New-AzStorageFileSASToken** genera un token di firma di accesso condiviso per un file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="65ffa-110">The **New-AzStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="65ffa-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65ffa-111">EXAMPLES</span></span>

### <span data-ttu-id="65ffa-112">Esempio 1: Generare un token di firma di accesso condiviso con autorizzazioni file complete</span><span class="sxs-lookup"><span data-stu-id="65ffa-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="65ffa-113">Questo comando genera un token di firma di accesso condiviso con autorizzazioni complete per il file denominato FilePath.</span><span class="sxs-lookup"><span data-stu-id="65ffa-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="65ffa-114">Esempio 2: Generare un token di firma di accesso condiviso con un limite di tempo</span><span class="sxs-lookup"><span data-stu-id="65ffa-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="65ffa-115">Il primo comando crea un **oggetto DateTime** usando il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="65ffa-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="65ffa-116">Il comando archivia l'ora corrente nella $StartTime variabile.</span><span class="sxs-lookup"><span data-stu-id="65ffa-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="65ffa-117">Il secondo comando aggiunge due ore all'oggetto in $StartTime e quindi archivia il risultato nella $EndTime variabile.</span><span class="sxs-lookup"><span data-stu-id="65ffa-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="65ffa-118">Questo oggetto rappresenta un periodo di tempo futuro di due ore.</span><span class="sxs-lookup"><span data-stu-id="65ffa-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="65ffa-119">Il terzo comando genera un token di firma di accesso condiviso con le autorizzazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="65ffa-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="65ffa-120">Questo token diventa valido al momento corrente.</span><span class="sxs-lookup"><span data-stu-id="65ffa-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="65ffa-121">Il token rimane valido fino al tempo archiviato in $EndTime.</span><span class="sxs-lookup"><span data-stu-id="65ffa-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="65ffa-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65ffa-122">PARAMETERS</span></span>

### <span data-ttu-id="65ffa-123">-Context</span><span class="sxs-lookup"><span data-stu-id="65ffa-123">-Context</span></span>
<span data-ttu-id="65ffa-124">Specifica un contesto di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="65ffa-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="65ffa-125">Per ottenere un contesto, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="65ffa-125">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="65ffa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ffa-126">-DefaultProfile</span></span>
<span data-ttu-id="65ffa-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65ffa-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65ffa-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="65ffa-128">-ExpiryTime</span></span>
<span data-ttu-id="65ffa-129">Specifica l'ora in cui la firma di accesso condiviso diventa non valida.</span><span class="sxs-lookup"><span data-stu-id="65ffa-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="65ffa-130">-File</span><span class="sxs-lookup"><span data-stu-id="65ffa-130">-File</span></span>
<span data-ttu-id="65ffa-131">Specifica un **oggetto CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="65ffa-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="65ffa-132">È possibile creare un file cloud o ottenerne uno usando il cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="65ffa-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: CloudFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65ffa-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="65ffa-133">-FullUri</span></span>
<span data-ttu-id="65ffa-134">Indica che questo cmdlet restituisce l'URI BLOB completo e il token di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="65ffa-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="65ffa-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="65ffa-135">-IPAddressOrRange</span></span>
<span data-ttu-id="65ffa-136">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="65ffa-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="65ffa-137">L'intervallo è inclusivo.</span><span class="sxs-lookup"><span data-stu-id="65ffa-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="65ffa-138">-Path</span><span class="sxs-lookup"><span data-stu-id="65ffa-138">-Path</span></span>
<span data-ttu-id="65ffa-139">Specifica il percorso del file relativo a una condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="65ffa-139">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="65ffa-140">-Permission</span><span class="sxs-lookup"><span data-stu-id="65ffa-140">-Permission</span></span>
<span data-ttu-id="65ffa-141">Specifica le autorizzazioni per un file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="65ffa-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="65ffa-142">È importante notare che si tratta di una stringa, ad esempio `rwd` (per Lettura, Scrittura ed Elimina).</span><span class="sxs-lookup"><span data-stu-id="65ffa-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="65ffa-143">-Policy</span><span class="sxs-lookup"><span data-stu-id="65ffa-143">-Policy</span></span>
<span data-ttu-id="65ffa-144">Specifica i criteri di accesso archiviati per un file.</span><span class="sxs-lookup"><span data-stu-id="65ffa-144">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="65ffa-145">-Protocol</span><span class="sxs-lookup"><span data-stu-id="65ffa-145">-Protocol</span></span>
<span data-ttu-id="65ffa-146">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="65ffa-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="65ffa-147">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="65ffa-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="65ffa-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="65ffa-148">HttpsOnly</span></span>
* <span data-ttu-id="65ffa-149">HttpsOrHttp Il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="65ffa-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="65ffa-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="65ffa-150">-ShareName</span></span>
<span data-ttu-id="65ffa-151">Specifica il nome della condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="65ffa-151">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="65ffa-152">-StartTime</span><span class="sxs-lookup"><span data-stu-id="65ffa-152">-StartTime</span></span>
<span data-ttu-id="65ffa-153">Specifica l'ora in cui la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="65ffa-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="65ffa-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ffa-154">CommonParameters</span></span>
<span data-ttu-id="65ffa-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65ffa-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ffa-156">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65ffa-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ffa-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="65ffa-157">INPUTS</span></span>

### <span data-ttu-id="65ffa-158">System.String</span><span class="sxs-lookup"><span data-stu-id="65ffa-158">System.String</span></span>

### <span data-ttu-id="65ffa-159">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="65ffa-159">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="65ffa-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="65ffa-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="65ffa-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65ffa-161">OUTPUTS</span></span>

### <span data-ttu-id="65ffa-162">System.String</span><span class="sxs-lookup"><span data-stu-id="65ffa-162">System.String</span></span>

## <span data-ttu-id="65ffa-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="65ffa-163">NOTES</span></span>

## <span data-ttu-id="65ffa-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65ffa-164">RELATED LINKS</span></span>

[<span data-ttu-id="65ffa-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="65ffa-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="65ffa-166">New-azStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="65ffa-166">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)
