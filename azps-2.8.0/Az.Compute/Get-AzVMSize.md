---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: 2ac1e336161d4cfad1bbef37ec98716456a8143c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675382"
---
# <span data-ttu-id="3e807-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="3e807-101">Get-AzVMSize</span></span>

## <span data-ttu-id="3e807-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e807-102">SYNOPSIS</span></span>
<span data-ttu-id="3e807-103">Ottiene le dimensioni della macchina virtuale disponibili.</span><span class="sxs-lookup"><span data-stu-id="3e807-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="3e807-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e807-104">SYNTAX</span></span>

### <span data-ttu-id="3e807-105">ListVirtualMachineSizeParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e807-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e807-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3e807-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e807-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3e807-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e807-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e807-108">DESCRIPTION</span></span>
<span data-ttu-id="3e807-109">Il cmdlet **Get-AzVMSize** ottiene le dimensioni della macchina virtuale disponibili.</span><span class="sxs-lookup"><span data-stu-id="3e807-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="3e807-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e807-110">EXAMPLES</span></span>

### <span data-ttu-id="3e807-111">Esempio 1: ottenere le dimensioni della macchina virtuale per una posizione</span><span class="sxs-lookup"><span data-stu-id="3e807-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="3e807-112">Questo comando consente di ottenere le dimensioni disponibili per le macchine virtuali nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="3e807-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="3e807-113">Esempio 2: ottenere le dimensioni per un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="3e807-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="3e807-114">Questo comando consente di ottenere le dimensioni disponibili per le macchine virtuali che è possibile distribuire nel set di disponibilità denominato AvailabilitySet17.</span><span class="sxs-lookup"><span data-stu-id="3e807-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="3e807-115">Esempio 3: ottenere le dimensioni per una macchina virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="3e807-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="3e807-116">Questo comando ottiene le dimensioni disponibili per la macchina virtuale esistente denominata VirtualMachine12.</span><span class="sxs-lookup"><span data-stu-id="3e807-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="3e807-117">È possibile ridimensionare la macchina virtuale in base alle dimensioni ottenute dal comando.</span><span class="sxs-lookup"><span data-stu-id="3e807-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="3e807-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e807-118">PARAMETERS</span></span>

### <span data-ttu-id="3e807-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="3e807-119">-AvailabilitySetName</span></span>
<span data-ttu-id="3e807-120">Specifica il nome del set di disponibilità per cui questo cmdlet ottiene le dimensioni della macchina virtuale disponibile.</span><span class="sxs-lookup"><span data-stu-id="3e807-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e807-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e807-121">-DefaultProfile</span></span>
<span data-ttu-id="3e807-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e807-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e807-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3e807-123">-Location</span></span>
<span data-ttu-id="3e807-124">Specifica la posizione per cui questo cmdlet ottiene le dimensioni della macchina virtuale disponibile.</span><span class="sxs-lookup"><span data-stu-id="3e807-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e807-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e807-125">-ResourceGroupName</span></span>
<span data-ttu-id="3e807-126">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3e807-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e807-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="3e807-127">-VMName</span></span>
<span data-ttu-id="3e807-128">Specifica il nome della macchina virtuale che questo cmdlet ottiene le dimensioni della macchina virtuale disponibile per il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="3e807-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e807-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e807-129">CommonParameters</span></span>
<span data-ttu-id="3e807-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e807-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e807-131">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e807-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e807-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e807-132">INPUTS</span></span>

### <span data-ttu-id="3e807-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3e807-133">System.String</span></span>

## <span data-ttu-id="3e807-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e807-134">OUTPUTS</span></span>

### <span data-ttu-id="3e807-135">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="3e807-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="3e807-136">Note</span><span class="sxs-lookup"><span data-stu-id="3e807-136">NOTES</span></span>

## <span data-ttu-id="3e807-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e807-137">RELATED LINKS</span></span>

[<span data-ttu-id="3e807-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="3e807-138">Get-AzVM</span></span>](./Get-AzVM.md)

