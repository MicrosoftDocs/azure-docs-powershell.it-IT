---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 40a80a975de56a867f0dcbc34aea0e46d42a155d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513843"
---
# <span data-ttu-id="82b68-101">Get-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="82b68-101">Get-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="82b68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82b68-102">SYNOPSIS</span></span>
<span data-ttu-id="82b68-103">Recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="82b68-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82b68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82b68-104">SYNTAX</span></span>

### <span data-ttu-id="82b68-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82b68-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82b68-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="82b68-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82b68-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82b68-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82b68-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82b68-108">DESCRIPTION</span></span>
<span data-ttu-id="82b68-109">**Get-AzureRmEventHubGeoDRConfiguration** recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="82b68-109">The **Get-AzureRmEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="82b68-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82b68-110">EXAMPLES</span></span>

### <span data-ttu-id="82b68-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="82b68-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="82b68-112">Recupera la configurazione alias "SampleDRCongifName" per lo spazio dei nomi principale "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="82b68-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="82b68-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82b68-113">PARAMETERS</span></span>

### <span data-ttu-id="82b68-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b68-114">-DefaultProfile</span></span>
<span data-ttu-id="82b68-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82b68-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82b68-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82b68-116">-InputObject</span></span>
<span data-ttu-id="82b68-117">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="82b68-117">Namespace Object</span></span>

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

### <span data-ttu-id="82b68-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="82b68-118">-Name</span></span>
<span data-ttu-id="82b68-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="82b68-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="82b68-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="82b68-120">-Namespace</span></span>
<span data-ttu-id="82b68-121">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="82b68-121">Namespace Name</span></span>

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

### <span data-ttu-id="82b68-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82b68-122">-ResourceGroupName</span></span>
<span data-ttu-id="82b68-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="82b68-123">Resource Group Name</span></span>

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

### <span data-ttu-id="82b68-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82b68-124">-ResourceId</span></span>
<span data-ttu-id="82b68-125">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="82b68-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="82b68-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b68-126">CommonParameters</span></span>
<span data-ttu-id="82b68-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82b68-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b68-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82b68-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b68-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82b68-129">INPUTS</span></span>

### <span data-ttu-id="82b68-130">System. String</span><span class="sxs-lookup"><span data-stu-id="82b68-130">System.String</span></span>

### <span data-ttu-id="82b68-131">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="82b68-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="82b68-132">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="82b68-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="82b68-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82b68-133">OUTPUTS</span></span>

### <span data-ttu-id="82b68-134">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="82b68-134">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="82b68-135">Note</span><span class="sxs-lookup"><span data-stu-id="82b68-135">NOTES</span></span>

## <span data-ttu-id="82b68-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82b68-136">RELATED LINKS</span></span>
