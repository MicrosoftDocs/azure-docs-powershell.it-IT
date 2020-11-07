---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: fd87311c59c0889a57cb22eb08aba855e5c3b49c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677168"
---
# <span data-ttu-id="c48c4-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="c48c4-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="c48c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c48c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c48c4-103">Recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="c48c4-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="c48c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c48c4-104">SYNTAX</span></span>

### <span data-ttu-id="c48c4-105">GeoDRPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c48c4-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c48c4-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c48c4-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c48c4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c48c4-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c48c4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c48c4-108">DESCRIPTION</span></span>
<span data-ttu-id="c48c4-109">**Get-AzServiceBusGeoDRConfiguration** recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="c48c4-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="c48c4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c48c4-110">EXAMPLES</span></span>

### <span data-ttu-id="c48c4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c48c4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="c48c4-112">Recupera la configurazione alias "SampleDRCongifName" per lo spazio dei nomi principale "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="c48c4-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="c48c4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c48c4-113">PARAMETERS</span></span>

### <span data-ttu-id="c48c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48c4-114">-DefaultProfile</span></span>
<span data-ttu-id="c48c4-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c48c4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c48c4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c48c4-116">-InputObject</span></span>
<span data-ttu-id="c48c4-117">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="c48c4-117">Namespace Object</span></span>

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

### <span data-ttu-id="c48c4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c48c4-118">-Name</span></span>
<span data-ttu-id="c48c4-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="c48c4-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="c48c4-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c48c4-120">-Namespace</span></span>
<span data-ttu-id="c48c4-121">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c48c4-121">Namespace Name</span></span>

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

### <span data-ttu-id="c48c4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c48c4-122">-ResourceGroupName</span></span>
<span data-ttu-id="c48c4-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c48c4-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c48c4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c48c4-124">-ResourceId</span></span>
<span data-ttu-id="c48c4-125">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c48c4-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="c48c4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48c4-126">CommonParameters</span></span>
<span data-ttu-id="c48c4-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c48c4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48c4-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c48c4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48c4-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c48c4-129">INPUTS</span></span>

### <span data-ttu-id="c48c4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c48c4-130">System.String</span></span>

### <span data-ttu-id="c48c4-131">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c48c4-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="c48c4-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c48c4-132">OUTPUTS</span></span>

### <span data-ttu-id="c48c4-133">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c48c4-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="c48c4-134">Note</span><span class="sxs-lookup"><span data-stu-id="c48c4-134">NOTES</span></span>

## <span data-ttu-id="c48c4-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c48c4-135">RELATED LINKS</span></span>
