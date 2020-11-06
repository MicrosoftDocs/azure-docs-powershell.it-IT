---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
ms.openlocfilehash: c86bf549c0de3643aaba67143b7df78f6fce798c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509996"
---
# <span data-ttu-id="0a1c0-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="0a1c0-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="0a1c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="0a1c0-103">Ottiene gli SKU disponibili per VMSS.</span><span class="sxs-lookup"><span data-stu-id="0a1c0-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a1c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a1c0-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String> [<CommonParameters>]
```

## <span data-ttu-id="0a1c0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a1c0-105">DESCRIPTION</span></span>
<span data-ttu-id="0a1c0-106">Il cmdlet **Get-AzureRmVmssSku** ottiene gli SKU disponibili per il set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="0a1c0-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="0a1c0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a1c0-107">EXAMPLES</span></span>

### <span data-ttu-id="0a1c0-108">Esempio 1: ottenere tutte le SKU disponibili da VMSS</span><span class="sxs-lookup"><span data-stu-id="0a1c0-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="0a1c0-109">Questo comando consente di ottenere tutte le SKU disponibili dalla VMSS denominata ContosoVMSS che appartiene al gruppo di risorse denominato ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="0a1c0-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="0a1c0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a1c0-110">PARAMETERS</span></span>

### <span data-ttu-id="0a1c0-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a1c0-111">-ResourceGroupName</span></span>
<span data-ttu-id="0a1c0-112">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="0a1c0-112">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="0a1c0-113">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0a1c0-113">-VMScaleSetName</span></span>
<span data-ttu-id="0a1c0-114">Specie il nome del VMSS.</span><span class="sxs-lookup"><span data-stu-id="0a1c0-114">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="0a1c0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a1c0-115">CommonParameters</span></span>
<span data-ttu-id="0a1c0-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a1c0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a1c0-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a1c0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a1c0-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a1c0-118">INPUTS</span></span>

### <span data-ttu-id="0a1c0-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0a1c0-119">None</span></span>
<span data-ttu-id="0a1c0-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0a1c0-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0a1c0-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a1c0-121">OUTPUTS</span></span>

### <span data-ttu-id="0a1c0-122">Questo cmdlet non produce alcun output.</span><span class="sxs-lookup"><span data-stu-id="0a1c0-122">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="0a1c0-123">Note</span><span class="sxs-lookup"><span data-stu-id="0a1c0-123">NOTES</span></span>

## <span data-ttu-id="0a1c0-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a1c0-124">RELATED LINKS</span></span>

[<span data-ttu-id="0a1c0-125">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a1c0-125">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


