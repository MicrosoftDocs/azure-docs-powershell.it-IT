---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 780e231f2ca512b5becf0ee068c004dd815cea89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515551"
---
# <span data-ttu-id="cfd5a-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="cfd5a-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="cfd5a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cfd5a-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd5a-103">Crea una nuova configurazione del gruppo di regole disabilitata.</span><span class="sxs-lookup"><span data-stu-id="cfd5a-103">Creates a new disabled rule group configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfd5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cfd5a-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String>
 [-Rules <System.Collections.Generic.List`1[System.Int32]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfd5a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfd5a-105">DESCRIPTION</span></span>
<span data-ttu-id="cfd5a-106">Il cmdlet **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** crea una nuova configurazione del gruppo di regole disabilitata.</span><span class="sxs-lookup"><span data-stu-id="cfd5a-106">The **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="cfd5a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cfd5a-107">EXAMPLES</span></span>

### <span data-ttu-id="cfd5a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cfd5a-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="cfd5a-109">Il comando crea una nuova configurazione del gruppo di regole disabilitata per il gruppo di regole denominato "REQUEST-942-APPLICATION-ATTACK-SQLI" con la regola 942130 e la regola 942140 disabilitata.</span><span class="sxs-lookup"><span data-stu-id="cfd5a-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="cfd5a-110">La nuova configurazione del gruppo di regole disabilitata viene salvata in $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="cfd5a-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="cfd5a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cfd5a-111">PARAMETERS</span></span>

### <span data-ttu-id="cfd5a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfd5a-112">-DefaultProfile</span></span>
<span data-ttu-id="cfd5a-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cfd5a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd5a-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="cfd5a-114">-RuleGroupName</span></span>
<span data-ttu-id="cfd5a-115">Nome del gruppo di regole che verrà disabilitato.</span><span class="sxs-lookup"><span data-stu-id="cfd5a-115">The name of the rule group that will be disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd5a-116">-Regole</span><span class="sxs-lookup"><span data-stu-id="cfd5a-116">-Rules</span></span>
<span data-ttu-id="cfd5a-117">Elenco di regole che verranno disabilitate.</span><span class="sxs-lookup"><span data-stu-id="cfd5a-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="cfd5a-118">Se null, tutte le regole del gruppo di regole verranno disabilitate.</span><span class="sxs-lookup"><span data-stu-id="cfd5a-118">If null, all rules of the rule group will be disabled.</span></span>

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

### <span data-ttu-id="cfd5a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfd5a-119">CommonParameters</span></span>
<span data-ttu-id="cfd5a-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfd5a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfd5a-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfd5a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfd5a-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cfd5a-122">INPUTS</span></span>

### <span data-ttu-id="cfd5a-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cfd5a-123">None</span></span>

## <span data-ttu-id="cfd5a-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cfd5a-124">OUTPUTS</span></span>

### <span data-ttu-id="cfd5a-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="cfd5a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="cfd5a-126">Note</span><span class="sxs-lookup"><span data-stu-id="cfd5a-126">NOTES</span></span>

## <span data-ttu-id="cfd5a-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cfd5a-127">RELATED LINKS</span></span>

[<span data-ttu-id="cfd5a-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfd5a-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="cfd5a-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfd5a-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

