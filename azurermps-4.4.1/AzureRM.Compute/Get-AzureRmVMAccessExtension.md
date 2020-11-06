---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: f5ba6ede0b57d2480a892efd47ed71aacd9fe553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522164"
---
# <span data-ttu-id="d898d-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d898d-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="d898d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d898d-102">SYNOPSIS</span></span>
<span data-ttu-id="d898d-103">Ottiene informazioni sull'estensione VMAccess.</span><span class="sxs-lookup"><span data-stu-id="d898d-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d898d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d898d-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d898d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d898d-105">DESCRIPTION</span></span>
<span data-ttu-id="d898d-106">Il cmdlet **Get-AzureRmVMAccessExtension** ottiene informazioni sull'estensione della macchina virtuale VMAccess (Virtual Machine Access).</span><span class="sxs-lookup"><span data-stu-id="d898d-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="d898d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d898d-107">EXAMPLES</span></span>

### <span data-ttu-id="d898d-108">Esempio 1: ottenere l'estensione VMAccess</span><span class="sxs-lookup"><span data-stu-id="d898d-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="d898d-109">Questo comando ottiene l'estensione VMAccess denominata ContosoTest per la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="d898d-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="d898d-110">Esempio 2: ottenere la visualizzazione dell'istanza dell'estensione VMAccess</span><span class="sxs-lookup"><span data-stu-id="d898d-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="d898d-111">Questo comando consente di ottenere la visualizzazione dell'istanza dell'estensione VMAccess denominata ContosoTest per la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="d898d-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="d898d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d898d-112">PARAMETERS</span></span>

### <span data-ttu-id="d898d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d898d-113">-DefaultProfile</span></span>
<span data-ttu-id="d898d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d898d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d898d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d898d-115">-Name</span></span>
<span data-ttu-id="d898d-116">Specifica il nome dell'estensione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d898d-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d898d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d898d-117">-ResourceGroupName</span></span>
<span data-ttu-id="d898d-118">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d898d-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d898d-119">-Stato</span><span class="sxs-lookup"><span data-stu-id="d898d-119">-Status</span></span>
<span data-ttu-id="d898d-120">Indica che questo cmdlet ottiene solo la visualizzazione istanza dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="d898d-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="d898d-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="d898d-121">-VMName</span></span>
<span data-ttu-id="d898d-122">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d898d-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d898d-123">Questo cmdlet consente di ottenere informazioni su VMAccess per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d898d-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d898d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d898d-124">CommonParameters</span></span>
<span data-ttu-id="d898d-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d898d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d898d-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d898d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d898d-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d898d-127">INPUTS</span></span>

## <span data-ttu-id="d898d-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d898d-128">OUTPUTS</span></span>

## <span data-ttu-id="d898d-129">Note</span><span class="sxs-lookup"><span data-stu-id="d898d-129">NOTES</span></span>

## <span data-ttu-id="d898d-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d898d-130">RELATED LINKS</span></span>

[<span data-ttu-id="d898d-131">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d898d-131">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="d898d-132">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d898d-132">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="d898d-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="d898d-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


