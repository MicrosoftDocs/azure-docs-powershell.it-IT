---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 4c9d4d1a4ec79da0677bc44d53a3843aa9a6d102
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674452"
---
# <span data-ttu-id="59cbb-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="59cbb-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="59cbb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="59cbb-103">Recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="59cbb-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="59cbb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59cbb-104">SYNTAX</span></span>

### <span data-ttu-id="59cbb-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59cbb-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59cbb-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="59cbb-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59cbb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59cbb-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59cbb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59cbb-108">DESCRIPTION</span></span>
<span data-ttu-id="59cbb-109">**Get-AzEventHubGeoDRConfiguration** recupera l'alias (configurazione del ripristino di emergenza) per lo spazio dei nomi primario o secondario</span><span class="sxs-lookup"><span data-stu-id="59cbb-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="59cbb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59cbb-110">EXAMPLES</span></span>

### <span data-ttu-id="59cbb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="59cbb-111">Example 1</span></span>
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

<span data-ttu-id="59cbb-112">Recupera la configurazione alias "SampleDRConfigName" per lo spazio dei nomi principale "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="59cbb-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="59cbb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59cbb-113">PARAMETERS</span></span>

### <span data-ttu-id="59cbb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59cbb-114">-DefaultProfile</span></span>
<span data-ttu-id="59cbb-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59cbb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59cbb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59cbb-116">-InputObject</span></span>
<span data-ttu-id="59cbb-117">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="59cbb-117">Namespace Object</span></span>

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

### <span data-ttu-id="59cbb-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="59cbb-118">-Name</span></span>
<span data-ttu-id="59cbb-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="59cbb-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="59cbb-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="59cbb-120">-Namespace</span></span>
<span data-ttu-id="59cbb-121">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="59cbb-121">Namespace Name</span></span>

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

### <span data-ttu-id="59cbb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59cbb-122">-ResourceGroupName</span></span>
<span data-ttu-id="59cbb-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="59cbb-123">Resource Group Name</span></span>

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

### <span data-ttu-id="59cbb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59cbb-124">-ResourceId</span></span>
<span data-ttu-id="59cbb-125">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="59cbb-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="59cbb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59cbb-126">CommonParameters</span></span>
<span data-ttu-id="59cbb-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59cbb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59cbb-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59cbb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59cbb-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59cbb-129">INPUTS</span></span>

### <span data-ttu-id="59cbb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="59cbb-130">System.String</span></span>

### <span data-ttu-id="59cbb-131">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="59cbb-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="59cbb-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59cbb-132">OUTPUTS</span></span>

### <span data-ttu-id="59cbb-133">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="59cbb-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="59cbb-134">Note</span><span class="sxs-lookup"><span data-stu-id="59cbb-134">NOTES</span></span>

## <span data-ttu-id="59cbb-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59cbb-135">RELATED LINKS</span></span>
