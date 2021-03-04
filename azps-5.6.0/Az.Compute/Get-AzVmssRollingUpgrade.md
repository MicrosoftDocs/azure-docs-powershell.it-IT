---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: e87c307592f4487de239245ef06a70ea084ef916
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957630"
---
# <span data-ttu-id="397fe-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="397fe-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="397fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="397fe-102">SYNOPSIS</span></span>
<span data-ttu-id="397fe-103">Mostra lo stato dell'ultimo aggiornamento del set di scalabilità delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="397fe-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="397fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="397fe-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="397fe-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="397fe-105">DESCRIPTION</span></span>
<span data-ttu-id="397fe-106">Mostra lo stato dell'ultimo aggiornamento del set di scalabilità delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="397fe-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="397fe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="397fe-107">EXAMPLES</span></span>

### <span data-ttu-id="397fe-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="397fe-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="397fe-109">Questo comando mostra lo stato dell'ultimo aggiornamento in sequenza del sistema VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="397fe-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="397fe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="397fe-110">PARAMETERS</span></span>

### <span data-ttu-id="397fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="397fe-111">-DefaultProfile</span></span>
<span data-ttu-id="397fe-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="397fe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="397fe-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="397fe-113">-ResourceGroupName</span></span>
<span data-ttu-id="397fe-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="397fe-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="397fe-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="397fe-115">-VMScaleSetName</span></span>
<span data-ttu-id="397fe-116">Nome del set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="397fe-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="397fe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="397fe-117">CommonParameters</span></span>
<span data-ttu-id="397fe-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="397fe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="397fe-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="397fe-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="397fe-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="397fe-120">INPUTS</span></span>

### <span data-ttu-id="397fe-121">System.String</span><span class="sxs-lookup"><span data-stu-id="397fe-121">System.String</span></span>

## <span data-ttu-id="397fe-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="397fe-122">OUTPUTS</span></span>

### <span data-ttu-id="397fe-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="397fe-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="397fe-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="397fe-124">NOTES</span></span>

## <span data-ttu-id="397fe-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="397fe-125">RELATED LINKS</span></span>
