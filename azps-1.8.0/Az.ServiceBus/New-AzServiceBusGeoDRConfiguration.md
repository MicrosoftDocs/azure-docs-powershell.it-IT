---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c6e711b31dceaf040065750195ce6990b027676b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677146"
---
# <span data-ttu-id="198fe-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="198fe-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="198fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="198fe-102">SYNOPSIS</span></span>
<span data-ttu-id="198fe-103">Crea un nuovo alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="198fe-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="198fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="198fe-104">SYNTAX</span></span>

### <span data-ttu-id="198fe-105">GeoDRPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="198fe-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="198fe-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="198fe-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="198fe-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="198fe-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="198fe-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="198fe-108">DESCRIPTION</span></span>
<span data-ttu-id="198fe-109">Il cmdlet **New-AzServiceBusGeoDRConfiguration** crea un nuovo alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="198fe-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="198fe-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="198fe-110">EXAMPLES</span></span>

### <span data-ttu-id="198fe-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="198fe-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="198fe-112">Crea un alias "SampleDRCongifName" con lo spazio dei nomi principale "SampleNamespace_Primary" con lo spazio dei nomi secondario "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="198fe-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="198fe-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="198fe-113">PARAMETERS</span></span>

### <span data-ttu-id="198fe-114">-Alternaname</span><span class="sxs-lookup"><span data-stu-id="198fe-114">-AlternateName</span></span>
<span data-ttu-id="198fe-115">Alternaname</span><span class="sxs-lookup"><span data-stu-id="198fe-115">AlternateName</span></span>

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

### <span data-ttu-id="198fe-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="198fe-116">-AsJob</span></span>
<span data-ttu-id="198fe-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="198fe-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="198fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="198fe-118">-DefaultProfile</span></span>
<span data-ttu-id="198fe-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="198fe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="198fe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="198fe-120">-InputObject</span></span>
<span data-ttu-id="198fe-121">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="198fe-121">Namespace Object</span></span>

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

### <span data-ttu-id="198fe-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="198fe-122">-Name</span></span>
<span data-ttu-id="198fe-123">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="198fe-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="198fe-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="198fe-124">-Namespace</span></span>
<span data-ttu-id="198fe-125">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="198fe-125">Namespace Name</span></span>

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

### <span data-ttu-id="198fe-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="198fe-126">-PartnerNamespace</span></span>
<span data-ttu-id="198fe-127">DR Configuration PartnerNamespace (ARM ID di PartnerNamespace [namespace secondario])</span><span class="sxs-lookup"><span data-stu-id="198fe-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="198fe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="198fe-128">-ResourceGroupName</span></span>
<span data-ttu-id="198fe-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="198fe-129">Resource Group Name</span></span>

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

### <span data-ttu-id="198fe-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="198fe-130">-ResourceId</span></span>
<span data-ttu-id="198fe-131">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="198fe-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="198fe-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="198fe-132">-Confirm</span></span>
<span data-ttu-id="198fe-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="198fe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="198fe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="198fe-134">-WhatIf</span></span>
<span data-ttu-id="198fe-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="198fe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="198fe-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="198fe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="198fe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="198fe-137">CommonParameters</span></span>
<span data-ttu-id="198fe-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="198fe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="198fe-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="198fe-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="198fe-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="198fe-140">INPUTS</span></span>

### <span data-ttu-id="198fe-141">System. String</span><span class="sxs-lookup"><span data-stu-id="198fe-141">System.String</span></span>

### <span data-ttu-id="198fe-142">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="198fe-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="198fe-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="198fe-143">OUTPUTS</span></span>

### <span data-ttu-id="198fe-144">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="198fe-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="198fe-145">Note</span><span class="sxs-lookup"><span data-stu-id="198fe-145">NOTES</span></span>

## <span data-ttu-id="198fe-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="198fe-146">RELATED LINKS</span></span>