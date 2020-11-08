---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 05a395ce1244130f5f11eb4e0593a1855dc8fb76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200176"
---
# <span data-ttu-id="9e2c9-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="9e2c9-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="9e2c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e2c9-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2c9-103">Richiama il failover GEO DR e riconfigura l'alias per puntare allo spazio dei nomi secondario</span><span class="sxs-lookup"><span data-stu-id="9e2c9-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="9e2c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e2c9-104">SYNTAX</span></span>

### <span data-ttu-id="9e2c9-105">GeoDRPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e2c9-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e2c9-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9e2c9-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e2c9-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e2c9-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e2c9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e2c9-108">DESCRIPTION</span></span>
<span data-ttu-id="9e2c9-109">Il cmdlet **set-AzServiceBusGeoDRConfigurationFailOver** richiama il failover Geo Dr e riconfigura l'alias per puntare allo spazio dei nomi secondario</span><span class="sxs-lookup"><span data-stu-id="9e2c9-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="9e2c9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e2c9-110">EXAMPLES</span></span>

### <span data-ttu-id="9e2c9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9e2c9-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="9e2c9-112">Richiama il failover su alias "SampleDRConfigName", riconfigura e punta allo spazio dei nomi secondario "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="9e2c9-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="9e2c9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e2c9-113">PARAMETERS</span></span>

### <span data-ttu-id="9e2c9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e2c9-114">-DefaultProfile</span></span>
<span data-ttu-id="9e2c9-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e2c9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e2c9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e2c9-116">-InputObject</span></span>
<span data-ttu-id="9e2c9-117">Oggetto di configurazione di Service Bus GeoDR</span><span class="sxs-lookup"><span data-stu-id="9e2c9-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="9e2c9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e2c9-118">-Name</span></span>
<span data-ttu-id="9e2c9-119">Nome configurazione DR-alias</span><span class="sxs-lookup"><span data-stu-id="9e2c9-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="9e2c9-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9e2c9-120">-Namespace</span></span>
<span data-ttu-id="9e2c9-121">Nome dello spazio dei nomi-spazio dei nomi secondario</span><span class="sxs-lookup"><span data-stu-id="9e2c9-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="9e2c9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e2c9-122">-PassThru</span></span>
<span data-ttu-id="9e2c9-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="9e2c9-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9e2c9-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="9e2c9-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9e2c9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e2c9-125">-ResourceGroupName</span></span>
<span data-ttu-id="9e2c9-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="9e2c9-126">Resource Group Name</span></span>

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

### <span data-ttu-id="9e2c9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e2c9-127">-ResourceId</span></span>
<span data-ttu-id="9e2c9-128">ID risorsa GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e2c9-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="9e2c9-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e2c9-129">-Confirm</span></span>
<span data-ttu-id="9e2c9-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e2c9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e2c9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e2c9-131">-WhatIf</span></span>
<span data-ttu-id="9e2c9-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e2c9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e2c9-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e2c9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e2c9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2c9-134">CommonParameters</span></span>
<span data-ttu-id="9e2c9-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e2c9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e2c9-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e2c9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2c9-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e2c9-137">INPUTS</span></span>

### <span data-ttu-id="9e2c9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9e2c9-138">System.String</span></span>

### <span data-ttu-id="9e2c9-139">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="9e2c9-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="9e2c9-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e2c9-140">OUTPUTS</span></span>

### <span data-ttu-id="9e2c9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e2c9-141">System.Boolean</span></span>

## <span data-ttu-id="9e2c9-142">Note</span><span class="sxs-lookup"><span data-stu-id="9e2c9-142">NOTES</span></span>

## <span data-ttu-id="9e2c9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e2c9-143">RELATED LINKS</span></span>
