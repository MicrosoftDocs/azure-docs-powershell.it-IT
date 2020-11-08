---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: 4b17cbb748a9841e0c22f4b8d8742562876fb9db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199876"
---
# <span data-ttu-id="69a15-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="69a15-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="69a15-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69a15-102">SYNOPSIS</span></span>
<span data-ttu-id="69a15-103">Ottiene gli SKU disponibili per VMSS.</span><span class="sxs-lookup"><span data-stu-id="69a15-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="69a15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69a15-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69a15-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69a15-105">DESCRIPTION</span></span>
<span data-ttu-id="69a15-106">Il cmdlet **Get-AzVmssSku** ottiene gli SKU disponibili per il set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="69a15-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="69a15-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69a15-107">EXAMPLES</span></span>

### <span data-ttu-id="69a15-108">Esempio 1: ottenere tutte le SKU disponibili da VMSS</span><span class="sxs-lookup"><span data-stu-id="69a15-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="69a15-109">Questo comando consente di ottenere tutte le SKU disponibili dalla VMSS denominata ContosoVMSS che appartiene al gruppo di risorse denominato ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="69a15-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="69a15-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69a15-110">PARAMETERS</span></span>

### <span data-ttu-id="69a15-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69a15-111">-DefaultProfile</span></span>
<span data-ttu-id="69a15-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69a15-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69a15-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69a15-113">-ResourceGroupName</span></span>
<span data-ttu-id="69a15-114">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="69a15-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="69a15-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="69a15-115">-VMScaleSetName</span></span>
<span data-ttu-id="69a15-116">Specie il nome del VMSS.</span><span class="sxs-lookup"><span data-stu-id="69a15-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="69a15-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a15-117">CommonParameters</span></span>
<span data-ttu-id="69a15-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69a15-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69a15-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69a15-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a15-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69a15-120">INPUTS</span></span>

### <span data-ttu-id="69a15-121">System. String</span><span class="sxs-lookup"><span data-stu-id="69a15-121">System.String</span></span>

## <span data-ttu-id="69a15-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69a15-122">OUTPUTS</span></span>

### <span data-ttu-id="69a15-123">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="69a15-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="69a15-124">Note</span><span class="sxs-lookup"><span data-stu-id="69a15-124">NOTES</span></span>

## <span data-ttu-id="69a15-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69a15-125">RELATED LINKS</span></span>

[<span data-ttu-id="69a15-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="69a15-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


