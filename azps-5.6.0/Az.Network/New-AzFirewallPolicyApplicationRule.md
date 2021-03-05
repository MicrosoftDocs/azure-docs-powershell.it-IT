---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 0c7e29b0c9b59842e885cf8763da63c2d65cfff2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001117"
---
# <span data-ttu-id="21055-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="21055-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="21055-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21055-102">SYNOPSIS</span></span>
<span data-ttu-id="21055-103">Creare una nuova regola per l'applicazione dei criteri del firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="21055-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="21055-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21055-104">SYNTAX</span></span>

### <span data-ttu-id="21055-105">SourceAddressAndTargetFqdn (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="21055-105">SourceAddressAndTargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21055-106">SourceAddressAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="21055-106">SourceAddressAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21055-107">SourceAddressAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="21055-107">SourceAddressAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21055-108">SourceAddressAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="21055-108">SourceAddressAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21055-109">SourceIpGroupAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="21055-109">SourceIpGroupAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21055-110">SourceIpGroupAndTargetFqdn</span><span class="sxs-lookup"><span data-stu-id="21055-110">SourceIpGroupAndTargetFqdn</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21055-111">SourceIpGroupAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="21055-111">SourceIpGroupAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21055-112">SourceIpGroupAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="21055-112">SourceIpGroupAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21055-113">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="21055-113">DESCRIPTION</span></span>
<span data-ttu-id="21055-114">Il cmdlet **New-AzFirewallPolicyApplicationRule** crea una regola dell'applicazione per un criterio del firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="21055-114">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="21055-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21055-115">EXAMPLES</span></span>

### <span data-ttu-id="21055-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="21055-116">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="21055-117">Questo esempio crea una regola dell'applicazione con l'indirizzo di origine, il protocollo e gli FQDN di destinazione.</span><span class="sxs-lookup"><span data-stu-id="21055-117">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

### <span data-ttu-id="21055-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="21055-118">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -WebCategory "DatingAndPersonals", "Tasteless"
```

<span data-ttu-id="21055-119">Questo esempio crea una regola dell'applicazione con l'indirizzo di origine, il protocollo e le categorie Web.</span><span class="sxs-lookup"><span data-stu-id="21055-119">This example creates an application rule with the source address, protocol and web categories.</span></span>

## <span data-ttu-id="21055-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21055-120">PARAMETERS</span></span>

### <span data-ttu-id="21055-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21055-121">-DefaultProfile</span></span>
<span data-ttu-id="21055-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21055-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21055-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="21055-123">-Description</span></span>
<span data-ttu-id="21055-124">Descrizione della regola</span><span class="sxs-lookup"><span data-stu-id="21055-124">The description of the rule</span></span>

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

### <span data-ttu-id="21055-125">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="21055-125">-FqdnTag</span></span>
<span data-ttu-id="21055-126">Fqdn Tag della regola</span><span class="sxs-lookup"><span data-stu-id="21055-126">The FQDN Tags of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndFqdnTag, SourceIpGroupAndFqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21055-127">-Name</span><span class="sxs-lookup"><span data-stu-id="21055-127">-Name</span></span>
<span data-ttu-id="21055-128">Nome della regola dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="21055-128">The name of the Application Rule</span></span>

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

### <span data-ttu-id="21055-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="21055-129">-Protocol</span></span>
<span data-ttu-id="21055-130">Protocolli della regola</span><span class="sxs-lookup"><span data-stu-id="21055-130">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndWebCategory, SourceIpGroupAndTargetFqdn, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21055-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="21055-131">-SourceAddress</span></span>
<span data-ttu-id="21055-132">Indirizzi di origine della regola</span><span class="sxs-lookup"><span data-stu-id="21055-132">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndFqdnTag, SourceAddressAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21055-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="21055-133">-SourceIpGroup</span></span>
<span data-ttu-id="21055-134">Ipgroup di origine della regola</span><span class="sxs-lookup"><span data-stu-id="21055-134">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTargetFqdn, SourceIpGroupAndFqdnTag, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21055-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="21055-135">-TargetFqdn</span></span>
<span data-ttu-id="21055-136">FQDN di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="21055-136">The target FQDNs of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceIpGroupAndTargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21055-137">-WebCategory</span><span class="sxs-lookup"><span data-stu-id="21055-137">-WebCategory</span></span>
<span data-ttu-id="21055-138">Categorie Web della regola</span><span class="sxs-lookup"><span data-stu-id="21055-138">The Web Categories of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndWebCategory, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21055-139">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="21055-139">-TargetUrl</span></span>
<span data-ttu-id="21055-140">URL di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="21055-140">The Target Url of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetUrl, SourceIpGroupAndTargetUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21055-141">-TerminateTLS</span><span class="sxs-lookup"><span data-stu-id="21055-141">-TerminateTLS</span></span>
<span data-ttu-id="21055-142">Indica la chiusura di TLS</span><span class="sxs-lookup"><span data-stu-id="21055-142">Indicates terminating TLS</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21055-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21055-143">CommonParameters</span></span>
<span data-ttu-id="21055-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21055-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21055-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="21055-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21055-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="21055-146">INPUTS</span></span>

### <span data-ttu-id="21055-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="21055-147">None</span></span>

## <span data-ttu-id="21055-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21055-148">OUTPUTS</span></span>

### <span data-ttu-id="21055-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="21055-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="21055-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="21055-150">NOTES</span></span>

## <span data-ttu-id="21055-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21055-151">RELATED LINKS</span></span>
