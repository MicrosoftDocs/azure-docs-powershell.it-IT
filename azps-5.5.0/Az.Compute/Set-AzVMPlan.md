---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 93837ff6618523f71fdd2b0a3b933b50892af429
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196967"
---
# <span data-ttu-id="65a58-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="65a58-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="65a58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65a58-102">SYNOPSIS</span></span>
<span data-ttu-id="65a58-103">Imposta le informazioni del piano Marketplace in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="65a58-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="65a58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65a58-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65a58-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="65a58-105">DESCRIPTION</span></span>
<span data-ttu-id="65a58-106">Il **cmdlet Set-AzVMPlan** imposta le informazioni sul piano di Azure Marketplace per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="65a58-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="65a58-107">Prima di poter distribuire un'immagine di Marketplace tramite la riga di comando, è necessario che sia abilitato l'accesso programmatico o che la macchina virtuale venga distribuita tramite il portale di Azure.</span><span class="sxs-lookup"><span data-stu-id="65a58-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="65a58-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65a58-108">EXAMPLES</span></span>

## <span data-ttu-id="65a58-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65a58-109">PARAMETERS</span></span>

### <span data-ttu-id="65a58-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65a58-110">-DefaultProfile</span></span>
<span data-ttu-id="65a58-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65a58-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65a58-112">-Name</span><span class="sxs-lookup"><span data-stu-id="65a58-112">-Name</span></span>
<span data-ttu-id="65a58-113">Specifica il nome dell'immagine dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="65a58-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="65a58-114">Si tratta dello stesso valore restituito dal cmdlet Get-AzVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a58-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="65a58-115">Per altre informazioni su come trovare le informazioni sull'immagine, vedere Esplorazione e selezione delle immagini di macchine virtuali di Azure con PowerShell e la cli di Azure (nella documentazione https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) di Microsoft Azure).</span><span class="sxs-lookup"><span data-stu-id="65a58-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="65a58-116">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="65a58-116">-Product</span></span>
<span data-ttu-id="65a58-117">Specifica il prodotto dell'immagine dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="65a58-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="65a58-118">Si tratta delle stesse informazioni del valore **dell'offerta** **dell'elemento imageReference.**</span><span class="sxs-lookup"><span data-stu-id="65a58-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="65a58-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="65a58-119">-PromotionCode</span></span>
<span data-ttu-id="65a58-120">Specifica un codice promozionale.</span><span class="sxs-lookup"><span data-stu-id="65a58-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="65a58-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="65a58-121">-Publisher</span></span>
<span data-ttu-id="65a58-122">Specifica l'autore dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="65a58-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="65a58-123">Per trovare queste informazioni, usare il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="65a58-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="65a58-124">-VM</span><span class="sxs-lookup"><span data-stu-id="65a58-124">-VM</span></span>
<span data-ttu-id="65a58-125">Specifica l'oggetto della macchina virtuale per cui impostare un piano di Marketplace.</span><span class="sxs-lookup"><span data-stu-id="65a58-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="65a58-126">È possibile usare il cmdlet Get-AzVM per ottenere un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="65a58-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="65a58-127">È possibile usare il cmdlet New-AzVMConfig per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="65a58-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="65a58-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a58-128">CommonParameters</span></span>
<span data-ttu-id="65a58-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65a58-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a58-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="65a58-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a58-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="65a58-131">INPUTS</span></span>

### <span data-ttu-id="65a58-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="65a58-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="65a58-133">System.String</span><span class="sxs-lookup"><span data-stu-id="65a58-133">System.String</span></span>

## <span data-ttu-id="65a58-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65a58-134">OUTPUTS</span></span>

### <span data-ttu-id="65a58-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="65a58-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="65a58-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="65a58-136">NOTES</span></span>

## <span data-ttu-id="65a58-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65a58-137">RELATED LINKS</span></span>

[<span data-ttu-id="65a58-138">Get-AZVM</span><span class="sxs-lookup"><span data-stu-id="65a58-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="65a58-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="65a58-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="65a58-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="65a58-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="65a58-141">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="65a58-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
