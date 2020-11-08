---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: 34c49bdd798e23e9c5d151ed3de577136fad5b03
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191046"
---
# <span data-ttu-id="e00cd-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="e00cd-101">Set-AzVM</span></span>

## <span data-ttu-id="e00cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e00cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e00cd-103">Contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="e00cd-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="e00cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e00cd-104">SYNTAX</span></span>

### <span data-ttu-id="e00cd-105">GeneralizeResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e00cd-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e00cd-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e00cd-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e00cd-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e00cd-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e00cd-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e00cd-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e00cd-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e00cd-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e00cd-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e00cd-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e00cd-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e00cd-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e00cd-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e00cd-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e00cd-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e00cd-113">DESCRIPTION</span></span>
<span data-ttu-id="e00cd-114">Il cmdlet **set-AzVM** contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="e00cd-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="e00cd-115">Prima di eseguire questo cmdlet, accedere alla macchina virtuale e usare Sysprep per preparare il disco rigido.</span><span class="sxs-lookup"><span data-stu-id="e00cd-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="e00cd-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e00cd-116">EXAMPLES</span></span>

### <span data-ttu-id="e00cd-117">Esempio 1: contrassegnare una macchina virtuale come generalizzata</span><span class="sxs-lookup"><span data-stu-id="e00cd-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="e00cd-118">Questo comando contrassegna la macchina virtuale denominata VirtualMachine07 come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="e00cd-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="e00cd-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e00cd-119">PARAMETERS</span></span>

### <span data-ttu-id="e00cd-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e00cd-120">-AsJob</span></span>
<span data-ttu-id="e00cd-121">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="e00cd-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e00cd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e00cd-122">-DefaultProfile</span></span>
<span data-ttu-id="e00cd-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e00cd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e00cd-124">-Generalizzato</span><span class="sxs-lookup"><span data-stu-id="e00cd-124">-Generalized</span></span>
<span data-ttu-id="e00cd-125">Indica che questo cmdlet contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="e00cd-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e00cd-126">-ID</span><span class="sxs-lookup"><span data-stu-id="e00cd-126">-Id</span></span>
<span data-ttu-id="e00cd-127">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e00cd-127">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e00cd-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e00cd-128">-Name</span></span>
<span data-ttu-id="e00cd-129">Specifica il nome della macchina virtuale in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e00cd-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e00cd-130">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="e00cd-130">-NoWait</span></span>
<span data-ttu-id="e00cd-131">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e00cd-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e00cd-132">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="e00cd-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e00cd-133">-Riapplicare</span><span class="sxs-lookup"><span data-stu-id="e00cd-133">-Reapply</span></span>
<span data-ttu-id="e00cd-134">Per riapplicare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e00cd-134">To reapply virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReapplyResourceGroupNameParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e00cd-135">-Ridistribuire</span><span class="sxs-lookup"><span data-stu-id="e00cd-135">-Redeploy</span></span>
<span data-ttu-id="e00cd-136">Indica che questo cmdlet ridistribuisce manualmente la macchina virtuale in un host Azure diverso per risolvere eventuali problemi.</span><span class="sxs-lookup"><span data-stu-id="e00cd-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="e00cd-137">Se si ridistribuisce una macchina virtuale, viene riavviata, con la conseguenza della perdita di dati dell'unità effimera.</span><span class="sxs-lookup"><span data-stu-id="e00cd-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e00cd-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e00cd-138">-ResourceGroupName</span></span>
<span data-ttu-id="e00cd-139">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e00cd-139">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e00cd-140">-SimulateEviction</span><span class="sxs-lookup"><span data-stu-id="e00cd-140">-SimulateEviction</span></span>
<span data-ttu-id="e00cd-141">Indica che questo cmdlet simula lo sfratto della macchina virtuale spot.</span><span class="sxs-lookup"><span data-stu-id="e00cd-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="e00cd-142">Lo sfratto si verificherà entro 30 minuti dalla chiamata dell'API.</span><span class="sxs-lookup"><span data-stu-id="e00cd-142">The eviction will occur within 30 minutes of calling the API.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimulateEvictionResourceGroupNameParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e00cd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e00cd-143">CommonParameters</span></span>
<span data-ttu-id="e00cd-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e00cd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e00cd-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e00cd-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e00cd-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e00cd-146">INPUTS</span></span>

### <span data-ttu-id="e00cd-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e00cd-147">System.String</span></span>

## <span data-ttu-id="e00cd-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e00cd-148">OUTPUTS</span></span>

### <span data-ttu-id="e00cd-149">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="e00cd-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="e00cd-150">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e00cd-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e00cd-151">Note</span><span class="sxs-lookup"><span data-stu-id="e00cd-151">NOTES</span></span>

## <span data-ttu-id="e00cd-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e00cd-152">RELATED LINKS</span></span>

[<span data-ttu-id="e00cd-153">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e00cd-153">Get-AzVM</span></span>](./Get-AzVM.md)

