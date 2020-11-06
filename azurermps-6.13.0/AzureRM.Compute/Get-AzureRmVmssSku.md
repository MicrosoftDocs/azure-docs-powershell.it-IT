---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssSku.md
ms.openlocfilehash: c906d7b0b10197e934ace7f9c913ee36e02be7ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520267"
---
# <span data-ttu-id="ead8b-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="ead8b-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="ead8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ead8b-102">SYNOPSIS</span></span>
<span data-ttu-id="ead8b-103">Ottiene gli SKU disponibili per VMSS.</span><span class="sxs-lookup"><span data-stu-id="ead8b-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ead8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ead8b-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ead8b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ead8b-105">DESCRIPTION</span></span>
<span data-ttu-id="ead8b-106">Il cmdlet **Get-AzureRmVmssSku** ottiene gli SKU disponibili per il set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ead8b-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ead8b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ead8b-107">EXAMPLES</span></span>

### <span data-ttu-id="ead8b-108">Esempio 1: ottenere tutte le SKU disponibili da VMSS</span><span class="sxs-lookup"><span data-stu-id="ead8b-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="ead8b-109">Questo comando consente di ottenere tutte le SKU disponibili dalla VMSS denominata ContosoVMSS che appartiene al gruppo di risorse denominato ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="ead8b-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="ead8b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ead8b-110">PARAMETERS</span></span>

### <span data-ttu-id="ead8b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead8b-111">-DefaultProfile</span></span>
<span data-ttu-id="ead8b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ead8b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead8b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ead8b-113">-ResourceGroupName</span></span>
<span data-ttu-id="ead8b-114">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="ead8b-114">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead8b-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ead8b-115">-VMScaleSetName</span></span>
<span data-ttu-id="ead8b-116">Specie il nome del VMSS.</span><span class="sxs-lookup"><span data-stu-id="ead8b-116">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead8b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead8b-117">CommonParameters</span></span>
<span data-ttu-id="ead8b-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ead8b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead8b-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ead8b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead8b-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ead8b-120">INPUTS</span></span>

### <span data-ttu-id="ead8b-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ead8b-121">System.String</span></span>

## <span data-ttu-id="ead8b-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ead8b-122">OUTPUTS</span></span>

### <span data-ttu-id="ead8b-123">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="ead8b-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="ead8b-124">Note</span><span class="sxs-lookup"><span data-stu-id="ead8b-124">NOTES</span></span>

## <span data-ttu-id="ead8b-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ead8b-125">RELATED LINKS</span></span>

[<span data-ttu-id="ead8b-126">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ead8b-126">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


