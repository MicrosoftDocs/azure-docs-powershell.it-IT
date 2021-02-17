---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: 34c49bdd798e23e9c5d151ed3de577136fad5b03
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209986"
---
# <span data-ttu-id="55707-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="55707-101">Set-AzVM</span></span>

## <span data-ttu-id="55707-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55707-102">SYNOPSIS</span></span>
<span data-ttu-id="55707-103">Contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="55707-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="55707-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55707-104">SYNTAX</span></span>

### <span data-ttu-id="55707-105">GeneralizeResourceGroupNameParameterSetName (Default)</span><span class="sxs-lookup"><span data-stu-id="55707-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55707-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="55707-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55707-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="55707-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55707-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="55707-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55707-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="55707-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55707-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="55707-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55707-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="55707-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55707-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="55707-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55707-113">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="55707-113">DESCRIPTION</span></span>
<span data-ttu-id="55707-114">Il cmdlet **Set-AzVM** contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="55707-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="55707-115">Prima di eseguire questo cmdlet, accedere alla macchina virtuale e usare sysprep per preparare il disco rigido.</span><span class="sxs-lookup"><span data-stu-id="55707-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="55707-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55707-116">EXAMPLES</span></span>

### <span data-ttu-id="55707-117">Esempio 1: Contrassegnare una macchina virtuale come generalizzata</span><span class="sxs-lookup"><span data-stu-id="55707-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="55707-118">Questo comando contrassegna come generalizzata la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="55707-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="55707-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55707-119">PARAMETERS</span></span>

### <span data-ttu-id="55707-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55707-120">-AsJob</span></span>
<span data-ttu-id="55707-121">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="55707-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="55707-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55707-122">-DefaultProfile</span></span>
<span data-ttu-id="55707-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55707-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55707-124">-Generalizzato</span><span class="sxs-lookup"><span data-stu-id="55707-124">-Generalized</span></span>
<span data-ttu-id="55707-125">Indica che questo cmdlet contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="55707-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="55707-126">-Id</span><span class="sxs-lookup"><span data-stu-id="55707-126">-Id</span></span>
<span data-ttu-id="55707-127">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="55707-127">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="55707-128">-Name</span><span class="sxs-lookup"><span data-stu-id="55707-128">-Name</span></span>
<span data-ttu-id="55707-129">Specifica il nome della macchina virtuale in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55707-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="55707-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="55707-130">-NoWait</span></span>
<span data-ttu-id="55707-131">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="55707-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="55707-132">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="55707-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="55707-133">-Riapplica</span><span class="sxs-lookup"><span data-stu-id="55707-133">-Reapply</span></span>
<span data-ttu-id="55707-134">Per riapplicare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="55707-134">To reapply virtual machine.</span></span>

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

### <span data-ttu-id="55707-135">-Redeploy</span><span class="sxs-lookup"><span data-stu-id="55707-135">-Redeploy</span></span>
<span data-ttu-id="55707-136">Indica che questo cmdlet ridistribuisce manualmente la macchina virtuale a un altro host azure per risolvere eventuali problemi.</span><span class="sxs-lookup"><span data-stu-id="55707-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="55707-137">Se si ridistribuisce una macchina virtuale, questa viene riavviata, con la perdita dei dati effimeri delle unità.</span><span class="sxs-lookup"><span data-stu-id="55707-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="55707-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55707-138">-ResourceGroupName</span></span>
<span data-ttu-id="55707-139">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="55707-139">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="55707-140">-SimulateEviction</span><span class="sxs-lookup"><span data-stu-id="55707-140">-SimulateEviction</span></span>
<span data-ttu-id="55707-141">Indica che questo cmdlet simula l'evizione della macchina virtuale spot.</span><span class="sxs-lookup"><span data-stu-id="55707-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="55707-142">Lo sgombero verrà eseguito entro 30 minuti dalla chiamata dell'API.</span><span class="sxs-lookup"><span data-stu-id="55707-142">The eviction will occur within 30 minutes of calling the API.</span></span>

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

### <span data-ttu-id="55707-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55707-143">CommonParameters</span></span>
<span data-ttu-id="55707-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55707-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55707-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="55707-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55707-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="55707-146">INPUTS</span></span>

### <span data-ttu-id="55707-147">System.String</span><span class="sxs-lookup"><span data-stu-id="55707-147">System.String</span></span>

## <span data-ttu-id="55707-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55707-148">OUTPUTS</span></span>

### <span data-ttu-id="55707-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="55707-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="55707-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="55707-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="55707-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="55707-151">NOTES</span></span>

## <span data-ttu-id="55707-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55707-152">RELATED LINKS</span></span>

[<span data-ttu-id="55707-153">Get-AZVM</span><span class="sxs-lookup"><span data-stu-id="55707-153">Get-AzVM</span></span>](./Get-AzVM.md)


