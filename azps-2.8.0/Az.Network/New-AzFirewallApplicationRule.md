---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: cc3ef8146d7a8ba9f5deb9ad65cf6fcc2dd6ac5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852977"
---
# <span data-ttu-id="f2b02-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="f2b02-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="f2b02-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2b02-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b02-103">Crea una regola di applicazione firewall.</span><span class="sxs-lookup"><span data-stu-id="f2b02-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="f2b02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2b02-104">SYNTAX</span></span>

### <span data-ttu-id="f2b02-105">TargetFqdn (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f2b02-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2b02-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="f2b02-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2b02-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2b02-107">DESCRIPTION</span></span>
<span data-ttu-id="f2b02-108">Il cmdlet **New-AzFirewallApplicationRule** crea una regola dell'applicazione per Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="f2b02-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="f2b02-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2b02-109">EXAMPLES</span></span>

### <span data-ttu-id="f2b02-110">1: creare una regola per consentire tutto il traffico HTTPS da 10.0.0.0</span><span class="sxs-lookup"><span data-stu-id="f2b02-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="f2b02-111">Questo esempio crea una regola che consentirà a tutto il traffico HTTPS sulla porta 443 da 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="f2b02-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="f2b02-112">2: creare una regola per consentire WindowsUpdate per 10.0.0.0/24 subnet</span><span class="sxs-lookup"><span data-stu-id="f2b02-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="f2b02-113">Questo esempio crea una regola che consentirà il traffico per gli aggiornamenti di Windows per 10.0.0.0/24 Domain.</span><span class="sxs-lookup"><span data-stu-id="f2b02-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="f2b02-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2b02-114">PARAMETERS</span></span>

### <span data-ttu-id="f2b02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b02-115">-DefaultProfile</span></span>
<span data-ttu-id="f2b02-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b02-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2b02-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2b02-117">-Description</span></span>
<span data-ttu-id="f2b02-118">Specifica una descrizione facoltativa della regola.</span><span class="sxs-lookup"><span data-stu-id="f2b02-118">Specifies an optional description of this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b02-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="f2b02-119">-FqdnTag</span></span>
<span data-ttu-id="f2b02-120">Specifica un elenco di tag FQDN per la regola.</span><span class="sxs-lookup"><span data-stu-id="f2b02-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="f2b02-121">I tag disponibili possono essere recuperati usando il cmdlet [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) .</span><span class="sxs-lookup"><span data-stu-id="f2b02-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b02-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2b02-122">-Name</span></span>
<span data-ttu-id="f2b02-123">Specifica il nome della regola dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2b02-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="f2b02-124">Il nome deve essere univoco all'interno di una raccolta di regole.</span><span class="sxs-lookup"><span data-stu-id="f2b02-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="f2b02-125">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="f2b02-125">-Protocol</span></span>
<span data-ttu-id="f2b02-126">Specifica il tipo di traffico che deve essere filtrato dalla regola.</span><span class="sxs-lookup"><span data-stu-id="f2b02-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="f2b02-127">Il formato è <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="f2b02-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="f2b02-128">Ad esempio, "http: 80" o "https: 443".</span><span class="sxs-lookup"><span data-stu-id="f2b02-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="f2b02-129">Il protocollo è obbligatorio quando viene usato TargetFqdn, ma non può essere usato con FqdnTag.</span><span class="sxs-lookup"><span data-stu-id="f2b02-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="f2b02-130">I protocolli supportati sono HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f2b02-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b02-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="f2b02-131">-SourceAddress</span></span>
<span data-ttu-id="f2b02-132">Gli indirizzi di origine della regola</span><span class="sxs-lookup"><span data-stu-id="f2b02-132">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b02-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="f2b02-133">-TargetFqdn</span></span>
<span data-ttu-id="f2b02-134">Specifica un elenco di nomi di dominio filtrati da questa regola.</span><span class="sxs-lookup"><span data-stu-id="f2b02-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="f2b02-135">Il carattere asterisco,' *', viene accettato solo come primo carattere di un nome di dominio completo nell'elenco. Quando viene usato, l'asterisco corrisponde a qualsiasi numero di caratteri. (ad esempio, "* MSN.com" corrisponderà a MSN.com e a tutti i relativi sottodomini)</span><span class="sxs-lookup"><span data-stu-id="f2b02-135">The asterisk character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterisk matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b02-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f2b02-136">-Confirm</span></span>
<span data-ttu-id="f2b02-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2b02-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b02-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2b02-138">-WhatIf</span></span>
<span data-ttu-id="f2b02-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2b02-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2b02-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2b02-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b02-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b02-141">CommonParameters</span></span>
<span data-ttu-id="f2b02-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2b02-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b02-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2b02-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b02-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2b02-144">INPUTS</span></span>

### <span data-ttu-id="f2b02-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f2b02-145">None</span></span>

## <span data-ttu-id="f2b02-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2b02-146">OUTPUTS</span></span>

### <span data-ttu-id="f2b02-147">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="f2b02-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="f2b02-148">Note</span><span class="sxs-lookup"><span data-stu-id="f2b02-148">NOTES</span></span>

## <span data-ttu-id="f2b02-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2b02-149">RELATED LINKS</span></span>

[<span data-ttu-id="f2b02-150">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f2b02-150">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="f2b02-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f2b02-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="f2b02-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f2b02-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="f2b02-153">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="f2b02-153">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)
