---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 82ab2f02d47b17342f71b09eebe826fc48c07b81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510015"
---
# <span data-ttu-id="1adff-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="1adff-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="1adff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1adff-102">SYNOPSIS</span></span>
<span data-ttu-id="1adff-103">Ottiene le proprietà delle estensioni della macchina virtuale installate in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1adff-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1adff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1adff-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="1adff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1adff-105">DESCRIPTION</span></span>
<span data-ttu-id="1adff-106">Il cmdlet **Get-AzureRmVMExtension** ottiene le proprietà delle estensioni della macchina virtuale installate in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1adff-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="1adff-107">Specificare il nome di un'estensione per cui ottenere le proprietà.</span><span class="sxs-lookup"><span data-stu-id="1adff-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="1adff-108">Per ottenere solo la visualizzazione istanza di un'estensione, specificare il parametro status.</span><span class="sxs-lookup"><span data-stu-id="1adff-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="1adff-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1adff-109">EXAMPLES</span></span>

### <span data-ttu-id="1adff-110">Esempio 1: ottenere le proprietà di un'estensione</span><span class="sxs-lookup"><span data-stu-id="1adff-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="1adff-111">Questo comando ottiene le proprietà per l'estensione denominata CustomScriptExtension nella macchina virtuale denominata VirtualMachine22 nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1adff-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="1adff-112">Esempio 2: ottenere la visualizzazione dell'istanza di un'estensione</span><span class="sxs-lookup"><span data-stu-id="1adff-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="1adff-113">Questo comando consente di ottenere la visualizzazione istanza per l'estensione denominata CustomScriptExtension nella macchina virtuale denominata VirtualMachine22 nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1adff-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="1adff-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1adff-114">PARAMETERS</span></span>

### <span data-ttu-id="1adff-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1adff-115">-Name</span></span>
<span data-ttu-id="1adff-116">Specifica il nome di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="1adff-116">Specifies the name of an extension.</span></span>
<span data-ttu-id="1adff-117">Questo cmdlet ottiene le proprietà per l'estensione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1adff-117">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1adff-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1adff-118">-ResourceGroupName</span></span>
<span data-ttu-id="1adff-119">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1adff-119">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1adff-120">-Stato</span><span class="sxs-lookup"><span data-stu-id="1adff-120">-Status</span></span>
<span data-ttu-id="1adff-121">Indica che questo cmdlet ottiene solo la visualizzazione dell'istanza di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="1adff-121">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1adff-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="1adff-122">-VMName</span></span>
<span data-ttu-id="1adff-123">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1adff-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1adff-124">Questo cmdlet ottiene le proprietà di un'estensione dalla macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1adff-124">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1adff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1adff-125">CommonParameters</span></span>
<span data-ttu-id="1adff-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1adff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1adff-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1adff-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1adff-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1adff-128">INPUTS</span></span>

### <span data-ttu-id="1adff-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1adff-129">None</span></span>
<span data-ttu-id="1adff-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1adff-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1adff-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1adff-131">OUTPUTS</span></span>

## <span data-ttu-id="1adff-132">Note</span><span class="sxs-lookup"><span data-stu-id="1adff-132">NOTES</span></span>

## <span data-ttu-id="1adff-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1adff-133">RELATED LINKS</span></span>

[<span data-ttu-id="1adff-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="1adff-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="1adff-135">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="1adff-135">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


