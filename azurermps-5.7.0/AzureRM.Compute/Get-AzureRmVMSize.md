---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: d75ff7f549ddb1efd9f5640b9b2d634449faa21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516876"
---
# <span data-ttu-id="07262-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="07262-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="07262-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07262-102">SYNOPSIS</span></span>
<span data-ttu-id="07262-103">Ottiene le dimensioni della macchina virtuale disponibili.</span><span class="sxs-lookup"><span data-stu-id="07262-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07262-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07262-104">SYNTAX</span></span>

### <span data-ttu-id="07262-105">ListVirtualMachineSizeParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="07262-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [<CommonParameters>]
```

### <span data-ttu-id="07262-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="07262-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="07262-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="07262-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [<CommonParameters>]
```

## <span data-ttu-id="07262-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07262-108">DESCRIPTION</span></span>
<span data-ttu-id="07262-109">Il cmdlet **Get-AzureRmVMSize** ottiene le dimensioni della macchina virtuale disponibili.</span><span class="sxs-lookup"><span data-stu-id="07262-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="07262-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07262-110">EXAMPLES</span></span>

### <span data-ttu-id="07262-111">Esempio 1: ottenere le dimensioni della macchina virtuale per una posizione</span><span class="sxs-lookup"><span data-stu-id="07262-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="07262-112">Questo comando consente di ottenere le dimensioni disponibili per le macchine virtuali nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="07262-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="07262-113">Esempio 2: ottenere le dimensioni per un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="07262-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="07262-114">Questo comando consente di ottenere le dimensioni disponibili per le macchine virtuali che è possibile distribuire nel set di disponibilità denominato AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="07262-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="07262-115">Esempio 3: ottenere le dimensioni per una macchina virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="07262-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="07262-116">Questo comando ottiene le dimensioni disponibili per la macchina virtuale esistente denominata VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="07262-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="07262-117">È possibile ridimensionare la macchina virtuale in base alle dimensioni ottenute dal comando.</span><span class="sxs-lookup"><span data-stu-id="07262-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="07262-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07262-118">PARAMETERS</span></span>

### <span data-ttu-id="07262-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="07262-119">-AvailabilitySetName</span></span>
<span data-ttu-id="07262-120">Specifica il nome del set di disponibilità per cui questo cmdlet ottiene le dimensioni della macchina virtuale disponibile.</span><span class="sxs-lookup"><span data-stu-id="07262-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07262-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="07262-121">-Location</span></span>
<span data-ttu-id="07262-122">Specifica la posizione per cui questo cmdlet ottiene le dimensioni della macchina virtuale disponibile.</span><span class="sxs-lookup"><span data-stu-id="07262-122">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07262-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07262-123">-ResourceGroupName</span></span>
<span data-ttu-id="07262-124">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="07262-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07262-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="07262-125">-VMName</span></span>
<span data-ttu-id="07262-126">Specifica il nome della macchina virtuale che questo cmdlet ottiene le dimensioni della macchina virtuale disponibile per il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="07262-126">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07262-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07262-127">CommonParameters</span></span>
<span data-ttu-id="07262-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07262-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07262-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07262-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07262-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07262-130">INPUTS</span></span>

### <span data-ttu-id="07262-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="07262-131">None</span></span>
<span data-ttu-id="07262-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="07262-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07262-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07262-133">OUTPUTS</span></span>

## <span data-ttu-id="07262-134">Note</span><span class="sxs-lookup"><span data-stu-id="07262-134">NOTES</span></span>

## <span data-ttu-id="07262-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07262-135">RELATED LINKS</span></span>

[<span data-ttu-id="07262-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="07262-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


