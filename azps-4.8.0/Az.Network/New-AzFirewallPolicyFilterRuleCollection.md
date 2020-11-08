---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: d5871a9e1a99a27cc0b2728ca3638a0548f42fc6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192793"
---
# <span data-ttu-id="06899-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="06899-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="06899-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06899-102">SYNOPSIS</span></span>
<span data-ttu-id="06899-103">Creare una nuova raccolta di regole dei criteri di filtro di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="06899-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="06899-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06899-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06899-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06899-105">DESCRIPTION</span></span>
<span data-ttu-id="06899-106">Il cmdlet **New-AzFirewallPolicyFilterRuleCollection** crea una raccolta di regole di filtro per un criterio di Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="06899-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="06899-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06899-107">EXAMPLES</span></span>

### <span data-ttu-id="06899-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="06899-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="06899-109">Questo esempio crea una regola di filtro con due condizioni di regola</span><span class="sxs-lookup"><span data-stu-id="06899-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="06899-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06899-110">PARAMETERS</span></span>

### <span data-ttu-id="06899-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="06899-111">-ActionType</span></span>
<span data-ttu-id="06899-112">Azione della raccolta regole</span><span class="sxs-lookup"><span data-stu-id="06899-112">The action of the rule collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06899-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06899-113">-DefaultProfile</span></span>
<span data-ttu-id="06899-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06899-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06899-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="06899-115">-Name</span></span>
<span data-ttu-id="06899-116">Nome della raccolta di regole applicazione</span><span class="sxs-lookup"><span data-stu-id="06899-116">The name of the Application Rule Collection</span></span>

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

### <span data-ttu-id="06899-117">-Priorità</span><span class="sxs-lookup"><span data-stu-id="06899-117">-Priority</span></span>
<span data-ttu-id="06899-118">Priorità della raccolta regole</span><span class="sxs-lookup"><span data-stu-id="06899-118">The priority of the rule collection</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06899-119">-Regola</span><span class="sxs-lookup"><span data-stu-id="06899-119">-Rule</span></span>
<span data-ttu-id="06899-120">Elenco delle regole dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="06899-120">The list of application rules</span></span>

```yaml
Type: PSAzureFirewallPolicyRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06899-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06899-121">-Confirm</span></span>
<span data-ttu-id="06899-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06899-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06899-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06899-123">-WhatIf</span></span>
<span data-ttu-id="06899-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06899-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06899-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06899-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06899-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06899-126">CommonParameters</span></span>
<span data-ttu-id="06899-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06899-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06899-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06899-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06899-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06899-129">INPUTS</span></span>

### <span data-ttu-id="06899-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="06899-130">None</span></span>

## <span data-ttu-id="06899-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06899-131">OUTPUTS</span></span>

### <span data-ttu-id="06899-132">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="06899-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="06899-133">Note</span><span class="sxs-lookup"><span data-stu-id="06899-133">NOTES</span></span>

## <span data-ttu-id="06899-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06899-134">RELATED LINKS</span></span>