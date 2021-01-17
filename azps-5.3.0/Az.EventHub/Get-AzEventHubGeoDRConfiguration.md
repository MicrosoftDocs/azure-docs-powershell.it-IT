---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 2e324524319a2eacd24bc08aa727892ef08928c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387043"
---
# <span data-ttu-id="183e5-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="183e5-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="183e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="183e5-102">SYNOPSIS</span></span>
<span data-ttu-id="183e5-103">Recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="183e5-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="183e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="183e5-104">SYNTAX</span></span>

### <span data-ttu-id="183e5-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="183e5-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="183e5-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="183e5-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="183e5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="183e5-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="183e5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="183e5-108">DESCRIPTION</span></span>
<span data-ttu-id="183e5-109">**Get-AzEventHubGeoDRConfiguration** recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="183e5-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="183e5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="183e5-110">EXAMPLES</span></span>

### <span data-ttu-id="183e5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="183e5-111">Example 1</span></span>
```
PS C:\> Get-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="183e5-112">Recupera la configurazione alias "SampleDRConfigName" per lo spazio dei nomi principale "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="183e5-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="183e5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="183e5-113">PARAMETERS</span></span>

### <span data-ttu-id="183e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="183e5-114">-DefaultProfile</span></span>
<span data-ttu-id="183e5-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="183e5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="183e5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="183e5-116">-InputObject</span></span>
<span data-ttu-id="183e5-117">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="183e5-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="183e5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="183e5-118">-Name</span></span>
<span data-ttu-id="183e5-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="183e5-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="183e5-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="183e5-120">-Namespace</span></span>
<span data-ttu-id="183e5-121">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="183e5-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="183e5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="183e5-122">-ResourceGroupName</span></span>
<span data-ttu-id="183e5-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="183e5-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="183e5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="183e5-124">-ResourceId</span></span>
<span data-ttu-id="183e5-125">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="183e5-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="183e5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="183e5-126">CommonParameters</span></span>
<span data-ttu-id="183e5-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="183e5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="183e5-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="183e5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="183e5-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="183e5-129">INPUTS</span></span>

### <span data-ttu-id="183e5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="183e5-130">System.String</span></span>

### <span data-ttu-id="183e5-131">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="183e5-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="183e5-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="183e5-132">OUTPUTS</span></span>

### <span data-ttu-id="183e5-133">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="183e5-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="183e5-134">Note</span><span class="sxs-lookup"><span data-stu-id="183e5-134">NOTES</span></span>

## <span data-ttu-id="183e5-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="183e5-135">RELATED LINKS</span></span>
