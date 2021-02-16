---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 773f21c189833bf8dd9817d224b83eaf29dd644e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185934"
---
# <span data-ttu-id="17b2c-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="17b2c-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="17b2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="17b2c-103">Recupera i dettagli di un set di regole di rete per gli hub eventi dello spazio dei nomi nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="17b2c-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="17b2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17b2c-104">SYNTAX</span></span>

### <span data-ttu-id="17b2c-105">NetworkRuleSetPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="17b2c-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17b2c-106">NetworkRuleSetPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="17b2c-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17b2c-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17b2c-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17b2c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="17b2c-108">DESCRIPTION</span></span>
<span data-ttu-id="17b2c-109">Recupera i dettagli di un set di regole di rete per gli hub eventi dello spazio dei nomi nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="17b2c-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="17b2c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17b2c-110">EXAMPLES</span></span>

### <span data-ttu-id="17b2c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="17b2c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="17b2c-112">Ottenere i dettagli di Event Hub NetworkruleSet dello spazio dei nomi usando i parametri ResourceGroup e Namespace.</span><span class="sxs-lookup"><span data-stu-id="17b2c-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="17b2c-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="17b2c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="17b2c-114">Ottenere i dettagli di Event Hub NetworkruleSet dello spazio dei nomi usando Spazio dei nomi, che si trova nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="17b2c-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="17b2c-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="17b2c-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="17b2c-116">Ottenere i dettagli di Event Hub NetworkruleSet dello spazio dei nomi usando ID risorsa di altro spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="17b2c-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="17b2c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17b2c-117">PARAMETERS</span></span>

### <span data-ttu-id="17b2c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b2c-118">-DefaultProfile</span></span>
<span data-ttu-id="17b2c-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17b2c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17b2c-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="17b2c-120">-Namespace</span></span>
<span data-ttu-id="17b2c-121">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="17b2c-121">Namespace Name</span></span>

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

### <span data-ttu-id="17b2c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17b2c-122">-ResourceGroupName</span></span>
<span data-ttu-id="17b2c-123">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="17b2c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="17b2c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17b2c-124">-ResourceId</span></span>
<span data-ttu-id="17b2c-125">ID risorsa spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="17b2c-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="17b2c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b2c-126">CommonParameters</span></span>
<span data-ttu-id="17b2c-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b2c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="17b2c-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17b2c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b2c-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="17b2c-129">INPUTS</span></span>

### <span data-ttu-id="17b2c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="17b2c-130">System.String</span></span>

## <span data-ttu-id="17b2c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17b2c-131">OUTPUTS</span></span>

### <span data-ttu-id="17b2c-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="17b2c-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="17b2c-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="17b2c-133">NOTES</span></span>

## <span data-ttu-id="17b2c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17b2c-134">RELATED LINKS</span></span>