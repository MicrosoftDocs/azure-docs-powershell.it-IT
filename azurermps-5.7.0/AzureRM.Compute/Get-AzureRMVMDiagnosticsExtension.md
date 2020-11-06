---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: 32d3d5a152f36c0e4e5f8e3e4e4ecc2b8eb6ee31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515791"
---
# <span data-ttu-id="d589c-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d589c-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="d589c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d589c-102">SYNOPSIS</span></span>
<span data-ttu-id="d589c-103">Ottiene le impostazioni dell'estensione di diagnostica in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d589c-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d589c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d589c-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="d589c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d589c-105">DESCRIPTION</span></span>
<span data-ttu-id="d589c-106">Il cmdlet **Get-AzureRmVMDiagnosticsExtension** ottiene le impostazioni dell'estensione di diagnostica di Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d589c-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="d589c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d589c-107">EXAMPLES</span></span>

### <span data-ttu-id="d589c-108">Esempio 1: ottenere l'estensione di diagnostica applicata a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="d589c-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="d589c-109">Questo comando consente di ottenere l'estensione di diagnostica applicata alla macchina virtuale denominata ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="d589c-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="d589c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d589c-110">PARAMETERS</span></span>

### <span data-ttu-id="d589c-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="d589c-111">-Name</span></span>
<span data-ttu-id="d589c-112">Specifica il nome dell'estensione di diagnostica per cui questo cmdlet ottiene le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="d589c-112">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="d589c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d589c-113">-ResourceGroupName</span></span>
<span data-ttu-id="d589c-114">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d589c-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d589c-115">-Stato</span><span class="sxs-lookup"><span data-stu-id="d589c-115">-Status</span></span>
<span data-ttu-id="d589c-116">Indica che questo cmdlet usa il valore di stato.</span><span class="sxs-lookup"><span data-stu-id="d589c-116">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="d589c-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="d589c-117">-VMName</span></span>
<span data-ttu-id="d589c-118">Specifica il nome della macchina virtuale da cui questo cmdlet ottiene l'estensione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="d589c-118">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="d589c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d589c-119">CommonParameters</span></span>
<span data-ttu-id="d589c-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d589c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d589c-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d589c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d589c-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d589c-122">INPUTS</span></span>

### <span data-ttu-id="d589c-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d589c-123">None</span></span>
<span data-ttu-id="d589c-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d589c-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d589c-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d589c-125">OUTPUTS</span></span>

## <span data-ttu-id="d589c-126">Note</span><span class="sxs-lookup"><span data-stu-id="d589c-126">NOTES</span></span>

## <span data-ttu-id="d589c-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d589c-127">RELATED LINKS</span></span>

[<span data-ttu-id="d589c-128">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d589c-128">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="d589c-129">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d589c-129">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


