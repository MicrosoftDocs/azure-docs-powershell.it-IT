---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: eb6611bef2499c9aaf164ddbe2e7a31c63051751
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951470"
---
# <span data-ttu-id="05cf5-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="05cf5-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="05cf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="05cf5-103">Aggiorna una WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="05cf5-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="05cf5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05cf5-104">SYNTAX</span></span>

### <span data-ttu-id="05cf5-105">ByVirtualWanName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="05cf5-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05cf5-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="05cf5-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05cf5-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="05cf5-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05cf5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="05cf5-108">DESCRIPTION</span></span>
<span data-ttu-id="05cf5-109">Aggiorna una WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="05cf5-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="05cf5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05cf5-110">EXAMPLES</span></span>

### <span data-ttu-id="05cf5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="05cf5-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="05cf5-112">La procedura precedente consente di creare un gruppo di risorse "testRG" nell'area "Stati Uniti occidentali" e una WAN virtuale di Azure in tale gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="05cf5-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="05cf5-113">VirtualWan viene aggiornato con nuove proprietà.</span><span class="sxs-lookup"><span data-stu-id="05cf5-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="05cf5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05cf5-114">PARAMETERS</span></span>

### <span data-ttu-id="05cf5-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="05cf5-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="05cf5-116">Consentire il traffico di succursale per VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="05cf5-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05cf5-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="05cf5-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="05cf5-118">Consentire il traffico da vnet a vnet per VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="05cf5-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05cf5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05cf5-119">-AsJob</span></span>
<span data-ttu-id="05cf5-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="05cf5-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05cf5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05cf5-121">-DefaultProfile</span></span>
<span data-ttu-id="05cf5-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05cf5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05cf5-123">-Force</span><span class="sxs-lookup"><span data-stu-id="05cf5-123">-Force</span></span>
<span data-ttu-id="05cf5-124">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="05cf5-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="05cf5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05cf5-125">-InputObject</span></span>
<span data-ttu-id="05cf5-126">L'oggetto Wan virtuale da modificare</span><span class="sxs-lookup"><span data-stu-id="05cf5-126">The virtual wan object to be modified</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05cf5-127">-Name</span><span class="sxs-lookup"><span data-stu-id="05cf5-127">-Name</span></span>
<span data-ttu-id="05cf5-128">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="05cf5-128">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05cf5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05cf5-129">-ResourceGroupName</span></span>
<span data-ttu-id="05cf5-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="05cf5-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05cf5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05cf5-131">-ResourceId</span></span>
<span data-ttu-id="05cf5-132">ID della risorsa Azure per la wan virtuale.</span><span class="sxs-lookup"><span data-stu-id="05cf5-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05cf5-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="05cf5-133">-Tag</span></span>
<span data-ttu-id="05cf5-134">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="05cf5-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05cf5-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="05cf5-135">-VirtualWANType</span></span>
<span data-ttu-id="05cf5-136">Tipo di wan virtuale.</span><span class="sxs-lookup"><span data-stu-id="05cf5-136">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05cf5-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05cf5-137">-Confirm</span></span>
<span data-ttu-id="05cf5-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05cf5-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05cf5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05cf5-139">-WhatIf</span></span>
<span data-ttu-id="05cf5-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05cf5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05cf5-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05cf5-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05cf5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05cf5-142">CommonParameters</span></span>
<span data-ttu-id="05cf5-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05cf5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05cf5-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="05cf5-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05cf5-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="05cf5-145">INPUTS</span></span>

### <span data-ttu-id="05cf5-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="05cf5-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="05cf5-147">System.String</span><span class="sxs-lookup"><span data-stu-id="05cf5-147">System.String</span></span>

## <span data-ttu-id="05cf5-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05cf5-148">OUTPUTS</span></span>

### <span data-ttu-id="05cf5-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="05cf5-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="05cf5-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="05cf5-150">NOTES</span></span>

## <span data-ttu-id="05cf5-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05cf5-151">RELATED LINKS</span></span>

[<span data-ttu-id="05cf5-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="05cf5-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="05cf5-153">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="05cf5-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="05cf5-154">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="05cf5-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
