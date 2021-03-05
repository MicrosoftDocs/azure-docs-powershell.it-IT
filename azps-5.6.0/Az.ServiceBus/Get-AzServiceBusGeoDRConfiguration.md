---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 21ccb8a16ff3622e6661bd5548721d6d1227e7e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997330"
---
# <span data-ttu-id="21bce-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="21bce-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="21bce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21bce-102">SYNOPSIS</span></span>
<span data-ttu-id="21bce-103">Recupera l'alias (configurazione di ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="21bce-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="21bce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21bce-104">SYNTAX</span></span>

### <span data-ttu-id="21bce-105">GeoDRPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="21bce-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21bce-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="21bce-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21bce-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21bce-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21bce-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="21bce-108">DESCRIPTION</span></span>
<span data-ttu-id="21bce-109">**Get-AzServiceBusGeoDRConfiguration** recupera l'alias (configurazione di ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="21bce-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="21bce-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21bce-110">EXAMPLES</span></span>

### <span data-ttu-id="21bce-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="21bce-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="21bce-112">Recupera la configurazione "SampleDRConfigName" dell'alias per lo spazio dei nomi principale "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="21bce-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="21bce-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21bce-113">PARAMETERS</span></span>

### <span data-ttu-id="21bce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21bce-114">-DefaultProfile</span></span>
<span data-ttu-id="21bce-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21bce-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21bce-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21bce-116">-InputObject</span></span>
<span data-ttu-id="21bce-117">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="21bce-117">Namespace Object</span></span>

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

### <span data-ttu-id="21bce-118">-Name</span><span class="sxs-lookup"><span data-stu-id="21bce-118">-Name</span></span>
<span data-ttu-id="21bce-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="21bce-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="21bce-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="21bce-120">-Namespace</span></span>
<span data-ttu-id="21bce-121">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="21bce-121">Namespace Name</span></span>

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

### <span data-ttu-id="21bce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21bce-122">-ResourceGroupName</span></span>
<span data-ttu-id="21bce-123">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="21bce-123">Resource Group Name</span></span>

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

### <span data-ttu-id="21bce-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21bce-124">-ResourceId</span></span>
<span data-ttu-id="21bce-125">ID risorsa spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="21bce-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21bce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21bce-126">CommonParameters</span></span>
<span data-ttu-id="21bce-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21bce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21bce-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21bce-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21bce-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="21bce-129">INPUTS</span></span>

### <span data-ttu-id="21bce-130">System.String</span><span class="sxs-lookup"><span data-stu-id="21bce-130">System.String</span></span>

### <span data-ttu-id="21bce-131">Microsoft.Azure.Commands.ServiceBus.Models.PSAttributes</span><span class="sxs-lookup"><span data-stu-id="21bce-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="21bce-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21bce-132">OUTPUTS</span></span>

### <span data-ttu-id="21bce-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="21bce-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="21bce-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="21bce-134">NOTES</span></span>

## <span data-ttu-id="21bce-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21bce-135">RELATED LINKS</span></span>
