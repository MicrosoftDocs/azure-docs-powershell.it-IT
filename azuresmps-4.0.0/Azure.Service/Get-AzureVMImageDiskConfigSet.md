---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: ACBE32E5-AA8C-43CA-9FF4-4B59906C6B85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 45d18179fba41d39456a11575fc2041ad4be8557
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029992"
---
# <span data-ttu-id="e3610-101">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="e3610-101">Get-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="e3610-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3610-102">SYNOPSIS</span></span>
<span data-ttu-id="e3610-103">Ottiene un oggetto set di configurazione del disco dal contesto dell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="e3610-103">Gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="e3610-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3610-104">SYNTAX</span></span>

```
Get-AzureVMImageDiskConfigSet [[-ImageContext] <OSImageContext>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e3610-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3610-105">DESCRIPTION</span></span>
<span data-ttu-id="e3610-106">Il cmdlet **Get-AzureVMImageDiskConfigSet** ottiene un oggetto set di configurazione del disco dal contesto dell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="e3610-106">The **Get-AzureVMImageDiskConfigSet** cmdlet gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="e3610-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3610-107">EXAMPLES</span></span>

### <span data-ttu-id="e3610-108">Esempio 1: ottenere un oggetto set configurazione disco da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="e3610-108">Example 1: Get a disk configuration set object from a virtual machine</span></span>
```
PS C:\> Get-AzureVMImage -ImageName $Img | Get-AzureVMImageDiskConfigSet
```

<span data-ttu-id="e3610-109">Questo comando ottiene un oggetto set di configurazione disco da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e3610-109">This command gets a disk configuration set object from a virtual machine.</span></span>

## <span data-ttu-id="e3610-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3610-110">PARAMETERS</span></span>

### <span data-ttu-id="e3610-111">-ImageContext</span><span class="sxs-lookup"><span data-stu-id="e3610-111">-ImageContext</span></span>
<span data-ttu-id="e3610-112">Specifica il contesto di immagine della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e3610-112">Specifies the virtual machine image context.</span></span>

```yaml
Type: OSImageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3610-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e3610-113">-InformationAction</span></span>
<span data-ttu-id="e3610-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="e3610-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e3610-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e3610-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e3610-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="e3610-116">Continue</span></span>
- <span data-ttu-id="e3610-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="e3610-117">Ignore</span></span>
- <span data-ttu-id="e3610-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="e3610-118">Inquire</span></span>
- <span data-ttu-id="e3610-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e3610-119">SilentlyContinue</span></span>
- <span data-ttu-id="e3610-120">Stop</span><span class="sxs-lookup"><span data-stu-id="e3610-120">Stop</span></span>
- <span data-ttu-id="e3610-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="e3610-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3610-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e3610-122">-InformationVariable</span></span>
<span data-ttu-id="e3610-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="e3610-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3610-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3610-124">CommonParameters</span></span>
<span data-ttu-id="e3610-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3610-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3610-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3610-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3610-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3610-127">INPUTS</span></span>

## <span data-ttu-id="e3610-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3610-128">OUTPUTS</span></span>

### <span data-ttu-id="e3610-129">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="e3610-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="e3610-130">Note</span><span class="sxs-lookup"><span data-stu-id="e3610-130">NOTES</span></span>

## <span data-ttu-id="e3610-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3610-131">RELATED LINKS</span></span>

[<span data-ttu-id="e3610-132">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="e3610-132">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="e3610-133">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="e3610-133">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)


