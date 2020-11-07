---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: a147565a61bc75d71083c69766138c3a5a4659db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836671"
---
# <span data-ttu-id="1e36c-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="1e36c-101">Set-AzVM</span></span>

## <span data-ttu-id="1e36c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e36c-102">SYNOPSIS</span></span>
<span data-ttu-id="1e36c-103">Contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="1e36c-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="1e36c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e36c-104">SYNTAX</span></span>

### <span data-ttu-id="1e36c-105">GeneralizeResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e36c-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e36c-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1e36c-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e36c-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1e36c-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [[-Name] <String>] [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e36c-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1e36c-108">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [[-Name] <String>] [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e36c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e36c-109">DESCRIPTION</span></span>
<span data-ttu-id="1e36c-110">Il cmdlet **set-AzVM** contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="1e36c-110">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="1e36c-111">Prima di eseguire questo cmdlet, accedere alla macchina virtuale e usare Sysprep per preparare il disco rigido.</span><span class="sxs-lookup"><span data-stu-id="1e36c-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="1e36c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e36c-112">EXAMPLES</span></span>

### <span data-ttu-id="1e36c-113">Esempio 1: contrassegnare una macchina virtuale come generalizzata</span><span class="sxs-lookup"><span data-stu-id="1e36c-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="1e36c-114">Questo comando contrassegna la macchina virtuale denominata VirtualMachine07 come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="1e36c-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="1e36c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e36c-115">PARAMETERS</span></span>

### <span data-ttu-id="1e36c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e36c-116">-AsJob</span></span>
<span data-ttu-id="1e36c-117">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="1e36c-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1e36c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e36c-118">-DefaultProfile</span></span>
<span data-ttu-id="1e36c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e36c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e36c-120">-Generalizzato</span><span class="sxs-lookup"><span data-stu-id="1e36c-120">-Generalized</span></span>
<span data-ttu-id="1e36c-121">Indica che questo cmdlet contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="1e36c-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="1e36c-122">-ID</span><span class="sxs-lookup"><span data-stu-id="1e36c-122">-Id</span></span>
<span data-ttu-id="1e36c-123">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1e36c-123">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="1e36c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e36c-124">-Name</span></span>
<span data-ttu-id="1e36c-125">Specifica il nome della macchina virtuale in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e36c-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e36c-126">-Ridistribuire</span><span class="sxs-lookup"><span data-stu-id="1e36c-126">-Redeploy</span></span>
<span data-ttu-id="1e36c-127">Indica che questo cmdlet ridistribuisce manualmente la macchina virtuale in un host Azure diverso per risolvere eventuali problemi.</span><span class="sxs-lookup"><span data-stu-id="1e36c-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="1e36c-128">Se si ridistribuisce una macchina virtuale, viene riavviata, con la conseguenza della perdita di dati dell'unità effimera.</span><span class="sxs-lookup"><span data-stu-id="1e36c-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="1e36c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e36c-129">-ResourceGroupName</span></span>
<span data-ttu-id="1e36c-130">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1e36c-130">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1e36c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e36c-131">CommonParameters</span></span>
<span data-ttu-id="1e36c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e36c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e36c-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e36c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e36c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e36c-134">INPUTS</span></span>

### <span data-ttu-id="1e36c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1e36c-135">System.String</span></span>

## <span data-ttu-id="1e36c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e36c-136">OUTPUTS</span></span>

### <span data-ttu-id="1e36c-137">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="1e36c-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="1e36c-138">Note</span><span class="sxs-lookup"><span data-stu-id="1e36c-138">NOTES</span></span>

## <span data-ttu-id="1e36c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e36c-139">RELATED LINKS</span></span>

[<span data-ttu-id="1e36c-140">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="1e36c-140">Get-AzVM</span></span>](./Get-AzVM.md)


