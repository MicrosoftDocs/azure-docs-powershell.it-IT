---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
ms.openlocfilehash: c6c17978840fd5c446d7d89350f1792091a5cffa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685620"
---
# <span data-ttu-id="c8e33-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="c8e33-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="c8e33-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8e33-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e33-103">Imposta le informazioni sul piano Marketplace in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c8e33-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8e33-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8e33-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [<CommonParameters>]
```

## <span data-ttu-id="c8e33-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8e33-105">DESCRIPTION</span></span>
<span data-ttu-id="c8e33-106">Il cmdlet **set-AzureRmVMPlan** imposta le informazioni sul piano di Azure Marketplace per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c8e33-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="c8e33-107">Prima di poter distribuire un'immagine Marketplace tramite la riga di comando, l'accesso a livello di codice deve essere abilitato o la macchina virtuale deve essere distribuita usando il portale di Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e33-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="c8e33-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8e33-108">EXAMPLES</span></span>

## <span data-ttu-id="c8e33-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8e33-109">PARAMETERS</span></span>

### <span data-ttu-id="c8e33-110">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8e33-110">-Name</span></span>
<span data-ttu-id="c8e33-111">Specifica il nome dell'immagine dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="c8e33-111">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="c8e33-112">Si tratta dello stesso valore restituito dal cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="c8e33-112">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="c8e33-113">Per altre informazioni su come trovare informazioni sulle immagini, vedere [spostamento e selezione di immagini di macchine virtuali di Azure con PowerShell e la CLI di Azure](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) nella documentazione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e33-113">For more information about how to find image information, see [Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLI](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="c8e33-114">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="c8e33-114">-Product</span></span>
<span data-ttu-id="c8e33-115">Specifica il prodotto dell'immagine dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="c8e33-115">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="c8e33-116">Queste sono le stesse informazioni del valore **offer** dell'elemento **imageReference** .</span><span class="sxs-lookup"><span data-stu-id="c8e33-116">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e33-117">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="c8e33-117">-PromotionCode</span></span>
<span data-ttu-id="c8e33-118">Specifica un codice promozionale.</span><span class="sxs-lookup"><span data-stu-id="c8e33-118">Specifies a promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e33-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c8e33-119">-Publisher</span></span>
<span data-ttu-id="c8e33-120">Specifica l'autore dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="c8e33-120">Specifies the publisher of the image.</span></span>
<span data-ttu-id="c8e33-121">Queste informazioni possono essere trovate usando il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="c8e33-121">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e33-122">-VM</span><span class="sxs-lookup"><span data-stu-id="c8e33-122">-VM</span></span>
<span data-ttu-id="c8e33-123">Specifica l'oggetto macchina virtuale per cui impostare un piano per Marketplace.</span><span class="sxs-lookup"><span data-stu-id="c8e33-123">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="c8e33-124">Puoi usare il cmdlet Get-AzureRmVM per ottenere un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c8e33-124">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="c8e33-125">Puoi usare il cmdlet New-AzureRmVMConfig per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c8e33-125">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e33-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e33-126">CommonParameters</span></span>
<span data-ttu-id="c8e33-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8e33-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e33-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8e33-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e33-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8e33-129">INPUTS</span></span>

### <span data-ttu-id="c8e33-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c8e33-130">None</span></span>
<span data-ttu-id="c8e33-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c8e33-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8e33-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8e33-132">OUTPUTS</span></span>

## <span data-ttu-id="c8e33-133">Note</span><span class="sxs-lookup"><span data-stu-id="c8e33-133">NOTES</span></span>

## <span data-ttu-id="c8e33-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8e33-134">RELATED LINKS</span></span>

[<span data-ttu-id="c8e33-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c8e33-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="c8e33-136">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c8e33-136">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="c8e33-137">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="c8e33-137">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="c8e33-138">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="c8e33-138">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
