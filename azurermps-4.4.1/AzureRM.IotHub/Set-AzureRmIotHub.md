---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
ms.openlocfilehash: aad54e42d628239f087e376eabe6b9950c07b6f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521225"
---
# <span data-ttu-id="36bc6-101">Set-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="36bc6-101">Set-AzureRmIotHub</span></span>

## <span data-ttu-id="36bc6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36bc6-102">SYNOPSIS</span></span>
<span data-ttu-id="36bc6-103">Aggiorna le proprietà di un IotHub.</span><span class="sxs-lookup"><span data-stu-id="36bc6-103">Updates the properties of an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36bc6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36bc6-104">SYNTAX</span></span>

### <span data-ttu-id="36bc6-105">UpdateSku (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36bc6-105">UpdateSku (Default)</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36bc6-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="36bc6-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36bc6-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="36bc6-107">UpdateFileUploadProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36bc6-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="36bc6-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36bc6-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="36bc6-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36bc6-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="36bc6-110">UpdateRoutingProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36bc6-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="36bc6-111">UpdateRouteProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36bc6-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="36bc6-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36bc6-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36bc6-113">DESCRIPTION</span></span>
<span data-ttu-id="36bc6-114">Aggiorna le proprietà di un IotHub.</span><span class="sxs-lookup"><span data-stu-id="36bc6-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="36bc6-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36bc6-115">EXAMPLES</span></span>

### <span data-ttu-id="36bc6-116">Esempio 1 aggiornare l'USK</span><span class="sxs-lookup"><span data-stu-id="36bc6-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="36bc6-117">Aggiornare l'USK a S1 e le unità a 5 per il IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="36bc6-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="36bc6-118">Esempio 2 aggiornare le proprietà di eventhub</span><span class="sxs-lookup"><span data-stu-id="36bc6-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="36bc6-119">Aggiornare il periodo di conservazione in giorni a 4 per gli eventi di telemetria e operationsmonitoringevents per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="36bc6-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="36bc6-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36bc6-120">PARAMETERS</span></span>

### <span data-ttu-id="36bc6-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="36bc6-121">-CloudToDevice</span></span>
<span data-ttu-id="36bc6-122">Proprietà della coda di comandi cloud to Device.</span><span class="sxs-lookup"><span data-stu-id="36bc6-122">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-123">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="36bc6-123">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="36bc6-124">Contrassegno che specifica se le notifiche devono essere abilitate per il caricamento di file.</span><span class="sxs-lookup"><span data-stu-id="36bc6-124">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: System.Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-125">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="36bc6-125">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="36bc6-126">Periodo di conservazione in giorni.</span><span class="sxs-lookup"><span data-stu-id="36bc6-126">Retention time in days.</span></span> 

```yaml
Type: System.Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-127">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="36bc6-127">-FallbackRoute</span></span>
<span data-ttu-id="36bc6-128">Route di fallback per il routing</span><span class="sxs-lookup"><span data-stu-id="36bc6-128">Fallback Route for Routing</span></span>

```yaml
Type: Microsoft.Azure.Management.IotHub.Models.PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-129">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="36bc6-129">-FileUploadContainerName</span></span>
<span data-ttu-id="36bc6-130">Nome del contenitore in cui caricare i file.</span><span class="sxs-lookup"><span data-stu-id="36bc6-130">The name of the container to upload the files to.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-131">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="36bc6-131">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="36bc6-132">Numero massimo di recapito per le notifiche di caricamento file.</span><span class="sxs-lookup"><span data-stu-id="36bc6-132">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-133">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="36bc6-133">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="36bc6-134">Valore time to Live per i messaggi nella coda di notifica di caricamento file.</span><span class="sxs-lookup"><span data-stu-id="36bc6-134">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-135">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="36bc6-135">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="36bc6-136">È ora di vivere per l'URI SAS generato per il caricamento di file.</span><span class="sxs-lookup"><span data-stu-id="36bc6-136">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-137">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="36bc6-137">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="36bc6-138">Stringa di connessione di archiviazione in cui caricare i file.</span><span class="sxs-lookup"><span data-stu-id="36bc6-138">The storage connection string to upload the files to.</span></span> 

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="36bc6-139">-Name</span></span>
<span data-ttu-id="36bc6-140">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="36bc6-140">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-141">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="36bc6-141">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="36bc6-142">Proprietà correlate al monitoraggio delle operazioni.</span><span class="sxs-lookup"><span data-stu-id="36bc6-142">The properties related to operations monitoring.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36bc6-143">-ResourceGroupName</span></span>
<span data-ttu-id="36bc6-144">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="36bc6-144">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-145">-Route</span><span class="sxs-lookup"><span data-stu-id="36bc6-145">-Routes</span></span>
<span data-ttu-id="36bc6-146">Route da aggiungere per il routing</span><span class="sxs-lookup"><span data-stu-id="36bc6-146">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="36bc6-147">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="36bc6-147">-RoutingProperties</span></span>
<span data-ttu-id="36bc6-148">Proprietà di routing per il routing dei messaggi agli endpoint esterni</span><span class="sxs-lookup"><span data-stu-id="36bc6-148">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-149">-SkuName</span><span class="sxs-lookup"><span data-stu-id="36bc6-149">-SkuName</span></span>
<span data-ttu-id="36bc6-150">Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="36bc6-150">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-151">-Unità</span><span class="sxs-lookup"><span data-stu-id="36bc6-151">-Units</span></span>
<span data-ttu-id="36bc6-152">Numero di unità</span><span class="sxs-lookup"><span data-stu-id="36bc6-152">Number of Units</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateSku
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="36bc6-153">-Confirm</span></span>
<span data-ttu-id="36bc6-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36bc6-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36bc6-155">-WhatIf</span></span>
<span data-ttu-id="36bc6-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36bc6-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36bc6-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36bc6-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bc6-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36bc6-158">-DefaultProfile</span></span>
<span data-ttu-id="36bc6-159">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36bc6-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36bc6-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36bc6-160">CommonParameters</span></span>
<span data-ttu-id="36bc6-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36bc6-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36bc6-162">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36bc6-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36bc6-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36bc6-163">INPUTS</span></span>

### <span data-ttu-id="36bc6-164">System. String</span><span class="sxs-lookup"><span data-stu-id="36bc6-164">System.String</span></span>
<span data-ttu-id="36bc6-165">Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceProperties Microsoft. Azure. Commands. Management. IotHub. Models. PSOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="36bc6-165">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties</span></span>

## <span data-ttu-id="36bc6-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36bc6-166">OUTPUTS</span></span>

### <span data-ttu-id="36bc6-167">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="36bc6-167">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="36bc6-168">Note</span><span class="sxs-lookup"><span data-stu-id="36bc6-168">NOTES</span></span>

## <span data-ttu-id="36bc6-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36bc6-169">RELATED LINKS</span></span>

