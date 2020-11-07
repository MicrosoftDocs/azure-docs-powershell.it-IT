---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: f7965e43c7a294d50d6f0774f76504a90c9d7148
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863486"
---
# <span data-ttu-id="d277d-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="d277d-101">Restart-AzVM</span></span>

## <span data-ttu-id="d277d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d277d-102">SYNOPSIS</span></span>
<span data-ttu-id="d277d-103">Riavvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="d277d-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="d277d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d277d-104">SYNTAX</span></span>

### <span data-ttu-id="d277d-105">RestartResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d277d-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d277d-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d277d-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d277d-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d277d-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d277d-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d277d-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d277d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d277d-109">DESCRIPTION</span></span>
<span data-ttu-id="d277d-110">Il cmdlet **Restart-AzVM riavvia** una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="d277d-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="d277d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d277d-111">EXAMPLES</span></span>

### <span data-ttu-id="d277d-112">Esempio 1: riavviare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="d277d-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="d277d-113">Questo comando Riavvia la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d277d-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="d277d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d277d-114">PARAMETERS</span></span>

### <span data-ttu-id="d277d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d277d-115">-AsJob</span></span>
<span data-ttu-id="d277d-116">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="d277d-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d277d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d277d-117">-DefaultProfile</span></span>
<span data-ttu-id="d277d-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d277d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d277d-119">-ID</span><span class="sxs-lookup"><span data-stu-id="d277d-119">-Id</span></span>
<span data-ttu-id="d277d-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d277d-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d277d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d277d-121">-Name</span></span>
<span data-ttu-id="d277d-122">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d277d-122">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d277d-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="d277d-123">-PerformMaintenance</span></span>
<span data-ttu-id="d277d-124">Per eseguire la manutenzione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d277d-124">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d277d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d277d-125">-ResourceGroupName</span></span>
<span data-ttu-id="d277d-126">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d277d-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d277d-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d277d-127">-Confirm</span></span>
<span data-ttu-id="d277d-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d277d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d277d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d277d-129">-WhatIf</span></span>
<span data-ttu-id="d277d-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d277d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d277d-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d277d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d277d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d277d-132">CommonParameters</span></span>
<span data-ttu-id="d277d-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d277d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d277d-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d277d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d277d-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d277d-135">INPUTS</span></span>

### <span data-ttu-id="d277d-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d277d-136">None</span></span>
<span data-ttu-id="d277d-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d277d-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d277d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d277d-138">OUTPUTS</span></span>

### <span data-ttu-id="d277d-139">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="d277d-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="d277d-140">Note</span><span class="sxs-lookup"><span data-stu-id="d277d-140">NOTES</span></span>

## <span data-ttu-id="d277d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d277d-141">RELATED LINKS</span></span>

[<span data-ttu-id="d277d-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d277d-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d277d-143">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d277d-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="d277d-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="d277d-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="d277d-145">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="d277d-145">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="d277d-146">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="d277d-146">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="d277d-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d277d-147">Update-AzVM</span></span>](./Update-AzVM.md)


