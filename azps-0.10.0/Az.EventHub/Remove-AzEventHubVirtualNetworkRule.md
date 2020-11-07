---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 9385d8ca958eab28f485e56fbcd6c926f5422ca0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861434"
---
# <span data-ttu-id="094aa-101">Remove-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="094aa-101">Remove-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="094aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="094aa-102">SYNOPSIS</span></span>
<span data-ttu-id="094aa-103">Rimuove il singolo VirtualNetworkRule specifico per la NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="094aa-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="094aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="094aa-104">SYNTAX</span></span>

### <span data-ttu-id="094aa-105">VirtualNetworkRulePropertiesParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="094aa-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="094aa-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="094aa-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="094aa-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="094aa-107">DESCRIPTION</span></span>
<span data-ttu-id="094aa-108">Rimuove il singolo VirtualNetworkRule specifico per la NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="094aa-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="094aa-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="094aa-109">EXAMPLES</span></span>

### <span data-ttu-id="094aa-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="094aa-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="094aa-111">Rimuove il singolo VirtualNetworkRule specifico per la NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="094aa-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="094aa-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="094aa-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="094aa-113">Rimuovere la $virtualruleset 1 di NetworkRuleSet per lo spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="094aa-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="094aa-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="094aa-114">PARAMETERS</span></span>

### <span data-ttu-id="094aa-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="094aa-115">-AsJob</span></span>
<span data-ttu-id="094aa-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="094aa-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="094aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="094aa-117">-DefaultProfile</span></span>
<span data-ttu-id="094aa-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="094aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="094aa-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="094aa-119">-Name</span></span>
<span data-ttu-id="094aa-120">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="094aa-120">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="094aa-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="094aa-121">-PassThru</span></span>
<span data-ttu-id="094aa-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="094aa-122">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="094aa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="094aa-123">-ResourceGroupName</span></span>
<span data-ttu-id="094aa-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="094aa-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="094aa-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="094aa-125">-SubnetId</span></span>
<span data-ttu-id="094aa-126">ID risorsa subnet</span><span class="sxs-lookup"><span data-stu-id="094aa-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="094aa-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="094aa-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="094aa-128">Oggetto di configurazione IPRule</span><span class="sxs-lookup"><span data-stu-id="094aa-128">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="094aa-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="094aa-129">-Confirm</span></span>
<span data-ttu-id="094aa-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="094aa-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="094aa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="094aa-131">-WhatIf</span></span>
<span data-ttu-id="094aa-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="094aa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="094aa-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="094aa-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="094aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="094aa-134">CommonParameters</span></span>
<span data-ttu-id="094aa-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="094aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="094aa-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="094aa-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="094aa-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="094aa-137">INPUTS</span></span>

### <span data-ttu-id="094aa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="094aa-138">System.String</span></span>

### <span data-ttu-id="094aa-139">Microsoft. Azure. Commands. EventHub. Models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="094aa-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="094aa-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="094aa-140">OUTPUTS</span></span>

### <span data-ttu-id="094aa-141">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="094aa-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="094aa-142">Note</span><span class="sxs-lookup"><span data-stu-id="094aa-142">NOTES</span></span>

## <span data-ttu-id="094aa-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="094aa-143">RELATED LINKS</span></span>