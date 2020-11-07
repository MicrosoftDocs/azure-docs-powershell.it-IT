---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 344f62f6114eb85e1a9e17b0e4d8c4da0acb93a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852097"
---
# <span data-ttu-id="5b286-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="5b286-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="5b286-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b286-102">SYNOPSIS</span></span>
<span data-ttu-id="5b286-103">Mostra lo stato dell'aggiornamento a rotazione della scala più recente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5b286-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="5b286-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b286-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b286-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b286-105">DESCRIPTION</span></span>
<span data-ttu-id="5b286-106">Mostra lo stato dell'aggiornamento a rotazione della scala più recente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5b286-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="5b286-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b286-107">EXAMPLES</span></span>

### <span data-ttu-id="5b286-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5b286-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="5b286-109">Questo comando Mostra lo stato dell'ultimo aggiornamento a rotazione del VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="5b286-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="5b286-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b286-110">PARAMETERS</span></span>

### <span data-ttu-id="5b286-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b286-111">-DefaultProfile</span></span>
<span data-ttu-id="5b286-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b286-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b286-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b286-113">-ResourceGroupName</span></span>
<span data-ttu-id="5b286-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5b286-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="5b286-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5b286-115">-VMScaleSetName</span></span>
<span data-ttu-id="5b286-116">Nome del set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="5b286-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="5b286-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b286-117">CommonParameters</span></span>
<span data-ttu-id="5b286-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b286-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b286-119">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b286-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b286-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b286-120">INPUTS</span></span>

### <span data-ttu-id="5b286-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5b286-121">System.String</span></span>

## <span data-ttu-id="5b286-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b286-122">OUTPUTS</span></span>

### <span data-ttu-id="5b286-123">Microsoft. Azure. Commands. Compute. Automation. Models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="5b286-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="5b286-124">Note</span><span class="sxs-lookup"><span data-stu-id="5b286-124">NOTES</span></span>

## <span data-ttu-id="5b286-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b286-125">RELATED LINKS</span></span>
