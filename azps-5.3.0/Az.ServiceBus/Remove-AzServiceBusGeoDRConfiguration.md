---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c226f11eecc7cf046234378be7f0417da301cf40
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486036"
---
# <span data-ttu-id="5a98e-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a98e-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="5a98e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a98e-102">SYNOPSIS</span></span>
<span data-ttu-id="5a98e-103">Elimina un alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="5a98e-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5a98e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a98e-104">SYNTAX</span></span>

### <span data-ttu-id="5a98e-105">GeoDRPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5a98e-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a98e-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5a98e-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a98e-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a98e-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a98e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a98e-108">DESCRIPTION</span></span>
<span data-ttu-id="5a98e-109">Il cmdlet **Remove-AzServiceBusGeoDRConfiguration** Elimina un alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="5a98e-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5a98e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a98e-110">EXAMPLES</span></span>

### <span data-ttu-id="5a98e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5a98e-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="5a98e-112">Elimina un alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="5a98e-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5a98e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a98e-113">PARAMETERS</span></span>

### <span data-ttu-id="5a98e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a98e-114">-AsJob</span></span>
<span data-ttu-id="5a98e-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5a98e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a98e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a98e-116">-DefaultProfile</span></span>
<span data-ttu-id="5a98e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a98e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a98e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a98e-118">-InputObject</span></span>
<span data-ttu-id="5a98e-119">Oggetto di configurazione di Service Bus GeoDR</span><span class="sxs-lookup"><span data-stu-id="5a98e-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="5a98e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a98e-120">-Name</span></span>
<span data-ttu-id="5a98e-121">Nome alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="5a98e-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="5a98e-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5a98e-122">-Namespace</span></span>
<span data-ttu-id="5a98e-123">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5a98e-123">Namespace Name</span></span>

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

### <span data-ttu-id="5a98e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a98e-124">-PassThru</span></span>
<span data-ttu-id="5a98e-125">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="5a98e-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5a98e-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="5a98e-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5a98e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a98e-127">-ResourceGroupName</span></span>
<span data-ttu-id="5a98e-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="5a98e-128">Resource Group Name</span></span>

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

### <span data-ttu-id="5a98e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a98e-129">-ResourceId</span></span>
<span data-ttu-id="5a98e-130">ID risorsa GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a98e-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="5a98e-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5a98e-131">-Confirm</span></span>
<span data-ttu-id="5a98e-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a98e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a98e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a98e-133">-WhatIf</span></span>
<span data-ttu-id="5a98e-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a98e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a98e-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a98e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a98e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a98e-136">CommonParameters</span></span>
<span data-ttu-id="5a98e-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a98e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a98e-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a98e-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a98e-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a98e-139">INPUTS</span></span>

### <span data-ttu-id="5a98e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5a98e-140">System.String</span></span>

### <span data-ttu-id="5a98e-141">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="5a98e-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="5a98e-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a98e-142">OUTPUTS</span></span>

### <span data-ttu-id="5a98e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5a98e-143">System.Boolean</span></span>

## <span data-ttu-id="5a98e-144">Note</span><span class="sxs-lookup"><span data-stu-id="5a98e-144">NOTES</span></span>

## <span data-ttu-id="5a98e-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a98e-145">RELATED LINKS</span></span>
