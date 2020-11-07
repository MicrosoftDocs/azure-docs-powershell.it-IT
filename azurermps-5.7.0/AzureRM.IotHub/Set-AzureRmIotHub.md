---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
ms.openlocfilehash: a9005819bb78e5393f3a617dd18886309d3defc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688467"
---
# <span data-ttu-id="8e0fc-101">Set-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="8e0fc-101">Set-AzureRmIotHub</span></span>

## <span data-ttu-id="8e0fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e0fc-102">SYNOPSIS</span></span>
<span data-ttu-id="8e0fc-103">Aggiorna le proprietà di un IotHub.</span><span class="sxs-lookup"><span data-stu-id="8e0fc-103">Updates the properties of an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e0fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e0fc-104">SYNTAX</span></span>

### <span data-ttu-id="8e0fc-105">UpdateSku (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8e0fc-105">UpdateSku (Default)</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e0fc-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="8e0fc-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e0fc-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="8e0fc-107">UpdateFileUploadProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e0fc-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="8e0fc-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e0fc-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="8e0fc-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e0fc-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="8e0fc-110">UpdateRoutingProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e0fc-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="8e0fc-111">UpdateRouteProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e0fc-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="8e0fc-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e0fc-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e0fc-113">DESCRIPTION</span></span>
<span data-ttu-id="8e0fc-114">Aggiorna le proprietà di un IotHub.</span><span class="sxs-lookup"><span data-stu-id="8e0fc-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="8e0fc-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e0fc-115">EXAMPLES</span></span>

### <span data-ttu-id="8e0fc-116">Esempio 1 aggiornare l'USK</span><span class="sxs-lookup"><span data-stu-id="8e0fc-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="8e0fc-117">Aggiornare l'USK a S1 e le unità a 5 per il IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="8e0fc-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="8e0fc-118">Esempio 2 aggiornare le proprietà di eventhub</span><span class="sxs-lookup"><span data-stu-id="8e0fc-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="8e0fc-119">Aggiornare il periodo di conservazione in giorni a 4 per gli eventi di telemetria e operationsmonitoringevents per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="8e0fc-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="8e0fc-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e0fc-120">PARAMETERS</span></span>

### <span data-ttu-id="8e0fc-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="8e0fc-121">-CloudToDevice</span></span>
<span data-ttu-id="8e0fc-122">Proprietà della coda di comandi cloud to Device.</span><span class="sxs-lookup"><span data-stu-id="8e0fc-122">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e0fc-123">-DefaultProfile</span></span>
<span data-ttu-id="8e0fc-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8e0fc-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-125">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="8e0fc-125">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="8e0fc-126">Contrassegno che specifica se le notifiche devono essere abilitate per il caricamento di file.</span><span class="sxs-lookup"><span data-stu-id="8e0fc-126">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-127">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="8e0fc-127">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="8e0fc-128">Periodo di conservazione in giorni.</span><span class="sxs-lookup"><span data-stu-id="8e0fc-128">Retention time in days.</span></span> 

```yaml
Type: Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-129">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="8e0fc-129">-FallbackRoute</span></span>
<span data-ttu-id="8e0fc-130">Route di fallback per il routing</span><span class="sxs-lookup"><span data-stu-id="8e0fc-130">Fallback Route for Routing</span></span>

```yaml
Type: PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-131">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="8e0fc-131">-FileUploadContainerName</span></span>
<span data-ttu-id="8e0fc-132">Nome del contenitore in cui caricare i file.</span><span class="sxs-lookup"><span data-stu-id="8e0fc-132">The name of the container to upload the files to.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-133">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="8e0fc-133">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="8e0fc-134">Numero massimo di recapito per le notifiche di caricamento file.</span><span class="sxs-lookup"><span data-stu-id="8e0fc-134">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: Int32
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-135">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="8e0fc-135">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="8e0fc-136">Valore time to Live per i messaggi nella coda di notifica di caricamento file.</span><span class="sxs-lookup"><span data-stu-id="8e0fc-136">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-137">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="8e0fc-137">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="8e0fc-138">È ora di vivere per l'URI SAS generato per il caricamento di file.</span><span class="sxs-lookup"><span data-stu-id="8e0fc-138">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-139">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="8e0fc-139">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="8e0fc-140">Stringa di connessione di archiviazione in cui caricare i file.</span><span class="sxs-lookup"><span data-stu-id="8e0fc-140">The storage connection string to upload the files to.</span></span> 

```yaml
Type: String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e0fc-141">-Name</span></span>
<span data-ttu-id="8e0fc-142">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="8e0fc-142">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-143">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="8e0fc-143">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="8e0fc-144">Proprietà correlate al monitoraggio delle operazioni.</span><span class="sxs-lookup"><span data-stu-id="8e0fc-144">The properties related to operations monitoring.</span></span> 

```yaml
Type: PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e0fc-145">-ResourceGroupName</span></span>
<span data-ttu-id="8e0fc-146">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="8e0fc-146">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-147">-Route</span><span class="sxs-lookup"><span data-stu-id="8e0fc-147">-Routes</span></span>
<span data-ttu-id="8e0fc-148">Route da aggiungere per il routing</span><span class="sxs-lookup"><span data-stu-id="8e0fc-148">Routes to be added for Routing</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]
Parameter Sets: UpdateRouteProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-149">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="8e0fc-149">-RoutingProperties</span></span>
<span data-ttu-id="8e0fc-150">Proprietà di routing per il routing dei messaggi agli endpoint esterni</span><span class="sxs-lookup"><span data-stu-id="8e0fc-150">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-151">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8e0fc-151">-SkuName</span></span>
<span data-ttu-id="8e0fc-152">Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="8e0fc-152">Name of the Sku.</span></span>

```yaml
Type: PSIotHubSku
Parameter Sets: UpdateSku
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-153">-Unità</span><span class="sxs-lookup"><span data-stu-id="8e0fc-153">-Units</span></span>
<span data-ttu-id="8e0fc-154">Numero di unità</span><span class="sxs-lookup"><span data-stu-id="8e0fc-154">Number of Units</span></span>

```yaml
Type: Int64
Parameter Sets: UpdateSku
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-155">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8e0fc-155">-Confirm</span></span>
<span data-ttu-id="8e0fc-156">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e0fc-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e0fc-157">-WhatIf</span></span>
<span data-ttu-id="8e0fc-158">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e0fc-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e0fc-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e0fc-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0fc-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e0fc-160">CommonParameters</span></span>
<span data-ttu-id="8e0fc-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e0fc-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e0fc-162">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e0fc-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e0fc-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e0fc-163">INPUTS</span></span>

### <span data-ttu-id="8e0fc-164">System. String</span><span class="sxs-lookup"><span data-stu-id="8e0fc-164">System.String</span></span>
<span data-ttu-id="8e0fc-165">Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceProperties Microsoft. Azure. Commands. Management. IotHub. Models. PSOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="8e0fc-165">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties</span></span>

## <span data-ttu-id="8e0fc-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e0fc-166">OUTPUTS</span></span>

### <span data-ttu-id="8e0fc-167">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8e0fc-167">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="8e0fc-168">Note</span><span class="sxs-lookup"><span data-stu-id="8e0fc-168">NOTES</span></span>

## <span data-ttu-id="8e0fc-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e0fc-169">RELATED LINKS</span></span>

