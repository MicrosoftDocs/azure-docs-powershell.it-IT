---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 4606ea7a9e403ad5963aacc9ee85b89068635325
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860470"
---
# <span data-ttu-id="d9c1f-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d9c1f-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="d9c1f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c1f-103">Crea un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-103">Creates a network security group.</span></span>

## <span data-ttu-id="d9c1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9c1f-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9c1f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9c1f-105">DESCRIPTION</span></span>
<span data-ttu-id="d9c1f-106">Il cmdlet **New-AzNetworkSecurityGroup** crea un gruppo di sicurezza di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="d9c1f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9c1f-107">EXAMPLES</span></span>

### <span data-ttu-id="d9c1f-108">1: creare un nuovo gruppo di Securtiy di rete</span><span class="sxs-lookup"><span data-stu-id="d9c1f-108">1: Create a new network securtiy group</span></span>
```
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="d9c1f-109">Questo comando Ceates un nuovo gruppo di sicurezza di rete di Azure denominato "nsg1" nel gruppo di risorse "RG1" in location "westus".</span><span class="sxs-lookup"><span data-stu-id="d9c1f-109">This command ceates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="d9c1f-110">2: creare un gruppo di sicurezza di rete dettagliato</span><span class="sxs-lookup"><span data-stu-id="d9c1f-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="d9c1f-111">Passaggio: 1 creare una regola di sicurezza che consente l'accesso da Internet alla porta 3389.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="d9c1f-112">Passaggio: 2 creare una regola di sicurezza che consente l'accesso da Internet alla porta 80.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="d9c1f-113">Passaggio: 3 aggiungere le regole create in precedenza a un nuovo NSG denominato NSG-FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="d9c1f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9c1f-114">PARAMETERS</span></span>

### <span data-ttu-id="d9c1f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9c1f-115">-AsJob</span></span>
<span data-ttu-id="d9c1f-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d9c1f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9c1f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c1f-117">-DefaultProfile</span></span>
<span data-ttu-id="d9c1f-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9c1f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d9c1f-119">-Force</span></span>
<span data-ttu-id="d9c1f-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9c1f-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d9c1f-121">-Location</span></span>
<span data-ttu-id="d9c1f-122">Specifica l'area geografica per la quale creare un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="d9c1f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9c1f-123">-Name</span></span>
<span data-ttu-id="d9c1f-124">Specifica il nome del gruppo di sicurezza di rete da creare.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="d9c1f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9c1f-125">-ResourceGroupName</span></span>
<span data-ttu-id="d9c1f-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d9c1f-127">Questo cmdlet crea un gruppo di sicurezza di rete nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9c1f-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="d9c1f-128">-SecurityRules</span></span>
<span data-ttu-id="d9c1f-129">Specifica un elenco di oggetti della regola di sicurezza della rete da creare in un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c1f-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="d9c1f-130">-Tag</span></span>
<span data-ttu-id="d9c1f-131">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d9c1f-132">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="d9c1f-132">For example:</span></span>

<span data-ttu-id="d9c1f-133">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d9c1f-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d9c1f-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d9c1f-134">-Confirm</span></span>
<span data-ttu-id="d9c1f-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9c1f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9c1f-136">-WhatIf</span></span>
<span data-ttu-id="d9c1f-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9c1f-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9c1f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c1f-139">CommonParameters</span></span>
<span data-ttu-id="d9c1f-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9c1f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c1f-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9c1f-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c1f-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9c1f-142">INPUTS</span></span>

## <span data-ttu-id="d9c1f-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9c1f-143">OUTPUTS</span></span>

### <span data-ttu-id="d9c1f-144">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d9c1f-144">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="d9c1f-145">Note</span><span class="sxs-lookup"><span data-stu-id="d9c1f-145">NOTES</span></span>

## <span data-ttu-id="d9c1f-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9c1f-146">RELATED LINKS</span></span>

[<span data-ttu-id="d9c1f-147">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d9c1f-147">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="d9c1f-148">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d9c1f-148">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="d9c1f-149">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d9c1f-149">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
