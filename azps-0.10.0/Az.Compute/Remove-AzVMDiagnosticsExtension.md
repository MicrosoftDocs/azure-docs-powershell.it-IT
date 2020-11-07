---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bec83334032b3d0e18c017bc24d19d381a765176
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863530"
---
# <span data-ttu-id="bcb68-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bcb68-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="bcb68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bcb68-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb68-103">Rimuove l'estensione di diagnostica da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bcb68-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="bcb68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcb68-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcb68-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcb68-105">DESCRIPTION</span></span>
<span data-ttu-id="bcb68-106">Il cmdlet **Remove-AzVMDiagnosticsExtension** rimuove un'estensione di diagnostica di Azure da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bcb68-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="bcb68-107">Per implementare le modifiche, è necessario passare l'output di questo cmdlet al cmdlet Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="bcb68-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="bcb68-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcb68-108">EXAMPLES</span></span>

### <span data-ttu-id="bcb68-109">Esempio 1: rimuovere l'estensione di diagnostica da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="bcb68-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="bcb68-110">Questo comando rimuove l'estensione di diagnostica da una macchina virtuale denominata ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="bcb68-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="bcb68-111">Il comando passa il risultato al cmdlet Update-AzVM usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="bcb68-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bcb68-112">Questo comando Aggiorna la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bcb68-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="bcb68-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcb68-113">PARAMETERS</span></span>

### <span data-ttu-id="bcb68-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb68-114">-DefaultProfile</span></span>
<span data-ttu-id="bcb68-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb68-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcb68-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="bcb68-116">-Name</span></span>
<span data-ttu-id="bcb68-117">Specifica il nome dell'estensione di diagnostica rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcb68-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb68-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcb68-118">-ResourceGroupName</span></span>
<span data-ttu-id="bcb68-119">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bcb68-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bcb68-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="bcb68-120">-VMName</span></span>
<span data-ttu-id="bcb68-121">Specifica il nome della macchina virtuale da cui questo cmdlet rimuove un'estensione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="bcb68-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="bcb68-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb68-122">CommonParameters</span></span>
<span data-ttu-id="bcb68-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcb68-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb68-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcb68-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb68-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bcb68-125">INPUTS</span></span>

### <span data-ttu-id="bcb68-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bcb68-126">None</span></span>
<span data-ttu-id="bcb68-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="bcb68-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bcb68-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcb68-128">OUTPUTS</span></span>

### <span data-ttu-id="bcb68-129">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bcb68-129">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bcb68-130">Note</span><span class="sxs-lookup"><span data-stu-id="bcb68-130">NOTES</span></span>

## <span data-ttu-id="bcb68-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcb68-131">RELATED LINKS</span></span>

[<span data-ttu-id="bcb68-132">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bcb68-132">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="bcb68-133">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bcb68-133">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="bcb68-134">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="bcb68-134">Update-AzVM</span></span>](./Update-AzVM.md)


