---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: d2027ac9778324cf1f0e39d4b5b6f5b7fe37b178
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675254"
---
# <span data-ttu-id="3238e-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3238e-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="3238e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3238e-102">SYNOPSIS</span></span>
<span data-ttu-id="3238e-103">Rimuove l'estensione di diagnostica da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3238e-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="3238e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3238e-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3238e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3238e-105">DESCRIPTION</span></span>
<span data-ttu-id="3238e-106">Il cmdlet **Remove-AzVMDiagnosticsExtension** rimuove un'estensione di diagnostica di Azure da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3238e-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="3238e-107">Per implementare le modifiche, è necessario passare l'output di questo cmdlet al cmdlet Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="3238e-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="3238e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3238e-108">EXAMPLES</span></span>

### <span data-ttu-id="3238e-109">Esempio 1: rimuovere l'estensione di diagnostica da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="3238e-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="3238e-110">Questo comando rimuove l'estensione di diagnostica da una macchina virtuale denominata ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="3238e-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="3238e-111">Il comando passa il risultato al cmdlet Update-AzVM usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="3238e-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3238e-112">Questo comando Aggiorna la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3238e-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="3238e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3238e-113">PARAMETERS</span></span>

### <span data-ttu-id="3238e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3238e-114">-DefaultProfile</span></span>
<span data-ttu-id="3238e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3238e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3238e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3238e-116">-Name</span></span>
<span data-ttu-id="3238e-117">Specifica il nome dell'estensione di diagnostica rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3238e-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3238e-118">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="3238e-118">-NoWait</span></span>
<span data-ttu-id="3238e-119">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3238e-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3238e-120">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="3238e-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3238e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3238e-121">-ResourceGroupName</span></span>
<span data-ttu-id="3238e-122">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3238e-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3238e-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="3238e-123">-VMName</span></span>
<span data-ttu-id="3238e-124">Specifica il nome della macchina virtuale da cui questo cmdlet rimuove un'estensione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="3238e-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="3238e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3238e-125">CommonParameters</span></span>
<span data-ttu-id="3238e-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3238e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3238e-127">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3238e-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3238e-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3238e-128">INPUTS</span></span>

### <span data-ttu-id="3238e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3238e-129">System.String</span></span>

## <span data-ttu-id="3238e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3238e-130">OUTPUTS</span></span>

### <span data-ttu-id="3238e-131">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3238e-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3238e-132">Note</span><span class="sxs-lookup"><span data-stu-id="3238e-132">NOTES</span></span>

## <span data-ttu-id="3238e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3238e-133">RELATED LINKS</span></span>

[<span data-ttu-id="3238e-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3238e-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="3238e-135">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3238e-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="3238e-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3238e-136">Update-AzVM</span></span>](./Update-AzVM.md)

