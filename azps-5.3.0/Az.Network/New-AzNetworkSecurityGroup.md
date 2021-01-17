---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 593891c19b9748c7a32019cfdaee0d069329cbea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476514"
---
# <span data-ttu-id="dba93-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dba93-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="dba93-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dba93-102">SYNOPSIS</span></span>
<span data-ttu-id="dba93-103">Crea un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="dba93-103">Creates a network security group.</span></span>

## <span data-ttu-id="dba93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dba93-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dba93-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dba93-105">DESCRIPTION</span></span>
<span data-ttu-id="dba93-106">Il cmdlet **New-AzNetworkSecurityGroup** crea un gruppo di sicurezza di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="dba93-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="dba93-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dba93-107">EXAMPLES</span></span>

### <span data-ttu-id="dba93-108">Esempio 1: creare un nuovo gruppo di sicurezza della rete</span><span class="sxs-lookup"><span data-stu-id="dba93-108">Example 1: Create a new network security group</span></span>
```powershell
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="dba93-109">Questo comando crea un nuovo gruppo di sicurezza di rete di Azure denominato "nsg1" nel gruppo di risorse "RG1" in location "westus".</span><span class="sxs-lookup"><span data-stu-id="dba93-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="dba93-110">Esempio 2: creare un gruppo di sicurezza di rete dettagliato</span><span class="sxs-lookup"><span data-stu-id="dba93-110">Example 2: Create a detailed network security group</span></span>
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

<span data-ttu-id="dba93-111">Passaggio: 1 creare una regola di sicurezza che consente l'accesso da Internet alla porta 3389.</span><span class="sxs-lookup"><span data-stu-id="dba93-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="dba93-112">Passaggio: 2 creare una regola di sicurezza che consente l'accesso da Internet alla porta 80.</span><span class="sxs-lookup"><span data-stu-id="dba93-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="dba93-113">Passaggio: 3 aggiungere le regole create in precedenza a un nuovo NSG denominato NSG-FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="dba93-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="dba93-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dba93-114">PARAMETERS</span></span>

### <span data-ttu-id="dba93-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dba93-115">-AsJob</span></span>
<span data-ttu-id="dba93-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="dba93-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dba93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba93-117">-DefaultProfile</span></span>
<span data-ttu-id="dba93-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dba93-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dba93-119">-Force</span><span class="sxs-lookup"><span data-stu-id="dba93-119">-Force</span></span>
<span data-ttu-id="dba93-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="dba93-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dba93-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="dba93-121">-Location</span></span>
<span data-ttu-id="dba93-122">Specifica l'area geografica per la quale creare un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="dba93-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="dba93-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="dba93-123">-Name</span></span>
<span data-ttu-id="dba93-124">Specifica il nome del gruppo di sicurezza di rete da creare.</span><span class="sxs-lookup"><span data-stu-id="dba93-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="dba93-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dba93-125">-ResourceGroupName</span></span>
<span data-ttu-id="dba93-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dba93-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="dba93-127">Questo cmdlet crea un gruppo di sicurezza di rete nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="dba93-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="dba93-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="dba93-128">-SecurityRules</span></span>
<span data-ttu-id="dba93-129">Specifica un elenco di oggetti della regola di sicurezza della rete da creare in un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="dba93-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="dba93-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="dba93-130">-Tag</span></span>
<span data-ttu-id="dba93-131">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="dba93-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dba93-132">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="dba93-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="dba93-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dba93-133">-Confirm</span></span>
<span data-ttu-id="dba93-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dba93-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dba93-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dba93-135">-WhatIf</span></span>
<span data-ttu-id="dba93-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dba93-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dba93-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dba93-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dba93-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba93-138">CommonParameters</span></span>
<span data-ttu-id="dba93-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dba93-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba93-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dba93-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba93-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dba93-141">INPUTS</span></span>

### <span data-ttu-id="dba93-142">System. String</span><span class="sxs-lookup"><span data-stu-id="dba93-142">System.String</span></span>

### <span data-ttu-id="dba93-143">Microsoft. Azure. Commands. Network. Models. PSSecurityRule []</span><span class="sxs-lookup"><span data-stu-id="dba93-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="dba93-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dba93-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dba93-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dba93-145">OUTPUTS</span></span>

### <span data-ttu-id="dba93-146">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dba93-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="dba93-147">Note</span><span class="sxs-lookup"><span data-stu-id="dba93-147">NOTES</span></span>

## <span data-ttu-id="dba93-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dba93-148">RELATED LINKS</span></span>

[<span data-ttu-id="dba93-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dba93-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="dba93-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dba93-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="dba93-151">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dba93-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
