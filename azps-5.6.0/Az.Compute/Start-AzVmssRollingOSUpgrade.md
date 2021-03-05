---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: fb3d6f08eaa540e208830a15563b8edd8c2432ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962446"
---
# <span data-ttu-id="38bc1-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="38bc1-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="38bc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="38bc1-103">Avvia un aggiornamento in sequenza per spostare tutte le istanze del set di scale di macchine virtuali alla versione più recente del sistema operativo immagine della piattaforma disponibile.</span><span class="sxs-lookup"><span data-stu-id="38bc1-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="38bc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38bc1-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38bc1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="38bc1-105">DESCRIPTION</span></span>
<span data-ttu-id="38bc1-106">Avvia un aggiornamento in sequenza per spostare tutte le istanze del set di scale di macchine virtuali alla versione più recente del sistema operativo immagine della piattaforma disponibile.</span><span class="sxs-lookup"><span data-stu-id="38bc1-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="38bc1-107">Le istanze che eseguono già l'ultima versione del sistema operativo disponibile non sono interessate.</span><span class="sxs-lookup"><span data-stu-id="38bc1-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="38bc1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38bc1-108">EXAMPLES</span></span>

### <span data-ttu-id="38bc1-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38bc1-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="38bc1-110">Questo comando avvia l'aggiornamento in sequenza di tutte le istanze della macchina virtuale del set di scala "VMSS001" nel gruppo di risorse "Group001".</span><span class="sxs-lookup"><span data-stu-id="38bc1-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="38bc1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38bc1-111">PARAMETERS</span></span>

### <span data-ttu-id="38bc1-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38bc1-112">-AsJob</span></span>
<span data-ttu-id="38bc1-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="38bc1-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38bc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38bc1-114">-DefaultProfile</span></span>
<span data-ttu-id="38bc1-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38bc1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38bc1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38bc1-116">-ResourceGroupName</span></span>
<span data-ttu-id="38bc1-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38bc1-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="38bc1-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="38bc1-118">-VMScaleSetName</span></span>
<span data-ttu-id="38bc1-119">Nome del set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="38bc1-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="38bc1-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38bc1-120">-Confirm</span></span>
<span data-ttu-id="38bc1-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38bc1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38bc1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38bc1-122">-WhatIf</span></span>
<span data-ttu-id="38bc1-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38bc1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38bc1-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38bc1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38bc1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38bc1-125">CommonParameters</span></span>
<span data-ttu-id="38bc1-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38bc1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38bc1-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38bc1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38bc1-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="38bc1-128">INPUTS</span></span>

### <span data-ttu-id="38bc1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="38bc1-129">System.String</span></span>

## <span data-ttu-id="38bc1-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38bc1-130">OUTPUTS</span></span>

### <span data-ttu-id="38bc1-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="38bc1-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="38bc1-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="38bc1-132">NOTES</span></span>

## <span data-ttu-id="38bc1-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38bc1-133">RELATED LINKS</span></span>
