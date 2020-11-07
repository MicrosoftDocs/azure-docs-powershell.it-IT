---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmplan
schema: 2.0.0
ms.openlocfilehash: ce0101140bc353eb52ee8d1af7f2878735da73db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867136"
---
# <span data-ttu-id="e9eb1-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="e9eb1-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="e9eb1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="e9eb1-103">Imposta le informazioni sul piano Marketplace in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e9eb1-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9eb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9eb1-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9eb1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9eb1-105">DESCRIPTION</span></span>
<span data-ttu-id="e9eb1-106">Il cmdlet **set-AzureRmVMPlan** imposta le informazioni sul piano di Azure Marketplace per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e9eb1-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="e9eb1-107">Prima di poter distribuire un'immagine Marketplace tramite la riga di comando, l'accesso a livello di codice deve essere abilitato o la macchina virtuale deve essere distribuita usando il portale di Azure.</span><span class="sxs-lookup"><span data-stu-id="e9eb1-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="e9eb1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9eb1-108">EXAMPLES</span></span>

## <span data-ttu-id="e9eb1-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9eb1-109">PARAMETERS</span></span>

### <span data-ttu-id="e9eb1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9eb1-110">-DefaultProfile</span></span>
<span data-ttu-id="e9eb1-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9eb1-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9eb1-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9eb1-112">-Name</span></span>
<span data-ttu-id="e9eb1-113">Specifica il nome dell'immagine dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="e9eb1-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="e9eb1-114">Si tratta dello stesso valore restituito dal cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="e9eb1-114">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="e9eb1-115">Per altre informazioni su come trovare informazioni sulle immagini, vedere Spostamento e selezione di immagini di macchine virtuali di Azure con PowerShell e la https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) di Azure (nella documentazione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e9eb1-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="e9eb1-116">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="e9eb1-116">-Product</span></span>
<span data-ttu-id="e9eb1-117">Specifica il prodotto dell'immagine dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="e9eb1-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="e9eb1-118">Queste sono le stesse informazioni del valore **offer** dell'elemento **imageReference** .</span><span class="sxs-lookup"><span data-stu-id="e9eb1-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="e9eb1-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="e9eb1-119">-PromotionCode</span></span>
<span data-ttu-id="e9eb1-120">Specifica un codice promozionale.</span><span class="sxs-lookup"><span data-stu-id="e9eb1-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="e9eb1-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="e9eb1-121">-Publisher</span></span>
<span data-ttu-id="e9eb1-122">Specifica l'autore dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="e9eb1-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="e9eb1-123">Queste informazioni possono essere trovate usando il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="e9eb1-123">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="e9eb1-124">-VM</span><span class="sxs-lookup"><span data-stu-id="e9eb1-124">-VM</span></span>
<span data-ttu-id="e9eb1-125">Specifica l'oggetto macchina virtuale per cui impostare un piano per Marketplace.</span><span class="sxs-lookup"><span data-stu-id="e9eb1-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="e9eb1-126">Puoi usare il cmdlet Get-AzureRmVM per ottenere un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e9eb1-126">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="e9eb1-127">Puoi usare il cmdlet New-AzureRmVMConfig per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e9eb1-127">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="e9eb1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9eb1-128">CommonParameters</span></span>
<span data-ttu-id="e9eb1-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9eb1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9eb1-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9eb1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9eb1-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9eb1-131">INPUTS</span></span>

### <span data-ttu-id="e9eb1-132">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e9eb1-132">PSVirtualMachine</span></span>
<span data-ttu-id="e9eb1-133">Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e9eb1-133">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="e9eb1-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9eb1-134">OUTPUTS</span></span>

### <span data-ttu-id="e9eb1-135">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e9eb1-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e9eb1-136">Note</span><span class="sxs-lookup"><span data-stu-id="e9eb1-136">NOTES</span></span>

## <span data-ttu-id="e9eb1-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9eb1-137">RELATED LINKS</span></span>

[<span data-ttu-id="e9eb1-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e9eb1-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="e9eb1-139">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e9eb1-139">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="e9eb1-140">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e9eb1-140">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="e9eb1-141">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="e9eb1-141">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
