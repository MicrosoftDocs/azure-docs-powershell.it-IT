---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: d005f3f182109399f5a74b934959951dfb02c48e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863705"
---
# <span data-ttu-id="8d315-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="8d315-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="8d315-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8d315-102">SYNOPSIS</span></span>
<span data-ttu-id="8d315-103">Ottiene gli SKU disponibili per VMSS.</span><span class="sxs-lookup"><span data-stu-id="8d315-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="8d315-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d315-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d315-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d315-105">DESCRIPTION</span></span>
<span data-ttu-id="8d315-106">Il cmdlet **Get-AzVmssSku** ottiene gli SKU disponibili per il set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8d315-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="8d315-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d315-107">EXAMPLES</span></span>

### <span data-ttu-id="8d315-108">Esempio 1: ottenere tutte le SKU disponibili da VMSS</span><span class="sxs-lookup"><span data-stu-id="8d315-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="8d315-109">Questo comando consente di ottenere tutte le SKU disponibili dalla VMSS denominata ContosoVMSS che appartiene al gruppo di risorse denominato ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="8d315-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="8d315-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8d315-110">PARAMETERS</span></span>

### <span data-ttu-id="8d315-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d315-111">-DefaultProfile</span></span>
<span data-ttu-id="8d315-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d315-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d315-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d315-113">-ResourceGroupName</span></span>
<span data-ttu-id="8d315-114">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="8d315-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="8d315-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8d315-115">-VMScaleSetName</span></span>
<span data-ttu-id="8d315-116">Specie il nome del VMSS.</span><span class="sxs-lookup"><span data-stu-id="8d315-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="8d315-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d315-117">CommonParameters</span></span>
<span data-ttu-id="8d315-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d315-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d315-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d315-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d315-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8d315-120">INPUTS</span></span>

### <span data-ttu-id="8d315-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8d315-121">None</span></span>
<span data-ttu-id="8d315-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8d315-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8d315-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d315-123">OUTPUTS</span></span>

### <span data-ttu-id="8d315-124">Questo cmdlet non produce alcun output.</span><span class="sxs-lookup"><span data-stu-id="8d315-124">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="8d315-125">Note</span><span class="sxs-lookup"><span data-stu-id="8d315-125">NOTES</span></span>

## <span data-ttu-id="8d315-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d315-126">RELATED LINKS</span></span>

[<span data-ttu-id="8d315-127">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d315-127">Get-AzVmss</span></span>](./Get-AzVmss.md)


