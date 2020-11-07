---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: b3e060680ee5df25708f153b239ec6c13b4e8a35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675192"
---
# <span data-ttu-id="a8f81-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="a8f81-101">Set-AzVM</span></span>

## <span data-ttu-id="a8f81-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8f81-102">SYNOPSIS</span></span>
<span data-ttu-id="a8f81-103">Contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="a8f81-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="a8f81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8f81-104">SYNTAX</span></span>

### <span data-ttu-id="a8f81-105">GeneralizeResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8f81-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8f81-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a8f81-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8f81-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a8f81-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8f81-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a8f81-108">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8f81-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8f81-109">DESCRIPTION</span></span>
<span data-ttu-id="a8f81-110">Il cmdlet **set-AzVM** contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="a8f81-110">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="a8f81-111">Prima di eseguire questo cmdlet, accedere alla macchina virtuale e usare Sysprep per preparare il disco rigido.</span><span class="sxs-lookup"><span data-stu-id="a8f81-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="a8f81-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8f81-112">EXAMPLES</span></span>

### <span data-ttu-id="a8f81-113">Esempio 1: contrassegnare una macchina virtuale come generalizzata</span><span class="sxs-lookup"><span data-stu-id="a8f81-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="a8f81-114">Questo comando contrassegna la macchina virtuale denominata VirtualMachine07 come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="a8f81-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="a8f81-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8f81-115">PARAMETERS</span></span>

### <span data-ttu-id="a8f81-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8f81-116">-AsJob</span></span>
<span data-ttu-id="a8f81-117">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="a8f81-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a8f81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f81-118">-DefaultProfile</span></span>
<span data-ttu-id="a8f81-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8f81-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8f81-120">-Generalizzato</span><span class="sxs-lookup"><span data-stu-id="a8f81-120">-Generalized</span></span>
<span data-ttu-id="a8f81-121">Indica che questo cmdlet contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="a8f81-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="a8f81-122">-ID</span><span class="sxs-lookup"><span data-stu-id="a8f81-122">-Id</span></span>
<span data-ttu-id="a8f81-123">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a8f81-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8f81-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8f81-124">-Name</span></span>
<span data-ttu-id="a8f81-125">Specifica il nome della macchina virtuale in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8f81-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8f81-126">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="a8f81-126">-NoWait</span></span>
<span data-ttu-id="a8f81-127">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a8f81-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a8f81-128">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="a8f81-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f81-129">-Ridistribuire</span><span class="sxs-lookup"><span data-stu-id="a8f81-129">-Redeploy</span></span>
<span data-ttu-id="a8f81-130">Indica che questo cmdlet ridistribuisce manualmente la macchina virtuale in un host Azure diverso per risolvere eventuali problemi.</span><span class="sxs-lookup"><span data-stu-id="a8f81-130">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="a8f81-131">Se si ridistribuisce una macchina virtuale, viene riavviata, con la conseguenza della perdita di dati dell'unità effimera.</span><span class="sxs-lookup"><span data-stu-id="a8f81-131">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="a8f81-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8f81-132">-ResourceGroupName</span></span>
<span data-ttu-id="a8f81-133">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a8f81-133">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8f81-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f81-134">CommonParameters</span></span>
<span data-ttu-id="a8f81-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8f81-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f81-136">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8f81-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f81-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8f81-137">INPUTS</span></span>

### <span data-ttu-id="a8f81-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a8f81-138">System.String</span></span>

## <span data-ttu-id="a8f81-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8f81-139">OUTPUTS</span></span>

### <span data-ttu-id="a8f81-140">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="a8f81-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="a8f81-141">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a8f81-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a8f81-142">Note</span><span class="sxs-lookup"><span data-stu-id="a8f81-142">NOTES</span></span>

## <span data-ttu-id="a8f81-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8f81-143">RELATED LINKS</span></span>

[<span data-ttu-id="a8f81-144">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a8f81-144">Get-AzVM</span></span>](./Get-AzVM.md)


