---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
ms.openlocfilehash: 0e8ad44ebbd8a5585626de27317caa14b408f87a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519493"
---
# <span data-ttu-id="b6bf1-101">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="b6bf1-101">New-AzureStorageContainerSASToken</span></span>

## <span data-ttu-id="b6bf1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="b6bf1-103">Genera un token SAS per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-103">Generates an SAS token for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6bf1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6bf1-104">SYNTAX</span></span>

### <span data-ttu-id="b6bf1-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="b6bf1-105">SasPolicy</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="b6bf1-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="b6bf1-106">SasPermission</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="b6bf1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6bf1-107">DESCRIPTION</span></span>
<span data-ttu-id="b6bf1-108">Il cmdlet **New-AzureStorageContainerSASToken** genera un token SAS (Shared Access Signature) per un contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-108">The **New-AzureStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="b6bf1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6bf1-109">EXAMPLES</span></span>

### <span data-ttu-id="b6bf1-110">Esempio 1: generare un token SAS contenitore con l'autorizzazione contenitore completo</span><span class="sxs-lookup"><span data-stu-id="b6bf1-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="b6bf1-111">Questo esempio genera un token SAS contenitore con l'autorizzazione contenitore completo.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="b6bf1-112">Esempio 2: generare più token SAS contenitore tramite pipeline</span><span class="sxs-lookup"><span data-stu-id="b6bf1-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="b6bf1-113">Questo esempio genera più token SAS contenitore usando la pipeline.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="b6bf1-114">Esempio 3: generare il token SAS contenitore con i criteri di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="b6bf1-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="b6bf1-115">Questo esempio genera un token SAS contenitore con criteri di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="b6bf1-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6bf1-116">PARAMETERS</span></span>

### <span data-ttu-id="b6bf1-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b6bf1-117">-Context</span></span>
<span data-ttu-id="b6bf1-118">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b6bf1-119">Puoi crearlo usando il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-119">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b6bf1-120">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b6bf1-120">-ExpiryTime</span></span>
<span data-ttu-id="b6bf1-121">Specifica il momento in cui la firma di accesso condiviso diventa non valida.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-121">Specifies the time at which the shared access signature becomes invalid.</span></span>

<span data-ttu-id="b6bf1-122">Se l'utente imposta l'ora di inizio ma non quella di scadenza, l'ora di scadenza viene impostata sull'ora di inizio più un'ora.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-122">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="b6bf1-123">Se non viene specificato né l'ora di inizio né l'ora di scadenza, il tempo di scadenza viene impostato sull'ora corrente e su un orario.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-123">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="b6bf1-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="b6bf1-124">-FullUri</span></span>
<span data-ttu-id="b6bf1-125">Indica che questo cmdlet restituisce l'URI BLOB completo e il token della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="b6bf1-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="b6bf1-126">-IPAddressOrRange</span></span>
<span data-ttu-id="b6bf1-127">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="b6bf1-128">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="b6bf1-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6bf1-129">-Name</span></span>
<span data-ttu-id="b6bf1-130">Specifica un nome di contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-130">Specifies an Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6bf1-131">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="b6bf1-131">-Permission</span></span>
<span data-ttu-id="b6bf1-132">Specifica le autorizzazioni per un contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-132">Specifies permissions for a storage container.</span></span>

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

### <span data-ttu-id="b6bf1-133">-Policy</span><span class="sxs-lookup"><span data-stu-id="b6bf1-133">-Policy</span></span>
<span data-ttu-id="b6bf1-134">Specifica un criterio di accesso archiviato in Azure.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-134">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="b6bf1-135">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="b6bf1-135">-Protocol</span></span>
<span data-ttu-id="b6bf1-136">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-136">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="b6bf1-137">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b6bf1-137">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="b6bf1-138">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b6bf1-138">HttpsOnly</span></span>
* <span data-ttu-id="b6bf1-139">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="b6bf1-139">HttpsOrHttp</span></span>

<span data-ttu-id="b6bf1-140">Il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-140">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="b6bf1-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b6bf1-141">-StartTime</span></span>
<span data-ttu-id="b6bf1-142">Specifica il momento in cui la firma di accesso condiviso diventa valida.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="b6bf1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6bf1-143">CommonParameters</span></span>
<span data-ttu-id="b6bf1-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6bf1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6bf1-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6bf1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6bf1-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6bf1-146">INPUTS</span></span>

### <span data-ttu-id="b6bf1-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b6bf1-147">IStorageContext</span></span>

<span data-ttu-id="b6bf1-148">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b6bf1-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="b6bf1-149">Stringa</span><span class="sxs-lookup"><span data-stu-id="b6bf1-149">String</span></span>

<span data-ttu-id="b6bf1-150">Il parametro "Name" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b6bf1-150">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="b6bf1-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6bf1-151">OUTPUTS</span></span>

### <span data-ttu-id="b6bf1-152">System. String</span><span class="sxs-lookup"><span data-stu-id="b6bf1-152">System.String</span></span>

## <span data-ttu-id="b6bf1-153">Note</span><span class="sxs-lookup"><span data-stu-id="b6bf1-153">NOTES</span></span>

## <span data-ttu-id="b6bf1-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6bf1-154">RELATED LINKS</span></span>

[<span data-ttu-id="b6bf1-155">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b6bf1-155">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)
