---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 1b9fd10e11cb283f880979e7e4a5d703521c9a87
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864142"
---
# <span data-ttu-id="f5cb6-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="f5cb6-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="f5cb6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f5cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="f5cb6-103">Creare una nuova regola per l'applicazione dei criteri di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="f5cb6-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="f5cb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5cb6-104">SYNTAX</span></span>

### <span data-ttu-id="f5cb6-105">TargetFqdn (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f5cb6-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5cb6-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="f5cb6-106">FqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5cb6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5cb6-107">DESCRIPTION</span></span>
<span data-ttu-id="f5cb6-108">Il cmdlet **New-AzFirewallPolicyApplicationRule** crea una regola dell'applicazione per i criteri di Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="f5cb6-108">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="f5cb6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5cb6-109">EXAMPLES</span></span>

### <span data-ttu-id="f5cb6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f5cb6-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="f5cb6-111">Questo esempio crea una regola dell'applicazione con l'indirizzo di origine, il protocollo e i nomi di dominio completi di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f5cb6-111">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

## <span data-ttu-id="f5cb6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f5cb6-112">PARAMETERS</span></span>

### <span data-ttu-id="f5cb6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5cb6-113">-DefaultProfile</span></span>
<span data-ttu-id="f5cb6-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f5cb6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5cb6-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5cb6-115">-Description</span></span>
<span data-ttu-id="f5cb6-116">Descrizione della regola</span><span class="sxs-lookup"><span data-stu-id="f5cb6-116">The description of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5cb6-117">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="f5cb6-117">-FqdnTag</span></span>
<span data-ttu-id="f5cb6-118">I tag FQDN della regola</span><span class="sxs-lookup"><span data-stu-id="f5cb6-118">The FQDN Tags of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5cb6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5cb6-119">-Name</span></span>
<span data-ttu-id="f5cb6-120">Nome della regola dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="f5cb6-120">The name of the Application Rule</span></span>

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

### <span data-ttu-id="f5cb6-121">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="f5cb6-121">-Protocol</span></span>
<span data-ttu-id="f5cb6-122">Protocolli della regola</span><span class="sxs-lookup"><span data-stu-id="f5cb6-122">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5cb6-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="f5cb6-123">-SourceAddress</span></span>
<span data-ttu-id="f5cb6-124">Gli indirizzi di origine della regola</span><span class="sxs-lookup"><span data-stu-id="f5cb6-124">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5cb6-125">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="f5cb6-125">-TargetFqdn</span></span>
<span data-ttu-id="f5cb6-126">FQDN di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="f5cb6-126">The target FQDNs of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5cb6-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f5cb6-127">-Confirm</span></span>
<span data-ttu-id="f5cb6-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5cb6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5cb6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5cb6-129">-WhatIf</span></span>
<span data-ttu-id="f5cb6-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5cb6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5cb6-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5cb6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5cb6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5cb6-132">CommonParameters</span></span>
<span data-ttu-id="f5cb6-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5cb6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5cb6-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5cb6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5cb6-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f5cb6-135">INPUTS</span></span>

### <span data-ttu-id="f5cb6-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f5cb6-136">None</span></span>

## <span data-ttu-id="f5cb6-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5cb6-137">OUTPUTS</span></span>

### <span data-ttu-id="f5cb6-138">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="f5cb6-138">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="f5cb6-139">Note</span><span class="sxs-lookup"><span data-stu-id="f5cb6-139">NOTES</span></span>

## <span data-ttu-id="f5cb6-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5cb6-140">RELATED LINKS</span></span>
