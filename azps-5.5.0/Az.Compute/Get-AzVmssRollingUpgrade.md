---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 3ab0dc0acb02d2efa9f7da29dd096ad03f1eb57e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177711"
---
# <span data-ttu-id="e7c65-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="e7c65-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="e7c65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7c65-102">SYNOPSIS</span></span>
<span data-ttu-id="e7c65-103">Mostra lo stato dell'ultimo aggiornamento del set di scalabilità delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="e7c65-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="e7c65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7c65-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7c65-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e7c65-105">DESCRIPTION</span></span>
<span data-ttu-id="e7c65-106">Mostra lo stato dell'ultimo aggiornamento del set di scalabilità delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="e7c65-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="e7c65-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7c65-107">EXAMPLES</span></span>

### <span data-ttu-id="e7c65-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e7c65-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="e7c65-109">Questo comando mostra lo stato dell'ultimo aggiornamento in sequenza del sistema VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="e7c65-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="e7c65-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7c65-110">PARAMETERS</span></span>

### <span data-ttu-id="e7c65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7c65-111">-DefaultProfile</span></span>
<span data-ttu-id="e7c65-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7c65-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7c65-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7c65-113">-ResourceGroupName</span></span>
<span data-ttu-id="e7c65-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e7c65-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="e7c65-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e7c65-115">-VMScaleSetName</span></span>
<span data-ttu-id="e7c65-116">Nome del set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e7c65-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="e7c65-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7c65-117">CommonParameters</span></span>
<span data-ttu-id="e7c65-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7c65-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7c65-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e7c65-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7c65-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="e7c65-120">INPUTS</span></span>

### <span data-ttu-id="e7c65-121">System.String</span><span class="sxs-lookup"><span data-stu-id="e7c65-121">System.String</span></span>

## <span data-ttu-id="e7c65-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7c65-122">OUTPUTS</span></span>

### <span data-ttu-id="e7c65-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="e7c65-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="e7c65-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="e7c65-124">NOTES</span></span>

## <span data-ttu-id="e7c65-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7c65-125">RELATED LINKS</span></span>
