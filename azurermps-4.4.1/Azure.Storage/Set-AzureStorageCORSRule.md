---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 9b3bc0f9a0d0345662f63ef8387239e0792057e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520839"
---
# <span data-ttu-id="d0041-101">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="d0041-101">Set-AzureStorageCORSRule</span></span>

## <span data-ttu-id="d0041-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0041-102">SYNOPSIS</span></span>
<span data-ttu-id="d0041-103">Imposta le regole di CORS per un tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d0041-103">Sets the CORS rules for a type of Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0041-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0041-104">SYNTAX</span></span>

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d0041-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0041-105">DESCRIPTION</span></span>
<span data-ttu-id="d0041-106">Il cmdlet **set-AzureStorageCORSRule** imposta le regole CORS (Cross-Origin Resource Sharing) per un tipo di servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d0041-106">The **Set-AzureStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="d0041-107">I tipi di servizi di archiviazione per questo cmdlet sono BLOB, Table, Queue e file.</span><span class="sxs-lookup"><span data-stu-id="d0041-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="d0041-108">Questo cmdlet sovrascrive le regole esistenti.</span><span class="sxs-lookup"><span data-stu-id="d0041-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="d0041-109">Per visualizzare le regole correnti, usare il cmdlet Get-AzureStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="d0041-109">To see the current rules, use the Get-AzureStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="d0041-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0041-110">EXAMPLES</span></span>

### <span data-ttu-id="d0041-111">Esempio 1: assegnare regole di CORS al servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="d0041-111">Example 1: Assign CORS rules to the blob service</span></span>
```
PS C:\>$CorsRules = (@{
    AllowedHeaders=@("x-ms-blob-content-type","x-ms-blob-content-disposition");
    AllowedOrigins=@("*");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Get","Connect")},
    @{
    AllowedOrigins=@("http://www.fabrikam.com","http://www.contoso.com"); 
    ExposedHeaders=@("x-ms-meta-data*","x-ms-meta-customheader"); 
    AllowedHeaders=@("x-ms-meta-target*","x-ms-meta-customheader");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Put")})
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="d0041-112">Il primo comando assegna una matrice di regole alla variabile $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="d0041-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="d0041-113">Questo comando USA standard si estende su più righe in questo blocco di codice.</span><span class="sxs-lookup"><span data-stu-id="d0041-113">This command uses standard extends over several lines in this code block.</span></span>

<span data-ttu-id="d0041-114">Il secondo comando assegna le regole in $CorsRules al tipo di servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="d0041-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="d0041-115">Esempio 2: modificare le proprietà di una regola CORS per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="d0041-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="d0041-116">Il primo comando ottiene le regole CORS correnti per il tipo di BLOB usando il cmdlet **Get-AzureStorageCORSRule** .</span><span class="sxs-lookup"><span data-stu-id="d0041-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzureStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="d0041-117">Il comando Archivia le regole nella variabile di matrice $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="d0041-117">The command stores the rules in the $CorsRules array variable.</span></span>

<span data-ttu-id="d0041-118">Il secondo e il terzo comando modificano la prima regola in $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="d0041-118">The second and third commands modify the first rule in $CorsRules.</span></span>

<span data-ttu-id="d0041-119">Il comando finale assegna le regole in $CorsRules al tipo di servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="d0041-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="d0041-120">Le regole modificate sovrascrivono le regole di CORS correnti.</span><span class="sxs-lookup"><span data-stu-id="d0041-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="d0041-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0041-121">PARAMETERS</span></span>

### <span data-ttu-id="d0041-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d0041-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d0041-123">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="d0041-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d0041-124">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d0041-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d0041-125">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="d0041-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0041-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d0041-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d0041-127">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="d0041-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d0041-128">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="d0041-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d0041-129">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="d0041-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d0041-130">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="d0041-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d0041-131">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="d0041-131">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0041-132">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d0041-132">-Context</span></span>
<span data-ttu-id="d0041-133">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d0041-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="d0041-134">Per ottenere un contesto, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d0041-134">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d0041-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="d0041-135">-CorsRules</span></span>
<span data-ttu-id="d0041-136">Specifica una matrice di regole CORS.</span><span class="sxs-lookup"><span data-stu-id="d0041-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="d0041-137">Puoi recuperare le regole esistenti usando il cmdlet Get-AzureStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="d0041-137">You can retrieve the existing rules using the Get-AzureStorageCORSRule cmdlet.</span></span>

```yaml
Type: PSCorsRule[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0041-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0041-138">-PassThru</span></span>
<span data-ttu-id="d0041-139">Indica che questo cmdlet restituisce un valore booleano che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d0041-139">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="d0041-140">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d0041-140">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d0041-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d0041-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d0041-142">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="d0041-142">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0041-143">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="d0041-143">-ServiceType</span></span>
<span data-ttu-id="d0041-144">Specifica il tipo di servizio di archiviazione di Azure per cui questo cmdlet assegna regole.</span><span class="sxs-lookup"><span data-stu-id="d0041-144">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="d0041-145">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d0041-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d0041-146">BLOB</span><span class="sxs-lookup"><span data-stu-id="d0041-146">Blob</span></span> 
- <span data-ttu-id="d0041-147">tavolo</span><span class="sxs-lookup"><span data-stu-id="d0041-147">Table</span></span> 
- <span data-ttu-id="d0041-148">Coda</span><span class="sxs-lookup"><span data-stu-id="d0041-148">Queue</span></span> 
- <span data-ttu-id="d0041-149">File</span><span class="sxs-lookup"><span data-stu-id="d0041-149">File</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0041-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0041-150">CommonParameters</span></span>
<span data-ttu-id="d0041-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0041-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0041-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0041-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0041-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0041-153">INPUTS</span></span>

### <span data-ttu-id="d0041-154">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d0041-154">IStorageContext</span></span>

<span data-ttu-id="d0041-155">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d0041-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="d0041-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0041-156">OUTPUTS</span></span>

### <span data-ttu-id="d0041-157">Microsoft. WindowsAzure. Commands. storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="d0041-157">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="d0041-158">Note</span><span class="sxs-lookup"><span data-stu-id="d0041-158">NOTES</span></span>

## <span data-ttu-id="d0041-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0041-159">RELATED LINKS</span></span>

[<span data-ttu-id="d0041-160">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="d0041-160">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="d0041-161">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d0041-161">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="d0041-162">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="d0041-162">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)


