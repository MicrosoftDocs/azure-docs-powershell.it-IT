---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 1f348a7cddc31a2a3d3d255aa6b4fe80d1808f36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514508"
---
# <span data-ttu-id="0bdae-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="0bdae-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="0bdae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0bdae-102">SYNOPSIS</span></span>
<span data-ttu-id="0bdae-103">Ottiene informazioni su un'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0bdae-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bdae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0bdae-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="0bdae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bdae-105">DESCRIPTION</span></span>
<span data-ttu-id="0bdae-106">Il cmdlet **Get-AzureRmVMCustomScriptExtension** ottiene informazioni su un'estensione di una macchina virtuale script personalizzata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0bdae-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="0bdae-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0bdae-107">EXAMPLES</span></span>

### <span data-ttu-id="0bdae-108">Esempio 1: ottenere un'estensione di script personalizzata</span><span class="sxs-lookup"><span data-stu-id="0bdae-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="0bdae-109">Questo comando consente di ottenere l'estensione di script personalizzata denominata ContosoCustomScript per la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="0bdae-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="0bdae-110">Esempio 2: ottenere la visualizzazione dell'istanza di un'estensione di script personalizzata</span><span class="sxs-lookup"><span data-stu-id="0bdae-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="0bdae-111">Questo comando consente di ottenere la visualizzazione dell'istanza dell'estensione di script personalizzata denominata ContosoCustomScript per la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="0bdae-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="0bdae-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0bdae-112">PARAMETERS</span></span>

### <span data-ttu-id="0bdae-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="0bdae-113">-Name</span></span>
<span data-ttu-id="0bdae-114">Specifica il nome dell'estensione di script personalizzata su cui questo cmdlet ottiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="0bdae-114">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="0bdae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bdae-115">-ResourceGroupName</span></span>
<span data-ttu-id="0bdae-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0bdae-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0bdae-117">-Stato</span><span class="sxs-lookup"><span data-stu-id="0bdae-117">-Status</span></span>
<span data-ttu-id="0bdae-118">Indica che questo cmdlet ottiene la visualizzazione dell'istanza dell'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0bdae-118">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="0bdae-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="0bdae-119">-VMName</span></span>
<span data-ttu-id="0bdae-120">Specifica il nome di una macchina virtuale per cui questo cmdlet ottiene l'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0bdae-120">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="0bdae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bdae-121">CommonParameters</span></span>
<span data-ttu-id="0bdae-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bdae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bdae-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bdae-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bdae-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0bdae-124">INPUTS</span></span>

### <span data-ttu-id="0bdae-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0bdae-125">None</span></span>
<span data-ttu-id="0bdae-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0bdae-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0bdae-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bdae-127">OUTPUTS</span></span>

## <span data-ttu-id="0bdae-128">Note</span><span class="sxs-lookup"><span data-stu-id="0bdae-128">NOTES</span></span>

## <span data-ttu-id="0bdae-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0bdae-129">RELATED LINKS</span></span>

[<span data-ttu-id="0bdae-130">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="0bdae-130">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="0bdae-131">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="0bdae-131">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="0bdae-132">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="0bdae-132">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


