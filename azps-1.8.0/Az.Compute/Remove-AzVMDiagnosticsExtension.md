---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bcfc7f3d80c5601d5797d9af2958d2bed6395fbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93851990"
---
# <span data-ttu-id="587f0-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="587f0-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="587f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="587f0-102">SYNOPSIS</span></span>
<span data-ttu-id="587f0-103">Rimuove l'estensione di diagnostica da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="587f0-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="587f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="587f0-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="587f0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="587f0-105">DESCRIPTION</span></span>
<span data-ttu-id="587f0-106">Il cmdlet **Remove-AzVMDiagnosticsExtension** rimuove un'estensione di diagnostica di Azure da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="587f0-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="587f0-107">Per implementare le modifiche, è necessario passare l'output di questo cmdlet al cmdlet Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="587f0-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="587f0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="587f0-108">EXAMPLES</span></span>

### <span data-ttu-id="587f0-109">Esempio 1: rimuovere l'estensione di diagnostica da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="587f0-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="587f0-110">Questo comando rimuove l'estensione di diagnostica da una macchina virtuale denominata ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="587f0-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="587f0-111">Il comando passa il risultato al cmdlet Update-AzVM usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="587f0-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="587f0-112">Questo comando Aggiorna la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="587f0-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="587f0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="587f0-113">PARAMETERS</span></span>

### <span data-ttu-id="587f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="587f0-114">-DefaultProfile</span></span>
<span data-ttu-id="587f0-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="587f0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="587f0-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="587f0-116">-Name</span></span>
<span data-ttu-id="587f0-117">Specifica il nome dell'estensione di diagnostica rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="587f0-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="587f0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="587f0-118">-ResourceGroupName</span></span>
<span data-ttu-id="587f0-119">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="587f0-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="587f0-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="587f0-120">-VMName</span></span>
<span data-ttu-id="587f0-121">Specifica il nome della macchina virtuale da cui questo cmdlet rimuove un'estensione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="587f0-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="587f0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="587f0-122">CommonParameters</span></span>
<span data-ttu-id="587f0-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="587f0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="587f0-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="587f0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="587f0-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="587f0-125">INPUTS</span></span>

### <span data-ttu-id="587f0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="587f0-126">System.String</span></span>

## <span data-ttu-id="587f0-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="587f0-127">OUTPUTS</span></span>

### <span data-ttu-id="587f0-128">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="587f0-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="587f0-129">Note</span><span class="sxs-lookup"><span data-stu-id="587f0-129">NOTES</span></span>

## <span data-ttu-id="587f0-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="587f0-130">RELATED LINKS</span></span>

[<span data-ttu-id="587f0-131">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="587f0-131">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="587f0-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="587f0-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="587f0-133">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="587f0-133">Update-AzVM</span></span>](./Update-AzVM.md)


