---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
ms.openlocfilehash: 39d45085c7f53bfeec6e18f38602fca48a3cefa3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022714"
---
# <span data-ttu-id="fc68f-101">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="fc68f-101">New-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="fc68f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc68f-102">SYNOPSIS</span></span>
<span data-ttu-id="fc68f-103">Crea un piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="fc68f-103">Creates a DDoS protection plan.</span></span>

## <span data-ttu-id="fc68f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc68f-104">SYNTAX</span></span>

```
New-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc68f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc68f-105">DESCRIPTION</span></span>
<span data-ttu-id="fc68f-106">Il cmdlet New-AzDdosProtectionPlan crea un piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="fc68f-106">The New-AzDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="fc68f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc68f-107">EXAMPLES</span></span>

### <span data-ttu-id="fc68f-108">Esempio 1: creare e associare un piano di protezione DDoS con una nuova rete virtuale</span><span class="sxs-lookup"><span data-stu-id="fc68f-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="fc68f-109">Prima di tutto creiamo un nuovo piano di protezione DDoS con il comando **New-AzDdosProtectionPlan** .</span><span class="sxs-lookup"><span data-stu-id="fc68f-109">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="fc68f-110">Creiamo quindi una nuova rete virtuale con **New-AzVirtualNetwork** e specifichiamo l'ID del piano appena creato nel parametro **DdosProtectionPlanId**.</span><span class="sxs-lookup"><span data-stu-id="fc68f-110">Then, we create a new virtual network with **New-AzVirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="fc68f-111">In questo caso, dato che stiamo associando la rete virtuale a un piano, possiamo anche specificare il parametro **EnableDdoSProtection**.</span><span class="sxs-lookup"><span data-stu-id="fc68f-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="fc68f-112">Esempio 2: creare e associare un piano di protezione DDoS con una rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="fc68f-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = New-Object Microsoft.Azure.Commands.Network.Models.PSResourceId
D:\> $vnet.DdosProtectionPlan.Id = $ddosProtectionPlan.Id
D:\> $vnet.EnableDdosProtection = $true
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb"
ResourceGuid           : fcb7bc1e-ee0d-4005-b3f1-feda76e3756c
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "10.0.0.0/16"
                           ]
                         }
DhcpOptions            : {
                           "DnsServers": [
                             "8.8.8.8"
                           ]
                         }
Subnets                : [
                           {
                             "Name": "SubnetName",
                             "Etag": "W/\"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : true
DdosProtectionPlan     : {
                           "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName"
                         }
EnableVmProtection     : false
```

<span data-ttu-id="fc68f-113">Prima di tutto creiamo un nuovo piano di protezione DDoS con il comando **New-AzDdosProtectionPlan** .</span><span class="sxs-lookup"><span data-stu-id="fc68f-113">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="fc68f-114">In secondo luogo, otteniamo la versione più aggiornata della rete virtuale che vogliamo associare al piano.</span><span class="sxs-lookup"><span data-stu-id="fc68f-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="fc68f-115">Aggiorniamo la proprietà **DdosProtectionPlan** con un oggetto **PSResourceId** contenente un riferimento all'ID del piano appena creato.</span><span class="sxs-lookup"><span data-stu-id="fc68f-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="fc68f-116">In questo caso, se associamo la rete virtuale a un piano di protezione DDoS, possiamo anche impostare il flag **EnableDdosProtection** su true.</span><span class="sxs-lookup"><span data-stu-id="fc68f-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="fc68f-117">Infine, persistiamo il nuovo stato eseguendo il piping della variabile locale in **set-AzVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="fc68f-117">Finally, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span>

## <span data-ttu-id="fc68f-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc68f-118">PARAMETERS</span></span>

### <span data-ttu-id="fc68f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc68f-119">-AsJob</span></span>
<span data-ttu-id="fc68f-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fc68f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc68f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc68f-121">-DefaultProfile</span></span>
<span data-ttu-id="fc68f-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc68f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc68f-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fc68f-123">-Location</span></span>
<span data-ttu-id="fc68f-124">Specifica la posizione del piano di protezione DDoS da creare.</span><span class="sxs-lookup"><span data-stu-id="fc68f-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="fc68f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc68f-125">-Name</span></span>
<span data-ttu-id="fc68f-126">Specifica il nome del piano di protezione DDoS da creare.</span><span class="sxs-lookup"><span data-stu-id="fc68f-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="fc68f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc68f-127">-ResourceGroupName</span></span>
<span data-ttu-id="fc68f-128">Specifica il gruppo di risorse del piano di protezione DDoS da creare.</span><span class="sxs-lookup"><span data-stu-id="fc68f-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="fc68f-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc68f-129">-Tag</span></span>
<span data-ttu-id="fc68f-130">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="fc68f-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fc68f-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fc68f-131">-Confirm</span></span>
<span data-ttu-id="fc68f-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc68f-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc68f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc68f-133">-WhatIf</span></span>
<span data-ttu-id="fc68f-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc68f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc68f-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc68f-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc68f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc68f-136">CommonParameters</span></span>
<span data-ttu-id="fc68f-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc68f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc68f-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc68f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc68f-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc68f-139">INPUTS</span></span>

### <span data-ttu-id="fc68f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fc68f-140">System.String</span></span>

### <span data-ttu-id="fc68f-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fc68f-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fc68f-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc68f-142">OUTPUTS</span></span>

### <span data-ttu-id="fc68f-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="fc68f-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="fc68f-144">Note</span><span class="sxs-lookup"><span data-stu-id="fc68f-144">NOTES</span></span>

## <span data-ttu-id="fc68f-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc68f-145">RELATED LINKS</span></span>

[<span data-ttu-id="fc68f-146">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="fc68f-146">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="fc68f-147">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="fc68f-147">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="fc68f-148">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fc68f-148">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="fc68f-149">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fc68f-149">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="fc68f-150">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fc68f-150">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)