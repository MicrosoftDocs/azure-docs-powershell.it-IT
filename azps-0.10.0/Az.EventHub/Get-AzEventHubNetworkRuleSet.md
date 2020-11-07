---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 64dae906f7f28e119d8550ecf5bb31d1b6ca7b27
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861494"
---
# <span data-ttu-id="b25e0-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b25e0-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="b25e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b25e0-102">SYNOPSIS</span></span>
<span data-ttu-id="b25e0-103">Ottiene i dettagli di un evento Hub NetworkruleSet dello spazio dei nomi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="b25e0-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="b25e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b25e0-104">SYNTAX</span></span>

### <span data-ttu-id="b25e0-105">NetworkRuleSetPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b25e0-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b25e0-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="b25e0-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b25e0-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b25e0-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b25e0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b25e0-108">DESCRIPTION</span></span>
<span data-ttu-id="b25e0-109">Ottiene i dettagli di un evento Hub NetworkruleSet dello spazio dei nomi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="b25e0-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="b25e0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b25e0-110">EXAMPLES</span></span>

### <span data-ttu-id="b25e0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b25e0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="b25e0-112">Ottenere i dettagli degli hub degli eventi NetworkruleSet dello spazio dei nomi usando i parametri ResourceGroup e Namespace.</span><span class="sxs-lookup"><span data-stu-id="b25e0-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="b25e0-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b25e0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="b25e0-114">Ottenere i dettagli degli hub degli eventi NetworkruleSet dello spazio dei nomi usando lo spazio dei nomi che si trova nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="b25e0-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="b25e0-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b25e0-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="b25e0-116">Ottenere i dettagli degli hub degli eventi NetworkruleSet dello spazio dei nomi usando l'ID risorsa di altri spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="b25e0-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="b25e0-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b25e0-117">PARAMETERS</span></span>

### <span data-ttu-id="b25e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b25e0-118">-DefaultProfile</span></span>
<span data-ttu-id="b25e0-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b25e0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b25e0-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b25e0-120">-Namespace</span></span>
<span data-ttu-id="b25e0-121">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b25e0-121">Namespace Name</span></span>

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

### <span data-ttu-id="b25e0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b25e0-122">-ResourceGroupName</span></span>
<span data-ttu-id="b25e0-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b25e0-123">Resource Group Name</span></span>

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

### <span data-ttu-id="b25e0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b25e0-124">-ResourceId</span></span>
<span data-ttu-id="b25e0-125">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b25e0-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="b25e0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b25e0-126">CommonParameters</span></span>
<span data-ttu-id="b25e0-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b25e0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b25e0-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b25e0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b25e0-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b25e0-129">INPUTS</span></span>

### <span data-ttu-id="b25e0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b25e0-130">System.String</span></span>

## <span data-ttu-id="b25e0-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b25e0-131">OUTPUTS</span></span>

### <span data-ttu-id="b25e0-132">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="b25e0-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="b25e0-133">Note</span><span class="sxs-lookup"><span data-stu-id="b25e0-133">NOTES</span></span>

## <span data-ttu-id="b25e0-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b25e0-134">RELATED LINKS</span></span>