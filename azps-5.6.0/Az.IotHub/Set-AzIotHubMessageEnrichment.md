---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 0e9b26b4bd22d167dffbee4449aa811381960732
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004126"
---
# <span data-ttu-id="18b93-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="18b93-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="18b93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18b93-102">SYNOPSIS</span></span>
<span data-ttu-id="18b93-103">Aggiornare l'arricchimento dei messaggi nell'hub IoT.</span><span class="sxs-lookup"><span data-stu-id="18b93-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="18b93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18b93-104">SYNTAX</span></span>

### <span data-ttu-id="18b93-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="18b93-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18b93-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="18b93-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18b93-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="18b93-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18b93-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="18b93-108">DESCRIPTION</span></span>
<span data-ttu-id="18b93-109">Per una spiegazione dettagliata dell'arricchimento dei messaggi nell'Hub IoT di Azure, vedi https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="18b93-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="18b93-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18b93-110">EXAMPLES</span></span>

### <span data-ttu-id="18b93-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="18b93-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="18b93-112">Aggiorna il valore di arricchimento in "updatedValue" per la chiave "newKey".</span><span class="sxs-lookup"><span data-stu-id="18b93-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="18b93-113">Per una spiegazione dettagliata dell'arricchimento dei messaggi nell'Hub IoT di Azure, vedi https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="18b93-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="18b93-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="18b93-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="18b93-115">Aggiorna l'endpoint di arricchimento a "endpoint1, endpoint2, endpoint3" per la chiave "newKey".</span><span class="sxs-lookup"><span data-stu-id="18b93-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="18b93-116">Per una spiegazione dettagliata dell'arricchimento dei messaggi nell'Hub IoT di Azure, vedi https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="18b93-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="18b93-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18b93-117">PARAMETERS</span></span>

### <span data-ttu-id="18b93-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b93-118">-DefaultProfile</span></span>
<span data-ttu-id="18b93-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18b93-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18b93-120">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="18b93-120">-Endpoint</span></span>
<span data-ttu-id="18b93-121">Endpoint a cui applicare l'arricchimento.</span><span class="sxs-lookup"><span data-stu-id="18b93-121">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b93-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18b93-122">-InputObject</span></span>
<span data-ttu-id="18b93-123">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="18b93-123">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18b93-124">-Key</span><span class="sxs-lookup"><span data-stu-id="18b93-124">-Key</span></span>
<span data-ttu-id="18b93-125">Chiave dell'arricchimento.</span><span class="sxs-lookup"><span data-stu-id="18b93-125">The enrichment's key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b93-126">-Name</span><span class="sxs-lookup"><span data-stu-id="18b93-126">-Name</span></span>
<span data-ttu-id="18b93-127">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="18b93-127">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b93-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b93-128">-ResourceGroupName</span></span>
<span data-ttu-id="18b93-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="18b93-129">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b93-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18b93-130">-ResourceId</span></span>
<span data-ttu-id="18b93-131">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="18b93-131">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b93-132">-Value</span><span class="sxs-lookup"><span data-stu-id="18b93-132">-Value</span></span>
<span data-ttu-id="18b93-133">Valore dell'arricchimento.</span><span class="sxs-lookup"><span data-stu-id="18b93-133">The enrichment's value.</span></span>

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

### <span data-ttu-id="18b93-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18b93-134">-Confirm</span></span>
<span data-ttu-id="18b93-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18b93-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b93-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18b93-136">-WhatIf</span></span>
<span data-ttu-id="18b93-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18b93-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18b93-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18b93-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b93-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b93-139">CommonParameters</span></span>
<span data-ttu-id="18b93-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18b93-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b93-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18b93-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b93-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="18b93-142">INPUTS</span></span>

### <span data-ttu-id="18b93-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="18b93-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="18b93-144">System.String</span><span class="sxs-lookup"><span data-stu-id="18b93-144">System.String</span></span>

## <span data-ttu-id="18b93-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18b93-145">OUTPUTS</span></span>

### <span data-ttu-id="18b93-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="18b93-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="18b93-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="18b93-147">NOTES</span></span>

## <span data-ttu-id="18b93-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18b93-148">RELATED LINKS</span></span>
