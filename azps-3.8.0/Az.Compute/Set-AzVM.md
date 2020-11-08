---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: c9b7ce0c55ff917839ff8047454dcced42653b3d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018877"
---
# <span data-ttu-id="b1c93-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="b1c93-101">Set-AzVM</span></span>

## <span data-ttu-id="b1c93-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1c93-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c93-103">Contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="b1c93-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="b1c93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1c93-104">SYNTAX</span></span>

### <span data-ttu-id="b1c93-105">GeneralizeResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1c93-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1c93-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b1c93-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1c93-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b1c93-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1c93-108">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b1c93-108">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1c93-109">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b1c93-109">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1c93-110">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b1c93-110">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1c93-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1c93-111">DESCRIPTION</span></span>
<span data-ttu-id="b1c93-112">Il cmdlet **set-AzVM** contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="b1c93-112">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="b1c93-113">Prima di eseguire questo cmdlet, accedere alla macchina virtuale e usare Sysprep per preparare il disco rigido.</span><span class="sxs-lookup"><span data-stu-id="b1c93-113">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="b1c93-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1c93-114">EXAMPLES</span></span>

### <span data-ttu-id="b1c93-115">Esempio 1: contrassegnare una macchina virtuale come generalizzata</span><span class="sxs-lookup"><span data-stu-id="b1c93-115">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="b1c93-116">Questo comando contrassegna la macchina virtuale denominata VirtualMachine07 come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="b1c93-116">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="b1c93-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1c93-117">PARAMETERS</span></span>

### <span data-ttu-id="b1c93-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1c93-118">-AsJob</span></span>
<span data-ttu-id="b1c93-119">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="b1c93-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b1c93-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1c93-120">-DefaultProfile</span></span>
<span data-ttu-id="b1c93-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1c93-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1c93-122">-Generalizzato</span><span class="sxs-lookup"><span data-stu-id="b1c93-122">-Generalized</span></span>
<span data-ttu-id="b1c93-123">Indica che questo cmdlet contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="b1c93-123">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="b1c93-124">-ID</span><span class="sxs-lookup"><span data-stu-id="b1c93-124">-Id</span></span>
<span data-ttu-id="b1c93-125">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b1c93-125">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c93-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1c93-126">-Name</span></span>
<span data-ttu-id="b1c93-127">Specifica il nome della macchina virtuale in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1c93-127">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c93-128">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="b1c93-128">-NoWait</span></span>
<span data-ttu-id="b1c93-129">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b1c93-129">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="b1c93-130">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="b1c93-130">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="b1c93-131">-Riapplicare</span><span class="sxs-lookup"><span data-stu-id="b1c93-131">-Reapply</span></span>
<span data-ttu-id="b1c93-132">Per riapplicare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b1c93-132">To reapply virtual machine.</span></span>

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

### <span data-ttu-id="b1c93-133">-Ridistribuire</span><span class="sxs-lookup"><span data-stu-id="b1c93-133">-Redeploy</span></span>
<span data-ttu-id="b1c93-134">Indica che questo cmdlet ridistribuisce manualmente la macchina virtuale in un host Azure diverso per risolvere eventuali problemi.</span><span class="sxs-lookup"><span data-stu-id="b1c93-134">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="b1c93-135">Se si ridistribuisce una macchina virtuale, viene riavviata, con la conseguenza della perdita di dati dell'unità effimera.</span><span class="sxs-lookup"><span data-stu-id="b1c93-135">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="b1c93-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c93-136">-ResourceGroupName</span></span>
<span data-ttu-id="b1c93-137">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b1c93-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c93-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c93-138">CommonParameters</span></span>
<span data-ttu-id="b1c93-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1c93-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c93-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1c93-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c93-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1c93-141">INPUTS</span></span>

### <span data-ttu-id="b1c93-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b1c93-142">System.String</span></span>

## <span data-ttu-id="b1c93-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1c93-143">OUTPUTS</span></span>

### <span data-ttu-id="b1c93-144">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="b1c93-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="b1c93-145">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b1c93-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b1c93-146">Note</span><span class="sxs-lookup"><span data-stu-id="b1c93-146">NOTES</span></span>

## <span data-ttu-id="b1c93-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1c93-147">RELATED LINKS</span></span>

[<span data-ttu-id="b1c93-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b1c93-148">Get-AzVM</span></span>](./Get-AzVM.md)


