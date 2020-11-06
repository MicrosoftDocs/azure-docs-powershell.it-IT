---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/repair-azurermvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Repair-AzureRmVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Repair-AzureRmVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: 73dd0ec70f2a39f9d96625e8ac5685301b38176f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509268"
---
# <span data-ttu-id="99a87-101">Repair-AzureRmVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="99a87-101">Repair-AzureRmVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="99a87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99a87-102">SYNOPSIS</span></span>
<span data-ttu-id="99a87-103">Manuale della piattaforma di aggiornamento del dominio per aggiornare le macchine virtuali in un set di scale della macchina virtuale in tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="99a87-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99a87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99a87-104">SYNTAX</span></span>

### <span data-ttu-id="99a87-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99a87-105">DefaultParameter (Default)</span></span>
```
Repair-AzureRmVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99a87-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="99a87-106">ResourceIdParameter</span></span>
```
Repair-AzureRmVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99a87-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="99a87-107">ObjectParameter</span></span>
```
Repair-AzureRmVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99a87-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99a87-108">DESCRIPTION</span></span>
<span data-ttu-id="99a87-109">Force Manual Platform Update Domain Walk per aggiornare le macchine virtuali in un set di scale della macchina virtuale in tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="99a87-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="99a87-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99a87-110">EXAMPLES</span></span>

### <span data-ttu-id="99a87-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99a87-111">Example 1</span></span>
```
PS C:\> Repair-AzureRmVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="99a87-112">Questo comando forza il percorso di aggiornamento di Service Fabric su UD 0 per il set di scale della macchina virtuale specificato dal nome del gruppo di risorse e dal nome del set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="99a87-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="99a87-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="99a87-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzureRmVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzureRmVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="99a87-114">Questo comando forza il percorso di aggiornamento del tessuto di servizio su UD 1 per il set di scale della macchina virtuale specificato dall'oggetto set scala VM.</span><span class="sxs-lookup"><span data-stu-id="99a87-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="99a87-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="99a87-115">Example 3</span></span>
```
PS C:\> Repair-AzureRmVmssServiceFabricUpdateDomain -ResourceId $resoureId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="99a87-116">Questo comando forza il percorso di aggiornamento del tessuto di servizio su UD 2 per il set di scale della macchina virtuale specificato dall'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="99a87-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="99a87-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99a87-117">PARAMETERS</span></span>

### <span data-ttu-id="99a87-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99a87-118">-AsJob</span></span>
<span data-ttu-id="99a87-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="99a87-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99a87-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99a87-120">-DefaultProfile</span></span>
<span data-ttu-id="99a87-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99a87-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99a87-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="99a87-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="99a87-123">Il dominio di aggiornamento della piattaforma per cui è richiesto un percorso di ripristino manuale.</span><span class="sxs-lookup"><span data-stu-id="99a87-123">The platform update domain for which a manual recovery walk is requested.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99a87-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99a87-124">-ResourceGroupName</span></span>
<span data-ttu-id="99a87-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="99a87-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99a87-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99a87-126">-ResourceId</span></span>
<span data-ttu-id="99a87-127">ID risorsa per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="99a87-127">The resource id for the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99a87-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="99a87-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="99a87-129">Oggetto set scala della macchina virtuale locale</span><span class="sxs-lookup"><span data-stu-id="99a87-129">Local virtual machine scale set object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99a87-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="99a87-130">-VMScaleSetName</span></span>
<span data-ttu-id="99a87-131">Nome del set di scale della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="99a87-131">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99a87-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99a87-132">-Confirm</span></span>
<span data-ttu-id="99a87-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99a87-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99a87-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99a87-134">-WhatIf</span></span>
<span data-ttu-id="99a87-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99a87-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99a87-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99a87-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99a87-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99a87-137">CommonParameters</span></span>
<span data-ttu-id="99a87-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99a87-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99a87-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99a87-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99a87-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99a87-140">INPUTS</span></span>

### <span data-ttu-id="99a87-141">System. String</span><span class="sxs-lookup"><span data-stu-id="99a87-141">System.String</span></span>

### <span data-ttu-id="99a87-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="99a87-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="99a87-143">Parametri: VirtualMachineScaleSet (ByValue)</span><span class="sxs-lookup"><span data-stu-id="99a87-143">Parameters: VirtualMachineScaleSet (ByValue)</span></span>

## <span data-ttu-id="99a87-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99a87-144">OUTPUTS</span></span>

### <span data-ttu-id="99a87-145">Microsoft. Azure. Commands. Compute. Automation. Models. PSRecoveryWalkResponse</span><span class="sxs-lookup"><span data-stu-id="99a87-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="99a87-146">Note</span><span class="sxs-lookup"><span data-stu-id="99a87-146">NOTES</span></span>

## <span data-ttu-id="99a87-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99a87-147">RELATED LINKS</span></span>