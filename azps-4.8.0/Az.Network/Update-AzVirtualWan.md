---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: e93bcc320f14a8311a29c6be9824da16506ea499
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189456"
---
# <span data-ttu-id="7d552-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7d552-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="7d552-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d552-102">SYNOPSIS</span></span>
<span data-ttu-id="7d552-103">Aggiorna una WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d552-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="7d552-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d552-104">SYNTAX</span></span>

### <span data-ttu-id="7d552-105">ByVirtualWanName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d552-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d552-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="7d552-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d552-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="7d552-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d552-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d552-108">DESCRIPTION</span></span>
<span data-ttu-id="7d552-109">Aggiorna una WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d552-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="7d552-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d552-110">EXAMPLES</span></span>

### <span data-ttu-id="7d552-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7d552-111">Example 1</span></span>

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

<span data-ttu-id="7d552-112">In precedenza verrà creato un gruppo di risorse "testRG" nell'area "West US" e una WAN virtuale di Azure in tale gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="7d552-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="7d552-113">VirtualWan viene aggiornato con le nuove proprietà.</span><span class="sxs-lookup"><span data-stu-id="7d552-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="7d552-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d552-114">PARAMETERS</span></span>

### <span data-ttu-id="7d552-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="7d552-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="7d552-116">Consenti Branch per il traffico di Branch per VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="7d552-116">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="7d552-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="7d552-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="7d552-118">Consenti a VNET di VNET il traffico per VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="7d552-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="7d552-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d552-119">-AsJob</span></span>
<span data-ttu-id="7d552-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7d552-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d552-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d552-121">-DefaultProfile</span></span>
<span data-ttu-id="7d552-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d552-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d552-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7d552-123">-Force</span></span>
<span data-ttu-id="7d552-124">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="7d552-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7d552-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d552-125">-InputObject</span></span>
<span data-ttu-id="7d552-126">Oggetto WAN virtuale da modificare</span><span class="sxs-lookup"><span data-stu-id="7d552-126">The virtual wan object to be modified</span></span>

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

### <span data-ttu-id="7d552-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d552-127">-Name</span></span>
<span data-ttu-id="7d552-128">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7d552-128">The resource name.</span></span>

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

### <span data-ttu-id="7d552-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d552-129">-ResourceGroupName</span></span>
<span data-ttu-id="7d552-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7d552-130">The resource group name.</span></span>

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

### <span data-ttu-id="7d552-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d552-131">-ResourceId</span></span>
<span data-ttu-id="7d552-132">ID risorsa Azure per la rete WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="7d552-132">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="7d552-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="7d552-133">-Tag</span></span>
<span data-ttu-id="7d552-134">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="7d552-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7d552-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="7d552-135">-VirtualWANType</span></span>
<span data-ttu-id="7d552-136">Tipo della WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="7d552-136">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="7d552-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7d552-137">-Confirm</span></span>
<span data-ttu-id="7d552-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d552-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d552-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d552-139">-WhatIf</span></span>
<span data-ttu-id="7d552-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d552-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d552-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d552-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d552-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d552-142">CommonParameters</span></span>
<span data-ttu-id="7d552-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d552-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d552-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d552-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d552-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d552-145">INPUTS</span></span>

### <span data-ttu-id="7d552-146">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7d552-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="7d552-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7d552-147">System.String</span></span>

## <span data-ttu-id="7d552-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d552-148">OUTPUTS</span></span>

### <span data-ttu-id="7d552-149">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7d552-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="7d552-150">Note</span><span class="sxs-lookup"><span data-stu-id="7d552-150">NOTES</span></span>

## <span data-ttu-id="7d552-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d552-151">RELATED LINKS</span></span>

[<span data-ttu-id="7d552-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7d552-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="7d552-153">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7d552-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="7d552-154">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7d552-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
