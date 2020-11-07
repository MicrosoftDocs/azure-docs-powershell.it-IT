---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 855e7f23c1deddd0e9f0b23e0c04375246e3aa21
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862014"
---
# <span data-ttu-id="6cb4e-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6cb4e-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="6cb4e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6cb4e-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb4e-103">Modifica le proprietà metriche per il servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="6cb4e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cb4e-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cb4e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cb4e-105">DESCRIPTION</span></span>
<span data-ttu-id="6cb4e-106">Il cmdlet **set-AzStorageServiceMetricsProperty** modifica le proprietà metriche per il servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="6cb4e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cb4e-107">EXAMPLES</span></span>

### <span data-ttu-id="6cb4e-108">Esempio 1: modificare le proprietà metriche per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="6cb4e-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="6cb4e-109">Questo comando modifica le metriche della versione 1,0 per l'archiviazione BLOB in un livello di servizio.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="6cb4e-110">Le metriche del servizio di archiviazione di Azure conservano le voci per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="6cb4e-111">Poiché questo comando specifica il parametro *PassThru* , il comando Visualizza le proprietà metriche modificate.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="6cb4e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6cb4e-112">PARAMETERS</span></span>

### <span data-ttu-id="6cb4e-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="6cb4e-113">-Context</span></span>
<span data-ttu-id="6cb4e-114">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6cb4e-115">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6cb4e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb4e-116">-DefaultProfile</span></span>
<span data-ttu-id="6cb4e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cb4e-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="6cb4e-118">-MetricsLevel</span></span>
<span data-ttu-id="6cb4e-119">Specifica il livello di metriche usato da Azure Storage per il servizio.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="6cb4e-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6cb4e-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6cb4e-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6cb4e-121">None</span></span>
- <span data-ttu-id="6cb4e-122">Servizio</span><span class="sxs-lookup"><span data-stu-id="6cb4e-122">Service</span></span>
- <span data-ttu-id="6cb4e-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="6cb4e-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAz.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb4e-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="6cb4e-124">-MetricsType</span></span>
<span data-ttu-id="6cb4e-125">Specifica un tipo di metriche.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-125">Specifies a metrics type.</span></span>
<span data-ttu-id="6cb4e-126">Questo cmldet imposta il tipo di metriche del servizio di archiviazione di Azure sul valore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-126">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="6cb4e-127">I valori accettabili per questo parametro sono: hour e minute.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb4e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cb4e-128">-PassThru</span></span>
<span data-ttu-id="6cb4e-129">Indica che questo cmdlet restituisce le proprietà metriche aggiornate.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="6cb4e-130">Se non specifichi questo parametro, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6cb4e-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="6cb4e-131">-RetentionDays</span></span>
<span data-ttu-id="6cb4e-132">Specifica il numero di giorni in cui il servizio di archiviazione di Azure mantiene le informazioni sulle metriche.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="6cb4e-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="6cb4e-133">-ServiceType</span></span>
<span data-ttu-id="6cb4e-134">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-134">Specifies the storage service type.</span></span>
<span data-ttu-id="6cb4e-135">Questo cmdlet modifica le proprietà metriche per il tipo di servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="6cb4e-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6cb4e-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6cb4e-137">BLOB</span><span class="sxs-lookup"><span data-stu-id="6cb4e-137">Blob</span></span> 
- <span data-ttu-id="6cb4e-138">tavolo</span><span class="sxs-lookup"><span data-stu-id="6cb4e-138">Table</span></span>
- <span data-ttu-id="6cb4e-139">Coda</span><span class="sxs-lookup"><span data-stu-id="6cb4e-139">Queue</span></span>
- <span data-ttu-id="6cb4e-140">File il valore di file non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="6cb4e-141">-Versione</span><span class="sxs-lookup"><span data-stu-id="6cb4e-141">-Version</span></span>
<span data-ttu-id="6cb4e-142">Specifica la versione delle metriche di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="6cb4e-143">Il valore predefinito è 1,0.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-143">The default value is 1.0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb4e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb4e-144">CommonParameters</span></span>
<span data-ttu-id="6cb4e-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb4e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb4e-146">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cb4e-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb4e-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6cb4e-147">INPUTS</span></span>

### <span data-ttu-id="6cb4e-148">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6cb4e-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6cb4e-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cb4e-149">OUTPUTS</span></span>

### <span data-ttu-id="6cb4e-150">Microsoft. WindowsAz. storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="6cb4e-150">Microsoft.WindowsAz.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="6cb4e-151">Note</span><span class="sxs-lookup"><span data-stu-id="6cb4e-151">NOTES</span></span>

## <span data-ttu-id="6cb4e-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cb4e-152">RELATED LINKS</span></span>

[<span data-ttu-id="6cb4e-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6cb4e-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="6cb4e-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6cb4e-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


