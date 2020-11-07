---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 558452481ed3feef979b78d7f134869d141caa20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674202"
---
# <span data-ttu-id="a4ff5-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a4ff5-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="a4ff5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4ff5-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ff5-103">Eliminare l'arricchimento di un messaggio in un hub di un sacco.</span><span class="sxs-lookup"><span data-stu-id="a4ff5-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="a4ff5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4ff5-104">SYNTAX</span></span>

### <span data-ttu-id="a4ff5-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a4ff5-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4ff5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a4ff5-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4ff5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a4ff5-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4ff5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4ff5-108">DESCRIPTION</span></span>
<span data-ttu-id="a4ff5-109">Per una spiegazione dettagliata degli arricchimenti dei messaggi in Azure molto Hub, vedere https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="a4ff5-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="a4ff5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4ff5-110">EXAMPLES</span></span>

### <span data-ttu-id="a4ff5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a4ff5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="a4ff5-112">Elimina l'arricchimento del messaggio "newKey".</span><span class="sxs-lookup"><span data-stu-id="a4ff5-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="a4ff5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4ff5-113">PARAMETERS</span></span>

### <span data-ttu-id="a4ff5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ff5-114">-DefaultProfile</span></span>
<span data-ttu-id="a4ff5-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4ff5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4ff5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4ff5-116">-InputObject</span></span>
<span data-ttu-id="a4ff5-117">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="a4ff5-117">IotHub object</span></span>

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

### <span data-ttu-id="a4ff5-118">-Key</span><span class="sxs-lookup"><span data-stu-id="a4ff5-118">-Key</span></span>
<span data-ttu-id="a4ff5-119">Chiave di arricchimento.</span><span class="sxs-lookup"><span data-stu-id="a4ff5-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="a4ff5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4ff5-120">-Name</span></span>
<span data-ttu-id="a4ff5-121">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="a4ff5-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a4ff5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4ff5-122">-PassThru</span></span>
<span data-ttu-id="a4ff5-123">Consente di restituire l'oggetto Boolean.</span><span class="sxs-lookup"><span data-stu-id="a4ff5-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="a4ff5-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a4ff5-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a4ff5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ff5-125">-ResourceGroupName</span></span>
<span data-ttu-id="a4ff5-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a4ff5-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a4ff5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4ff5-127">-ResourceId</span></span>
<span data-ttu-id="a4ff5-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="a4ff5-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a4ff5-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a4ff5-129">-Confirm</span></span>
<span data-ttu-id="a4ff5-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4ff5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4ff5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4ff5-131">-WhatIf</span></span>
<span data-ttu-id="a4ff5-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4ff5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4ff5-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4ff5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4ff5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ff5-134">CommonParameters</span></span>
<span data-ttu-id="a4ff5-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4ff5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ff5-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4ff5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ff5-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4ff5-137">INPUTS</span></span>

### <span data-ttu-id="a4ff5-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a4ff5-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a4ff5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a4ff5-139">System.String</span></span>

## <span data-ttu-id="a4ff5-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4ff5-140">OUTPUTS</span></span>

### <span data-ttu-id="a4ff5-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4ff5-141">System.Boolean</span></span>

## <span data-ttu-id="a4ff5-142">Note</span><span class="sxs-lookup"><span data-stu-id="a4ff5-142">NOTES</span></span>

## <span data-ttu-id="a4ff5-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4ff5-143">RELATED LINKS</span></span>
