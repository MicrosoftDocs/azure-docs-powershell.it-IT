---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 98e5a6c869fba2a49f56e3f69170602ce1d443a3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861505"
---
# <span data-ttu-id="e8bf3-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8bf3-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="e8bf3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="e8bf3-103">Recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="e8bf3-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="e8bf3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8bf3-104">SYNTAX</span></span>

### <span data-ttu-id="e8bf3-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e8bf3-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8bf3-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e8bf3-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8bf3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8bf3-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8bf3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8bf3-108">DESCRIPTION</span></span>
<span data-ttu-id="e8bf3-109">**Get-AzEventHubGeoDRConfiguration** recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="e8bf3-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="e8bf3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8bf3-110">EXAMPLES</span></span>

### <span data-ttu-id="e8bf3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e8bf3-111">Example 1</span></span>
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

<span data-ttu-id="e8bf3-112">Recupera la configurazione alias "SampleDRConfigName" per lo spazio dei nomi principale "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="e8bf3-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="e8bf3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8bf3-113">PARAMETERS</span></span>

### <span data-ttu-id="e8bf3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8bf3-114">-DefaultProfile</span></span>
<span data-ttu-id="e8bf3-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8bf3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8bf3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8bf3-116">-InputObject</span></span>
<span data-ttu-id="e8bf3-117">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="e8bf3-117">Namespace Object</span></span>

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

### <span data-ttu-id="e8bf3-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8bf3-118">-Name</span></span>
<span data-ttu-id="e8bf3-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="e8bf3-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="e8bf3-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e8bf3-120">-Namespace</span></span>
<span data-ttu-id="e8bf3-121">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e8bf3-121">Namespace Name</span></span>

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

### <span data-ttu-id="e8bf3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8bf3-122">-ResourceGroupName</span></span>
<span data-ttu-id="e8bf3-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="e8bf3-123">Resource Group Name</span></span>

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

### <span data-ttu-id="e8bf3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8bf3-124">-ResourceId</span></span>
<span data-ttu-id="e8bf3-125">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e8bf3-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="e8bf3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8bf3-126">CommonParameters</span></span>
<span data-ttu-id="e8bf3-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8bf3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8bf3-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8bf3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8bf3-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8bf3-129">INPUTS</span></span>

### <span data-ttu-id="e8bf3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e8bf3-130">System.String</span></span>

### <span data-ttu-id="e8bf3-131">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e8bf3-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="e8bf3-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8bf3-132">OUTPUTS</span></span>

### <span data-ttu-id="e8bf3-133">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="e8bf3-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="e8bf3-134">Note</span><span class="sxs-lookup"><span data-stu-id="e8bf3-134">NOTES</span></span>

## <span data-ttu-id="e8bf3-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8bf3-135">RELATED LINKS</span></span>
