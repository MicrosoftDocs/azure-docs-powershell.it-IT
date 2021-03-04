---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 001023fd313db4228d7fb1f155b5a686f9649277
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953933"
---
# <span data-ttu-id="dde93-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dde93-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="dde93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dde93-102">SYNOPSIS</span></span>
<span data-ttu-id="dde93-103">Crea un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="dde93-103">Creates a network security group.</span></span>

## <span data-ttu-id="dde93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dde93-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dde93-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dde93-105">DESCRIPTION</span></span>
<span data-ttu-id="dde93-106">Il cmdlet **New-AzNetworkSecurityGroup** crea un gruppo di sicurezza di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="dde93-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="dde93-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dde93-107">EXAMPLES</span></span>

### <span data-ttu-id="dde93-108">Esempio 1: Creare un nuovo gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="dde93-108">Example 1: Create a new network security group</span></span>
```powershell
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="dde93-109">Questo comando crea un nuovo gruppo di sicurezza di rete Azure denominato "nsg1" nel gruppo di risorse "rg1" nel percorso "westus".</span><span class="sxs-lookup"><span data-stu-id="dde93-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="dde93-110">Esempio 2: Creare un gruppo di sicurezza di rete dettagliato</span><span class="sxs-lookup"><span data-stu-id="dde93-110">Example 2: Create a detailed network security group</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name `
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="dde93-111">Passaggio:1 Creare una regola di sicurezza che consenta l'accesso da Internet alla porta 3389.</span><span class="sxs-lookup"><span data-stu-id="dde93-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="dde93-112">Passaggio:2 Creare una regola di sicurezza che consenta l'accesso da Internet alla porta 80.</span><span class="sxs-lookup"><span data-stu-id="dde93-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="dde93-113">Passaggio 3 Aggiungere le regole create in precedenza a un nuovo NSG denominato NSG-FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="dde93-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="dde93-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dde93-114">PARAMETERS</span></span>

### <span data-ttu-id="dde93-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dde93-115">-AsJob</span></span>
<span data-ttu-id="dde93-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="dde93-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde93-117">-DefaultProfile</span></span>
<span data-ttu-id="dde93-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dde93-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dde93-119">-Force</span><span class="sxs-lookup"><span data-stu-id="dde93-119">-Force</span></span>
<span data-ttu-id="dde93-120">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="dde93-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde93-121">-Location</span><span class="sxs-lookup"><span data-stu-id="dde93-121">-Location</span></span>
<span data-ttu-id="dde93-122">Specifica l'area geografica per cui creare un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="dde93-122">Specifies the region for which to create a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde93-123">-Name</span><span class="sxs-lookup"><span data-stu-id="dde93-123">-Name</span></span>
<span data-ttu-id="dde93-124">Specifica il nome del gruppo di sicurezza di rete da creare.</span><span class="sxs-lookup"><span data-stu-id="dde93-124">Specifies the name of the network security group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde93-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dde93-125">-ResourceGroupName</span></span>
<span data-ttu-id="dde93-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dde93-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="dde93-127">Questo cmdlet crea un gruppo di sicurezza di rete nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="dde93-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde93-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="dde93-128">-SecurityRules</span></span>
<span data-ttu-id="dde93-129">Specifica un elenco di oggetti delle regole di sicurezza di rete da creare in un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="dde93-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde93-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="dde93-130">-Tag</span></span>
<span data-ttu-id="dde93-131">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="dde93-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dde93-132">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="dde93-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde93-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dde93-133">-Confirm</span></span>
<span data-ttu-id="dde93-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dde93-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dde93-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dde93-135">-WhatIf</span></span>
<span data-ttu-id="dde93-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dde93-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dde93-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dde93-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dde93-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde93-138">CommonParameters</span></span>
<span data-ttu-id="dde93-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dde93-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde93-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dde93-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde93-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="dde93-141">INPUTS</span></span>

### <span data-ttu-id="dde93-142">System.String</span><span class="sxs-lookup"><span data-stu-id="dde93-142">System.String</span></span>

### <span data-ttu-id="dde93-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span><span class="sxs-lookup"><span data-stu-id="dde93-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="dde93-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="dde93-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dde93-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dde93-145">OUTPUTS</span></span>

### <span data-ttu-id="dde93-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dde93-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="dde93-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="dde93-147">NOTES</span></span>

## <span data-ttu-id="dde93-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dde93-148">RELATED LINKS</span></span>

[<span data-ttu-id="dde93-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dde93-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="dde93-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dde93-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="dde93-151">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dde93-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
