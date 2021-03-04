---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 36d86f701bfdeea67869b45512a79eeee45c0457
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990428"
---
# <span data-ttu-id="3e0bc-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="3e0bc-101">Stop-AzVM</span></span>

## <span data-ttu-id="3e0bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e0bc-102">SYNOPSIS</span></span>
<span data-ttu-id="3e0bc-103">Arresta una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="3e0bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e0bc-104">SYNTAX</span></span>

### <span data-ttu-id="3e0bc-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e0bc-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e0bc-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3e0bc-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e0bc-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3e0bc-107">DESCRIPTION</span></span>
<span data-ttu-id="3e0bc-108">Il cmdlet **Stop-AzVM** interrompe una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="3e0bc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e0bc-109">EXAMPLES</span></span>

### <span data-ttu-id="3e0bc-110">Esempio 1: Arrestare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="3e0bc-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="3e0bc-111">Questo comando interrompe la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="3e0bc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e0bc-112">PARAMETERS</span></span>

### <span data-ttu-id="3e0bc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e0bc-113">-AsJob</span></span>
<span data-ttu-id="3e0bc-114">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3e0bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e0bc-115">-DefaultProfile</span></span>
<span data-ttu-id="3e0bc-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e0bc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3e0bc-117">-Force</span></span>
<span data-ttu-id="3e0bc-118">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3e0bc-119">-Id</span><span class="sxs-lookup"><span data-stu-id="3e0bc-119">-Id</span></span>
<span data-ttu-id="3e0bc-120">ID della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e0bc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3e0bc-121">-Name</span></span>
<span data-ttu-id="3e0bc-122">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e0bc-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3e0bc-123">-NoWait</span></span>
<span data-ttu-id="3e0bc-124">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3e0bc-125">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3e0bc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e0bc-126">-ResourceGroupName</span></span>
<span data-ttu-id="3e0bc-127">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-127">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e0bc-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="3e0bc-128">-SkipShutdown</span></span>
<span data-ttu-id="3e0bc-129">Per richiedere l'arresto non graceful della macchina virtuale durante il provisioning della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="3e0bc-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="3e0bc-130">-StayProvisioned</span></span>
<span data-ttu-id="3e0bc-131">Il cmdlet interrompe tutte le macchine virtuali nel sistema VMS, ma non le deassegna.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="3e0bc-132">L'addebito per l'account viene addebitato per le macchine virtuali arrestate.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="3e0bc-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e0bc-133">-Confirm</span></span>
<span data-ttu-id="3e0bc-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e0bc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e0bc-135">-WhatIf</span></span>
<span data-ttu-id="3e0bc-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e0bc-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e0bc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e0bc-138">CommonParameters</span></span>
<span data-ttu-id="3e0bc-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e0bc-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3e0bc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e0bc-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="3e0bc-141">INPUTS</span></span>

### <span data-ttu-id="3e0bc-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3e0bc-142">System.String</span></span>

## <span data-ttu-id="3e0bc-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e0bc-143">OUTPUTS</span></span>

### <span data-ttu-id="3e0bc-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="3e0bc-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="3e0bc-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3e0bc-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3e0bc-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="3e0bc-146">NOTES</span></span>

## <span data-ttu-id="3e0bc-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e0bc-147">RELATED LINKS</span></span>

[<span data-ttu-id="3e0bc-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="3e0bc-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="3e0bc-149">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="3e0bc-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="3e0bc-150">Remove-AZVM</span><span class="sxs-lookup"><span data-stu-id="3e0bc-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="3e0bc-151">Restart-AZVM</span><span class="sxs-lookup"><span data-stu-id="3e0bc-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="3e0bc-152">Start-AZVM</span><span class="sxs-lookup"><span data-stu-id="3e0bc-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="3e0bc-153">Update-AZVM</span><span class="sxs-lookup"><span data-stu-id="3e0bc-153">Update-AzVM</span></span>](./Update-AzVM.md)


