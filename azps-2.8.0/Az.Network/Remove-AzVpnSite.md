---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 950e2d3e36695646bba16c098fc3abbd63cae113
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854178"
---
# <span data-ttu-id="870ab-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="870ab-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="870ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="870ab-102">SYNOPSIS</span></span>
<span data-ttu-id="870ab-103">Rimuove una risorsa di Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="870ab-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="870ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="870ab-104">SYNTAX</span></span>

### <span data-ttu-id="870ab-105">ByVpnSiteName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="870ab-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="870ab-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="870ab-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="870ab-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="870ab-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="870ab-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="870ab-108">DESCRIPTION</span></span>
<span data-ttu-id="870ab-109">Rimuove una risorsa di Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="870ab-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="870ab-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="870ab-110">EXAMPLES</span></span>

### <span data-ttu-id="870ab-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="870ab-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="870ab-112">Quanto sopra creerà un gruppo di risorse, Virtual WAN in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="870ab-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="870ab-113">Crea quindi un VpnSite per rappresentare un ramo Customer e lo collega alla rete WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="870ab-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="870ab-114">Dopo aver creato il sito, viene immediatamente rimosso tramite il comando Remove-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="870ab-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="870ab-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="870ab-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="870ab-116">Come l'esempio 1, ma qui la rimozione avviene usando l'output tramite pipe di Get-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="870ab-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="870ab-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="870ab-117">PARAMETERS</span></span>

### <span data-ttu-id="870ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="870ab-118">-DefaultProfile</span></span>
<span data-ttu-id="870ab-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="870ab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="870ab-120">-Force</span><span class="sxs-lookup"><span data-stu-id="870ab-120">-Force</span></span>
<span data-ttu-id="870ab-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="870ab-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870ab-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="870ab-122">-InputObject</span></span>
<span data-ttu-id="870ab-123">Oggetto vpnSite da eliminare.</span><span class="sxs-lookup"><span data-stu-id="870ab-123">The vpnSite object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObject
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="870ab-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="870ab-124">-Name</span></span>
<span data-ttu-id="870ab-125">Il nome vpnSite.</span><span class="sxs-lookup"><span data-stu-id="870ab-125">The vpnSite name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870ab-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="870ab-126">-PassThru</span></span>
<span data-ttu-id="870ab-127">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="870ab-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="870ab-128">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="870ab-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870ab-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="870ab-129">-ResourceGroupName</span></span>
<span data-ttu-id="870ab-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="870ab-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870ab-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="870ab-131">-ResourceId</span></span>
<span data-ttu-id="870ab-132">ID risorsa di Azure per l'vpnSite da eliminare.</span><span class="sxs-lookup"><span data-stu-id="870ab-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceId
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="870ab-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="870ab-133">-Confirm</span></span>
<span data-ttu-id="870ab-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="870ab-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="870ab-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="870ab-135">-WhatIf</span></span>
<span data-ttu-id="870ab-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="870ab-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="870ab-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="870ab-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="870ab-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="870ab-138">CommonParameters</span></span>
<span data-ttu-id="870ab-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="870ab-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="870ab-140">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="870ab-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="870ab-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="870ab-141">INPUTS</span></span>

### <span data-ttu-id="870ab-142">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="870ab-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="870ab-143">System. String</span><span class="sxs-lookup"><span data-stu-id="870ab-143">System.String</span></span>

## <span data-ttu-id="870ab-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="870ab-144">OUTPUTS</span></span>

### <span data-ttu-id="870ab-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="870ab-145">System.Boolean</span></span>

## <span data-ttu-id="870ab-146">Note</span><span class="sxs-lookup"><span data-stu-id="870ab-146">NOTES</span></span>

## <span data-ttu-id="870ab-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="870ab-147">RELATED LINKS</span></span>

[<span data-ttu-id="870ab-148">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="870ab-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="870ab-149">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="870ab-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="870ab-150">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="870ab-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
