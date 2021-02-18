---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
ms.openlocfilehash: c565c78e7f95e02d3449a04f0a53f4b84ef7a9f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206626"
---
# <span data-ttu-id="2f85d-101">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="2f85d-101">Remove-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="2f85d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f85d-102">SYNOPSIS</span></span>
<span data-ttu-id="2f85d-103">Rimuove un piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="2f85d-103">Removes a DDoS protection plan.</span></span>

## <span data-ttu-id="2f85d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f85d-104">SYNTAX</span></span>

```
Remove-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f85d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2f85d-105">DESCRIPTION</span></span>
<span data-ttu-id="2f85d-106">Il cmdlet Remove-AzDdosProtectionPlan rimuove un piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="2f85d-106">The Remove-AzDdosProtectionPlan cmdlet removes a DDoS protection plan.</span></span>

## <span data-ttu-id="2f85d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f85d-107">EXAMPLES</span></span>

### <span data-ttu-id="2f85d-108">Esempio 1: Rimuovere un piano di protezione DDoS vuoto</span><span class="sxs-lookup"><span data-stu-id="2f85d-108">Example 1: Remove an empty DDoS protection plan</span></span>
```
D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="2f85d-109">In questo caso, viene rimosso un piano di protezione DDoS come specificato.</span><span class="sxs-lookup"><span data-stu-id="2f85d-109">In this case, we remove a DDoS protection plan as specified.</span></span>

### <span data-ttu-id="2f85d-110">Esempio 2: Rimuovere un piano di protezione DDoS associato a una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="2f85d-110">Example 2: Remove a DDoS protection plan associated with a virtual network</span></span>
```
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = $null
D:\> $vnet.EnableDdosProtection = $false
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"65947351-747e-4686-aa8b-c40da58f6c8b"
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
                             "Etag": "W/\"65947351-747e-4686-aa8b-c40da58f6c8b\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
EnableVmProtection     : false


D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="2f85d-111">I piani di protezione DDoS non possono essere eliminati se sono associati a una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2f85d-111">DDoS protection plans cannot be deleted if they are associated with a virtual network.</span></span> <span data-ttu-id="2f85d-112">Quindi, il primo passaggio consiste nel disassociare entrambi gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="2f85d-112">So the first step is to disassociate both objects.</span></span> <span data-ttu-id="2f85d-113">Qui viene scaricata la versione più aggiornata della rete virtuale associata al piano e la proprietà **DdosProtectionPlan** viene impostata su un valore vuoto e il flag **EnableDdosProtection** (questo flag non può essere true senza un piano).</span><span class="sxs-lookup"><span data-stu-id="2f85d-113">Here, we get the most updated version of the virtual network associated with the plan, and we set the property **DdosProtectionPlan** to an empty value and the flag **EnableDdosProtection** (this flag cannot be true without a plan).</span></span>
<span data-ttu-id="2f85d-114">Quindi, persistono il nuovo stato impostando la variabile locale su **Set-AzVirtualNetwork.**</span><span class="sxs-lookup"><span data-stu-id="2f85d-114">Then, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span> <span data-ttu-id="2f85d-115">A questo punto, il piano non è più associato alla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2f85d-115">At this point, the plan is no longer associated with the virtual network.</span></span>
<span data-ttu-id="2f85d-116">Se questo è l'ultimo associato al piano, è possibile rimuovere il piano di protezione DDoS usando il comando Remove-AzDdosProtectionPlan.</span><span class="sxs-lookup"><span data-stu-id="2f85d-116">If this is the last one associated with the plan, we can remove the DDoS protection plan by using the command Remove-AzDdosProtectionPlan.</span></span>

## <span data-ttu-id="2f85d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f85d-117">PARAMETERS</span></span>

### <span data-ttu-id="2f85d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f85d-118">-DefaultProfile</span></span>
<span data-ttu-id="2f85d-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f85d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f85d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2f85d-120">-Name</span></span>
<span data-ttu-id="2f85d-121">Specifica il nome del piano di protezione DDoS da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2f85d-121">Specifies the name of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="2f85d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f85d-122">-PassThru</span></span>
<span data-ttu-id="2f85d-123">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="2f85d-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2f85d-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="2f85d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2f85d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f85d-125">-ResourceGroupName</span></span>
<span data-ttu-id="2f85d-126">Specifica il gruppo di risorse del piano di protezione DDoS da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2f85d-126">Specifies the resource group of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="2f85d-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f85d-127">-Confirm</span></span>
<span data-ttu-id="2f85d-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f85d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f85d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f85d-129">-WhatIf</span></span>
<span data-ttu-id="2f85d-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f85d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f85d-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f85d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f85d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f85d-132">CommonParameters</span></span>
<span data-ttu-id="2f85d-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f85d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f85d-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f85d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f85d-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="2f85d-135">INPUTS</span></span>

### <span data-ttu-id="2f85d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2f85d-136">System.String</span></span>

## <span data-ttu-id="2f85d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f85d-137">OUTPUTS</span></span>

### <span data-ttu-id="2f85d-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f85d-138">System.Boolean</span></span>

## <span data-ttu-id="2f85d-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="2f85d-139">NOTES</span></span>

## <span data-ttu-id="2f85d-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f85d-140">RELATED LINKS</span></span>

[<span data-ttu-id="2f85d-141">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="2f85d-141">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="2f85d-142">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="2f85d-142">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="2f85d-143">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2f85d-143">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="2f85d-144">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2f85d-144">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="2f85d-145">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2f85d-145">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)