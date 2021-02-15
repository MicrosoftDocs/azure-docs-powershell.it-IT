---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 9969ee8009e1a0cd3cf5e071f01bd03035455bde
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202669"
---
# <span data-ttu-id="12ac6-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="12ac6-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="12ac6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12ac6-102">SYNOPSIS</span></span>
<span data-ttu-id="12ac6-103">Crea una WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="12ac6-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="12ac6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12ac6-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12ac6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="12ac6-105">DESCRIPTION</span></span>
<span data-ttu-id="12ac6-106">Crea una nuova risorsa Azure VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="12ac6-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="12ac6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12ac6-107">EXAMPLES</span></span>

### <span data-ttu-id="12ac6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="12ac6-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="12ac6-109">La procedura descritta in precedenza consente di creare un gruppo di risorse "testRG" nell'area "Stati Uniti occidentali" e una WAN virtuale di Azure con traffico di succursale consentito in quel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="12ac6-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="12ac6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12ac6-110">PARAMETERS</span></span>

### <span data-ttu-id="12ac6-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="12ac6-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="12ac6-112">Consentire il traffico di succursale per VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="12ac6-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="12ac6-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="12ac6-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="12ac6-114">Consentire il traffico da vnet a vnet per VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="12ac6-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="12ac6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12ac6-115">-AsJob</span></span>
<span data-ttu-id="12ac6-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="12ac6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12ac6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ac6-117">-DefaultProfile</span></span>
<span data-ttu-id="12ac6-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12ac6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12ac6-119">-Location</span><span class="sxs-lookup"><span data-stu-id="12ac6-119">-Location</span></span>
<span data-ttu-id="12ac6-120">Posizione della risorsa VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="12ac6-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ac6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="12ac6-121">-Name</span></span>
<span data-ttu-id="12ac6-122">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="12ac6-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ac6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12ac6-123">-ResourceGroupName</span></span>
<span data-ttu-id="12ac6-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="12ac6-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ac6-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="12ac6-125">-Tag</span></span>
<span data-ttu-id="12ac6-126">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="12ac6-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="12ac6-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="12ac6-127">-VirtualWANType</span></span>
<span data-ttu-id="12ac6-128">Tipo di wan virtuale.</span><span class="sxs-lookup"><span data-stu-id="12ac6-128">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="12ac6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12ac6-129">-Confirm</span></span>
<span data-ttu-id="12ac6-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12ac6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12ac6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12ac6-131">-WhatIf</span></span>
<span data-ttu-id="12ac6-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12ac6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12ac6-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12ac6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12ac6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ac6-134">CommonParameters</span></span>
<span data-ttu-id="12ac6-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12ac6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ac6-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="12ac6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ac6-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="12ac6-137">INPUTS</span></span>

### <span data-ttu-id="12ac6-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="12ac6-138">None</span></span>

## <span data-ttu-id="12ac6-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12ac6-139">OUTPUTS</span></span>

### <span data-ttu-id="12ac6-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="12ac6-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="12ac6-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="12ac6-141">NOTES</span></span>

## <span data-ttu-id="12ac6-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12ac6-142">RELATED LINKS</span></span>

[<span data-ttu-id="12ac6-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="12ac6-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="12ac6-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="12ac6-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="12ac6-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="12ac6-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
