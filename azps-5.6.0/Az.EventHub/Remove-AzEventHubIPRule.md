---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: c8a42bd69cc253d66fede2339f4080558e2f07cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986073"
---
# <span data-ttu-id="3d02e-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="3d02e-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="3d02e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d02e-102">SYNOPSIS</span></span>
<span data-ttu-id="3d02e-103">Rimuovere una singola regola IP in NetworkRuleSet dello spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="3d02e-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="3d02e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d02e-104">SYNTAX</span></span>

### <span data-ttu-id="3d02e-105">IPRulePropertiesParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3d02e-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d02e-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d02e-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d02e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3d02e-107">DESCRIPTION</span></span>
<span data-ttu-id="3d02e-108">Rimuovere una singola regola IP in NetworkRuleSet dello spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="3d02e-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="3d02e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d02e-109">EXAMPLES</span></span>

### <span data-ttu-id="3d02e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3d02e-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="3d02e-111">Rimuove IpMask di NetworkRuleSet dello spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="3d02e-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="3d02e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d02e-112">PARAMETERS</span></span>

### <span data-ttu-id="3d02e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d02e-113">-AsJob</span></span>
<span data-ttu-id="3d02e-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3d02e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d02e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d02e-115">-DefaultProfile</span></span>
<span data-ttu-id="3d02e-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d02e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d02e-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="3d02e-117">-IpMask</span></span>
<span data-ttu-id="3d02e-118">ID risorsa subnet</span><span class="sxs-lookup"><span data-stu-id="3d02e-118">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d02e-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="3d02e-119">-IpRuleObject</span></span>
<span data-ttu-id="3d02e-120">Oggetto di configurazione IPRule</span><span class="sxs-lookup"><span data-stu-id="3d02e-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d02e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3d02e-121">-Name</span></span>
<span data-ttu-id="3d02e-122">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3d02e-122">Namespace Name</span></span>

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

### <span data-ttu-id="3d02e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d02e-123">-PassThru</span></span>
<span data-ttu-id="3d02e-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3d02e-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3d02e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d02e-125">-ResourceGroupName</span></span>
<span data-ttu-id="3d02e-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3d02e-126">Resource Group Name</span></span>

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

### <span data-ttu-id="3d02e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d02e-127">-Confirm</span></span>
<span data-ttu-id="3d02e-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d02e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d02e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d02e-129">-WhatIf</span></span>
<span data-ttu-id="3d02e-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d02e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d02e-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d02e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d02e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d02e-132">CommonParameters</span></span>
<span data-ttu-id="3d02e-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d02e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3d02e-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d02e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d02e-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="3d02e-135">INPUTS</span></span>

### <span data-ttu-id="3d02e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3d02e-136">System.String</span></span>

### <span data-ttu-id="3d02e-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="3d02e-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="3d02e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d02e-138">OUTPUTS</span></span>

### <span data-ttu-id="3d02e-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="3d02e-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="3d02e-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="3d02e-140">NOTES</span></span>

## <span data-ttu-id="3d02e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d02e-141">RELATED LINKS</span></span>