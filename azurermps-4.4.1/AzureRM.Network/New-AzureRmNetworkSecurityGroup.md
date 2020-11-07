---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: f2d9781f205df70e5becbc53f597f27791ca6495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686164"
---
# <span data-ttu-id="59eb8-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="59eb8-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="59eb8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="59eb8-103">Crea un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="59eb8-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59eb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59eb8-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59eb8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59eb8-105">DESCRIPTION</span></span>
<span data-ttu-id="59eb8-106">Il cmdlet **New-AzureRmNetworkSecurityGroup** crea un gruppo di sicurezza di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="59eb8-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="59eb8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59eb8-107">EXAMPLES</span></span>

### <span data-ttu-id="59eb8-108">1: creare un nuovo gruppo di sicurezza della rete</span><span class="sxs-lookup"><span data-stu-id="59eb8-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="59eb8-109">Questo comando crea un nuovo gruppo di sicurezza di rete di Azure denominato "nsg1" nel gruppo di risorse "RG1" in location "westus".</span><span class="sxs-lookup"><span data-stu-id="59eb8-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="59eb8-110">2: creare un gruppo di sicurezza di rete dettagliato</span><span class="sxs-lookup"><span data-stu-id="59eb8-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="59eb8-111">Passaggio: 1 creare una regola di sicurezza che consente l'accesso da Internet alla porta 3389.</span><span class="sxs-lookup"><span data-stu-id="59eb8-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="59eb8-112">Passaggio: 2 creare una regola di sicurezza che consente l'accesso da Internet alla porta 80.</span><span class="sxs-lookup"><span data-stu-id="59eb8-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="59eb8-113">Passaggio: 3 aggiungere le regole create in precedenza a un nuovo NSG denominato NSG-FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="59eb8-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="59eb8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59eb8-114">PARAMETERS</span></span>

### <span data-ttu-id="59eb8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="59eb8-115">-Force</span></span>
<span data-ttu-id="59eb8-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="59eb8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="59eb8-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="59eb8-117">-Location</span></span>
<span data-ttu-id="59eb8-118">Specifica l'area geografica per la quale creare un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="59eb8-118">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="59eb8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="59eb8-119">-Name</span></span>
<span data-ttu-id="59eb8-120">Specifica il nome del gruppo di sicurezza di rete da creare.</span><span class="sxs-lookup"><span data-stu-id="59eb8-120">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="59eb8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59eb8-121">-ResourceGroupName</span></span>
<span data-ttu-id="59eb8-122">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="59eb8-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="59eb8-123">Questo cmdlet crea un gruppo di sicurezza di rete nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="59eb8-123">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="59eb8-124">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="59eb8-124">-SecurityRules</span></span>
<span data-ttu-id="59eb8-125">Specifica un elenco di oggetti della regola di sicurezza della rete da creare in un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="59eb8-125">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="59eb8-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="59eb8-126">-Tag</span></span>
<span data-ttu-id="59eb8-127">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="59eb8-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="59eb8-128">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="59eb8-128">For example:</span></span>

<span data-ttu-id="59eb8-129">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="59eb8-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="59eb8-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="59eb8-130">-Confirm</span></span>
<span data-ttu-id="59eb8-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59eb8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59eb8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59eb8-132">-WhatIf</span></span>
<span data-ttu-id="59eb8-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59eb8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59eb8-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59eb8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59eb8-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59eb8-135">-DefaultProfile</span></span>
<span data-ttu-id="59eb8-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59eb8-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59eb8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59eb8-137">CommonParameters</span></span>
<span data-ttu-id="59eb8-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59eb8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59eb8-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59eb8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59eb8-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59eb8-140">INPUTS</span></span>

## <span data-ttu-id="59eb8-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59eb8-141">OUTPUTS</span></span>

### <span data-ttu-id="59eb8-142">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="59eb8-142">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="59eb8-143">Note</span><span class="sxs-lookup"><span data-stu-id="59eb8-143">NOTES</span></span>

## <span data-ttu-id="59eb8-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59eb8-144">RELATED LINKS</span></span>

[<span data-ttu-id="59eb8-145">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="59eb8-145">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="59eb8-146">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="59eb8-146">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="59eb8-147">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="59eb8-147">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
