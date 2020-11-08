---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: 9011adbbfc7d23c2b9737e315fbec6001428d53c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019375"
---
# <span data-ttu-id="bb44b-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="bb44b-101">Set-AzIotHub</span></span>

## <span data-ttu-id="bb44b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb44b-102">SYNOPSIS</span></span>
<span data-ttu-id="bb44b-103">Aggiorna le proprietà di un IotHub.</span><span class="sxs-lookup"><span data-stu-id="bb44b-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="bb44b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb44b-104">SYNTAX</span></span>

### <span data-ttu-id="bb44b-105">UpdateSku (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bb44b-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb44b-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="bb44b-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb44b-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="bb44b-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb44b-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="bb44b-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb44b-109">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="bb44b-109">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb44b-110">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="bb44b-110">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb44b-111">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="bb44b-111">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb44b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb44b-112">DESCRIPTION</span></span>
<span data-ttu-id="bb44b-113">Aggiorna le proprietà di un IotHub.</span><span class="sxs-lookup"><span data-stu-id="bb44b-113">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="bb44b-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb44b-114">EXAMPLES</span></span>

### <span data-ttu-id="bb44b-115">Esempio 1 aggiornare l'USK</span><span class="sxs-lookup"><span data-stu-id="bb44b-115">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="bb44b-116">Aggiornare l'USK a S1 e le unità a 5 per il IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="bb44b-116">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="bb44b-117">Esempio 2 aggiornare le proprietà di eventhub</span><span class="sxs-lookup"><span data-stu-id="bb44b-117">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="bb44b-118">Aggiornare il periodo di ritenzione della telemetria in giorni fino a 4 per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="bb44b-118">Update the retention time of telemetry in days to 4 for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="bb44b-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb44b-119">PARAMETERS</span></span>

### <span data-ttu-id="bb44b-120">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="bb44b-120">-CloudToDevice</span></span>
<span data-ttu-id="bb44b-121">Proprietà della coda di comandi cloud to Device.</span><span class="sxs-lookup"><span data-stu-id="bb44b-121">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="bb44b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb44b-122">-DefaultProfile</span></span>
<span data-ttu-id="bb44b-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bb44b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb44b-124">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="bb44b-124">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="bb44b-125">Contrassegno che specifica se le notifiche devono essere abilitate per il caricamento di file.</span><span class="sxs-lookup"><span data-stu-id="bb44b-125">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="bb44b-126">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="bb44b-126">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="bb44b-127">Periodo di conservazione in giorni.</span><span class="sxs-lookup"><span data-stu-id="bb44b-127">Retention time in days.</span></span> 

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

### <span data-ttu-id="bb44b-128">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="bb44b-128">-FallbackRoute</span></span>
<span data-ttu-id="bb44b-129">Route di fallback per il routing</span><span class="sxs-lookup"><span data-stu-id="bb44b-129">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="bb44b-130">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="bb44b-130">-FileUploadContainerName</span></span>
<span data-ttu-id="bb44b-131">Nome del contenitore in cui caricare i file.</span><span class="sxs-lookup"><span data-stu-id="bb44b-131">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="bb44b-132">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="bb44b-132">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="bb44b-133">Numero massimo di recapito per le notifiche di caricamento file.</span><span class="sxs-lookup"><span data-stu-id="bb44b-133">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="bb44b-134">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="bb44b-134">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="bb44b-135">Valore time to Live per i messaggi nella coda di notifica di caricamento file.</span><span class="sxs-lookup"><span data-stu-id="bb44b-135">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="bb44b-136">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="bb44b-136">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="bb44b-137">È ora di vivere per l'URI SAS generato per il caricamento di file.</span><span class="sxs-lookup"><span data-stu-id="bb44b-137">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="bb44b-138">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="bb44b-138">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="bb44b-139">Stringa di connessione di archiviazione in cui caricare i file.</span><span class="sxs-lookup"><span data-stu-id="bb44b-139">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="bb44b-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb44b-140">-Name</span></span>
<span data-ttu-id="bb44b-141">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="bb44b-141">Name of the IotHub</span></span>

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

### <span data-ttu-id="bb44b-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb44b-142">-ResourceGroupName</span></span>
<span data-ttu-id="bb44b-143">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="bb44b-143">Resource Group Name</span></span>

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

### <span data-ttu-id="bb44b-144">-Route</span><span class="sxs-lookup"><span data-stu-id="bb44b-144">-Routes</span></span>
<span data-ttu-id="bb44b-145">Route da aggiungere per il routing</span><span class="sxs-lookup"><span data-stu-id="bb44b-145">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="bb44b-146">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="bb44b-146">-RoutingProperties</span></span>
<span data-ttu-id="bb44b-147">Proprietà di routing per il routing dei messaggi agli endpoint esterni</span><span class="sxs-lookup"><span data-stu-id="bb44b-147">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="bb44b-148">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bb44b-148">-SkuName</span></span>
<span data-ttu-id="bb44b-149">Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="bb44b-149">Name of the Sku.</span></span>

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

### <span data-ttu-id="bb44b-150">-Unità</span><span class="sxs-lookup"><span data-stu-id="bb44b-150">-Units</span></span>
<span data-ttu-id="bb44b-151">Numero di unità</span><span class="sxs-lookup"><span data-stu-id="bb44b-151">Number of Units</span></span>

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

### <span data-ttu-id="bb44b-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bb44b-152">-Confirm</span></span>
<span data-ttu-id="bb44b-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb44b-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb44b-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb44b-154">-WhatIf</span></span>
<span data-ttu-id="bb44b-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb44b-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb44b-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb44b-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb44b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb44b-157">CommonParameters</span></span>
<span data-ttu-id="bb44b-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb44b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb44b-159">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb44b-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb44b-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb44b-160">INPUTS</span></span>

### <span data-ttu-id="bb44b-161">System. String</span><span class="sxs-lookup"><span data-stu-id="bb44b-161">System.String</span></span>

## <span data-ttu-id="bb44b-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb44b-162">OUTPUTS</span></span>

### <span data-ttu-id="bb44b-163">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="bb44b-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="bb44b-164">Note</span><span class="sxs-lookup"><span data-stu-id="bb44b-164">NOTES</span></span>

## <span data-ttu-id="bb44b-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb44b-165">RELATED LINKS</span></span>
