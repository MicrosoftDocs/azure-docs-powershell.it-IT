---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 331f390890e6349c5a48f9b57c3d0e99fa972532
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200233"
---
# <span data-ttu-id="cd750-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="cd750-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="cd750-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd750-102">SYNOPSIS</span></span>
<span data-ttu-id="cd750-103">Annulla l'aggiornamento a rotazione della scala della macchina virtuale corrente.</span><span class="sxs-lookup"><span data-stu-id="cd750-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="cd750-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd750-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd750-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd750-105">DESCRIPTION</span></span>
<span data-ttu-id="cd750-106">Annulla l'aggiornamento a rotazione della scala della macchina virtuale corrente.</span><span class="sxs-lookup"><span data-stu-id="cd750-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="cd750-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd750-107">EXAMPLES</span></span>

### <span data-ttu-id="cd750-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd750-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="cd750-109">Questo comando Annulla l'aggiornamento in corso del rollforward della scala VM imposta "VMSS001" nel gruppo di risorse "Group001".</span><span class="sxs-lookup"><span data-stu-id="cd750-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="cd750-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd750-110">PARAMETERS</span></span>

### <span data-ttu-id="cd750-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd750-111">-AsJob</span></span>
<span data-ttu-id="cd750-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cd750-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd750-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd750-113">-DefaultProfile</span></span>
<span data-ttu-id="cd750-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd750-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd750-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cd750-115">-Force</span></span>
<span data-ttu-id="cd750-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cd750-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cd750-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd750-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd750-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd750-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd750-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cd750-119">-VMScaleSetName</span></span>
<span data-ttu-id="cd750-120">Nome del set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="cd750-120">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd750-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd750-121">-Confirm</span></span>
<span data-ttu-id="cd750-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd750-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd750-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd750-123">-WhatIf</span></span>
<span data-ttu-id="cd750-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd750-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd750-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd750-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd750-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd750-126">CommonParameters</span></span>
<span data-ttu-id="cd750-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd750-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd750-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd750-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd750-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd750-129">INPUTS</span></span>

### <span data-ttu-id="cd750-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cd750-130">System.String</span></span>

## <span data-ttu-id="cd750-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd750-131">OUTPUTS</span></span>

### <span data-ttu-id="cd750-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="cd750-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="cd750-133">Note</span><span class="sxs-lookup"><span data-stu-id="cd750-133">NOTES</span></span>

## <span data-ttu-id="cd750-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd750-134">RELATED LINKS</span></span>
