---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: 9e7cb85bf29d6982271768af6948db1d3c5b8605
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512719"
---
# <span data-ttu-id="d1fef-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d1fef-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="d1fef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1fef-102">SYNOPSIS</span></span>
<span data-ttu-id="d1fef-103">Ottiene informazioni sull'estensione VMAccess.</span><span class="sxs-lookup"><span data-stu-id="d1fef-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1fef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1fef-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="d1fef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1fef-105">DESCRIPTION</span></span>
<span data-ttu-id="d1fef-106">Il cmdlet **Get-AzureRmVMAccessExtension** ottiene informazioni sull'estensione della macchina virtuale VMAccess (Virtual Machine Access).</span><span class="sxs-lookup"><span data-stu-id="d1fef-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="d1fef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1fef-107">EXAMPLES</span></span>

### <span data-ttu-id="d1fef-108">Esempio 1: ottenere l'estensione VMAccess</span><span class="sxs-lookup"><span data-stu-id="d1fef-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="d1fef-109">Questo comando ottiene l'estensione VMAccess denominata ContosoTest per la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="d1fef-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="d1fef-110">Esempio 2: ottenere la visualizzazione dell'istanza dell'estensione VMAccess</span><span class="sxs-lookup"><span data-stu-id="d1fef-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="d1fef-111">Questo comando consente di ottenere la visualizzazione dell'istanza dell'estensione VMAccess denominata ContosoTest per la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="d1fef-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="d1fef-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1fef-112">PARAMETERS</span></span>

### <span data-ttu-id="d1fef-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1fef-113">-Name</span></span>
<span data-ttu-id="d1fef-114">Specifica il nome dell'estensione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1fef-114">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d1fef-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1fef-115">-ResourceGroupName</span></span>
<span data-ttu-id="d1fef-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1fef-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d1fef-117">-Stato</span><span class="sxs-lookup"><span data-stu-id="d1fef-117">-Status</span></span>
<span data-ttu-id="d1fef-118">Indica che questo cmdlet ottiene solo la visualizzazione istanza dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="d1fef-118">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="d1fef-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="d1fef-119">-VMName</span></span>
<span data-ttu-id="d1fef-120">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1fef-120">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d1fef-121">Questo cmdlet consente di ottenere informazioni su VMAccess per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d1fef-121">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d1fef-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1fef-122">CommonParameters</span></span>
<span data-ttu-id="d1fef-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1fef-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1fef-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1fef-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1fef-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1fef-125">INPUTS</span></span>

### <span data-ttu-id="d1fef-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d1fef-126">None</span></span>
<span data-ttu-id="d1fef-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d1fef-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d1fef-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1fef-128">OUTPUTS</span></span>

## <span data-ttu-id="d1fef-129">Note</span><span class="sxs-lookup"><span data-stu-id="d1fef-129">NOTES</span></span>

## <span data-ttu-id="d1fef-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1fef-130">RELATED LINKS</span></span>

[<span data-ttu-id="d1fef-131">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d1fef-131">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="d1fef-132">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d1fef-132">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="d1fef-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="d1fef-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


