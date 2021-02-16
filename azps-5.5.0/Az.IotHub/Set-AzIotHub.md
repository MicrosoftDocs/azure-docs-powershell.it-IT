---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: 9011adbbfc7d23c2b9737e315fbec6001428d53c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190350"
---
# <span data-ttu-id="0acf3-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="0acf3-101">Set-AzIotHub</span></span>

## <span data-ttu-id="0acf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0acf3-102">SYNOPSIS</span></span>
<span data-ttu-id="0acf3-103">Aggiorna le proprietà di un iotHub.</span><span class="sxs-lookup"><span data-stu-id="0acf3-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="0acf3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0acf3-104">SYNTAX</span></span>

### <span data-ttu-id="0acf3-105">UpdateSku (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0acf3-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0acf3-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="0acf3-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0acf3-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="0acf3-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0acf3-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="0acf3-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0acf3-109">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="0acf3-109">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0acf3-110">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="0acf3-110">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0acf3-111">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="0acf3-111">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0acf3-112">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0acf3-112">DESCRIPTION</span></span>
<span data-ttu-id="0acf3-113">Aggiorna le proprietà di un iotHub.</span><span class="sxs-lookup"><span data-stu-id="0acf3-113">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="0acf3-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0acf3-114">EXAMPLES</span></span>

### <span data-ttu-id="0acf3-115">Esempio 1: Aggiornare la SKU</span><span class="sxs-lookup"><span data-stu-id="0acf3-115">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="0acf3-116">Aggiornare la sKU a S1 e le unità a 5 per IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="0acf3-116">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="0acf3-117">Esempio 2: Aggiornare le proprietà di eventhub</span><span class="sxs-lookup"><span data-stu-id="0acf3-117">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="0acf3-118">Aggiornare il tempo di conservazione della telemetria in giorni a 4 per il sito IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="0acf3-118">Update the retention time of telemetry in days to 4 for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="0acf3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0acf3-119">PARAMETERS</span></span>

### <span data-ttu-id="0acf3-120">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="0acf3-120">-CloudToDevice</span></span>
<span data-ttu-id="0acf3-121">Le proprietà della coda di comandi da cloud a dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0acf3-121">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="0acf3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0acf3-122">-DefaultProfile</span></span>
<span data-ttu-id="0acf3-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="0acf3-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0acf3-124">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="0acf3-124">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="0acf3-125">Flag che specifica se le notifiche devono essere abilitate per il caricamento dei file.</span><span class="sxs-lookup"><span data-stu-id="0acf3-125">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="0acf3-126">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="0acf3-126">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="0acf3-127">Tempo di conservazione in giorni.</span><span class="sxs-lookup"><span data-stu-id="0acf3-127">Retention time in days.</span></span> 

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

### <span data-ttu-id="0acf3-128">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="0acf3-128">-FallbackRoute</span></span>
<span data-ttu-id="0acf3-129">Fallback Route for Routing</span><span class="sxs-lookup"><span data-stu-id="0acf3-129">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="0acf3-130">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="0acf3-130">-FileUploadContainerName</span></span>
<span data-ttu-id="0acf3-131">Nome del contenitore in cui caricare i file.</span><span class="sxs-lookup"><span data-stu-id="0acf3-131">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="0acf3-132">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="0acf3-132">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="0acf3-133">Il numero massimo di consegne per le notifiche di caricamento dei file.</span><span class="sxs-lookup"><span data-stu-id="0acf3-133">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="0acf3-134">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="0acf3-134">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="0acf3-135">Time to live value for the messages in the file upload notification queue.</span><span class="sxs-lookup"><span data-stu-id="0acf3-135">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="0acf3-136">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="0acf3-136">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="0acf3-137">Ora di live per l'URI della firma di accesso condiviso generato per il caricamento dei file.</span><span class="sxs-lookup"><span data-stu-id="0acf3-137">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="0acf3-138">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="0acf3-138">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="0acf3-139">Stringa di connessione di archiviazione in cui caricare i file.</span><span class="sxs-lookup"><span data-stu-id="0acf3-139">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="0acf3-140">-Name</span><span class="sxs-lookup"><span data-stu-id="0acf3-140">-Name</span></span>
<span data-ttu-id="0acf3-141">Nome del file IotHub</span><span class="sxs-lookup"><span data-stu-id="0acf3-141">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0acf3-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0acf3-142">-ResourceGroupName</span></span>
<span data-ttu-id="0acf3-143">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0acf3-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0acf3-144">-Percorsi</span><span class="sxs-lookup"><span data-stu-id="0acf3-144">-Routes</span></span>
<span data-ttu-id="0acf3-145">Route da aggiungere per il routing</span><span class="sxs-lookup"><span data-stu-id="0acf3-145">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="0acf3-146">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="0acf3-146">-RoutingProperties</span></span>
<span data-ttu-id="0acf3-147">Proprietà di routing per il routing dei messaggi agli endpoint esterni</span><span class="sxs-lookup"><span data-stu-id="0acf3-147">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="0acf3-148">-SKUName</span><span class="sxs-lookup"><span data-stu-id="0acf3-148">-SkuName</span></span>
<span data-ttu-id="0acf3-149">Nome della SKU.</span><span class="sxs-lookup"><span data-stu-id="0acf3-149">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0acf3-150">-Unità</span><span class="sxs-lookup"><span data-stu-id="0acf3-150">-Units</span></span>
<span data-ttu-id="0acf3-151">Numero di unità</span><span class="sxs-lookup"><span data-stu-id="0acf3-151">Number of Units</span></span>

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

### <span data-ttu-id="0acf3-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0acf3-152">-Confirm</span></span>
<span data-ttu-id="0acf3-153">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0acf3-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0acf3-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0acf3-154">-WhatIf</span></span>
<span data-ttu-id="0acf3-155">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0acf3-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0acf3-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0acf3-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0acf3-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0acf3-157">CommonParameters</span></span>
<span data-ttu-id="0acf3-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0acf3-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0acf3-159">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0acf3-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0acf3-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="0acf3-160">INPUTS</span></span>

### <span data-ttu-id="0acf3-161">System.String</span><span class="sxs-lookup"><span data-stu-id="0acf3-161">System.String</span></span>

## <span data-ttu-id="0acf3-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0acf3-162">OUTPUTS</span></span>

### <span data-ttu-id="0acf3-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0acf3-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="0acf3-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="0acf3-164">NOTES</span></span>

## <span data-ttu-id="0acf3-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0acf3-165">RELATED LINKS</span></span>
