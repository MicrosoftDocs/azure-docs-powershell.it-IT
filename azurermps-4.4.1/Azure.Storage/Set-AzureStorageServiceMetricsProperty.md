---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3f295d42075054d676852c42028dc2e9fd8b82b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520827"
---
# <span data-ttu-id="5cf9f-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="5cf9f-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="5cf9f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5cf9f-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf9f-103">Modifica le proprietà metriche per il servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-103">Modifies metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cf9f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5cf9f-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="5cf9f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5cf9f-105">DESCRIPTION</span></span>
<span data-ttu-id="5cf9f-106">Il cmdlet **set-AzureStorageServiceMetricsProperty** modifica le proprietà metriche per il servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="5cf9f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5cf9f-107">EXAMPLES</span></span>

### <span data-ttu-id="5cf9f-108">Esempio 1: modificare le proprietà metriche per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="5cf9f-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="5cf9f-109">Questo comando modifica le metriche della versione 1,0 per l'archiviazione BLOB in un livello di servizio.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="5cf9f-110">Le metriche del servizio di archiviazione di Azure conservano le voci per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="5cf9f-111">Poiché questo comando specifica il parametro *PassThru* , il comando Visualizza le proprietà metriche modificate.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="5cf9f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5cf9f-112">PARAMETERS</span></span>

### <span data-ttu-id="5cf9f-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="5cf9f-113">-Context</span></span>
<span data-ttu-id="5cf9f-114">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5cf9f-115">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5cf9f-116">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="5cf9f-116">-MetricsLevel</span></span>
<span data-ttu-id="5cf9f-117">Specifica il livello di metriche usato da Azure Storage per il servizio.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-117">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="5cf9f-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5cf9f-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5cf9f-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5cf9f-119">None</span></span>
- <span data-ttu-id="5cf9f-120">Servizio</span><span class="sxs-lookup"><span data-stu-id="5cf9f-120">Service</span></span>
- <span data-ttu-id="5cf9f-121">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="5cf9f-121">ServiceAndApi</span></span>

```yaml
Type: MetricsLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cf9f-122">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="5cf9f-122">-MetricsType</span></span>
<span data-ttu-id="5cf9f-123">Specifica un tipo di metriche.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-123">Specifies a metrics type.</span></span>
<span data-ttu-id="5cf9f-124">Questo cmldet imposta il tipo di metriche del servizio di archiviazione di Azure sul valore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-124">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="5cf9f-125">I valori accettabili per questo parametro sono: hour e minute.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-125">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cf9f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cf9f-126">-PassThru</span></span>
<span data-ttu-id="5cf9f-127">Indica che questo cmdlet restituisce le proprietà metriche aggiornate.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-127">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="5cf9f-128">Se non specifichi questo parametro, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-128">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="5cf9f-129">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="5cf9f-129">-RetentionDays</span></span>
<span data-ttu-id="5cf9f-130">Specifica il numero di giorni in cui il servizio di archiviazione di Azure mantiene le informazioni sulle metriche.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-130">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="5cf9f-131">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="5cf9f-131">-ServiceType</span></span>
<span data-ttu-id="5cf9f-132">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-132">Specifies the storage service type.</span></span>
<span data-ttu-id="5cf9f-133">Questo cmdlet modifica le proprietà metriche per il tipo di servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-133">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="5cf9f-134">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5cf9f-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5cf9f-135">BLOB</span><span class="sxs-lookup"><span data-stu-id="5cf9f-135">Blob</span></span> 
- <span data-ttu-id="5cf9f-136">tavolo</span><span class="sxs-lookup"><span data-stu-id="5cf9f-136">Table</span></span>
- <span data-ttu-id="5cf9f-137">Coda</span><span class="sxs-lookup"><span data-stu-id="5cf9f-137">Queue</span></span>
- <span data-ttu-id="5cf9f-138">File</span><span class="sxs-lookup"><span data-stu-id="5cf9f-138">File</span></span>

<span data-ttu-id="5cf9f-139">Il valore di file non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-139">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="5cf9f-140">-Versione</span><span class="sxs-lookup"><span data-stu-id="5cf9f-140">-Version</span></span>
<span data-ttu-id="5cf9f-141">Specifica la versione delle metriche di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-141">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="5cf9f-142">Il valore predefinito è 1,0.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-142">The default value is 1.0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cf9f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf9f-143">CommonParameters</span></span>
<span data-ttu-id="5cf9f-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cf9f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf9f-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cf9f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf9f-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5cf9f-146">INPUTS</span></span>

### <span data-ttu-id="5cf9f-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5cf9f-147">IStorageContext</span></span>

<span data-ttu-id="5cf9f-148">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5cf9f-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="5cf9f-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5cf9f-149">OUTPUTS</span></span>

### <span data-ttu-id="5cf9f-150">Microsoft. WindowsAzure. storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="5cf9f-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="5cf9f-151">Note</span><span class="sxs-lookup"><span data-stu-id="5cf9f-151">NOTES</span></span>

## <span data-ttu-id="5cf9f-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5cf9f-152">RELATED LINKS</span></span>

[<span data-ttu-id="5cf9f-153">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="5cf9f-153">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="5cf9f-154">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5cf9f-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


