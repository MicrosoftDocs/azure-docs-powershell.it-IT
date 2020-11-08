---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 9969ee8009e1a0cd3cf5e071f01bd03035455bde
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188458"
---
# <span data-ttu-id="8d9a8-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8d9a8-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="8d9a8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8d9a8-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9a8-103">Crea una WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="8d9a8-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="8d9a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d9a8-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d9a8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d9a8-105">DESCRIPTION</span></span>
<span data-ttu-id="8d9a8-106">Crea una nuova risorsa di Azure VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="8d9a8-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="8d9a8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d9a8-107">EXAMPLES</span></span>

### <span data-ttu-id="8d9a8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8d9a8-108">Example 1</span></span>

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

<span data-ttu-id="8d9a8-109">In precedenza verrà creato un gruppo di risorse "testRG" in Region "West US" e una WAN virtuale di Azure con Branch per il traffico di Branch consentiti nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="8d9a8-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="8d9a8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8d9a8-110">PARAMETERS</span></span>

### <span data-ttu-id="8d9a8-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="8d9a8-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="8d9a8-112">Consenti Branch per il traffico di Branch per VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="8d9a8-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="8d9a8-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="8d9a8-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="8d9a8-114">Consenti a VNET di VNET il traffico per VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="8d9a8-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="8d9a8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d9a8-115">-AsJob</span></span>
<span data-ttu-id="8d9a8-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8d9a8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d9a8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d9a8-117">-DefaultProfile</span></span>
<span data-ttu-id="8d9a8-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d9a8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d9a8-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8d9a8-119">-Location</span></span>
<span data-ttu-id="8d9a8-120">Posizione della risorsa VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="8d9a8-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="8d9a8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d9a8-121">-Name</span></span>
<span data-ttu-id="8d9a8-122">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8d9a8-122">The resource name.</span></span>

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

### <span data-ttu-id="8d9a8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d9a8-123">-ResourceGroupName</span></span>
<span data-ttu-id="8d9a8-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8d9a8-124">The resource group name.</span></span>

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

### <span data-ttu-id="8d9a8-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="8d9a8-125">-Tag</span></span>
<span data-ttu-id="8d9a8-126">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="8d9a8-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8d9a8-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="8d9a8-127">-VirtualWANType</span></span>
<span data-ttu-id="8d9a8-128">Tipo della WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="8d9a8-128">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="8d9a8-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8d9a8-129">-Confirm</span></span>
<span data-ttu-id="8d9a8-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d9a8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d9a8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d9a8-131">-WhatIf</span></span>
<span data-ttu-id="8d9a8-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d9a8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d9a8-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d9a8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d9a8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9a8-134">CommonParameters</span></span>
<span data-ttu-id="8d9a8-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d9a8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9a8-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d9a8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9a8-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8d9a8-137">INPUTS</span></span>

### <span data-ttu-id="8d9a8-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8d9a8-138">None</span></span>

## <span data-ttu-id="8d9a8-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d9a8-139">OUTPUTS</span></span>

### <span data-ttu-id="8d9a8-140">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8d9a8-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="8d9a8-141">Note</span><span class="sxs-lookup"><span data-stu-id="8d9a8-141">NOTES</span></span>

## <span data-ttu-id="8d9a8-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d9a8-142">RELATED LINKS</span></span>

[<span data-ttu-id="8d9a8-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8d9a8-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="8d9a8-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8d9a8-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="8d9a8-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8d9a8-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
