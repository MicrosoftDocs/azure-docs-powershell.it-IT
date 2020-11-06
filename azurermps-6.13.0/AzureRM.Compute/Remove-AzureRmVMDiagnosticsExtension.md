---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: 4a14c5138a0dac983067e6deb4b1e05b88d85259
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520264"
---
# <span data-ttu-id="e5160-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e5160-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="e5160-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5160-102">SYNOPSIS</span></span>
<span data-ttu-id="e5160-103">Rimuove l'estensione di diagnostica da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e5160-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5160-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5160-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5160-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5160-105">DESCRIPTION</span></span>
<span data-ttu-id="e5160-106">Il cmdlet **Remove-AzureRmVMDiagnosticsExtension** rimuove un'estensione di diagnostica di Azure da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e5160-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="e5160-107">Per implementare le modifiche, è necessario passare l'output di questo cmdlet al cmdlet Update-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="e5160-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="e5160-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5160-108">EXAMPLES</span></span>

### <span data-ttu-id="e5160-109">Esempio 1: rimuovere l'estensione di diagnostica da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="e5160-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="e5160-110">Questo comando rimuove l'estensione di diagnostica da una macchina virtuale denominata ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="e5160-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="e5160-111">Il comando passa il risultato al cmdlet Update-AzureRmVM usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="e5160-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e5160-112">Questo comando Aggiorna la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e5160-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="e5160-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5160-113">PARAMETERS</span></span>

### <span data-ttu-id="e5160-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5160-114">-DefaultProfile</span></span>
<span data-ttu-id="e5160-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5160-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5160-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5160-116">-Name</span></span>
<span data-ttu-id="e5160-117">Specifica il nome dell'estensione di diagnostica rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5160-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e5160-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5160-118">-ResourceGroupName</span></span>
<span data-ttu-id="e5160-119">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e5160-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e5160-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="e5160-120">-VMName</span></span>
<span data-ttu-id="e5160-121">Specifica il nome della macchina virtuale da cui questo cmdlet rimuove un'estensione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="e5160-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="e5160-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5160-122">CommonParameters</span></span>
<span data-ttu-id="e5160-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5160-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5160-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5160-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5160-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5160-125">INPUTS</span></span>

### <span data-ttu-id="e5160-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e5160-126">System.String</span></span>

## <span data-ttu-id="e5160-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5160-127">OUTPUTS</span></span>

### <span data-ttu-id="e5160-128">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e5160-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e5160-129">Note</span><span class="sxs-lookup"><span data-stu-id="e5160-129">NOTES</span></span>

## <span data-ttu-id="e5160-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5160-130">RELATED LINKS</span></span>

[<span data-ttu-id="e5160-131">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e5160-131">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="e5160-132">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e5160-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="e5160-133">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e5160-133">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


