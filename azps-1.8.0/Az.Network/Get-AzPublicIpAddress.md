---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 38eff375baa948098ac66c8e2b3c3fe1849f3bc0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678463"
---
# <span data-ttu-id="b5b59-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b5b59-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="b5b59-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5b59-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b59-103">Ottiene un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="b5b59-103">Gets a public IP address.</span></span>

## <span data-ttu-id="b5b59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5b59-104">SYNTAX</span></span>

### <span data-ttu-id="b5b59-105">NoExpandStandAloneIp (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5b59-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5b59-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="b5b59-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5b59-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="b5b59-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5b59-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="b5b59-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5b59-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5b59-109">DESCRIPTION</span></span>
<span data-ttu-id="b5b59-110">Il cmdlet **Get-AzPublicIPAddress** ottiene uno o più indirizzi IP pubblici in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5b59-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="b5b59-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5b59-111">EXAMPLES</span></span>

### <span data-ttu-id="b5b59-112">1: ottenere una risorsa IP pubblica</span><span class="sxs-lookup"><span data-stu-id="b5b59-112">1: Get a public IP resource</span></span>
```
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
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="b5b59-113">Questo comando consente di ottenere una risorsa indirizzo IP pubblico con il nome myPublicIp nel gruppo di risorse myRg.</span><span class="sxs-lookup"><span data-stu-id="b5b59-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="b5b59-114">2: ottenere risorse IP pubbliche tramite filtri</span><span class="sxs-lookup"><span data-stu-id="b5b59-114">2: Get public IP resources using filtering</span></span>
```
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
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="b5b59-115">Questo comando consente di ottenere tutte le risorse degli indirizzi IP pubblici il cui nome inizia con myPublicIp.</span><span class="sxs-lookup"><span data-stu-id="b5b59-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="b5b59-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5b59-116">PARAMETERS</span></span>

### <span data-ttu-id="b5b59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b59-117">-DefaultProfile</span></span>
<span data-ttu-id="b5b59-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b59-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5b59-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="b5b59-119">-ExpandResource</span></span>
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

### <span data-ttu-id="b5b59-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b5b59-120">-IpConfigurationName</span></span>
<span data-ttu-id="b5b59-121">Nome della configurazione dell'interfaccia di rete IP.</span><span class="sxs-lookup"><span data-stu-id="b5b59-121">Network Interface IP Configuration Name.</span></span>

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

### <span data-ttu-id="b5b59-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5b59-122">-Name</span></span>
<span data-ttu-id="b5b59-123">Specifica il nome dell'indirizzo IP pubblico ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b59-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b5b59-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="b5b59-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="b5b59-125">Nome dell'interfaccia di rete della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b5b59-125">Virtual Machine Network Interface Name.</span></span>

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

### <span data-ttu-id="b5b59-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5b59-126">-ResourceGroupName</span></span>
<span data-ttu-id="b5b59-127">Specifica il nome del gruppo di risorse che contiene l'indirizzo IP pubblico ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b59-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b5b59-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="b5b59-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="b5b59-129">Indice della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b5b59-129">Virtual Machine Index.</span></span>

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

### <span data-ttu-id="b5b59-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b5b59-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="b5b59-131">Nome set scala macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b5b59-131">Virtual Machine Scale Set Name.</span></span>

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

### <span data-ttu-id="b5b59-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b59-132">CommonParameters</span></span>
<span data-ttu-id="b5b59-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b59-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b59-134">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5b59-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b59-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5b59-135">INPUTS</span></span>

### <span data-ttu-id="b5b59-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b5b59-136">System.String</span></span>

## <span data-ttu-id="b5b59-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5b59-137">OUTPUTS</span></span>

### <span data-ttu-id="b5b59-138">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b5b59-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="b5b59-139">Note</span><span class="sxs-lookup"><span data-stu-id="b5b59-139">NOTES</span></span>

## <span data-ttu-id="b5b59-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5b59-140">RELATED LINKS</span></span>

[<span data-ttu-id="b5b59-141">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b5b59-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="b5b59-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b5b59-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="b5b59-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b5b59-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


