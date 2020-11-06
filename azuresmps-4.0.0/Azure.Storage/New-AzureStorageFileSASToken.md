---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19d3017ffdff2ebc0f0c8d614b5b9c4d4b0514d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491441"
---
# <span data-ttu-id="3fadd-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="3fadd-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="3fadd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3fadd-102">SYNOPSIS</span></span>
<span data-ttu-id="3fadd-103">Genera un token della firma di accesso condiviso per un file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3fadd-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="3fadd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3fadd-104">SYNTAX</span></span>

### <span data-ttu-id="3fadd-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="3fadd-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="3fadd-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="3fadd-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="3fadd-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="3fadd-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### <span data-ttu-id="3fadd-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="3fadd-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## <span data-ttu-id="3fadd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fadd-109">DESCRIPTION</span></span>
<span data-ttu-id="3fadd-110">Il cmdlet **New-AzureStorageFileSASToken** genera un token della firma di accesso condiviso per un file di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3fadd-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="3fadd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3fadd-111">EXAMPLES</span></span>

### <span data-ttu-id="3fadd-112">Esempio 1: generare un token della firma di accesso condiviso con autorizzazioni di file completo</span><span class="sxs-lookup"><span data-stu-id="3fadd-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="3fadd-113">Questo comando genera un token della firma di accesso condiviso con le autorizzazioni complete per il file denominato FilePath.</span><span class="sxs-lookup"><span data-stu-id="3fadd-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="3fadd-114">Esempio 2: generare un token della firma di accesso condiviso con un limite di tempo</span><span class="sxs-lookup"><span data-stu-id="3fadd-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="3fadd-115">Il primo comando crea un oggetto **DateTime** usando il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="3fadd-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="3fadd-116">Il comando Archivia l'ora corrente nella variabile $StartTime.</span><span class="sxs-lookup"><span data-stu-id="3fadd-116">The command stores the current time in the $StartTime variable.</span></span>

<span data-ttu-id="3fadd-117">Il secondo comando aggiunge due ore all'oggetto in $StartTime e quindi archivia il risultato nella variabile $EndTime.</span><span class="sxs-lookup"><span data-stu-id="3fadd-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="3fadd-118">Questo oggetto è un tempo di due ore nel futuro.</span><span class="sxs-lookup"><span data-stu-id="3fadd-118">This object is a time two hours in the future.</span></span>

<span data-ttu-id="3fadd-119">Il terzo comando genera un token della firma di accesso condiviso con le autorizzazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="3fadd-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="3fadd-120">Questo token diventa valido in corrispondenza dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3fadd-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="3fadd-121">Il token rimane valido fino a quando non viene archiviato il tempo in $EndTime.</span><span class="sxs-lookup"><span data-stu-id="3fadd-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="3fadd-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3fadd-122">PARAMETERS</span></span>

### <span data-ttu-id="3fadd-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3fadd-123">-Context</span></span>
<span data-ttu-id="3fadd-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3fadd-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="3fadd-125">Per ottenere un contesto, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3fadd-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fadd-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3fadd-126">-ExpiryTime</span></span>
<span data-ttu-id="3fadd-127">Specifica il momento in cui la firma di accesso condiviso diventa non valida.</span><span class="sxs-lookup"><span data-stu-id="3fadd-127">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="3fadd-128">-File</span><span class="sxs-lookup"><span data-stu-id="3fadd-128">-File</span></span>
<span data-ttu-id="3fadd-129">Specifica un oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="3fadd-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="3fadd-130">È possibile creare un file cloud o ottenerne uno usando il cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="3fadd-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fadd-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="3fadd-131">-FullUri</span></span>
<span data-ttu-id="3fadd-132">Indica che questo cmdlet restituisce l'URI BLOB completo e il token della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="3fadd-132">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="3fadd-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3fadd-133">-IPAddressOrRange</span></span>
<span data-ttu-id="3fadd-134">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="3fadd-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="3fadd-135">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="3fadd-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="3fadd-136">-Path</span><span class="sxs-lookup"><span data-stu-id="3fadd-136">-Path</span></span>
<span data-ttu-id="3fadd-137">Specifica il percorso del file relativo a una condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3fadd-137">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fadd-138">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="3fadd-138">-Permission</span></span>
<span data-ttu-id="3fadd-139">Specifica le autorizzazioni per un file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3fadd-139">Specifies the permissions for a Storage file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fadd-140">-Policy</span><span class="sxs-lookup"><span data-stu-id="3fadd-140">-Policy</span></span>
<span data-ttu-id="3fadd-141">Specifica i criteri di accesso archiviati per un file.</span><span class="sxs-lookup"><span data-stu-id="3fadd-141">Specifies the stored access policy for a file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fadd-142">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="3fadd-142">-Protocol</span></span>
<span data-ttu-id="3fadd-143">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="3fadd-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="3fadd-144">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3fadd-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="3fadd-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3fadd-145">HttpsOnly</span></span>
* <span data-ttu-id="3fadd-146">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="3fadd-146">HttpsOrHttp</span></span>

<span data-ttu-id="3fadd-147">Il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="3fadd-147">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="3fadd-148">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3fadd-148">-ShareName</span></span>
<span data-ttu-id="3fadd-149">Specifica il nome della condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3fadd-149">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fadd-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3fadd-150">-StartTime</span></span>
<span data-ttu-id="3fadd-151">Specifica il momento in cui la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="3fadd-151">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="3fadd-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fadd-152">CommonParameters</span></span>
<span data-ttu-id="3fadd-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fadd-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fadd-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fadd-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fadd-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3fadd-155">INPUTS</span></span>

## <span data-ttu-id="3fadd-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3fadd-156">OUTPUTS</span></span>

## <span data-ttu-id="3fadd-157">Note</span><span class="sxs-lookup"><span data-stu-id="3fadd-157">NOTES</span></span>

## <span data-ttu-id="3fadd-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3fadd-158">RELATED LINKS</span></span>

[<span data-ttu-id="3fadd-159">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3fadd-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3fadd-160">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="3fadd-160">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
