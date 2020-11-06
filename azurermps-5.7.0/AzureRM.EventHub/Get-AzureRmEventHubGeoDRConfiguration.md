---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 8c48e6dc8fb095258953a57498b76219dec4ef42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520455"
---
# <span data-ttu-id="7da94-101">Get-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="7da94-101">Get-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="7da94-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7da94-102">SYNOPSIS</span></span>
<span data-ttu-id="7da94-103">Recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="7da94-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7da94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7da94-104">SYNTAX</span></span>

### <span data-ttu-id="7da94-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7da94-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7da94-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7da94-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7da94-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7da94-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7da94-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7da94-108">DESCRIPTION</span></span>
<span data-ttu-id="7da94-109">**Get-AzureRmEventHubGeoDRConfiguration** recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="7da94-109">The **Get-AzureRmEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="7da94-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7da94-110">EXAMPLES</span></span>

### <span data-ttu-id="7da94-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7da94-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="7da94-112">Recupera la configurazione alias "SampleDRCongifName" per lo spazio dei nomi principale "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="7da94-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="7da94-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7da94-113">PARAMETERS</span></span>

### <span data-ttu-id="7da94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da94-114">-DefaultProfile</span></span>
<span data-ttu-id="7da94-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7da94-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7da94-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7da94-116">-InputObject</span></span>
<span data-ttu-id="7da94-117">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="7da94-117">Namespace Object</span></span>

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

### <span data-ttu-id="7da94-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7da94-118">-Name</span></span>
<span data-ttu-id="7da94-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="7da94-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da94-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7da94-120">-Namespace</span></span>
<span data-ttu-id="7da94-121">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7da94-121">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da94-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7da94-122">-ResourceGroupName</span></span>
<span data-ttu-id="7da94-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7da94-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da94-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7da94-124">-ResourceId</span></span>
<span data-ttu-id="7da94-125">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7da94-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="7da94-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da94-126">CommonParameters</span></span>
<span data-ttu-id="7da94-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7da94-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da94-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7da94-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da94-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7da94-129">INPUTS</span></span>

### <span data-ttu-id="7da94-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7da94-130">System.String</span></span>
<span data-ttu-id="7da94-131">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="7da94-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="7da94-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7da94-132">OUTPUTS</span></span>

### <span data-ttu-id="7da94-133">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7da94-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7da94-134">Note</span><span class="sxs-lookup"><span data-stu-id="7da94-134">NOTES</span></span>

## <span data-ttu-id="7da94-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7da94-135">RELATED LINKS</span></span>
