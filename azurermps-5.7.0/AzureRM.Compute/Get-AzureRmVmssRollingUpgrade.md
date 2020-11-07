---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: ef9d1ac2e5bca51ee1addf8fdffd87c5045d23eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687936"
---
# <span data-ttu-id="e1ff4-101">Get-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="e1ff4-101">Get-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="e1ff4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ff4-103">Mostra lo stato dell'aggiornamento a rotazione della scala più recente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e1ff4-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1ff4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1ff4-104">SYNTAX</span></span>

```
Get-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1ff4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1ff4-105">DESCRIPTION</span></span>
<span data-ttu-id="e1ff4-106">Mostra lo stato dell'aggiornamento a rotazione della scala più recente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e1ff4-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="e1ff4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1ff4-107">EXAMPLES</span></span>

### <span data-ttu-id="e1ff4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e1ff4-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="e1ff4-109">Questo comando Mostra lo stato dell'ultimo aggiornamento a rotazione del VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="e1ff4-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="e1ff4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1ff4-110">PARAMETERS</span></span>

### <span data-ttu-id="e1ff4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ff4-111">-DefaultProfile</span></span>
<span data-ttu-id="e1ff4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ff4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ff4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1ff4-113">-ResourceGroupName</span></span>
<span data-ttu-id="e1ff4-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e1ff4-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ff4-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e1ff4-115">-VMScaleSetName</span></span>
<span data-ttu-id="e1ff4-116">Nome del set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="e1ff4-116">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ff4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ff4-117">CommonParameters</span></span>
<span data-ttu-id="e1ff4-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ff4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ff4-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ff4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ff4-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1ff4-120">INPUTS</span></span>

### <span data-ttu-id="e1ff4-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e1ff4-121">System.String</span></span>

## <span data-ttu-id="e1ff4-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1ff4-122">OUTPUTS</span></span>

### <span data-ttu-id="e1ff4-123">Microsoft. Azure. Commands. Compute. Automation. Models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="e1ff4-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="e1ff4-124">Note</span><span class="sxs-lookup"><span data-stu-id="e1ff4-124">NOTES</span></span>

## <span data-ttu-id="e1ff4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1ff4-125">RELATED LINKS</span></span>