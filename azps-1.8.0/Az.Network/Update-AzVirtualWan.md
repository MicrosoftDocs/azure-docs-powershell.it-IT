---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: 3a1d30f3ae44b0e6893682cf0c1d700207682803
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677881"
---
# <span data-ttu-id="6ca54-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6ca54-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="6ca54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ca54-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca54-103">Aggiorna una WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="6ca54-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="6ca54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ca54-104">SYNTAX</span></span>

### <span data-ttu-id="6ca54-105">ByVirtualWanName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ca54-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca54-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="6ca54-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca54-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="6ca54-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ca54-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ca54-108">DESCRIPTION</span></span>
<span data-ttu-id="6ca54-109">Aggiorna una WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="6ca54-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="6ca54-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ca54-110">EXAMPLES</span></span>

### <span data-ttu-id="6ca54-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6ca54-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="6ca54-112">In precedenza verrà creato un gruppo di risorse "testRG" nell'area "West US" e una WAN virtuale di Azure in tale gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="6ca54-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="6ca54-113">VirtualWan viene aggiornato con le nuove proprietà.</span><span class="sxs-lookup"><span data-stu-id="6ca54-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="6ca54-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ca54-114">PARAMETERS</span></span>

### <span data-ttu-id="6ca54-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="6ca54-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="6ca54-116">Consenti Branch per il traffico di Branch per VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="6ca54-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca54-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="6ca54-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="6ca54-118">Consenti a VNET di VNET il traffico per VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="6ca54-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca54-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ca54-119">-AsJob</span></span>
<span data-ttu-id="6ca54-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6ca54-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ca54-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca54-121">-DefaultProfile</span></span>
<span data-ttu-id="6ca54-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ca54-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ca54-123">-Force</span><span class="sxs-lookup"><span data-stu-id="6ca54-123">-Force</span></span>
<span data-ttu-id="6ca54-124">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="6ca54-124">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="6ca54-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ca54-125">-InputObject</span></span>
<span data-ttu-id="6ca54-126">Oggetto WAN virtuale da modificare</span><span class="sxs-lookup"><span data-stu-id="6ca54-126">The virtual wan object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca54-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ca54-127">-Name</span></span>
<span data-ttu-id="6ca54-128">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6ca54-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca54-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca54-129">-ResourceGroupName</span></span>
<span data-ttu-id="6ca54-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6ca54-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca54-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ca54-131">-ResourceId</span></span>
<span data-ttu-id="6ca54-132">ID risorsa Azure per la rete WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="6ca54-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca54-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ca54-133">-Tag</span></span>
<span data-ttu-id="6ca54-134">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="6ca54-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca54-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6ca54-135">-Confirm</span></span>
<span data-ttu-id="6ca54-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ca54-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ca54-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ca54-137">-WhatIf</span></span>
<span data-ttu-id="6ca54-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ca54-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ca54-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ca54-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ca54-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca54-140">CommonParameters</span></span>
<span data-ttu-id="6ca54-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca54-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca54-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ca54-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca54-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ca54-143">INPUTS</span></span>

### <span data-ttu-id="6ca54-144">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6ca54-144">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="6ca54-145">System. String</span><span class="sxs-lookup"><span data-stu-id="6ca54-145">System.String</span></span>

## <span data-ttu-id="6ca54-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ca54-146">OUTPUTS</span></span>

### <span data-ttu-id="6ca54-147">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6ca54-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="6ca54-148">Note</span><span class="sxs-lookup"><span data-stu-id="6ca54-148">NOTES</span></span>

## <span data-ttu-id="6ca54-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ca54-149">RELATED LINKS</span></span>

[<span data-ttu-id="6ca54-150">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6ca54-150">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="6ca54-151">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6ca54-151">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="6ca54-152">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6ca54-152">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
