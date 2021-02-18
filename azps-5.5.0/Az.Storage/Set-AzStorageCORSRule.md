---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: d7951e53c7cbd8c799c7158bb3cc5c3fabb5b039
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190711"
---
# <span data-ttu-id="03dce-101">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="03dce-101">Set-AzStorageCORSRule</span></span>

## <span data-ttu-id="03dce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03dce-102">SYNOPSIS</span></span>
<span data-ttu-id="03dce-103">Imposta le regole CORS per un tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="03dce-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="03dce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03dce-104">SYNTAX</span></span>

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="03dce-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="03dce-105">DESCRIPTION</span></span>
<span data-ttu-id="03dce-106">Il cmdlet **Set-AzStorageCORSRule** imposta le regole di condivisione delle risorse tra origini (CORS) per un tipo di servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="03dce-106">The **Set-AzStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="03dce-107">I tipi di servizi di archiviazione per questo cmdlet sono BLOB, tabella, coda e file.</span><span class="sxs-lookup"><span data-stu-id="03dce-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="03dce-108">Questo cmdlet sovrascrive le regole esistenti.</span><span class="sxs-lookup"><span data-stu-id="03dce-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="03dce-109">Per visualizzare le regole correnti, usare il cmdlet Get-AzStorageCORSRule regola.</span><span class="sxs-lookup"><span data-stu-id="03dce-109">To see the current rules, use the Get-AzStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="03dce-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03dce-110">EXAMPLES</span></span>

### <span data-ttu-id="03dce-111">Esempio 1: Assegnare regole CORS al servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="03dce-111">Example 1: Assign CORS rules to the blob service</span></span>
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
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="03dce-112">Il primo comando assegna una matrice di regole alla $CorsRules variabile.</span><span class="sxs-lookup"><span data-stu-id="03dce-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="03dce-113">Questo comando usa l'estensione standard su più righe in questo blocco di codice.</span><span class="sxs-lookup"><span data-stu-id="03dce-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="03dce-114">Il secondo comando assegna le regole in $CorsRules al tipo di servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="03dce-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="03dce-115">Esempio 2: Modificare le proprietà di una regola CORS per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="03dce-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="03dce-116">Il primo comando ottiene le regole CORS correnti per il tipo di BLOB usando il cmdlet **Get-AzStorageCORSRule.**</span><span class="sxs-lookup"><span data-stu-id="03dce-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="03dce-117">Il comando archivia le regole nella variabile $CorsRules di matrice.</span><span class="sxs-lookup"><span data-stu-id="03dce-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="03dce-118">Il secondo e il terzo comando modificano la prima regola in $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="03dce-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="03dce-119">Il comando finale assegna le regole in $CorsRules al tipo di servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="03dce-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="03dce-120">Le regole modificate sovrascrivono le regole CORS correnti.</span><span class="sxs-lookup"><span data-stu-id="03dce-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="03dce-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03dce-121">PARAMETERS</span></span>

### <span data-ttu-id="03dce-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="03dce-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="03dce-123">Specifica l'intervallo di timeout sul lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="03dce-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="03dce-124">Se la chiamata precedente non riesce nell'intervallo specificato, il cmdlet riprova la richiesta.</span><span class="sxs-lookup"><span data-stu-id="03dce-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="03dce-125">Se questo cmdlet non riceve una risposta corretta prima che sia trascorso l'intervallo, il cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="03dce-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03dce-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="03dce-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="03dce-127">Specifica il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="03dce-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="03dce-128">È possibile usare questo parametro per limitare la simultaneità alla limitazione dell'utilizzo di CPU e larghezza di banda locale specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="03dce-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="03dce-129">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero principale.</span><span class="sxs-lookup"><span data-stu-id="03dce-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="03dce-130">Questo parametro consente di ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="03dce-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="03dce-131">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="03dce-131">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03dce-132">-Context</span><span class="sxs-lookup"><span data-stu-id="03dce-132">-Context</span></span>
<span data-ttu-id="03dce-133">Specifica un contesto di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="03dce-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="03dce-134">Per ottenere un contesto, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="03dce-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="03dce-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="03dce-135">-CorsRules</span></span>
<span data-ttu-id="03dce-136">Specifica una matrice di regole CORS.</span><span class="sxs-lookup"><span data-stu-id="03dce-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="03dce-137">È possibile recuperare le regole esistenti con il cmdlet Get-AzStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="03dce-137">You can retrieve the existing rules using the Get-AzStorageCORSRule cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03dce-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03dce-138">-DefaultProfile</span></span>
<span data-ttu-id="03dce-139">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03dce-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03dce-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03dce-140">-PassThru</span></span>
<span data-ttu-id="03dce-141">Indica che questo cmdlet restituisce un valore booleano che riflette l'esito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="03dce-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="03dce-142">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="03dce-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="03dce-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="03dce-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="03dce-144">Specifica la durata del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="03dce-144">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03dce-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="03dce-145">-ServiceType</span></span>
<span data-ttu-id="03dce-146">Specifica il tipo di servizio di archiviazione di Azure a cui questo cmdlet assegna regole.</span><span class="sxs-lookup"><span data-stu-id="03dce-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="03dce-147">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="03dce-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03dce-148">BLOB</span><span class="sxs-lookup"><span data-stu-id="03dce-148">Blob</span></span> 
- <span data-ttu-id="03dce-149">tavolo</span><span class="sxs-lookup"><span data-stu-id="03dce-149">Table</span></span> 
- <span data-ttu-id="03dce-150">Coda</span><span class="sxs-lookup"><span data-stu-id="03dce-150">Queue</span></span> 
- <span data-ttu-id="03dce-151">File</span><span class="sxs-lookup"><span data-stu-id="03dce-151">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03dce-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03dce-152">CommonParameters</span></span>
<span data-ttu-id="03dce-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03dce-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03dce-154">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03dce-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03dce-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="03dce-155">INPUTS</span></span>

### <span data-ttu-id="03dce-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="03dce-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="03dce-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03dce-157">OUTPUTS</span></span>

### <span data-ttu-id="03dce-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="03dce-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="03dce-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="03dce-159">NOTES</span></span>

## <span data-ttu-id="03dce-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03dce-160">RELATED LINKS</span></span>

[<span data-ttu-id="03dce-161">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="03dce-161">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="03dce-162">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="03dce-162">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="03dce-163">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="03dce-163">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)


