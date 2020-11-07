---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 6b857356ea35476117a58f8f31f7174a7a91767a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684811"
---
# <span data-ttu-id="b16f7-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b16f7-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="b16f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b16f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b16f7-103">Ottiene le impostazioni dell'estensione di diagnostica in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b16f7-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="b16f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b16f7-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b16f7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b16f7-105">DESCRIPTION</span></span>
<span data-ttu-id="b16f7-106">Il cmdlet **Get-AzVMDiagnosticsExtension** ottiene le impostazioni dell'estensione di diagnostica di Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b16f7-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="b16f7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b16f7-107">EXAMPLES</span></span>

### <span data-ttu-id="b16f7-108">Esempio 1: ottenere l'estensione di diagnostica applicata a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="b16f7-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="b16f7-109">Questo comando consente di ottenere l'estensione di diagnostica applicata alla macchina virtuale denominata ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="b16f7-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="b16f7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b16f7-110">PARAMETERS</span></span>

### <span data-ttu-id="b16f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b16f7-111">-DefaultProfile</span></span>
<span data-ttu-id="b16f7-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b16f7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b16f7-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="b16f7-113">-Name</span></span>
<span data-ttu-id="b16f7-114">Specifica il nome dell'estensione di diagnostica per cui questo cmdlet ottiene le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="b16f7-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b16f7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b16f7-115">-ResourceGroupName</span></span>
<span data-ttu-id="b16f7-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b16f7-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b16f7-117">-Stato</span><span class="sxs-lookup"><span data-stu-id="b16f7-117">-Status</span></span>
<span data-ttu-id="b16f7-118">Indica che questo cmdlet usa il valore di stato.</span><span class="sxs-lookup"><span data-stu-id="b16f7-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="b16f7-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="b16f7-119">-VMName</span></span>
<span data-ttu-id="b16f7-120">Specifica il nome della macchina virtuale da cui questo cmdlet ottiene l'estensione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="b16f7-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="b16f7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b16f7-121">CommonParameters</span></span>
<span data-ttu-id="b16f7-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b16f7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b16f7-123">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b16f7-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b16f7-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b16f7-124">INPUTS</span></span>

### <span data-ttu-id="b16f7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b16f7-125">System.String</span></span>

### <span data-ttu-id="b16f7-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b16f7-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b16f7-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b16f7-127">OUTPUTS</span></span>

### <span data-ttu-id="b16f7-128">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="b16f7-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="b16f7-129">Note</span><span class="sxs-lookup"><span data-stu-id="b16f7-129">NOTES</span></span>

## <span data-ttu-id="b16f7-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b16f7-130">RELATED LINKS</span></span>

[<span data-ttu-id="b16f7-131">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b16f7-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="b16f7-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b16f7-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


