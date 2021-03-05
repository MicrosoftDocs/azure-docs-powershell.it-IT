---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 3fa1dd4c3f926e0c6011d8ffec3a510340a7eab3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999725"
---
# <span data-ttu-id="f8471-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8471-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="f8471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8471-102">SYNOPSIS</span></span>
<span data-ttu-id="f8471-103">Elimina un alias (configurazione di ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="f8471-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f8471-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8471-104">SYNTAX</span></span>

### <span data-ttu-id="f8471-105">GeoDRPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f8471-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8471-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f8471-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8471-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8471-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8471-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f8471-108">DESCRIPTION</span></span>
<span data-ttu-id="f8471-109">Il cmdlet **Remove-AzServiceBusGeoDRConfiguration** elimina un alias (configurazione di ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="f8471-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f8471-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8471-110">EXAMPLES</span></span>

### <span data-ttu-id="f8471-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f8471-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="f8471-112">Elimina un alias (configurazione di ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="f8471-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f8471-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8471-113">PARAMETERS</span></span>

### <span data-ttu-id="f8471-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8471-114">-AsJob</span></span>
<span data-ttu-id="f8471-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f8471-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8471-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8471-116">-DefaultProfile</span></span>
<span data-ttu-id="f8471-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8471-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8471-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8471-118">-InputObject</span></span>
<span data-ttu-id="f8471-119">Oggetto di configurazione GeoDR del bus di servizio</span><span class="sxs-lookup"><span data-stu-id="f8471-119">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8471-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f8471-120">-Name</span></span>
<span data-ttu-id="f8471-121">Nome alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="f8471-121">Alias (GeoDR) Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8471-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f8471-122">-Namespace</span></span>
<span data-ttu-id="f8471-123">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f8471-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8471-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8471-124">-PassThru</span></span>
<span data-ttu-id="f8471-125">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="f8471-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f8471-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f8471-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f8471-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8471-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8471-128">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f8471-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8471-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8471-129">-ResourceId</span></span>
<span data-ttu-id="f8471-130">ID risorsa GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8471-130">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8471-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8471-131">-Confirm</span></span>
<span data-ttu-id="f8471-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8471-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8471-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8471-133">-WhatIf</span></span>
<span data-ttu-id="f8471-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8471-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8471-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8471-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8471-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8471-136">CommonParameters</span></span>
<span data-ttu-id="f8471-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8471-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8471-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8471-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8471-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="f8471-139">INPUTS</span></span>

### <span data-ttu-id="f8471-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f8471-140">System.String</span></span>

### <span data-ttu-id="f8471-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f8471-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="f8471-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8471-142">OUTPUTS</span></span>

### <span data-ttu-id="f8471-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f8471-143">System.Boolean</span></span>

## <span data-ttu-id="f8471-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="f8471-144">NOTES</span></span>

## <span data-ttu-id="f8471-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8471-145">RELATED LINKS</span></span>
