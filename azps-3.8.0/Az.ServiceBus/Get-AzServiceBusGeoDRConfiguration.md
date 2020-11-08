---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 5a2f3a3310675324fde3ff262cf88325224193c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021711"
---
# <span data-ttu-id="de796-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="de796-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="de796-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de796-102">SYNOPSIS</span></span>
<span data-ttu-id="de796-103">Recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="de796-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="de796-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de796-104">SYNTAX</span></span>

### <span data-ttu-id="de796-105">GeoDRPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de796-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de796-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="de796-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de796-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de796-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de796-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de796-108">DESCRIPTION</span></span>
<span data-ttu-id="de796-109">**Get-AzServiceBusGeoDRConfiguration** recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="de796-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="de796-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de796-110">EXAMPLES</span></span>

### <span data-ttu-id="de796-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="de796-111">Example 1</span></span>
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

<span data-ttu-id="de796-112">Recupera la configurazione alias "SampleDRConfigName" per lo spazio dei nomi principale "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="de796-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="de796-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de796-113">PARAMETERS</span></span>

### <span data-ttu-id="de796-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de796-114">-DefaultProfile</span></span>
<span data-ttu-id="de796-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de796-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de796-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de796-116">-InputObject</span></span>
<span data-ttu-id="de796-117">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="de796-117">Namespace Object</span></span>

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

### <span data-ttu-id="de796-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="de796-118">-Name</span></span>
<span data-ttu-id="de796-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="de796-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="de796-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="de796-120">-Namespace</span></span>
<span data-ttu-id="de796-121">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="de796-121">Namespace Name</span></span>

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

### <span data-ttu-id="de796-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de796-122">-ResourceGroupName</span></span>
<span data-ttu-id="de796-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="de796-123">Resource Group Name</span></span>

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

### <span data-ttu-id="de796-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de796-124">-ResourceId</span></span>
<span data-ttu-id="de796-125">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="de796-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="de796-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de796-126">CommonParameters</span></span>
<span data-ttu-id="de796-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de796-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de796-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de796-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de796-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de796-129">INPUTS</span></span>

### <span data-ttu-id="de796-130">System. String</span><span class="sxs-lookup"><span data-stu-id="de796-130">System.String</span></span>

### <span data-ttu-id="de796-131">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="de796-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="de796-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de796-132">OUTPUTS</span></span>

### <span data-ttu-id="de796-133">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="de796-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="de796-134">Note</span><span class="sxs-lookup"><span data-stu-id="de796-134">NOTES</span></span>

## <span data-ttu-id="de796-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de796-135">RELATED LINKS</span></span>
