---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 7a369fafec712d23c7ac2aac30d3aa6928877355
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475484"
---
# <span data-ttu-id="65706-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="65706-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="65706-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65706-102">SYNOPSIS</span></span>
<span data-ttu-id="65706-103">Ottiene un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="65706-103">Gets a public IP address.</span></span>

## <span data-ttu-id="65706-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65706-104">SYNTAX</span></span>

### <span data-ttu-id="65706-105">NoExpandStandAloneIp (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="65706-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65706-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="65706-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65706-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="65706-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65706-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="65706-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65706-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65706-109">DESCRIPTION</span></span>
<span data-ttu-id="65706-110">Il cmdlet **Get-AzPublicIPAddress** ottiene uno o più indirizzi IP pubblici in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="65706-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="65706-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65706-111">EXAMPLES</span></span>

### <span data-ttu-id="65706-112">Esempio 1: ottenere una risorsa IP pubblica</span><span class="sxs-lookup"><span data-stu-id="65706-112">Example 1: Get a public IP resource</span></span>
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

<span data-ttu-id="65706-113">Questo comando consente di ottenere una risorsa indirizzo IP pubblico con il nome myPublicIp nel gruppo di risorse myRg.</span><span class="sxs-lookup"><span data-stu-id="65706-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="65706-114">Esempio 2: ottenere risorse IP pubbliche tramite filtri</span><span class="sxs-lookup"><span data-stu-id="65706-114">Example 2: Get public IP resources using filtering</span></span>
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

<span data-ttu-id="65706-115">Questo comando consente di ottenere tutte le risorse degli indirizzi IP pubblici il cui nome inizia con myPublicIp.</span><span class="sxs-lookup"><span data-stu-id="65706-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="65706-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65706-116">PARAMETERS</span></span>

### <span data-ttu-id="65706-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65706-117">-DefaultProfile</span></span>
<span data-ttu-id="65706-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65706-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65706-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="65706-119">-ExpandResource</span></span>
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

### <span data-ttu-id="65706-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="65706-120">-IpConfigurationName</span></span>
<span data-ttu-id="65706-121">Nome della configurazione dell'interfaccia di rete IP.</span><span class="sxs-lookup"><span data-stu-id="65706-121">Network Interface IP Configuration Name.</span></span>

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

### <span data-ttu-id="65706-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="65706-122">-Name</span></span>
<span data-ttu-id="65706-123">Specifica il nome dell'indirizzo IP pubblico ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65706-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="65706-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="65706-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="65706-125">Nome dell'interfaccia di rete della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="65706-125">Virtual Machine Network Interface Name.</span></span>

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

### <span data-ttu-id="65706-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65706-126">-ResourceGroupName</span></span>
<span data-ttu-id="65706-127">Specifica il nome del gruppo di risorse che contiene l'indirizzo IP pubblico ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65706-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="65706-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="65706-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="65706-129">Indice della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="65706-129">Virtual Machine Index.</span></span>

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

### <span data-ttu-id="65706-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="65706-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="65706-131">Nome set scala macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="65706-131">Virtual Machine Scale Set Name.</span></span>

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

### <span data-ttu-id="65706-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65706-132">CommonParameters</span></span>
<span data-ttu-id="65706-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65706-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65706-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65706-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65706-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65706-135">INPUTS</span></span>

### <span data-ttu-id="65706-136">System. String</span><span class="sxs-lookup"><span data-stu-id="65706-136">System.String</span></span>

## <span data-ttu-id="65706-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65706-137">OUTPUTS</span></span>

### <span data-ttu-id="65706-138">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="65706-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="65706-139">Note</span><span class="sxs-lookup"><span data-stu-id="65706-139">NOTES</span></span>

## <span data-ttu-id="65706-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65706-140">RELATED LINKS</span></span>

[<span data-ttu-id="65706-141">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="65706-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="65706-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="65706-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="65706-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="65706-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


