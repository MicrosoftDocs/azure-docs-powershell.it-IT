---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 02335868ca9984d4da57be905b9600b81333b484
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956622"
---
# <span data-ttu-id="550ce-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="550ce-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="550ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="550ce-102">SYNOPSIS</span></span>
<span data-ttu-id="550ce-103">Crea un nuovo alias (configurazione di ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="550ce-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="550ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="550ce-104">SYNTAX</span></span>

### <span data-ttu-id="550ce-105">GeoDRPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="550ce-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="550ce-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="550ce-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="550ce-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="550ce-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="550ce-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="550ce-108">DESCRIPTION</span></span>
<span data-ttu-id="550ce-109">Il cmdlet **New-AzServiceBusGeoDRConfiguration** crea un nuovo alias (configurazione di ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="550ce-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="550ce-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="550ce-110">EXAMPLES</span></span>

### <span data-ttu-id="550ce-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="550ce-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="550ce-112">Crea un alias "SampleDRConfigName" con lo spazio dei nomi primario "SampleNamespace_Primary" con lo spazio dei nomi secondario "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="550ce-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="550ce-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="550ce-113">PARAMETERS</span></span>

### <span data-ttu-id="550ce-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="550ce-114">-AlternateName</span></span>
<span data-ttu-id="550ce-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="550ce-115">AlternateName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="550ce-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="550ce-116">-AsJob</span></span>
<span data-ttu-id="550ce-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="550ce-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="550ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="550ce-118">-DefaultProfile</span></span>
<span data-ttu-id="550ce-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="550ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="550ce-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="550ce-120">-InputObject</span></span>
<span data-ttu-id="550ce-121">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="550ce-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="550ce-122">-Name</span><span class="sxs-lookup"><span data-stu-id="550ce-122">-Name</span></span>
<span data-ttu-id="550ce-123">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="550ce-123">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="550ce-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="550ce-124">-Namespace</span></span>
<span data-ttu-id="550ce-125">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="550ce-125">Namespace Name</span></span>

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

### <span data-ttu-id="550ce-126">-PartnerEnne</span><span class="sxs-lookup"><span data-stu-id="550ce-126">-PartnerNamespace</span></span>
<span data-ttu-id="550ce-127">DR Configuration Partner Informazioni (ARM ID partner Di Partner Consente di [Spazio dei nomi secondario])</span><span class="sxs-lookup"><span data-stu-id="550ce-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="550ce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="550ce-128">-ResourceGroupName</span></span>
<span data-ttu-id="550ce-129">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="550ce-129">Resource Group Name</span></span>

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

### <span data-ttu-id="550ce-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="550ce-130">-ResourceId</span></span>
<span data-ttu-id="550ce-131">ID risorsa spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="550ce-131">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="550ce-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="550ce-132">-Confirm</span></span>
<span data-ttu-id="550ce-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="550ce-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="550ce-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="550ce-134">-WhatIf</span></span>
<span data-ttu-id="550ce-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="550ce-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="550ce-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="550ce-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="550ce-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="550ce-137">CommonParameters</span></span>
<span data-ttu-id="550ce-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="550ce-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="550ce-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="550ce-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="550ce-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="550ce-140">INPUTS</span></span>

### <span data-ttu-id="550ce-141">System.String</span><span class="sxs-lookup"><span data-stu-id="550ce-141">System.String</span></span>

### <span data-ttu-id="550ce-142">Microsoft.Azure.Commands.ServiceBus.Models.PSAttributes</span><span class="sxs-lookup"><span data-stu-id="550ce-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="550ce-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="550ce-143">OUTPUTS</span></span>

### <span data-ttu-id="550ce-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="550ce-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="550ce-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="550ce-145">NOTES</span></span>

## <span data-ttu-id="550ce-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="550ce-146">RELATED LINKS</span></span>
