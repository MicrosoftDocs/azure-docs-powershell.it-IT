---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 7a369fafec712d23c7ac2aac30d3aa6928877355
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184702"
---
# <span data-ttu-id="e43d2-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e43d2-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="e43d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e43d2-102">SYNOPSIS</span></span>
<span data-ttu-id="e43d2-103">Ottiene un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="e43d2-103">Gets a public IP address.</span></span>

## <span data-ttu-id="e43d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e43d2-104">SYNTAX</span></span>

### <span data-ttu-id="e43d2-105">NoExpandStandAloneIp (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e43d2-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e43d2-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="e43d2-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e43d2-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="e43d2-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e43d2-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="e43d2-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e43d2-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e43d2-109">DESCRIPTION</span></span>
<span data-ttu-id="e43d2-110">Il cmdlet **Get-AzPublicIPAddress** ottiene uno o più indirizzi IP pubblici in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e43d2-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="e43d2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e43d2-111">EXAMPLES</span></span>

### <span data-ttu-id="e43d2-112">Esempio 1: Ottenere una risorsa IP pubblica</span><span class="sxs-lookup"><span data-stu-id="e43d2-112">Example 1: Get a public IP resource</span></span>
```powershell
Get-AzPublicIpAddress -Name myPublicIp1 -ResourceGroupName myRg

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic", 
                             "Tier": "Regional"
                           }
IpTags                   : []
```

<span data-ttu-id="e43d2-113">Questo comando ottiene una risorsa indirizzo IP pubblico con nome myPublicIp nel gruppo di risorse myRg.</span><span class="sxs-lookup"><span data-stu-id="e43d2-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="e43d2-114">Esempio 2: Ottenere risorse IP pubbliche con i filtri</span><span class="sxs-lookup"><span data-stu-id="e43d2-114">Example 2: Get public IP resources using filtering</span></span>
```powershell
Get-AzPublicIpAddress -Name myPublicIp*

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
IpTags                   : []
```

<span data-ttu-id="e43d2-115">Questo comando recupera tutte le risorse di indirizzi IP pubblici il cui nome inizia con myPublicIp.</span><span class="sxs-lookup"><span data-stu-id="e43d2-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="e43d2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e43d2-116">PARAMETERS</span></span>

### <span data-ttu-id="e43d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e43d2-117">-DefaultProfile</span></span>
<span data-ttu-id="e43d2-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e43d2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e43d2-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="e43d2-119">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43d2-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e43d2-120">-IpConfigurationName</span></span>
<span data-ttu-id="e43d2-121">Nome configurazione IP interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="e43d2-121">Network Interface IP Configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43d2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e43d2-122">-Name</span></span>
<span data-ttu-id="e43d2-123">Specifica il nome dell'indirizzo IP pubblico che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e43d2-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e43d2-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="e43d2-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="e43d2-125">Nome interfaccia di rete della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e43d2-125">Virtual Machine Network Interface Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43d2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e43d2-126">-ResourceGroupName</span></span>
<span data-ttu-id="e43d2-127">Specifica il nome del gruppo di risorse che contiene l'indirizzo IP pubblico che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e43d2-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e43d2-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="e43d2-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="e43d2-129">Indice macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e43d2-129">Virtual Machine Index.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43d2-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e43d2-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="e43d2-131">Nome set di scalabilità macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e43d2-131">Virtual Machine Scale Set Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e43d2-132">CommonParameters</span></span>
<span data-ttu-id="e43d2-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e43d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e43d2-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e43d2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e43d2-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="e43d2-135">INPUTS</span></span>

### <span data-ttu-id="e43d2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e43d2-136">System.String</span></span>

## <span data-ttu-id="e43d2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e43d2-137">OUTPUTS</span></span>

### <span data-ttu-id="e43d2-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e43d2-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="e43d2-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="e43d2-139">NOTES</span></span>

## <span data-ttu-id="e43d2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e43d2-140">RELATED LINKS</span></span>

[<span data-ttu-id="e43d2-141">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e43d2-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="e43d2-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e43d2-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="e43d2-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e43d2-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


