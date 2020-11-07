---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: fb35bac6f43ca444762ed1cbf8511d93eab10daf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836615"
---
# <span data-ttu-id="a8a88-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="a8a88-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="a8a88-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8a88-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a88-103">Annulla l'aggiornamento a rotazione della scala della macchina virtuale corrente.</span><span class="sxs-lookup"><span data-stu-id="a8a88-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="a8a88-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8a88-104">SYNTAX</span></span>

### <span data-ttu-id="a8a88-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8a88-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8a88-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="a8a88-106">FriendMethod</span></span>
```
Stop-AzVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8a88-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8a88-107">DESCRIPTION</span></span>
<span data-ttu-id="a8a88-108">Annulla l'aggiornamento a rotazione della scala della macchina virtuale corrente.</span><span class="sxs-lookup"><span data-stu-id="a8a88-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="a8a88-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8a88-109">EXAMPLES</span></span>

### <span data-ttu-id="a8a88-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a8a88-110">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="a8a88-111">Questo comando Annulla l'aggiornamento in corso del rollforward della scala VM imposta "VMSS001" nel gruppo di risorse "Group001".</span><span class="sxs-lookup"><span data-stu-id="a8a88-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="a8a88-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8a88-112">PARAMETERS</span></span>

### <span data-ttu-id="a8a88-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8a88-113">-AsJob</span></span>
<span data-ttu-id="a8a88-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a8a88-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8a88-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8a88-115">-DefaultProfile</span></span>
<span data-ttu-id="a8a88-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8a88-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8a88-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a8a88-117">-Force</span></span>
<span data-ttu-id="a8a88-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a8a88-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a8a88-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8a88-119">-ResourceGroupName</span></span>
<span data-ttu-id="a8a88-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a8a88-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8a88-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a8a88-121">-VMScaleSetName</span></span>
<span data-ttu-id="a8a88-122">Nome del set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="a8a88-122">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8a88-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a8a88-123">-Confirm</span></span>
<span data-ttu-id="a8a88-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8a88-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8a88-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8a88-125">-WhatIf</span></span>
<span data-ttu-id="a8a88-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8a88-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8a88-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8a88-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8a88-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a88-128">CommonParameters</span></span>
<span data-ttu-id="a8a88-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8a88-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8a88-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8a88-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a88-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8a88-131">INPUTS</span></span>

### <span data-ttu-id="a8a88-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a8a88-132">System.String</span></span>

## <span data-ttu-id="a8a88-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8a88-133">OUTPUTS</span></span>

### <span data-ttu-id="a8a88-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a8a88-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a8a88-135">Note</span><span class="sxs-lookup"><span data-stu-id="a8a88-135">NOTES</span></span>

## <span data-ttu-id="a8a88-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8a88-136">RELATED LINKS</span></span>
