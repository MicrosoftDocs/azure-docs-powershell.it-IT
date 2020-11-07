---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: fa3e46db14c7bba17ba87813285d0f7b119dc6c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674249"
---
# <span data-ttu-id="962d9-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="962d9-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="962d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="962d9-102">SYNOPSIS</span></span>
<span data-ttu-id="962d9-103">Crea un arricchimento del messaggio per gli endpoint scelti nell'hub degli altri.</span><span class="sxs-lookup"><span data-stu-id="962d9-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="962d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="962d9-104">SYNTAX</span></span>

### <span data-ttu-id="962d9-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="962d9-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="962d9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="962d9-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="962d9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="962d9-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="962d9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="962d9-108">DESCRIPTION</span></span>
<span data-ttu-id="962d9-109">Aggiungere fino a 10 arricchimenti di messaggi per hub.</span><span class="sxs-lookup"><span data-stu-id="962d9-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="962d9-110">Questi vengono aggiunti come proprietà dell'applicazione ai messaggi inviati agli endpoint scelti.</span><span class="sxs-lookup"><span data-stu-id="962d9-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="962d9-111">Per saperne di più, Vedi https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="962d9-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="962d9-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="962d9-112">EXAMPLES</span></span>

### <span data-ttu-id="962d9-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="962d9-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="962d9-114">Aggiungere un nuovo arricchimento con la chiave "newKey" e il valore "newValue".</span><span class="sxs-lookup"><span data-stu-id="962d9-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="962d9-115">Questo nuovo arricchimento viene applicato agli endpoint "endpoint1" e "endpoint2".</span><span class="sxs-lookup"><span data-stu-id="962d9-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="962d9-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="962d9-116">PARAMETERS</span></span>

### <span data-ttu-id="962d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="962d9-117">-DefaultProfile</span></span>
<span data-ttu-id="962d9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="962d9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="962d9-119">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="962d9-119">-Endpoint</span></span>
<span data-ttu-id="962d9-120">Endpoint a cui applicare gli arricchimenti.</span><span class="sxs-lookup"><span data-stu-id="962d9-120">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="962d9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="962d9-121">-InputObject</span></span>
<span data-ttu-id="962d9-122">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="962d9-122">IotHub object</span></span>

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

### <span data-ttu-id="962d9-123">-Key</span><span class="sxs-lookup"><span data-stu-id="962d9-123">-Key</span></span>
<span data-ttu-id="962d9-124">Chiave di arricchimento.</span><span class="sxs-lookup"><span data-stu-id="962d9-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="962d9-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="962d9-125">-Name</span></span>
<span data-ttu-id="962d9-126">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="962d9-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="962d9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="962d9-127">-ResourceGroupName</span></span>
<span data-ttu-id="962d9-128">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="962d9-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="962d9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="962d9-129">-ResourceId</span></span>
<span data-ttu-id="962d9-130">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="962d9-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="962d9-131">-Valore</span><span class="sxs-lookup"><span data-stu-id="962d9-131">-Value</span></span>
<span data-ttu-id="962d9-132">Valore di arricchimento.</span><span class="sxs-lookup"><span data-stu-id="962d9-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="962d9-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="962d9-133">-Confirm</span></span>
<span data-ttu-id="962d9-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="962d9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="962d9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="962d9-135">-WhatIf</span></span>
<span data-ttu-id="962d9-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="962d9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="962d9-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="962d9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="962d9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="962d9-138">CommonParameters</span></span>
<span data-ttu-id="962d9-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="962d9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="962d9-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="962d9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="962d9-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="962d9-141">INPUTS</span></span>

### <span data-ttu-id="962d9-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="962d9-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="962d9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="962d9-143">System.String</span></span>

## <span data-ttu-id="962d9-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="962d9-144">OUTPUTS</span></span>

### <span data-ttu-id="962d9-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="962d9-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="962d9-146">Note</span><span class="sxs-lookup"><span data-stu-id="962d9-146">NOTES</span></span>

## <span data-ttu-id="962d9-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="962d9-147">RELATED LINKS</span></span>