---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: 1d1ccb7f8e47ce34b798124d54fdd85aa18c7d69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177719"
---
# <span data-ttu-id="d5a4c-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d5a4c-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="d5a4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5a4c-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a4c-103">Ottiene informazioni su un'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="d5a4c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5a4c-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5a4c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d5a4c-105">DESCRIPTION</span></span>
<span data-ttu-id="d5a4c-106">Il cmdlet **Get-AzVMCustomScriptExtension** ottiene informazioni su uno script personalizzato Virtual Machine Extension in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="d5a4c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5a4c-107">EXAMPLES</span></span>

### <span data-ttu-id="d5a4c-108">Esempio 1: Ottenere un'estensione di script personalizzata</span><span class="sxs-lookup"><span data-stu-id="d5a4c-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="d5a4c-109">Questo comando ottiene l'estensione di script personalizzata denominata ContosoCustomScript per la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="d5a4c-110">Esempio 2: Ottenere la visualizzazione dell'istanza di un'estensione di script personalizzata</span><span class="sxs-lookup"><span data-stu-id="d5a4c-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="d5a4c-111">Questo comando ottiene la visualizzazione dell'istanza dell'estensione di script personalizzata denominata ContosoCustomScript per la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="d5a4c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5a4c-112">PARAMETERS</span></span>

### <span data-ttu-id="d5a4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a4c-113">-DefaultProfile</span></span>
<span data-ttu-id="d5a4c-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5a4c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d5a4c-115">-Name</span></span>
<span data-ttu-id="d5a4c-116">Specifica il nome dell'estensione di script personalizzata su cui il cmdlet riceve informazioni.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a4c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a4c-117">-ResourceGroupName</span></span>
<span data-ttu-id="d5a4c-118">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-118">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a4c-119">-Stato</span><span class="sxs-lookup"><span data-stu-id="d5a4c-119">-Status</span></span>
<span data-ttu-id="d5a4c-120">Indica che questo cmdlet ottiene la visualizzazione dell'istanza dell'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a4c-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="d5a4c-121">-VMName</span></span>
<span data-ttu-id="d5a4c-122">Specifica il nome di una macchina virtuale per cui questo cmdlet ottiene l'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a4c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a4c-123">CommonParameters</span></span>
<span data-ttu-id="d5a4c-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a4c-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a4c-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="d5a4c-126">INPUTS</span></span>

### <span data-ttu-id="d5a4c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d5a4c-127">System.String</span></span>

### <span data-ttu-id="d5a4c-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d5a4c-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d5a4c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5a4c-129">OUTPUTS</span></span>

### <span data-ttu-id="d5a4c-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="d5a4c-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="d5a4c-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="d5a4c-131">NOTES</span></span>

## <span data-ttu-id="d5a4c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5a4c-132">RELATED LINKS</span></span>

[<span data-ttu-id="d5a4c-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d5a4c-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="d5a4c-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d5a4c-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="d5a4c-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="d5a4c-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


