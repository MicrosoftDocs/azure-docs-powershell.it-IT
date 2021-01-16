---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 5a2f3a3310675324fde3ff262cf88325224193c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343687"
---
# <span data-ttu-id="cf8ea-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf8ea-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="cf8ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf8ea-102">SYNOPSIS</span></span>
<span data-ttu-id="cf8ea-103">Recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="cf8ea-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="cf8ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf8ea-104">SYNTAX</span></span>

### <span data-ttu-id="cf8ea-105">GeoDRPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cf8ea-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf8ea-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cf8ea-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf8ea-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf8ea-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf8ea-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf8ea-108">DESCRIPTION</span></span>
<span data-ttu-id="cf8ea-109">**Get-AzServiceBusGeoDRConfiguration** recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="cf8ea-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="cf8ea-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf8ea-110">EXAMPLES</span></span>

### <span data-ttu-id="cf8ea-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cf8ea-111">Example 1</span></span>
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

<span data-ttu-id="cf8ea-112">Recupera la configurazione alias "SampleDRConfigName" per lo spazio dei nomi principale "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="cf8ea-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="cf8ea-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf8ea-113">PARAMETERS</span></span>

### <span data-ttu-id="cf8ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf8ea-114">-DefaultProfile</span></span>
<span data-ttu-id="cf8ea-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf8ea-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf8ea-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf8ea-116">-InputObject</span></span>
<span data-ttu-id="cf8ea-117">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="cf8ea-117">Namespace Object</span></span>

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

### <span data-ttu-id="cf8ea-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf8ea-118">-Name</span></span>
<span data-ttu-id="cf8ea-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="cf8ea-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="cf8ea-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cf8ea-120">-Namespace</span></span>
<span data-ttu-id="cf8ea-121">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cf8ea-121">Namespace Name</span></span>

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

### <span data-ttu-id="cf8ea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf8ea-122">-ResourceGroupName</span></span>
<span data-ttu-id="cf8ea-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="cf8ea-123">Resource Group Name</span></span>

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

### <span data-ttu-id="cf8ea-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf8ea-124">-ResourceId</span></span>
<span data-ttu-id="cf8ea-125">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cf8ea-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="cf8ea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf8ea-126">CommonParameters</span></span>
<span data-ttu-id="cf8ea-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf8ea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf8ea-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf8ea-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf8ea-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf8ea-129">INPUTS</span></span>

### <span data-ttu-id="cf8ea-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cf8ea-130">System.String</span></span>

### <span data-ttu-id="cf8ea-131">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="cf8ea-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="cf8ea-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf8ea-132">OUTPUTS</span></span>

### <span data-ttu-id="cf8ea-133">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="cf8ea-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="cf8ea-134">Note</span><span class="sxs-lookup"><span data-stu-id="cf8ea-134">NOTES</span></span>

## <span data-ttu-id="cf8ea-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf8ea-135">RELATED LINKS</span></span>
