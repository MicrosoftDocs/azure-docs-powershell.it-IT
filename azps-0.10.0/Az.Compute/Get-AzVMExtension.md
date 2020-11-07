---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: a8ac31efd77d5b8ff5c07920bb14b44f80ac0955
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863754"
---
# <span data-ttu-id="d57f6-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d57f6-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="d57f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d57f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d57f6-103">Ottiene le proprietà delle estensioni della macchina virtuale installate in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d57f6-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="d57f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d57f6-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d57f6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d57f6-105">DESCRIPTION</span></span>
<span data-ttu-id="d57f6-106">Il cmdlet **Get-AzVMExtension** ottiene le proprietà delle estensioni della macchina virtuale installate in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d57f6-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="d57f6-107">Specificare il nome di un'estensione per cui ottenere le proprietà.</span><span class="sxs-lookup"><span data-stu-id="d57f6-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="d57f6-108">Per ottenere solo la visualizzazione istanza di un'estensione, specificare il parametro status.</span><span class="sxs-lookup"><span data-stu-id="d57f6-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="d57f6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d57f6-109">EXAMPLES</span></span>

### <span data-ttu-id="d57f6-110">Esempio 1: ottenere le proprietà di un'estensione</span><span class="sxs-lookup"><span data-stu-id="d57f6-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="d57f6-111">Questo comando ottiene le proprietà per l'estensione denominata CustomScriptExtension nella macchina virtuale denominata VirtualMachine22 nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d57f6-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="d57f6-112">Esempio 2: ottenere la visualizzazione dell'istanza di un'estensione</span><span class="sxs-lookup"><span data-stu-id="d57f6-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="d57f6-113">Questo comando consente di ottenere la visualizzazione istanza per l'estensione denominata CustomScriptExtension nella macchina virtuale denominata VirtualMachine22 nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d57f6-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="d57f6-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d57f6-114">PARAMETERS</span></span>

### <span data-ttu-id="d57f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d57f6-115">-DefaultProfile</span></span>
<span data-ttu-id="d57f6-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d57f6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d57f6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d57f6-117">-Name</span></span>
<span data-ttu-id="d57f6-118">Specifica il nome di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="d57f6-118">Specifies the name of an extension.</span></span>
<span data-ttu-id="d57f6-119">Questo cmdlet ottiene le proprietà per l'estensione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d57f6-119">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="d57f6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d57f6-120">-ResourceGroupName</span></span>
<span data-ttu-id="d57f6-121">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d57f6-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d57f6-122">-Stato</span><span class="sxs-lookup"><span data-stu-id="d57f6-122">-Status</span></span>
<span data-ttu-id="d57f6-123">Indica che questo cmdlet ottiene solo la visualizzazione dell'istanza di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="d57f6-123">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="d57f6-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="d57f6-124">-VMName</span></span>
<span data-ttu-id="d57f6-125">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d57f6-125">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d57f6-126">Questo cmdlet ottiene le proprietà di un'estensione dalla macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d57f6-126">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d57f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57f6-127">CommonParameters</span></span>
<span data-ttu-id="d57f6-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d57f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d57f6-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d57f6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57f6-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d57f6-130">INPUTS</span></span>

### <span data-ttu-id="d57f6-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d57f6-131">None</span></span>
<span data-ttu-id="d57f6-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d57f6-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d57f6-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d57f6-133">OUTPUTS</span></span>

### <span data-ttu-id="d57f6-134">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d57f6-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="d57f6-135">Note</span><span class="sxs-lookup"><span data-stu-id="d57f6-135">NOTES</span></span>

## <span data-ttu-id="d57f6-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d57f6-136">RELATED LINKS</span></span>

[<span data-ttu-id="d57f6-137">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d57f6-137">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="d57f6-138">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d57f6-138">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


