---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: bf17a44b4f67d545ed464670776a5fc4c81b315a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479411"
---
# <span data-ttu-id="c5aba-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="c5aba-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="c5aba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5aba-102">SYNOPSIS</span></span>
<span data-ttu-id="c5aba-103">Genera un token SAS per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c5aba-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="c5aba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5aba-104">SYNTAX</span></span>

### <span data-ttu-id="c5aba-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="c5aba-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5aba-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="c5aba-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5aba-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5aba-107">DESCRIPTION</span></span>
<span data-ttu-id="c5aba-108">Il cmdlet **New-AzStorageTableSASToken** genera un token SAS (Shared Access Signature) per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c5aba-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="c5aba-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5aba-109">EXAMPLES</span></span>

### <span data-ttu-id="c5aba-110">Esempio 1: generare un token SAS con autorizzazioni complete per una tabella</span><span class="sxs-lookup"><span data-stu-id="c5aba-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="c5aba-111">Questo comando genera un token SAS con autorizzazioni complete per la tabella denominata ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="c5aba-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="c5aba-112">Il token è per le autorizzazioni di lettura, aggiunta, aggiornamento ed eliminazione.</span><span class="sxs-lookup"><span data-stu-id="c5aba-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="c5aba-113">Esempio 2: generare un token SAS per un intervallo di partizioni</span><span class="sxs-lookup"><span data-stu-id="c5aba-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="c5aba-114">Questo comando genera e token SAS con autorizzazioni complete per la tabella denominata ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="c5aba-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="c5aba-115">Il comando limita il token all'intervallo specificato dai parametri *StartPartitionKey* e *EndPartitionKey* .</span><span class="sxs-lookup"><span data-stu-id="c5aba-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="c5aba-116">Esempio 3: generare un token SAS con criteri di accesso archiviati per una tabella</span><span class="sxs-lookup"><span data-stu-id="c5aba-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="c5aba-117">Questo comando genera un token SAS per la tabella denominata ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="c5aba-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="c5aba-118">Il comando specifica i criteri di accesso archiviati denominati ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="c5aba-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="c5aba-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5aba-119">PARAMETERS</span></span>

### <span data-ttu-id="c5aba-120">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c5aba-120">-Context</span></span>
<span data-ttu-id="c5aba-121">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c5aba-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c5aba-122">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c5aba-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c5aba-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5aba-123">-DefaultProfile</span></span>
<span data-ttu-id="c5aba-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5aba-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5aba-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="c5aba-125">-EndPartitionKey</span></span>
<span data-ttu-id="c5aba-126">Specifica la chiave di partizione della fine dell'intervallo per il token creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5aba-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5aba-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="c5aba-127">-EndRowKey</span></span>
<span data-ttu-id="c5aba-128">Specifica la chiave della riga per la fine dell'intervallo per il token creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5aba-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5aba-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c5aba-129">-ExpiryTime</span></span>
<span data-ttu-id="c5aba-130">Specifica quando scade il token SAS.</span><span class="sxs-lookup"><span data-stu-id="c5aba-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="c5aba-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="c5aba-131">-FullUri</span></span>
<span data-ttu-id="c5aba-132">Indica che questo cmdlet restituisce l'URI della coda completa con il token SAS.</span><span class="sxs-lookup"><span data-stu-id="c5aba-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="c5aba-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c5aba-133">-IPAddressOrRange</span></span>
<span data-ttu-id="c5aba-134">Specifica l'indirizzo IP o l'intervallo di indirizzi IP da cui accettare le richieste, ad esempio 168.1.5.65 o 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="c5aba-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="c5aba-135">L'intervallo è incluso.</span><span class="sxs-lookup"><span data-stu-id="c5aba-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="c5aba-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5aba-136">-Name</span></span>
<span data-ttu-id="c5aba-137">Specifica il nome di una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c5aba-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="c5aba-138">Questo cmdlet crea un token SAS per la tabella specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c5aba-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5aba-139">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="c5aba-139">-Permission</span></span>
<span data-ttu-id="c5aba-140">Specifica le autorizzazioni per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c5aba-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="c5aba-141">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="c5aba-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="c5aba-142">-Policy</span><span class="sxs-lookup"><span data-stu-id="c5aba-142">-Policy</span></span>
<span data-ttu-id="c5aba-143">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS.</span><span class="sxs-lookup"><span data-stu-id="c5aba-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="c5aba-144">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="c5aba-144">-Protocol</span></span>
<span data-ttu-id="c5aba-145">Specifica il protocollo consentito per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="c5aba-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="c5aba-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5aba-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="c5aba-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c5aba-147">HttpsOnly</span></span>
* <span data-ttu-id="c5aba-148">HttpsOrHttp il valore predefinito è HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="c5aba-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Cosmos.Table.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5aba-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="c5aba-149">-StartPartitionKey</span></span>
<span data-ttu-id="c5aba-150">Specifica la chiave di partizione dell'inizio dell'intervallo per il token creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5aba-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5aba-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="c5aba-151">-StartRowKey</span></span>
<span data-ttu-id="c5aba-152">Specifica la chiave di riga per l'inizio dell'intervallo per il token creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5aba-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5aba-153">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c5aba-153">-StartTime</span></span>
<span data-ttu-id="c5aba-154">Specifica quando il token SAS diventa valido.</span><span class="sxs-lookup"><span data-stu-id="c5aba-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="c5aba-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5aba-155">CommonParameters</span></span>
<span data-ttu-id="c5aba-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5aba-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5aba-157">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5aba-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5aba-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5aba-158">INPUTS</span></span>

### <span data-ttu-id="c5aba-159">System. String</span><span class="sxs-lookup"><span data-stu-id="c5aba-159">System.String</span></span>

### <span data-ttu-id="c5aba-160">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c5aba-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c5aba-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5aba-161">OUTPUTS</span></span>

### <span data-ttu-id="c5aba-162">System. String</span><span class="sxs-lookup"><span data-stu-id="c5aba-162">System.String</span></span>

## <span data-ttu-id="c5aba-163">Note</span><span class="sxs-lookup"><span data-stu-id="c5aba-163">NOTES</span></span>

## <span data-ttu-id="c5aba-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5aba-164">RELATED LINKS</span></span>

[<span data-ttu-id="c5aba-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c5aba-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
