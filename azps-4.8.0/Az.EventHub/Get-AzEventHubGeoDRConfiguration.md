---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 2e324524319a2eacd24bc08aa727892ef08928c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190744"
---
# <span data-ttu-id="3c327-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c327-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="3c327-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c327-102">SYNOPSIS</span></span>
<span data-ttu-id="3c327-103">Recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="3c327-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="3c327-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c327-104">SYNTAX</span></span>

### <span data-ttu-id="3c327-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c327-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c327-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3c327-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c327-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c327-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c327-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c327-108">DESCRIPTION</span></span>
<span data-ttu-id="3c327-109">**Get-AzEventHubGeoDRConfiguration** recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="3c327-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="3c327-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c327-110">EXAMPLES</span></span>

### <span data-ttu-id="3c327-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3c327-111">Example 1</span></span>
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

<span data-ttu-id="3c327-112">Recupera la configurazione alias "SampleDRConfigName" per lo spazio dei nomi principale "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="3c327-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="3c327-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c327-113">PARAMETERS</span></span>

### <span data-ttu-id="3c327-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c327-114">-DefaultProfile</span></span>
<span data-ttu-id="3c327-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c327-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c327-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c327-116">-InputObject</span></span>
<span data-ttu-id="3c327-117">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="3c327-117">Namespace Object</span></span>

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

### <span data-ttu-id="3c327-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c327-118">-Name</span></span>
<span data-ttu-id="3c327-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="3c327-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="3c327-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3c327-120">-Namespace</span></span>
<span data-ttu-id="3c327-121">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3c327-121">Namespace Name</span></span>

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

### <span data-ttu-id="3c327-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c327-122">-ResourceGroupName</span></span>
<span data-ttu-id="3c327-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="3c327-123">Resource Group Name</span></span>

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

### <span data-ttu-id="3c327-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c327-124">-ResourceId</span></span>
<span data-ttu-id="3c327-125">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3c327-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="3c327-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c327-126">CommonParameters</span></span>
<span data-ttu-id="3c327-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c327-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c327-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c327-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c327-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c327-129">INPUTS</span></span>

### <span data-ttu-id="3c327-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3c327-130">System.String</span></span>

### <span data-ttu-id="3c327-131">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3c327-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="3c327-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c327-132">OUTPUTS</span></span>

### <span data-ttu-id="3c327-133">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="3c327-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="3c327-134">Note</span><span class="sxs-lookup"><span data-stu-id="3c327-134">NOTES</span></span>

## <span data-ttu-id="3c327-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c327-135">RELATED LINKS</span></span>