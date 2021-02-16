---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: 05b89c164b8a6cd3f91880edac1536d22817ea57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191862"
---
# <span data-ttu-id="18dbc-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="18dbc-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="18dbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="18dbc-103">Creare una nuova regola NAT per i criteri del firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="18dbc-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="18dbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18dbc-104">SYNTAX</span></span>

### <span data-ttu-id="18dbc-105">SourceAddressAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="18dbc-105">SourceAddressAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18dbc-106">SourceAddressAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="18dbc-106">SourceAddressAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18dbc-107">SourceIpGroupAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="18dbc-107">SourceIpGroupAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18dbc-108">SourceIpGroupAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="18dbc-108">SourceIpGroupAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18dbc-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="18dbc-109">DESCRIPTION</span></span>
<span data-ttu-id="18dbc-110">Il cmdlet **New-AzFirewallPolicyNatRule** crea una regola NAT per un criterio firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="18dbc-110">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="18dbc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18dbc-111">EXAMPLES</span></span>

### <span data-ttu-id="18dbc-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="18dbc-112">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="18dbc-113">Questo esempio crea una regola NAT con l'indirizzo di origine, il protocollo, l'indirizzo di destinazione, la porta di destinazione, l'indirizzo tradotto e la porta tradotta.</span><span class="sxs-lookup"><span data-stu-id="18dbc-113">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

### <span data-ttu-id="18dbc-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="18dbc-114">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedFqdn "internalhttp.server.net" -TranslatedPort "100"
```

<span data-ttu-id="18dbc-115">Questo esempio crea una regola NAT con l'indirizzo di origine, il protocollo, l'indirizzo di destinazione, la porta di destinazione, l'FQDN tradotto e la porta tradotta.</span><span class="sxs-lookup"><span data-stu-id="18dbc-115">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated fqdn, and translated port.</span></span>

## <span data-ttu-id="18dbc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18dbc-116">PARAMETERS</span></span>

### <span data-ttu-id="18dbc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18dbc-117">-DefaultProfile</span></span>
<span data-ttu-id="18dbc-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18dbc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18dbc-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="18dbc-119">-Description</span></span>
<span data-ttu-id="18dbc-120">Descrizione della regola</span><span class="sxs-lookup"><span data-stu-id="18dbc-120">The description of the rule</span></span>

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

### <span data-ttu-id="18dbc-121">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="18dbc-121">-DestinationAddress</span></span>
<span data-ttu-id="18dbc-122">Indirizzi di destinazione della regola.</span><span class="sxs-lookup"><span data-stu-id="18dbc-122">The destination addresses of the rule.</span></span> <span data-ttu-id="18dbc-123">Questo deve essere l'indirizzo IP pubblico del firewall.</span><span class="sxs-lookup"><span data-stu-id="18dbc-123">This has to be Public IP of the Firewall.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18dbc-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="18dbc-124">-DestinationPort</span></span>
<span data-ttu-id="18dbc-125">Porte di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="18dbc-125">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18dbc-126">-Name</span><span class="sxs-lookup"><span data-stu-id="18dbc-126">-Name</span></span>
<span data-ttu-id="18dbc-127">Nome della raccolta di regole NAT</span><span class="sxs-lookup"><span data-stu-id="18dbc-127">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="18dbc-128">-Protocol</span><span class="sxs-lookup"><span data-stu-id="18dbc-128">-Protocol</span></span>
<span data-ttu-id="18dbc-129">Protocolli della regola</span><span class="sxs-lookup"><span data-stu-id="18dbc-129">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18dbc-130">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="18dbc-130">-SourceAddress</span></span>
<span data-ttu-id="18dbc-131">Indirizzi di origine della regola</span><span class="sxs-lookup"><span data-stu-id="18dbc-131">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTranslatedAddress, SourceAddressAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18dbc-132">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="18dbc-132">-SourceIpGroup</span></span>
<span data-ttu-id="18dbc-133">Gli ipgroup di origine della regola</span><span class="sxs-lookup"><span data-stu-id="18dbc-133">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTranslatedAddress, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18dbc-134">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="18dbc-134">-TranslatedAddress</span></span>
<span data-ttu-id="18dbc-135">Indirizzo tradotto per questa regola NAT</span><span class="sxs-lookup"><span data-stu-id="18dbc-135">The translated address for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedAddress, SourceIpGroupAndTranslatedAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18dbc-136">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="18dbc-136">-TranslatedFqdn</span></span>
<span data-ttu-id="18dbc-137">FQDN tradotti per questa regola NAT</span><span class="sxs-lookup"><span data-stu-id="18dbc-137">The translated FQDN for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedFqdn, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18dbc-138">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="18dbc-138">-TranslatedPort</span></span>
<span data-ttu-id="18dbc-139">La porta tradotta per questa regola NAT</span><span class="sxs-lookup"><span data-stu-id="18dbc-139">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="18dbc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18dbc-140">CommonParameters</span></span>
<span data-ttu-id="18dbc-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18dbc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18dbc-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="18dbc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18dbc-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="18dbc-143">INPUTS</span></span>

### <span data-ttu-id="18dbc-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="18dbc-144">None</span></span>

## <span data-ttu-id="18dbc-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18dbc-145">OUTPUTS</span></span>

### <span data-ttu-id="18dbc-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="18dbc-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="18dbc-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="18dbc-147">NOTES</span></span>

## <span data-ttu-id="18dbc-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18dbc-148">RELATED LINKS</span></span>
