---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: d3f32e44e5653d0d6a9c9b5a9a1eee27b66d43cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188847"
---
# <span data-ttu-id="4f56c-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4f56c-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="4f56c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f56c-102">SYNOPSIS</span></span>
<span data-ttu-id="4f56c-103">Modifica le proprietà delle metriche per il servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f56c-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="4f56c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f56c-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f56c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4f56c-105">DESCRIPTION</span></span>
<span data-ttu-id="4f56c-106">Il cmdlet **Set-AzStorageServiceMetricsProperty** modifica le proprietà delle metriche per il servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f56c-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="4f56c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f56c-107">EXAMPLES</span></span>

### <span data-ttu-id="4f56c-108">Esempio 1: Modificare le proprietà delle metriche per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="4f56c-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="4f56c-109">Questo comando modifica le metriche della versione 1.0 per l'archiviazione BLOB a un livello di servizio.</span><span class="sxs-lookup"><span data-stu-id="4f56c-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="4f56c-110">Le metriche del servizio Archiviazione di Azure conservano le voci per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="4f56c-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="4f56c-111">Poiché questo comando specifica il *parametro PassThru,* il comando visualizza le proprietà modificate per le metriche.</span><span class="sxs-lookup"><span data-stu-id="4f56c-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="4f56c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f56c-112">PARAMETERS</span></span>

### <span data-ttu-id="4f56c-113">-Context</span><span class="sxs-lookup"><span data-stu-id="4f56c-113">-Context</span></span>
<span data-ttu-id="4f56c-114">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f56c-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4f56c-115">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4f56c-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4f56c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f56c-116">-DefaultProfile</span></span>
<span data-ttu-id="4f56c-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f56c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f56c-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="4f56c-118">-MetricsLevel</span></span>
<span data-ttu-id="4f56c-119">Specifica il livello di metriche che viene utilizzato da Archiviazione di Azure per il servizio.</span><span class="sxs-lookup"><span data-stu-id="4f56c-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="4f56c-120">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="4f56c-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4f56c-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4f56c-121">None</span></span>
- <span data-ttu-id="4f56c-122">Servizio</span><span class="sxs-lookup"><span data-stu-id="4f56c-122">Service</span></span>
- <span data-ttu-id="4f56c-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="4f56c-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f56c-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="4f56c-124">-MetricsType</span></span>
<span data-ttu-id="4f56c-125">Specifica un tipo di metriche.</span><span class="sxs-lookup"><span data-stu-id="4f56c-125">Specifies a metrics type.</span></span>
<span data-ttu-id="4f56c-126">Questo cmdlet imposta il tipo di metriche del servizio di archiviazione di Azure sul valore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="4f56c-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="4f56c-127">I valori accettabili per questo parametro sono: Ora e Minuto.</span><span class="sxs-lookup"><span data-stu-id="4f56c-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="4f56c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f56c-128">-PassThru</span></span>
<span data-ttu-id="4f56c-129">Indica che questo cmdlet restituisce le proprietà aggiornate delle metriche.</span><span class="sxs-lookup"><span data-stu-id="4f56c-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="4f56c-130">Se non si specifica questo parametro, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4f56c-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4f56c-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="4f56c-131">-RetentionDays</span></span>
<span data-ttu-id="4f56c-132">Specifica il numero di giorni per cui il servizio di archiviazione di Azure conserva le informazioni sulle metriche.</span><span class="sxs-lookup"><span data-stu-id="4f56c-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="4f56c-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="4f56c-133">-ServiceType</span></span>
<span data-ttu-id="4f56c-134">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4f56c-134">Specifies the storage service type.</span></span>
<span data-ttu-id="4f56c-135">Questo cmdlet modifica le proprietà delle metriche per il tipo di servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="4f56c-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="4f56c-136">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="4f56c-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4f56c-137">BLOB</span><span class="sxs-lookup"><span data-stu-id="4f56c-137">Blob</span></span> 
- <span data-ttu-id="4f56c-138">tavolo</span><span class="sxs-lookup"><span data-stu-id="4f56c-138">Table</span></span>
- <span data-ttu-id="4f56c-139">Coda</span><span class="sxs-lookup"><span data-stu-id="4f56c-139">Queue</span></span>
- <span data-ttu-id="4f56c-140">File Il valore di File non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="4f56c-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="4f56c-141">-Version</span><span class="sxs-lookup"><span data-stu-id="4f56c-141">-Version</span></span>
<span data-ttu-id="4f56c-142">Specifica la versione delle metriche di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f56c-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="4f56c-143">Il valore predefinito è 1,0.</span><span class="sxs-lookup"><span data-stu-id="4f56c-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="4f56c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f56c-144">CommonParameters</span></span>
<span data-ttu-id="4f56c-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f56c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f56c-146">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f56c-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f56c-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="4f56c-147">INPUTS</span></span>

### <span data-ttu-id="4f56c-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4f56c-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4f56c-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f56c-149">OUTPUTS</span></span>

### <span data-ttu-id="4f56c-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="4f56c-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="4f56c-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="4f56c-151">NOTES</span></span>

## <span data-ttu-id="4f56c-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f56c-152">RELATED LINKS</span></span>

[<span data-ttu-id="4f56c-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4f56c-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="4f56c-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4f56c-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


