---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 46e6e29b9a79fb5a8273fb3872d09e2cd290accd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477628"
---
# <span data-ttu-id="2e08a-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="2e08a-101">Stop-AzVM</span></span>

## <span data-ttu-id="2e08a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e08a-102">SYNOPSIS</span></span>
<span data-ttu-id="2e08a-103">Interrompe una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e08a-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="2e08a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e08a-104">SYNTAX</span></span>

### <span data-ttu-id="2e08a-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2e08a-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e08a-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2e08a-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e08a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e08a-107">DESCRIPTION</span></span>
<span data-ttu-id="2e08a-108">Il cmdlet **Stop-AzVM** arresta una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e08a-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="2e08a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e08a-109">EXAMPLES</span></span>

### <span data-ttu-id="2e08a-110">Esempio 1: arrestare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="2e08a-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="2e08a-111">Questo comando Arresta la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2e08a-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="2e08a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e08a-112">PARAMETERS</span></span>

### <span data-ttu-id="2e08a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e08a-113">-AsJob</span></span>
<span data-ttu-id="2e08a-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="2e08a-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2e08a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e08a-115">-DefaultProfile</span></span>
<span data-ttu-id="2e08a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e08a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e08a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2e08a-117">-Force</span></span>
<span data-ttu-id="2e08a-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2e08a-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2e08a-119">-ID</span><span class="sxs-lookup"><span data-stu-id="2e08a-119">-Id</span></span>
<span data-ttu-id="2e08a-120">ID della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2e08a-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="2e08a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e08a-121">-Name</span></span>
<span data-ttu-id="2e08a-122">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2e08a-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="2e08a-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="2e08a-123">-NoWait</span></span>
<span data-ttu-id="2e08a-124">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2e08a-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="2e08a-125">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="2e08a-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="2e08a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e08a-126">-ResourceGroupName</span></span>
<span data-ttu-id="2e08a-127">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2e08a-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2e08a-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="2e08a-128">-SkipShutdown</span></span>
<span data-ttu-id="2e08a-129">Per richiedere l'arresto non grazioso della VM quando si mantiene il provisioning della VM.</span><span class="sxs-lookup"><span data-stu-id="2e08a-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="2e08a-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="2e08a-130">-StayProvisioned</span></span>
<span data-ttu-id="2e08a-131">Il cmdlet arresta tutte le macchine virtuali all'interno di VMSS, ma non le rilascia.</span><span class="sxs-lookup"><span data-stu-id="2e08a-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="2e08a-132">L'account viene addebitato per le macchine virtuali interrotte.</span><span class="sxs-lookup"><span data-stu-id="2e08a-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="2e08a-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2e08a-133">-Confirm</span></span>
<span data-ttu-id="2e08a-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e08a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e08a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e08a-135">-WhatIf</span></span>
<span data-ttu-id="2e08a-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e08a-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e08a-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e08a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e08a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e08a-138">CommonParameters</span></span>
<span data-ttu-id="2e08a-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e08a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e08a-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e08a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e08a-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e08a-141">INPUTS</span></span>

### <span data-ttu-id="2e08a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2e08a-142">System.String</span></span>

## <span data-ttu-id="2e08a-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e08a-143">OUTPUTS</span></span>

### <span data-ttu-id="2e08a-144">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="2e08a-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="2e08a-145">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2e08a-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2e08a-146">Note</span><span class="sxs-lookup"><span data-stu-id="2e08a-146">NOTES</span></span>

## <span data-ttu-id="2e08a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e08a-147">RELATED LINKS</span></span>

[<span data-ttu-id="2e08a-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2e08a-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="2e08a-149">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2e08a-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="2e08a-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="2e08a-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="2e08a-151">Riavviare-AzVM</span><span class="sxs-lookup"><span data-stu-id="2e08a-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="2e08a-152">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="2e08a-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="2e08a-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="2e08a-153">Update-AzVM</span></span>](./Update-AzVM.md)


