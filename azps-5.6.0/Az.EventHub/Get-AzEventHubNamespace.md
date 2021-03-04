---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: e550afd0b7f580c46b15bd8b6ac68b3b0ad1bc89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957229"
---
# <span data-ttu-id="d5159-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="d5159-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="d5159-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5159-102">SYNOPSIS</span></span>
<span data-ttu-id="d5159-103">Recupera i dettagli di uno spazio dei nomi Hub eventi o ottiene un elenco di tutti gli spazi dei nomi Hub eventi nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="d5159-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="d5159-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5159-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5159-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d5159-105">DESCRIPTION</span></span>
<span data-ttu-id="d5159-106">Il cmdlet Get-AzEventHubNamespace deve recuperare i dettagli di uno spazio dei nomi Hub eventi specificato oppure un elenco di tutti gli spazi dei nomi Hub eventi nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="d5159-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="d5159-107">Se si specifica il nome dello spazio dei nomi, vengono restituiti i dettagli di un singolo spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="d5159-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="d5159-108">Se il nome dello spazio dei nomi non viene specificato, viene restituito un elenco di spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="d5159-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="d5159-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5159-109">EXAMPLES</span></span>

### <span data-ttu-id="d5159-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d5159-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="d5159-111">Ottiene i dettagli dello spazio \` dei nomi MyWithName nel gruppo di risorse \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="d5159-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d5159-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5159-112">PARAMETERS</span></span>

### <span data-ttu-id="d5159-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5159-113">-DefaultProfile</span></span>
<span data-ttu-id="d5159-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5159-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5159-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d5159-115">-Name</span></span>
<span data-ttu-id="d5159-116">Nome spazio dei nomi di EventHub</span><span class="sxs-lookup"><span data-stu-id="d5159-116">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5159-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5159-117">-ResourceGroupName</span></span>
<span data-ttu-id="d5159-118">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d5159-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5159-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5159-119">CommonParameters</span></span>
<span data-ttu-id="d5159-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5159-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5159-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5159-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5159-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="d5159-122">INPUTS</span></span>

### <span data-ttu-id="d5159-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d5159-123">System.String</span></span>

## <span data-ttu-id="d5159-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5159-124">OUTPUTS</span></span>

### <span data-ttu-id="d5159-125">Microsoft.Azure.Commands.EventHub.Models.PSAttributeAttributes</span><span class="sxs-lookup"><span data-stu-id="d5159-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="d5159-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="d5159-126">NOTES</span></span>

## <span data-ttu-id="d5159-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5159-127">RELATED LINKS</span></span>
