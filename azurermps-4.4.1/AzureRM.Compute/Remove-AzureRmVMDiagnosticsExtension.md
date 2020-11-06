---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: 6a47e5a248c5de3c2dd87af67393f60d215e44c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508695"
---
# <span data-ttu-id="7237b-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7237b-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="7237b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7237b-102">SYNOPSIS</span></span>
<span data-ttu-id="7237b-103">Rimuove l'estensione di diagnostica da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7237b-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7237b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7237b-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7237b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7237b-105">DESCRIPTION</span></span>
<span data-ttu-id="7237b-106">Il cmdlet **Remove-AzureRmVMDiagnosticsExtension** rimuove un'estensione di diagnostica di Azure da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7237b-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="7237b-107">Per implementare le modifiche, è necessario passare l'output di questo cmdlet al cmdlet Update-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="7237b-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="7237b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7237b-108">EXAMPLES</span></span>

### <span data-ttu-id="7237b-109">Esempio 1: rimuovere l'estensione di diagnostica da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="7237b-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="7237b-110">Questo comando rimuove l'estensione di diagnostica da una macchina virtuale denominata ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="7237b-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="7237b-111">Il comando passa il risultato al cmdlet Update-AzureRmVM usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="7237b-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7237b-112">Questo comando Aggiorna la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7237b-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="7237b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7237b-113">PARAMETERS</span></span>

### <span data-ttu-id="7237b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7237b-114">-DefaultProfile</span></span>
<span data-ttu-id="7237b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7237b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7237b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7237b-116">-Name</span></span>
<span data-ttu-id="7237b-117">Specifica il nome dell'estensione di diagnostica rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7237b-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7237b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7237b-118">-ResourceGroupName</span></span>
<span data-ttu-id="7237b-119">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7237b-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7237b-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="7237b-120">-VMName</span></span>
<span data-ttu-id="7237b-121">Specifica il nome della macchina virtuale da cui questo cmdlet rimuove un'estensione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="7237b-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="7237b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7237b-122">CommonParameters</span></span>
<span data-ttu-id="7237b-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7237b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7237b-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7237b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7237b-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7237b-125">INPUTS</span></span>

## <span data-ttu-id="7237b-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7237b-126">OUTPUTS</span></span>

## <span data-ttu-id="7237b-127">Note</span><span class="sxs-lookup"><span data-stu-id="7237b-127">NOTES</span></span>

## <span data-ttu-id="7237b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7237b-128">RELATED LINKS</span></span>

[<span data-ttu-id="7237b-129">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7237b-129">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="7237b-130">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7237b-130">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="7237b-131">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7237b-131">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


