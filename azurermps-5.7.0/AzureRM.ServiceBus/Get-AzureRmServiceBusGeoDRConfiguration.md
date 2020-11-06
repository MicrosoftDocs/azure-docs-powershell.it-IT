---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e5623ed840b9b1d2a7f75150fa686d6f488dc2ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512291"
---
# <span data-ttu-id="d9003-101">Get-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9003-101">Get-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="d9003-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9003-102">SYNOPSIS</span></span>
<span data-ttu-id="d9003-103">Recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="d9003-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9003-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9003-104">SYNTAX</span></span>

### <span data-ttu-id="d9003-105">GeoDRPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9003-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9003-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d9003-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9003-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9003-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9003-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9003-108">DESCRIPTION</span></span>
<span data-ttu-id="d9003-109">**Get-AzureRmServiceBusGeoDRConfiguration** recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="d9003-109">The **Get-AzureRmServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="d9003-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9003-110">EXAMPLES</span></span>

### <span data-ttu-id="d9003-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d9003-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="d9003-112">Recupera la configurazione alias "SampleDRCongifName" per lo spazio dei nomi principale "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="d9003-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="d9003-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9003-113">PARAMETERS</span></span>

### <span data-ttu-id="d9003-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9003-114">-DefaultProfile</span></span>
<span data-ttu-id="d9003-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9003-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9003-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9003-116">-InputObject</span></span>
<span data-ttu-id="d9003-117">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="d9003-117">Namespace Object</span></span>

```yaml
Type: PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9003-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9003-118">-Name</span></span>
<span data-ttu-id="d9003-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="d9003-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9003-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d9003-120">-Namespace</span></span>
<span data-ttu-id="d9003-121">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d9003-121">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9003-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9003-122">-ResourceGroupName</span></span>
<span data-ttu-id="d9003-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d9003-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9003-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9003-124">-ResourceId</span></span>
<span data-ttu-id="d9003-125">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d9003-125">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9003-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9003-126">CommonParameters</span></span>
<span data-ttu-id="d9003-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9003-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d9003-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9003-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9003-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9003-129">INPUTS</span></span>

### <span data-ttu-id="d9003-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d9003-130">System.String</span></span>
<span data-ttu-id="d9003-131">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d9003-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="d9003-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9003-132">OUTPUTS</span></span>

### <span data-ttu-id="d9003-133">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d9003-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="d9003-134">Note</span><span class="sxs-lookup"><span data-stu-id="d9003-134">NOTES</span></span>

## <span data-ttu-id="d9003-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9003-135">RELATED LINKS</span></span>
