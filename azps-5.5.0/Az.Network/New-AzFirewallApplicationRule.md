---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: d5c3a560f0afcfb28224cf4681af78d6bd5249ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189686"
---
# <span data-ttu-id="662e2-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="662e2-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="662e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="662e2-102">SYNOPSIS</span></span>
<span data-ttu-id="662e2-103">Crea una regola per l'applicazione del firewall.</span><span class="sxs-lookup"><span data-stu-id="662e2-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="662e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="662e2-104">SYNTAX</span></span>

### <span data-ttu-id="662e2-105">TargetFqdn (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="662e2-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -TargetFqdn <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="662e2-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="662e2-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="662e2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="662e2-107">DESCRIPTION</span></span>
<span data-ttu-id="662e2-108">Il cmdlet **New-AzFirewallApplicationRule** crea una regola dell'applicazione per il firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="662e2-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="662e2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="662e2-109">EXAMPLES</span></span>

### <span data-ttu-id="662e2-110">Esempio 1: Creare una regola per consentire tutto il traffico HTTPS da 10.0.0.0</span><span class="sxs-lookup"><span data-stu-id="662e2-110">Example 1: Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```powershell
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="662e2-111">Questo esempio crea una regola che consente tutto il traffico HTTPS sulla porta 443 da 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="662e2-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="662e2-112">Esempio 2: Creare una regola per consentire WindowsUpdate per la subnet 10.0.0.0/24</span><span class="sxs-lookup"><span data-stu-id="662e2-112">Example 2: Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```powershell
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="662e2-113">Questo esempio crea una regola che consente il traffico per gli aggiornamenti di Windows per il dominio 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="662e2-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="662e2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="662e2-114">PARAMETERS</span></span>

### <span data-ttu-id="662e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="662e2-115">-DefaultProfile</span></span>
<span data-ttu-id="662e2-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="662e2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="662e2-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="662e2-117">-Description</span></span>
<span data-ttu-id="662e2-118">Specifica una descrizione facoltativa della regola.</span><span class="sxs-lookup"><span data-stu-id="662e2-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="662e2-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="662e2-119">-FqdnTag</span></span>
<span data-ttu-id="662e2-120">Specifica un elenco di tag FQDN per la regola.</span><span class="sxs-lookup"><span data-stu-id="662e2-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="662e2-121">I tag disponibili possono essere recuperati con il cmdlet [Get-AzFirewallFqdnTag.](./Get-AzFirewallFqdnTag.md)</span><span class="sxs-lookup"><span data-stu-id="662e2-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

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

### <span data-ttu-id="662e2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="662e2-122">-Name</span></span>
<span data-ttu-id="662e2-123">Specifica il nome della regola dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="662e2-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="662e2-124">Il nome deve essere univoco all'interno di una raccolta di regole.</span><span class="sxs-lookup"><span data-stu-id="662e2-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="662e2-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="662e2-125">-Protocol</span></span>
<span data-ttu-id="662e2-126">Specifica il tipo di traffico da filtrare in base alla regola.</span><span class="sxs-lookup"><span data-stu-id="662e2-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="662e2-127">Il formato <protocol type> è: <port> .</span><span class="sxs-lookup"><span data-stu-id="662e2-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="662e2-128">Ad esempio, "http:80" o "https:443".</span><span class="sxs-lookup"><span data-stu-id="662e2-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="662e2-129">Protocollo obbligatorio quando viene usato TargetFqdn, ma non può essere usato con FqdnTag.</span><span class="sxs-lookup"><span data-stu-id="662e2-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="662e2-130">I protocolli supportati sono HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="662e2-130">The supported protocols are HTTP and HTTPS.</span></span>

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

### <span data-ttu-id="662e2-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="662e2-131">-SourceAddress</span></span>
<span data-ttu-id="662e2-132">Indirizzi di origine della regola</span><span class="sxs-lookup"><span data-stu-id="662e2-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="662e2-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="662e2-133">-SourceIpGroup</span></span>
<span data-ttu-id="662e2-134">Ipgroup di origine della regola</span><span class="sxs-lookup"><span data-stu-id="662e2-134">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="662e2-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="662e2-135">-TargetFqdn</span></span>
<span data-ttu-id="662e2-136">Specifica un elenco di nomi di dominio filtrati in base alla regola.</span><span class="sxs-lookup"><span data-stu-id="662e2-136">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="662e2-137">Il carattere asterisco ' ' viene accettato solo come *primo carattere di un FQDN nell'elenco. Se usato, l'asterisco corrisponde a un numero qualsiasi di caratteri. (ad esempio, "msn.com"* corrisponderà msn.com e a tutti i relativi sottodomini)</span><span class="sxs-lookup"><span data-stu-id="662e2-137">The asterisk character, '*', is accepted only as the first character of an FQDN in the list. When used, the asterisk matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

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

### <span data-ttu-id="662e2-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="662e2-138">-Confirm</span></span>
<span data-ttu-id="662e2-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="662e2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="662e2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="662e2-140">-WhatIf</span></span>
<span data-ttu-id="662e2-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="662e2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="662e2-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="662e2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="662e2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="662e2-143">CommonParameters</span></span>
<span data-ttu-id="662e2-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="662e2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="662e2-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="662e2-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="662e2-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="662e2-146">INPUTS</span></span>

### <span data-ttu-id="662e2-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="662e2-147">None</span></span>

## <span data-ttu-id="662e2-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="662e2-148">OUTPUTS</span></span>

### <span data-ttu-id="662e2-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="662e2-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="662e2-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="662e2-150">NOTES</span></span>

## <span data-ttu-id="662e2-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="662e2-151">RELATED LINKS</span></span>

[<span data-ttu-id="662e2-152">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="662e2-152">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="662e2-153">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="662e2-153">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="662e2-154">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="662e2-154">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="662e2-155">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="662e2-155">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)
