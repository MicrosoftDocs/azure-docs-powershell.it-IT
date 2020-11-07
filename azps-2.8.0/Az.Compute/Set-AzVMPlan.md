---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 39ee23006490ce1dfbca1387a1e058df49850c5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675158"
---
# <span data-ttu-id="c3920-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="c3920-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="c3920-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3920-102">SYNOPSIS</span></span>
<span data-ttu-id="c3920-103">Imposta le informazioni sul piano Marketplace in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c3920-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="c3920-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3920-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3920-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3920-105">DESCRIPTION</span></span>
<span data-ttu-id="c3920-106">Il cmdlet **set-AzVMPlan** imposta le informazioni sul piano di Azure Marketplace per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c3920-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="c3920-107">Prima di poter distribuire un'immagine Marketplace tramite la riga di comando, l'accesso a livello di codice deve essere abilitato o la macchina virtuale deve essere distribuita usando il portale di Azure.</span><span class="sxs-lookup"><span data-stu-id="c3920-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="c3920-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3920-108">EXAMPLES</span></span>

## <span data-ttu-id="c3920-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3920-109">PARAMETERS</span></span>

### <span data-ttu-id="c3920-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3920-110">-DefaultProfile</span></span>
<span data-ttu-id="c3920-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3920-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3920-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3920-112">-Name</span></span>
<span data-ttu-id="c3920-113">Specifica il nome dell'immagine dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="c3920-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="c3920-114">Si tratta dello stesso valore restituito dal cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="c3920-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="c3920-115">Per altre informazioni su come trovare informazioni sulle immagini, vedere Spostamento e selezione di immagini di macchine virtuali di Azure con PowerShell e la https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) di Azure (nella documentazione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c3920-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="c3920-116">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="c3920-116">-Product</span></span>
<span data-ttu-id="c3920-117">Specifica il prodotto dell'immagine dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="c3920-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="c3920-118">Queste sono le stesse informazioni del valore **offer** dell'elemento **imageReference** .</span><span class="sxs-lookup"><span data-stu-id="c3920-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3920-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="c3920-119">-PromotionCode</span></span>
<span data-ttu-id="c3920-120">Specifica un codice promozionale.</span><span class="sxs-lookup"><span data-stu-id="c3920-120">Specifies a promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3920-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c3920-121">-Publisher</span></span>
<span data-ttu-id="c3920-122">Specifica l'autore dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="c3920-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="c3920-123">Queste informazioni possono essere trovate usando il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="c3920-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3920-124">-VM</span><span class="sxs-lookup"><span data-stu-id="c3920-124">-VM</span></span>
<span data-ttu-id="c3920-125">Specifica l'oggetto macchina virtuale per cui impostare un piano per Marketplace.</span><span class="sxs-lookup"><span data-stu-id="c3920-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="c3920-126">Puoi usare il cmdlet Get-AzVM per ottenere un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c3920-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="c3920-127">Puoi usare il cmdlet New-AzVMConfig per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c3920-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3920-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3920-128">CommonParameters</span></span>
<span data-ttu-id="c3920-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3920-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3920-130">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3920-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3920-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3920-131">INPUTS</span></span>

### <span data-ttu-id="c3920-132">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c3920-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="c3920-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c3920-133">System.String</span></span>

## <span data-ttu-id="c3920-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3920-134">OUTPUTS</span></span>

### <span data-ttu-id="c3920-135">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c3920-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c3920-136">Note</span><span class="sxs-lookup"><span data-stu-id="c3920-136">NOTES</span></span>

## <span data-ttu-id="c3920-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3920-137">RELATED LINKS</span></span>

[<span data-ttu-id="c3920-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c3920-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="c3920-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c3920-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="c3920-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="c3920-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="c3920-141">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="c3920-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
