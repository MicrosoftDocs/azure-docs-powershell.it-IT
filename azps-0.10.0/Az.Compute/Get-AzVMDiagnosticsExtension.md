---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 9137b62098a1441cea8acc53c52c0e0ea835ff09
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863773"
---
# <span data-ttu-id="a255f-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a255f-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="a255f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a255f-102">SYNOPSIS</span></span>
<span data-ttu-id="a255f-103">Ottiene le impostazioni dell'estensione di diagnostica in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a255f-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="a255f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a255f-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a255f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a255f-105">DESCRIPTION</span></span>
<span data-ttu-id="a255f-106">Il cmdlet **Get-AzVMDiagnosticsExtension** ottiene le impostazioni dell'estensione di diagnostica di Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a255f-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="a255f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a255f-107">EXAMPLES</span></span>

### <span data-ttu-id="a255f-108">Esempio 1: ottenere l'estensione di diagnostica applicata a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="a255f-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="a255f-109">Questo comando consente di ottenere l'estensione di diagnostica applicata alla macchina virtuale denominata ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="a255f-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="a255f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a255f-110">PARAMETERS</span></span>

### <span data-ttu-id="a255f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a255f-111">-DefaultProfile</span></span>
<span data-ttu-id="a255f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a255f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a255f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a255f-113">-Name</span></span>
<span data-ttu-id="a255f-114">Specifica il nome dell'estensione di diagnostica per cui questo cmdlet ottiene le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="a255f-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="a255f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a255f-115">-ResourceGroupName</span></span>
<span data-ttu-id="a255f-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a255f-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a255f-117">-Stato</span><span class="sxs-lookup"><span data-stu-id="a255f-117">-Status</span></span>
<span data-ttu-id="a255f-118">Indica che questo cmdlet usa il valore di stato.</span><span class="sxs-lookup"><span data-stu-id="a255f-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="a255f-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="a255f-119">-VMName</span></span>
<span data-ttu-id="a255f-120">Specifica il nome della macchina virtuale da cui questo cmdlet ottiene l'estensione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="a255f-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="a255f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a255f-121">CommonParameters</span></span>
<span data-ttu-id="a255f-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a255f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a255f-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a255f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a255f-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a255f-124">INPUTS</span></span>

### <span data-ttu-id="a255f-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a255f-125">None</span></span>
<span data-ttu-id="a255f-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a255f-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a255f-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a255f-127">OUTPUTS</span></span>

### <span data-ttu-id="a255f-128">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="a255f-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="a255f-129">Note</span><span class="sxs-lookup"><span data-stu-id="a255f-129">NOTES</span></span>

## <span data-ttu-id="a255f-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a255f-130">RELATED LINKS</span></span>

[<span data-ttu-id="a255f-131">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a255f-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="a255f-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a255f-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


