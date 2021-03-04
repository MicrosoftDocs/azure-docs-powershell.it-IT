---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 7fa9cb54a6790a473be419dd934927ed26783d11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957213"
---
# <span data-ttu-id="a6396-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6396-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="a6396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6396-102">SYNOPSIS</span></span>
<span data-ttu-id="a6396-103">Recupera i dettagli di un set di regole di rete per gli hub eventi dello spazio dei nomi nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="a6396-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="a6396-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6396-104">SYNTAX</span></span>

### <span data-ttu-id="a6396-105">NetworkRuleSetPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6396-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6396-106">NetworkRuleSetPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="a6396-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6396-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6396-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6396-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a6396-108">DESCRIPTION</span></span>
<span data-ttu-id="a6396-109">Recupera i dettagli di un set di regole di rete per gli hub eventi dello spazio dei nomi nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="a6396-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="a6396-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6396-110">EXAMPLES</span></span>

### <span data-ttu-id="a6396-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a6396-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="a6396-112">Ottenere i dettagli di Event Hub NetworkruleSet dello spazio dei nomi usando i parametri ResourceGroup e Namespace.</span><span class="sxs-lookup"><span data-stu-id="a6396-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="a6396-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a6396-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="a6396-114">Ottenere i dettagli di Event Hub NetworkruleSet dello spazio dei nomi usando Spazio dei nomi, che si trova nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="a6396-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="a6396-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a6396-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="a6396-116">Ottenere i dettagli di Event Hub NetworkruleSet dello spazio dei nomi usando ID risorsa di altro spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a6396-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="a6396-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6396-117">PARAMETERS</span></span>

### <span data-ttu-id="a6396-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6396-118">-DefaultProfile</span></span>
<span data-ttu-id="a6396-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6396-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6396-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a6396-120">-Namespace</span></span>
<span data-ttu-id="a6396-121">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a6396-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6396-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6396-122">-ResourceGroupName</span></span>
<span data-ttu-id="a6396-123">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a6396-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6396-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6396-124">-ResourceId</span></span>
<span data-ttu-id="a6396-125">ID risorsa spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a6396-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6396-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6396-126">CommonParameters</span></span>
<span data-ttu-id="a6396-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6396-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a6396-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6396-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6396-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="a6396-129">INPUTS</span></span>

### <span data-ttu-id="a6396-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a6396-130">System.String</span></span>

## <span data-ttu-id="a6396-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6396-131">OUTPUTS</span></span>

### <span data-ttu-id="a6396-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="a6396-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="a6396-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="a6396-133">NOTES</span></span>

## <span data-ttu-id="a6396-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6396-134">RELATED LINKS</span></span>