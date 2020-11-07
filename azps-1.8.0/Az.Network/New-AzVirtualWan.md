---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 17ace5a209a34fc65d79efaac0bfb477e00b2472
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678210"
---
# <span data-ttu-id="4651e-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="4651e-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="4651e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4651e-102">SYNOPSIS</span></span>
<span data-ttu-id="4651e-103">Crea una WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="4651e-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="4651e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4651e-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4651e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4651e-105">DESCRIPTION</span></span>
<span data-ttu-id="4651e-106">Crea una nuova risorsa di Azure VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="4651e-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="4651e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4651e-107">EXAMPLES</span></span>

### <span data-ttu-id="4651e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4651e-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="4651e-109">In precedenza verrà creato un gruppo di risorse "testRG" in Region "West US" e una WAN virtuale di Azure con Branch per il traffico di Branch consentiti nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="4651e-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="4651e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4651e-110">PARAMETERS</span></span>

### <span data-ttu-id="4651e-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="4651e-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="4651e-112">Consenti Branch per il traffico di Branch per VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="4651e-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="4651e-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="4651e-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="4651e-114">Consenti a VNET di VNET il traffico per VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="4651e-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="4651e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4651e-115">-AsJob</span></span>
<span data-ttu-id="4651e-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4651e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4651e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4651e-117">-DefaultProfile</span></span>
<span data-ttu-id="4651e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4651e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4651e-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4651e-119">-Location</span></span>
<span data-ttu-id="4651e-120">Posizione della risorsa VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="4651e-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4651e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4651e-121">-Name</span></span>
<span data-ttu-id="4651e-122">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4651e-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4651e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4651e-123">-ResourceGroupName</span></span>
<span data-ttu-id="4651e-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4651e-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4651e-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="4651e-125">-Tag</span></span>
<span data-ttu-id="4651e-126">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4651e-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4651e-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4651e-127">-Confirm</span></span>
<span data-ttu-id="4651e-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4651e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4651e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4651e-129">-WhatIf</span></span>
<span data-ttu-id="4651e-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4651e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4651e-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4651e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4651e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4651e-132">CommonParameters</span></span>
<span data-ttu-id="4651e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4651e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4651e-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4651e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4651e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4651e-135">INPUTS</span></span>

### <span data-ttu-id="4651e-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4651e-136">None</span></span>

## <span data-ttu-id="4651e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4651e-137">OUTPUTS</span></span>

### <span data-ttu-id="4651e-138">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="4651e-138">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="4651e-139">Note</span><span class="sxs-lookup"><span data-stu-id="4651e-139">NOTES</span></span>

## <span data-ttu-id="4651e-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4651e-140">RELATED LINKS</span></span>

[<span data-ttu-id="4651e-141">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="4651e-141">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="4651e-142">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="4651e-142">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="4651e-143">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="4651e-143">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)