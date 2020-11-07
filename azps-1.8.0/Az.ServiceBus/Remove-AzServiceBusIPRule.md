---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: 3fc71bb4e460cb7763fc437f0bc2ac31860dccdf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677128"
---
# <span data-ttu-id="f203f-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="f203f-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="f203f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f203f-102">SYNOPSIS</span></span>
<span data-ttu-id="f203f-103">Rimuovere un singolo IPrule in NetworkRuleSet dello spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="f203f-103">Remove a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="f203f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f203f-104">SYNTAX</span></span>

### <span data-ttu-id="f203f-105">IPRulePropertiesParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f203f-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f203f-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f203f-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f203f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f203f-107">DESCRIPTION</span></span>
<span data-ttu-id="f203f-108">Rimuovere un singolo IPrule in NetworkRuleSet dello spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="f203f-108">Remove a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="f203f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f203f-109">EXAMPLES</span></span>

### <span data-ttu-id="f203f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f203f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="f203f-111">Rimuove IpMask della NetworkRuleSet dello spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="f203f-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="f203f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f203f-112">PARAMETERS</span></span>

### <span data-ttu-id="f203f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f203f-113">-AsJob</span></span>
<span data-ttu-id="f203f-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f203f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f203f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f203f-115">-DefaultProfile</span></span>
<span data-ttu-id="f203f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f203f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f203f-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="f203f-117">-IpMask</span></span>
<span data-ttu-id="f203f-118">ID risorsa subnet</span><span class="sxs-lookup"><span data-stu-id="f203f-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="f203f-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="f203f-119">-IpRuleObject</span></span>
<span data-ttu-id="f203f-120">Oggetto di configurazione IPRule</span><span class="sxs-lookup"><span data-stu-id="f203f-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f203f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f203f-121">-Name</span></span>
<span data-ttu-id="f203f-122">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f203f-122">Namespace Name</span></span>

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

### <span data-ttu-id="f203f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f203f-123">-PassThru</span></span>
<span data-ttu-id="f203f-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f203f-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f203f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f203f-125">-ResourceGroupName</span></span>
<span data-ttu-id="f203f-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="f203f-126">Resource Group Name</span></span>

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

### <span data-ttu-id="f203f-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f203f-127">-Confirm</span></span>
<span data-ttu-id="f203f-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f203f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f203f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f203f-129">-WhatIf</span></span>
<span data-ttu-id="f203f-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f203f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f203f-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f203f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f203f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f203f-132">CommonParameters</span></span>
<span data-ttu-id="f203f-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f203f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f203f-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f203f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f203f-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f203f-135">INPUTS</span></span>

### <span data-ttu-id="f203f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f203f-136">System.String</span></span>

### <span data-ttu-id="f203f-137">Microsoft. Azure. Commands. ServiceBus. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="f203f-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="f203f-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f203f-138">OUTPUTS</span></span>

### <span data-ttu-id="f203f-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="f203f-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="f203f-140">Note</span><span class="sxs-lookup"><span data-stu-id="f203f-140">NOTES</span></span>

## <span data-ttu-id="f203f-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f203f-141">RELATED LINKS</span></span>
