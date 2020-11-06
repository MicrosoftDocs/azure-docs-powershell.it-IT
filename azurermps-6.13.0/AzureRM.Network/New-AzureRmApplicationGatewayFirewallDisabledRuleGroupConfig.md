---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5ccbeb355834cf1fccb7b4da87c70df72c1f8666
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515076"
---
# <span data-ttu-id="4e287-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="4e287-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="4e287-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e287-102">SYNOPSIS</span></span>
<span data-ttu-id="4e287-103">Crea una nuova configurazione del gruppo di regole disabilitata.</span><span class="sxs-lookup"><span data-stu-id="4e287-103">Creates a new disabled rule group configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e287-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e287-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String>
 [-Rules <System.Collections.Generic.List`1[System.Int32]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e287-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e287-105">DESCRIPTION</span></span>
<span data-ttu-id="4e287-106">Il cmdlet **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** crea una nuova configurazione del gruppo di regole disabilitata.</span><span class="sxs-lookup"><span data-stu-id="4e287-106">The **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="4e287-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e287-107">EXAMPLES</span></span>

### <span data-ttu-id="4e287-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e287-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="4e287-109">Il comando crea una nuova configurazione del gruppo di regole disabilitata per il gruppo di regole denominato "REQUEST-942-APPLICATION-ATTACK-SQLI" con la regola 942130 e la regola 942140 disabilitata.</span><span class="sxs-lookup"><span data-stu-id="4e287-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="4e287-110">La nuova configurazione del gruppo di regole disabilitata viene salvata in $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="4e287-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="4e287-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e287-111">PARAMETERS</span></span>

### <span data-ttu-id="4e287-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e287-112">-DefaultProfile</span></span>
<span data-ttu-id="4e287-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e287-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e287-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="4e287-114">-RuleGroupName</span></span>
<span data-ttu-id="4e287-115">Nome del gruppo di regole che verrà disabilitato.</span><span class="sxs-lookup"><span data-stu-id="4e287-115">The name of the rule group that will be disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e287-116">-Regole</span><span class="sxs-lookup"><span data-stu-id="4e287-116">-Rules</span></span>
<span data-ttu-id="4e287-117">Elenco di regole che verranno disabilitate.</span><span class="sxs-lookup"><span data-stu-id="4e287-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="4e287-118">Se null, tutte le regole del gruppo di regole verranno disabilitate.</span><span class="sxs-lookup"><span data-stu-id="4e287-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e287-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e287-119">CommonParameters</span></span>
<span data-ttu-id="4e287-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e287-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e287-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e287-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e287-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e287-122">INPUTS</span></span>

### <span data-ttu-id="4e287-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4e287-123">None</span></span>

## <span data-ttu-id="4e287-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e287-124">OUTPUTS</span></span>

### <span data-ttu-id="4e287-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="4e287-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="4e287-126">Note</span><span class="sxs-lookup"><span data-stu-id="4e287-126">NOTES</span></span>

## <span data-ttu-id="4e287-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e287-127">RELATED LINKS</span></span>

[<span data-ttu-id="4e287-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e287-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="4e287-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e287-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

