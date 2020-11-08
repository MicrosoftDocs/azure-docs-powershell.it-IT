---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 683d03537f410b38260b502bc25ed90c9da9b4d2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189707"
---
# <span data-ttu-id="04508-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="04508-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="04508-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="04508-102">SYNOPSIS</span></span>
<span data-ttu-id="04508-103">Eliminare l'arricchimento di un messaggio in un hub di un sacco.</span><span class="sxs-lookup"><span data-stu-id="04508-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="04508-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04508-104">SYNTAX</span></span>

### <span data-ttu-id="04508-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="04508-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04508-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="04508-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04508-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="04508-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04508-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04508-108">DESCRIPTION</span></span>
<span data-ttu-id="04508-109">Per una spiegazione dettagliata degli arricchimenti dei messaggi in Azure molto Hub, vedere https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="04508-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="04508-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04508-110">EXAMPLES</span></span>

### <span data-ttu-id="04508-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="04508-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="04508-112">Elimina l'arricchimento del messaggio "newKey".</span><span class="sxs-lookup"><span data-stu-id="04508-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="04508-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04508-113">PARAMETERS</span></span>

### <span data-ttu-id="04508-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04508-114">-DefaultProfile</span></span>
<span data-ttu-id="04508-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="04508-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04508-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04508-116">-InputObject</span></span>
<span data-ttu-id="04508-117">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="04508-117">IotHub object</span></span>

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

### <span data-ttu-id="04508-118">-Key</span><span class="sxs-lookup"><span data-stu-id="04508-118">-Key</span></span>
<span data-ttu-id="04508-119">Chiave di arricchimento.</span><span class="sxs-lookup"><span data-stu-id="04508-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="04508-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="04508-120">-Name</span></span>
<span data-ttu-id="04508-121">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="04508-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="04508-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04508-122">-PassThru</span></span>
<span data-ttu-id="04508-123">Consente di restituire l'oggetto Boolean.</span><span class="sxs-lookup"><span data-stu-id="04508-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="04508-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="04508-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="04508-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04508-125">-ResourceGroupName</span></span>
<span data-ttu-id="04508-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="04508-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="04508-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04508-127">-ResourceId</span></span>
<span data-ttu-id="04508-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="04508-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="04508-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="04508-129">-Confirm</span></span>
<span data-ttu-id="04508-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04508-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04508-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04508-131">-WhatIf</span></span>
<span data-ttu-id="04508-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04508-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04508-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04508-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04508-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04508-134">CommonParameters</span></span>
<span data-ttu-id="04508-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04508-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04508-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04508-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04508-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="04508-137">INPUTS</span></span>

### <span data-ttu-id="04508-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="04508-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="04508-139">System. String</span><span class="sxs-lookup"><span data-stu-id="04508-139">System.String</span></span>

## <span data-ttu-id="04508-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04508-140">OUTPUTS</span></span>

### <span data-ttu-id="04508-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04508-141">System.Boolean</span></span>

## <span data-ttu-id="04508-142">Note</span><span class="sxs-lookup"><span data-stu-id="04508-142">NOTES</span></span>

## <span data-ttu-id="04508-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04508-143">RELATED LINKS</span></span>
