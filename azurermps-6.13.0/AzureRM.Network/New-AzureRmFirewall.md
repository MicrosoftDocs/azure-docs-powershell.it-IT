---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
ms.openlocfilehash: 6486c7db87e8c71b0703b90a765fa30287b82769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521340"
---
# <span data-ttu-id="11f1f-101">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="11f1f-101">New-AzureRmFirewall</span></span>

## <span data-ttu-id="11f1f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="11f1f-103">Crea un nuovo firewall in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="11f1f-103">Creates a new Firewall in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11f1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11f1f-104">SYNTAX</span></span>

```
New-AzureRmFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-VirtualNetworkName <String>] [-PublicIpName <String>]
 [-ApplicationRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]>]
 [-NatRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]>]
 [-NetworkRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11f1f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11f1f-105">DESCRIPTION</span></span>
<span data-ttu-id="11f1f-106">Il cmdlet **New-AzureRmFirewall** crea un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="11f1f-106">The **New-AzureRmFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="11f1f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11f1f-107">EXAMPLES</span></span>

### <span data-ttu-id="11f1f-108">1: creare un firewall collegato a una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="11f1f-108">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="11f1f-109">Questo esempio crea un firewall collegato alla rete virtuale "VNET" nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="11f1f-109">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="11f1f-110">Dato che non sono state specificate regole, il firewall bloccherà tutto il traffico (comportamento predefinito).</span><span class="sxs-lookup"><span data-stu-id="11f1f-110">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>

### <span data-ttu-id="11f1f-111">2: creare un firewall che consente tutto il traffico HTTPS</span><span class="sxs-lookup"><span data-stu-id="11f1f-111">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="11f1f-112">Questo esempio crea un firewall che consente tutto il traffico HTTPS sulla porta 443.</span><span class="sxs-lookup"><span data-stu-id="11f1f-112">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>

### <span data-ttu-id="11f1f-113">3: DNAT-reindirizza il traffico destinato a 10.1.2.3:80 a 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="11f1f-113">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection
```

<span data-ttu-id="11f1f-114">Questo esempio ha creato un firewall che ha tradotto l'indirizzo IP di destinazione e la porta di tutti i pacchetti destinati a 10.1.2.3: da 80 a 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="11f1f-114">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>

## <span data-ttu-id="11f1f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11f1f-115">PARAMETERS</span></span>

### <span data-ttu-id="11f1f-116">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="11f1f-116">-ApplicationRuleCollection</span></span>
<span data-ttu-id="11f1f-117">Specifica le raccolte di regole dell'applicazione per il nuovo firewall.</span><span class="sxs-lookup"><span data-stu-id="11f1f-117">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f1f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11f1f-118">-AsJob</span></span>
<span data-ttu-id="11f1f-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="11f1f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11f1f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11f1f-120">-DefaultProfile</span></span>
<span data-ttu-id="11f1f-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11f1f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11f1f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="11f1f-122">-Force</span></span>
<span data-ttu-id="11f1f-123">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="11f1f-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="11f1f-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="11f1f-124">-Location</span></span>
<span data-ttu-id="11f1f-125">Specifica l'area geografica per il firewall.</span><span class="sxs-lookup"><span data-stu-id="11f1f-125">Specifies the region for the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f1f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="11f1f-126">-Name</span></span>
<span data-ttu-id="11f1f-127">Specifica il nome del firewall di Azure creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11f1f-127">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f1f-128">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="11f1f-128">-NatRuleCollection</span></span>
<span data-ttu-id="11f1f-129">Elenco di AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="11f1f-129">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f1f-130">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="11f1f-130">-NetworkRuleCollection</span></span>
<span data-ttu-id="11f1f-131">Elenco di AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="11f1f-131">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f1f-132">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="11f1f-132">-PublicIpName</span></span>
<span data-ttu-id="11f1f-133">Nome IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="11f1f-133">Public Ip Name.</span></span> <span data-ttu-id="11f1f-134">L'IP pubblico deve usare SKU standard e deve appartenere allo stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="11f1f-134">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f1f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11f1f-135">-ResourceGroupName</span></span>
<span data-ttu-id="11f1f-136">Specifica il nome di un gruppo di risorse che contiene il firewall.</span><span class="sxs-lookup"><span data-stu-id="11f1f-136">Specifies the name of a resource group to contain the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f1f-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="11f1f-137">-Tag</span></span>
<span data-ttu-id="11f1f-138">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="11f1f-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="11f1f-139">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="11f1f-139">For example:</span></span>

<span data-ttu-id="11f1f-140">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="11f1f-140">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f1f-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="11f1f-141">-VirtualNetworkName</span></span>
<span data-ttu-id="11f1f-142">Specifica il nome della rete virtuale per cui verrà distribuito il firewall.</span><span class="sxs-lookup"><span data-stu-id="11f1f-142">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="11f1f-143">La rete virtuale e il firewall devono appartenere allo stesso gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="11f1f-143">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f1f-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="11f1f-144">-Confirm</span></span>
<span data-ttu-id="11f1f-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11f1f-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f1f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11f1f-146">-WhatIf</span></span>
<span data-ttu-id="11f1f-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11f1f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11f1f-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11f1f-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f1f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f1f-149">CommonParameters</span></span>
<span data-ttu-id="11f1f-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11f1f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f1f-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11f1f-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f1f-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11f1f-152">INPUTS</span></span>

### <span data-ttu-id="11f1f-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="11f1f-153">None</span></span>
<span data-ttu-id="11f1f-154">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="11f1f-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="11f1f-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11f1f-155">OUTPUTS</span></span>

### <span data-ttu-id="11f1f-156">Microsoft. Azure. Commands. Network. Models. PSFirewall</span><span class="sxs-lookup"><span data-stu-id="11f1f-156">Microsoft.Azure.Commands.Network.Models.PSFirewall</span></span>

## <span data-ttu-id="11f1f-157">Note</span><span class="sxs-lookup"><span data-stu-id="11f1f-157">NOTES</span></span>

## <span data-ttu-id="11f1f-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11f1f-158">RELATED LINKS</span></span>

[<span data-ttu-id="11f1f-159">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="11f1f-159">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="11f1f-160">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="11f1f-160">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="11f1f-161">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="11f1f-161">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)

[<span data-ttu-id="11f1f-162">New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="11f1f-162">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="11f1f-163">New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="11f1f-163">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="11f1f-164">New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="11f1f-164">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)
