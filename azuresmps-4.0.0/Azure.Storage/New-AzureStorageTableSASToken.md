---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: ''
schema: 2.0.0
ms.openlocfilehash: 39870fe9fe9ac4223bccf15908c960db29d25252
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507227"
---
# <span data-ttu-id="5ed56-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="5ed56-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="5ed56-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ed56-102">SYNOPSIS</span></span>
<span data-ttu-id="5ed56-103">Genera un token SAS per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ed56-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="5ed56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ed56-104">SYNTAX</span></span>

### <span data-ttu-id="5ed56-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="5ed56-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="5ed56-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="5ed56-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="5ed56-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ed56-107">DESCRIPTION</span></span>
<span data-ttu-id="5ed56-108">Il cmdlet **New-AzureStorageTableSASToken** genera un token SAS (Shared Access Signature) per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ed56-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="5ed56-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ed56-109">EXAMPLES</span></span>

### <span data-ttu-id="5ed56-110">Esempio 1: generare un token SAS con autorizzazioni complete per una tabella</span><span class="sxs-lookup"><span data-stu-id="5ed56-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="5ed56-111">Questo comando genera un token SAS con autorizzazioni complete per la tabella denominata ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="5ed56-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="5ed56-112">Il token è per le autorizzazioni di lettura, aggiunta, aggiornamento ed eliminazione.</span><span class="sxs-lookup"><span data-stu-id="5ed56-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="5ed56-113">Esempio 2: generare un token SAS per un intervallo di partizioni</span><span class="sxs-lookup"><span data-stu-id="5ed56-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="5ed56-114">Questo comando genera e token SAS con autorizzazioni complete per la tabella denominata ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="5ed56-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="5ed56-115">Il comando limita il token all'intervallo specificato dai parametri *StartPartitionKey* e *EndPartitionKey* .</span><span class="sxs-lookup"><span data-stu-id="5ed56-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="5ed56-116">Esempio 3: generare un token SAS con criteri di accesso archiviati per una tabella</span><span class="sxs-lookup"><span data-stu-id="5ed56-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="5ed56-117">Questo comando genera un token SAS per la tabella denominata ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="5ed56-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="5ed56-118">Il comando specifica i criteri di accesso archiviati denominati ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="5ed56-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="5ed56-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ed56-119">PARAMETERS</span></span>

### <span data-ttu-id="5ed56-120">-Contesto</span><span class="sxs-lookup"><span data-stu-id="5ed56-120">-Context</span></span>
<span data-ttu-id="5ed56-121">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ed56-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5ed56-122">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="5ed56-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5ed56-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="5ed56-123">-EndPartitionKey</span></span>
<span data-ttu-id="5ed56-124">Specifica la chiave di partizione della fine dell'intervallo per il token creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ed56-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5ed56-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="5ed56-125">-EndRowKey</span></span>
<span data-ttu-id="5ed56-126">Specifica la chiave della riga per la fine dell'intervallo per il token creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ed56-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5ed56-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5ed56-127">-ExpiryTime</span></span>
<span data-ttu-id="5ed56-128">Specifica quando scade il token SAS.</span><span class="sxs-lookup"><span data-stu-id="5ed56-128">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="5ed56-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="5ed56-129">-FullUri</span></span>
<span data-ttu-id="5ed56-130">Indica che questo cmdlet restituisce l'URI della coda completa con il token SAS.</span><span class="sxs-lookup"><span data-stu-id="5ed56-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="5ed56-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5ed56-131">-IPAddressOrRange</span></span>
<span data-ttu-id="5ed56-132">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="5ed56-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="5ed56-133">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="5ed56-133">The range is inclusive.</span></span>

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

### <span data-ttu-id="5ed56-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ed56-134">-Name</span></span>
<span data-ttu-id="5ed56-135">Specifica il nome di una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ed56-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="5ed56-136">Questo cmdlet crea un token SAS per la tabella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5ed56-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

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

### <span data-ttu-id="5ed56-137">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="5ed56-137">-Permission</span></span>
<span data-ttu-id="5ed56-138">Specifica le autorizzazioni per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ed56-138">Specifies permissions for an Azure Storage table.</span></span>

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

### <span data-ttu-id="5ed56-139">-Policy</span><span class="sxs-lookup"><span data-stu-id="5ed56-139">-Policy</span></span>
<span data-ttu-id="5ed56-140">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS.</span><span class="sxs-lookup"><span data-stu-id="5ed56-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="5ed56-141">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="5ed56-141">-Protocol</span></span>
<span data-ttu-id="5ed56-142">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="5ed56-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="5ed56-143">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5ed56-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="5ed56-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="5ed56-144">HttpsOnly</span></span>
* <span data-ttu-id="5ed56-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="5ed56-145">HttpsOrHttp</span></span>

<span data-ttu-id="5ed56-146">Il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="5ed56-146">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="5ed56-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="5ed56-147">-StartPartitionKey</span></span>
<span data-ttu-id="5ed56-148">Specifica la chiave di partizione dell'inizio dell'intervallo per il token creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ed56-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5ed56-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="5ed56-149">-StartRowKey</span></span>
<span data-ttu-id="5ed56-150">Specifica la chiave di riga per l'inizio dell'intervallo per il token creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ed56-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5ed56-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5ed56-151">-StartTime</span></span>
<span data-ttu-id="5ed56-152">Specifica quando il token SAS diventa valido.</span><span class="sxs-lookup"><span data-stu-id="5ed56-152">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="5ed56-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ed56-153">CommonParameters</span></span>
<span data-ttu-id="5ed56-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ed56-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ed56-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ed56-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ed56-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ed56-156">INPUTS</span></span>

## <span data-ttu-id="5ed56-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ed56-157">OUTPUTS</span></span>

## <span data-ttu-id="5ed56-158">Note</span><span class="sxs-lookup"><span data-stu-id="5ed56-158">NOTES</span></span>

## <span data-ttu-id="5ed56-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ed56-159">RELATED LINKS</span></span>

[<span data-ttu-id="5ed56-160">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5ed56-160">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
