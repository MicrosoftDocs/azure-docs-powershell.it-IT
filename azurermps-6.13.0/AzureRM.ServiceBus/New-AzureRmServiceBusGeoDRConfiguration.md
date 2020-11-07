---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e2f1edfa0d1b5fa081754457fa3fc53f310eb345
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686356"
---
# <span data-ttu-id="257e7-101">New-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="257e7-101">New-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="257e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="257e7-102">SYNOPSIS</span></span>
<span data-ttu-id="257e7-103">Crea un nuovo alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="257e7-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="257e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="257e7-104">SYNTAX</span></span>

### <span data-ttu-id="257e7-105">GeoDRPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="257e7-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257e7-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="257e7-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257e7-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="257e7-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="257e7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="257e7-108">DESCRIPTION</span></span>
<span data-ttu-id="257e7-109">Il cmdlet **New-AzureRmServiceBusGeoDRConfiguration** crea un nuovo alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="257e7-109">The **New-AzureRmServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="257e7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="257e7-110">EXAMPLES</span></span>

### <span data-ttu-id="257e7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="257e7-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="257e7-112">Crea un alias "SampleDRCongifName" con lo spazio dei nomi principale "SampleNamespace_Primary" con lo spazio dei nomi secondario "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="257e7-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="257e7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="257e7-113">PARAMETERS</span></span>

### <span data-ttu-id="257e7-114">-Alternaname</span><span class="sxs-lookup"><span data-stu-id="257e7-114">-AlternateName</span></span>
<span data-ttu-id="257e7-115">Alternaname</span><span class="sxs-lookup"><span data-stu-id="257e7-115">AlternateName</span></span>

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

### <span data-ttu-id="257e7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="257e7-116">-AsJob</span></span>
<span data-ttu-id="257e7-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="257e7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="257e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="257e7-118">-DefaultProfile</span></span>
<span data-ttu-id="257e7-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="257e7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257e7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="257e7-120">-InputObject</span></span>
<span data-ttu-id="257e7-121">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="257e7-121">Namespace Object</span></span>

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

### <span data-ttu-id="257e7-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="257e7-122">-Name</span></span>
<span data-ttu-id="257e7-123">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="257e7-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="257e7-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="257e7-124">-Namespace</span></span>
<span data-ttu-id="257e7-125">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="257e7-125">Namespace Name</span></span>

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

### <span data-ttu-id="257e7-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="257e7-126">-PartnerNamespace</span></span>
<span data-ttu-id="257e7-127">DR Configuration PartnerNamespace (ARM ID di PartnerNamespace [namespace secondario])</span><span class="sxs-lookup"><span data-stu-id="257e7-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="257e7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="257e7-128">-ResourceGroupName</span></span>
<span data-ttu-id="257e7-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="257e7-129">Resource Group Name</span></span>

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

### <span data-ttu-id="257e7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="257e7-130">-ResourceId</span></span>
<span data-ttu-id="257e7-131">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="257e7-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="257e7-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="257e7-132">-Confirm</span></span>
<span data-ttu-id="257e7-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="257e7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="257e7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="257e7-134">-WhatIf</span></span>
<span data-ttu-id="257e7-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="257e7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="257e7-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="257e7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="257e7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="257e7-137">CommonParameters</span></span>
<span data-ttu-id="257e7-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="257e7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="257e7-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="257e7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="257e7-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="257e7-140">INPUTS</span></span>

### <span data-ttu-id="257e7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="257e7-141">System.String</span></span>

### <span data-ttu-id="257e7-142">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="257e7-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="257e7-143">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="257e7-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="257e7-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="257e7-144">OUTPUTS</span></span>

### <span data-ttu-id="257e7-145">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="257e7-145">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="257e7-146">Note</span><span class="sxs-lookup"><span data-stu-id="257e7-146">NOTES</span></span>

## <span data-ttu-id="257e7-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="257e7-147">RELATED LINKS</span></span>
