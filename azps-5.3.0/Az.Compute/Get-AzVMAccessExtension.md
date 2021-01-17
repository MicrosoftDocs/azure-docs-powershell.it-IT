---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: c139e1bac6f910a1759e4482abdd7c67d2e7fa55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477816"
---
# <span data-ttu-id="81043-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="81043-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="81043-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81043-102">SYNOPSIS</span></span>
<span data-ttu-id="81043-103">Ottiene informazioni sull'estensione VMAccess.</span><span class="sxs-lookup"><span data-stu-id="81043-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="81043-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81043-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81043-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81043-105">DESCRIPTION</span></span>
<span data-ttu-id="81043-106">Il cmdlet **Get-AzVMAccessExtension** ottiene informazioni sull'estensione della macchina virtuale VMAccess (Virtual Machine Access).</span><span class="sxs-lookup"><span data-stu-id="81043-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="81043-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81043-107">EXAMPLES</span></span>

### <span data-ttu-id="81043-108">Esempio 1: ottenere l'estensione VMAccess</span><span class="sxs-lookup"><span data-stu-id="81043-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="81043-109">Questo comando ottiene l'estensione VMAccess denominata ContosoTest per la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="81043-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="81043-110">Esempio 2: ottenere la visualizzazione dell'istanza dell'estensione VMAccess</span><span class="sxs-lookup"><span data-stu-id="81043-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="81043-111">Questo comando consente di ottenere la visualizzazione dell'istanza dell'estensione VMAccess denominata ContosoTest per la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="81043-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="81043-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81043-112">PARAMETERS</span></span>

### <span data-ttu-id="81043-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81043-113">-DefaultProfile</span></span>
<span data-ttu-id="81043-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81043-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81043-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="81043-115">-Name</span></span>
<span data-ttu-id="81043-116">Specifica il nome dell'estensione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81043-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="81043-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81043-117">-ResourceGroupName</span></span>
<span data-ttu-id="81043-118">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="81043-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="81043-119">-Stato</span><span class="sxs-lookup"><span data-stu-id="81043-119">-Status</span></span>
<span data-ttu-id="81043-120">Indica che questo cmdlet ottiene solo la visualizzazione istanza dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="81043-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="81043-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="81043-121">-VMName</span></span>
<span data-ttu-id="81043-122">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="81043-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="81043-123">Questo cmdlet consente di ottenere informazioni su VMAccess per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="81043-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="81043-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81043-124">CommonParameters</span></span>
<span data-ttu-id="81043-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81043-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81043-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81043-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81043-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81043-127">INPUTS</span></span>

### <span data-ttu-id="81043-128">System. String</span><span class="sxs-lookup"><span data-stu-id="81043-128">System.String</span></span>

### <span data-ttu-id="81043-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="81043-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="81043-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81043-130">OUTPUTS</span></span>

### <span data-ttu-id="81043-131">Microsoft. Azure. Commands. Compute. Models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="81043-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="81043-132">Note</span><span class="sxs-lookup"><span data-stu-id="81043-132">NOTES</span></span>

## <span data-ttu-id="81043-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81043-133">RELATED LINKS</span></span>

[<span data-ttu-id="81043-134">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="81043-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="81043-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="81043-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="81043-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="81043-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


