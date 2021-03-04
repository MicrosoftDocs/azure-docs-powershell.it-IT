---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: b89bf343c1737080867bbe5e8cb5397fd52f6a4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952798"
---
# <span data-ttu-id="8c018-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="8c018-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="8c018-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c018-102">SYNOPSIS</span></span>
<span data-ttu-id="8c018-103">Ottiene gli SKU disponibili per VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c018-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="8c018-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c018-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c018-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8c018-105">DESCRIPTION</span></span>
<span data-ttu-id="8c018-106">Il cmdlet **Get-AzVmssSku** ottiene gli SKU disponibili per il set di scala delle macchine virtuali (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8c018-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="8c018-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c018-107">EXAMPLES</span></span>

### <span data-ttu-id="8c018-108">Esempio 1: Ottenere tutti gli SKU disponibili da VMSS</span><span class="sxs-lookup"><span data-stu-id="8c018-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="8c018-109">Questo comando recupera tutti gli SKU disponibili dal sistema VMSS denominato ContosoVMSS che appartiene al gruppo di risorse denominato ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="8c018-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="8c018-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c018-110">PARAMETERS</span></span>

### <span data-ttu-id="8c018-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c018-111">-DefaultProfile</span></span>
<span data-ttu-id="8c018-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c018-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c018-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c018-113">-ResourceGroupName</span></span>
<span data-ttu-id="8c018-114">Specifica il nome del gruppo di risorse del sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c018-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="8c018-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8c018-115">-VMScaleSetName</span></span>
<span data-ttu-id="8c018-116">Specie il nome del sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c018-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="8c018-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c018-117">CommonParameters</span></span>
<span data-ttu-id="8c018-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c018-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c018-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8c018-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c018-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="8c018-120">INPUTS</span></span>

### <span data-ttu-id="8c018-121">System.String</span><span class="sxs-lookup"><span data-stu-id="8c018-121">System.String</span></span>

## <span data-ttu-id="8c018-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c018-122">OUTPUTS</span></span>

### <span data-ttu-id="8c018-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="8c018-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="8c018-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="8c018-124">NOTES</span></span>

## <span data-ttu-id="8c018-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c018-125">RELATED LINKS</span></span>

[<span data-ttu-id="8c018-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8c018-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


