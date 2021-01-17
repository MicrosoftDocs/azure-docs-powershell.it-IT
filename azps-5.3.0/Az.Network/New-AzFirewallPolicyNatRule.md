---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: 05b89c164b8a6cd3f91880edac1536d22817ea57
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475916"
---
# <span data-ttu-id="7cd90-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="7cd90-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="7cd90-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7cd90-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd90-103">Creare una nuova regola NAT per i criteri di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="7cd90-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="7cd90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7cd90-104">SYNTAX</span></span>

### <span data-ttu-id="7cd90-105">SourceAddressAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="7cd90-105">SourceAddressAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cd90-106">SourceAddressAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="7cd90-106">SourceAddressAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cd90-107">SourceIpGroupAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="7cd90-107">SourceIpGroupAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cd90-108">SourceIpGroupAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="7cd90-108">SourceIpGroupAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cd90-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cd90-109">DESCRIPTION</span></span>
<span data-ttu-id="7cd90-110">Il cmdlet **New-AzFirewallPolicyNatRule** crea una regola NAT per un criterio di Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="7cd90-110">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="7cd90-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7cd90-111">EXAMPLES</span></span>

### <span data-ttu-id="7cd90-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7cd90-112">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="7cd90-113">Questo esempio crea una regola NAT con l'indirizzo di origine, il protocollo, l'indirizzo di destinazione, la porta di destinazione, l'indirizzo tradotto e la porta tradotta.</span><span class="sxs-lookup"><span data-stu-id="7cd90-113">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

### <span data-ttu-id="7cd90-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7cd90-114">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedFqdn "internalhttp.server.net" -TranslatedPort "100"
```

<span data-ttu-id="7cd90-115">Questo esempio crea una regola NAT con l'indirizzo di origine, il protocollo, l'indirizzo di destinazione, la porta di destinazione, l'FQDN tradotto e la porta tradotta.</span><span class="sxs-lookup"><span data-stu-id="7cd90-115">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated fqdn, and translated port.</span></span>

## <span data-ttu-id="7cd90-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7cd90-116">PARAMETERS</span></span>

### <span data-ttu-id="7cd90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd90-117">-DefaultProfile</span></span>
<span data-ttu-id="7cd90-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7cd90-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cd90-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cd90-119">-Description</span></span>
<span data-ttu-id="7cd90-120">Descrizione della regola</span><span class="sxs-lookup"><span data-stu-id="7cd90-120">The description of the rule</span></span>

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

### <span data-ttu-id="7cd90-121">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="7cd90-121">-DestinationAddress</span></span>
<span data-ttu-id="7cd90-122">Gli indirizzi di destinazione della regola.</span><span class="sxs-lookup"><span data-stu-id="7cd90-122">The destination addresses of the rule.</span></span> <span data-ttu-id="7cd90-123">Questo deve essere IP pubblico del firewall.</span><span class="sxs-lookup"><span data-stu-id="7cd90-123">This has to be Public IP of the Firewall.</span></span>

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

### <span data-ttu-id="7cd90-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="7cd90-124">-DestinationPort</span></span>
<span data-ttu-id="7cd90-125">Porte di destinazione della regola</span><span class="sxs-lookup"><span data-stu-id="7cd90-125">The destination ports of the rule</span></span>

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

### <span data-ttu-id="7cd90-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="7cd90-126">-Name</span></span>
<span data-ttu-id="7cd90-127">Nome della raccolta di regole NAT</span><span class="sxs-lookup"><span data-stu-id="7cd90-127">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="7cd90-128">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="7cd90-128">-Protocol</span></span>
<span data-ttu-id="7cd90-129">Protocolli della regola</span><span class="sxs-lookup"><span data-stu-id="7cd90-129">The protocols of the rule</span></span>

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

### <span data-ttu-id="7cd90-130">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="7cd90-130">-SourceAddress</span></span>
<span data-ttu-id="7cd90-131">Gli indirizzi di origine della regola</span><span class="sxs-lookup"><span data-stu-id="7cd90-131">The source addresses of the rule</span></span>

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

### <span data-ttu-id="7cd90-132">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="7cd90-132">-SourceIpGroup</span></span>
<span data-ttu-id="7cd90-133">Ipgroups di origine della regola</span><span class="sxs-lookup"><span data-stu-id="7cd90-133">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="7cd90-134">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="7cd90-134">-TranslatedAddress</span></span>
<span data-ttu-id="7cd90-135">Indirizzo tradotto per la regola NAT</span><span class="sxs-lookup"><span data-stu-id="7cd90-135">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="7cd90-136">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="7cd90-136">-TranslatedFqdn</span></span>
<span data-ttu-id="7cd90-137">Nome di dominio completo tradotto per la regola NAT</span><span class="sxs-lookup"><span data-stu-id="7cd90-137">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="7cd90-138">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="7cd90-138">-TranslatedPort</span></span>
<span data-ttu-id="7cd90-139">Porta tradotta per la regola NAT</span><span class="sxs-lookup"><span data-stu-id="7cd90-139">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="7cd90-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd90-140">CommonParameters</span></span>
<span data-ttu-id="7cd90-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cd90-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd90-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cd90-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd90-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7cd90-143">INPUTS</span></span>

### <span data-ttu-id="7cd90-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7cd90-144">None</span></span>

## <span data-ttu-id="7cd90-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7cd90-145">OUTPUTS</span></span>

### <span data-ttu-id="7cd90-146">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="7cd90-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="7cd90-147">Note</span><span class="sxs-lookup"><span data-stu-id="7cd90-147">NOTES</span></span>

## <span data-ttu-id="7cd90-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7cd90-148">RELATED LINKS</span></span>
