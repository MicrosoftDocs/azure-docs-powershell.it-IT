---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsssku
schema: 2.0.0
ms.openlocfilehash: 307b9852f506368e1e13c02fac4532dab4d2ddd2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866571"
---
# <span data-ttu-id="f7d9d-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="f7d9d-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="f7d9d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d9d-103">Ottiene gli SKU disponibili per VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7d9d-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7d9d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7d9d-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7d9d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7d9d-105">DESCRIPTION</span></span>
<span data-ttu-id="f7d9d-106">Il cmdlet **Get-AzureRmVmssSku** ottiene gli SKU disponibili per il set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f7d9d-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="f7d9d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7d9d-107">EXAMPLES</span></span>

### <span data-ttu-id="f7d9d-108">Esempio 1: ottenere tutte le SKU disponibili da VMSS</span><span class="sxs-lookup"><span data-stu-id="f7d9d-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="f7d9d-109">Questo comando consente di ottenere tutte le SKU disponibili dalla VMSS denominata ContosoVMSS che appartiene al gruppo di risorse denominato ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="f7d9d-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="f7d9d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7d9d-110">PARAMETERS</span></span>

### <span data-ttu-id="f7d9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d9d-111">-DefaultProfile</span></span>
<span data-ttu-id="f7d9d-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d9d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7d9d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d9d-113">-ResourceGroupName</span></span>
<span data-ttu-id="f7d9d-114">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7d9d-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="f7d9d-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f7d9d-115">-VMScaleSetName</span></span>
<span data-ttu-id="f7d9d-116">Specie il nome del VMSS.</span><span class="sxs-lookup"><span data-stu-id="f7d9d-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="f7d9d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d9d-117">CommonParameters</span></span>
<span data-ttu-id="f7d9d-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7d9d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d9d-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7d9d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d9d-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7d9d-120">INPUTS</span></span>

### <span data-ttu-id="f7d9d-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f7d9d-121">None</span></span>
<span data-ttu-id="f7d9d-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f7d9d-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7d9d-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7d9d-123">OUTPUTS</span></span>

### <span data-ttu-id="f7d9d-124">Questo cmdlet non produce alcun output.</span><span class="sxs-lookup"><span data-stu-id="f7d9d-124">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="f7d9d-125">Note</span><span class="sxs-lookup"><span data-stu-id="f7d9d-125">NOTES</span></span>

## <span data-ttu-id="f7d9d-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7d9d-126">RELATED LINKS</span></span>

[<span data-ttu-id="f7d9d-127">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f7d9d-127">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


