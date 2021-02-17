---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 04c65bf74d6c32dcaf93d2183936f9c0980aae4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188246"
---
# <span data-ttu-id="0c89c-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0c89c-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="0c89c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c89c-102">SYNOPSIS</span></span>
<span data-ttu-id="0c89c-103">Crea un arricchimento dei messaggi per gli endpoint scelti nell'Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0c89c-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="0c89c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c89c-104">SYNTAX</span></span>

### <span data-ttu-id="0c89c-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c89c-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c89c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0c89c-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c89c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0c89c-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c89c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0c89c-108">DESCRIPTION</span></span>
<span data-ttu-id="0c89c-109">Aggiungere fino a 10 arricchimenti dei messaggi per l'Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0c89c-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="0c89c-110">Vengono aggiunte come proprietà dell'applicazione ai messaggi inviati agli endpoint selezionati.</span><span class="sxs-lookup"><span data-stu-id="0c89c-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="0c89c-111">Per saperne di più, vedi https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="0c89c-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="0c89c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c89c-112">EXAMPLES</span></span>

### <span data-ttu-id="0c89c-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c89c-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="0c89c-114">Aggiungere un nuovo arricchimento con la chiave "newKey" e il valore "newValue".</span><span class="sxs-lookup"><span data-stu-id="0c89c-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="0c89c-115">Questo nuovo arricchimento viene applicato agli endpoint "endpoint1" e "endpoint2".</span><span class="sxs-lookup"><span data-stu-id="0c89c-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="0c89c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c89c-116">PARAMETERS</span></span>

### <span data-ttu-id="0c89c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c89c-117">-DefaultProfile</span></span>
<span data-ttu-id="0c89c-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c89c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c89c-119">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="0c89c-119">-Endpoint</span></span>
<span data-ttu-id="0c89c-120">Endpoint a cui applicare l'arricchimento.</span><span class="sxs-lookup"><span data-stu-id="0c89c-120">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c89c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c89c-121">-InputObject</span></span>
<span data-ttu-id="0c89c-122">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="0c89c-122">IotHub object</span></span>

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

### <span data-ttu-id="0c89c-123">-Key</span><span class="sxs-lookup"><span data-stu-id="0c89c-123">-Key</span></span>
<span data-ttu-id="0c89c-124">Chiave dell'arricchimento.</span><span class="sxs-lookup"><span data-stu-id="0c89c-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="0c89c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0c89c-125">-Name</span></span>
<span data-ttu-id="0c89c-126">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="0c89c-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0c89c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c89c-127">-ResourceGroupName</span></span>
<span data-ttu-id="0c89c-128">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0c89c-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0c89c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c89c-129">-ResourceId</span></span>
<span data-ttu-id="0c89c-130">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="0c89c-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0c89c-131">-Value</span><span class="sxs-lookup"><span data-stu-id="0c89c-131">-Value</span></span>
<span data-ttu-id="0c89c-132">Valore dell'arricchimento.</span><span class="sxs-lookup"><span data-stu-id="0c89c-132">The enrichment's value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c89c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c89c-133">-Confirm</span></span>
<span data-ttu-id="0c89c-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c89c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c89c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c89c-135">-WhatIf</span></span>
<span data-ttu-id="0c89c-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c89c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c89c-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c89c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c89c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c89c-138">CommonParameters</span></span>
<span data-ttu-id="0c89c-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c89c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c89c-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c89c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c89c-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="0c89c-141">INPUTS</span></span>

### <span data-ttu-id="0c89c-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0c89c-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0c89c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="0c89c-143">System.String</span></span>

## <span data-ttu-id="0c89c-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c89c-144">OUTPUTS</span></span>

### <span data-ttu-id="0c89c-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="0c89c-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="0c89c-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="0c89c-146">NOTES</span></span>

## <span data-ttu-id="0c89c-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c89c-147">RELATED LINKS</span></span>
