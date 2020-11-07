---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
ms.openlocfilehash: 76ed7737acb26cd713aa84b26a743f3e5e43874f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686126"
---
# <span data-ttu-id="3237a-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="3237a-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="3237a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3237a-102">SYNOPSIS</span></span>
<span data-ttu-id="3237a-103">Genera un token SAS per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3237a-103">Generates an SAS token for an Azure Storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3237a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3237a-104">SYNTAX</span></span>

### <span data-ttu-id="3237a-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="3237a-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="3237a-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="3237a-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="3237a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3237a-107">DESCRIPTION</span></span>
<span data-ttu-id="3237a-108">Il cmdlet **New-AzureStorageTableSASToken** genera un token SAS (Shared Access Signature) per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3237a-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="3237a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3237a-109">EXAMPLES</span></span>

### <span data-ttu-id="3237a-110">Esempio 1: generare un token SAS con autorizzazioni complete per una tabella</span><span class="sxs-lookup"><span data-stu-id="3237a-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="3237a-111">Questo comando genera un token SAS con autorizzazioni complete per la tabella denominata ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="3237a-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="3237a-112">Il token è per le autorizzazioni di lettura, aggiunta, aggiornamento ed eliminazione.</span><span class="sxs-lookup"><span data-stu-id="3237a-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="3237a-113">Esempio 2: generare un token SAS per un intervallo di partizioni</span><span class="sxs-lookup"><span data-stu-id="3237a-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="3237a-114">Questo comando genera e token SAS con autorizzazioni complete per la tabella denominata ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="3237a-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="3237a-115">Il comando limita il token all'intervallo specificato dai parametri *StartPartitionKey* e *EndPartitionKey* .</span><span class="sxs-lookup"><span data-stu-id="3237a-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="3237a-116">Esempio 3: generare un token SAS con criteri di accesso archiviati per una tabella</span><span class="sxs-lookup"><span data-stu-id="3237a-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="3237a-117">Questo comando genera un token SAS per la tabella denominata ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="3237a-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="3237a-118">Il comando specifica i criteri di accesso archiviati denominati ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="3237a-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="3237a-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3237a-119">PARAMETERS</span></span>

### <span data-ttu-id="3237a-120">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3237a-120">-Context</span></span>
<span data-ttu-id="3237a-121">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3237a-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3237a-122">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3237a-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3237a-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="3237a-123">-EndPartitionKey</span></span>
<span data-ttu-id="3237a-124">Specifica la chiave di partizione della fine dell'intervallo per il token creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3237a-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3237a-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="3237a-125">-EndRowKey</span></span>
<span data-ttu-id="3237a-126">Specifica la chiave della riga per la fine dell'intervallo per il token creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3237a-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3237a-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3237a-127">-ExpiryTime</span></span>
<span data-ttu-id="3237a-128">Specifica quando scade il token SAS.</span><span class="sxs-lookup"><span data-stu-id="3237a-128">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="3237a-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="3237a-129">-FullUri</span></span>
<span data-ttu-id="3237a-130">Indica che questo cmdlet restituisce l'URI della coda completa con il token SAS.</span><span class="sxs-lookup"><span data-stu-id="3237a-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="3237a-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3237a-131">-IPAddressOrRange</span></span>
<span data-ttu-id="3237a-132">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="3237a-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="3237a-133">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="3237a-133">The range is inclusive.</span></span>

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

### <span data-ttu-id="3237a-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="3237a-134">-Name</span></span>
<span data-ttu-id="3237a-135">Specifica il nome di una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3237a-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="3237a-136">Questo cmdlet crea un token SAS per la tabella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3237a-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3237a-137">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="3237a-137">-Permission</span></span>
<span data-ttu-id="3237a-138">Specifica le autorizzazioni per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3237a-138">Specifies permissions for an Azure Storage table.</span></span>

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

### <span data-ttu-id="3237a-139">-Policy</span><span class="sxs-lookup"><span data-stu-id="3237a-139">-Policy</span></span>
<span data-ttu-id="3237a-140">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS.</span><span class="sxs-lookup"><span data-stu-id="3237a-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="3237a-141">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="3237a-141">-Protocol</span></span>
<span data-ttu-id="3237a-142">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="3237a-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="3237a-143">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3237a-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="3237a-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3237a-144">HttpsOnly</span></span>
* <span data-ttu-id="3237a-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="3237a-145">HttpsOrHttp</span></span>

<span data-ttu-id="3237a-146">Il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="3237a-146">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="3237a-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="3237a-147">-StartPartitionKey</span></span>
<span data-ttu-id="3237a-148">Specifica la chiave di partizione dell'inizio dell'intervallo per il token creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3237a-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3237a-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="3237a-149">-StartRowKey</span></span>
<span data-ttu-id="3237a-150">Specifica la chiave di riga per l'inizio dell'intervallo per il token creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3237a-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3237a-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3237a-151">-StartTime</span></span>
<span data-ttu-id="3237a-152">Specifica quando il token SAS diventa valido.</span><span class="sxs-lookup"><span data-stu-id="3237a-152">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="3237a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3237a-153">CommonParameters</span></span>
<span data-ttu-id="3237a-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3237a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3237a-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3237a-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3237a-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3237a-156">INPUTS</span></span>

### <span data-ttu-id="3237a-157">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3237a-157">IStorageContext</span></span>

<span data-ttu-id="3237a-158">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3237a-158">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="3237a-159">Stringa</span><span class="sxs-lookup"><span data-stu-id="3237a-159">String</span></span>

<span data-ttu-id="3237a-160">Il parametro "Name" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3237a-160">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="3237a-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3237a-161">OUTPUTS</span></span>

### <span data-ttu-id="3237a-162">System. String</span><span class="sxs-lookup"><span data-stu-id="3237a-162">System.String</span></span>

## <span data-ttu-id="3237a-163">Note</span><span class="sxs-lookup"><span data-stu-id="3237a-163">NOTES</span></span>

## <span data-ttu-id="3237a-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3237a-164">RELATED LINKS</span></span>

[<span data-ttu-id="3237a-165">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3237a-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
