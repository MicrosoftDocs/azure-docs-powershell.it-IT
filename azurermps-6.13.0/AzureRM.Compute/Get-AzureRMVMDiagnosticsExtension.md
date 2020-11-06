---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: fbc357decbf4bdcd2e378294fed43125d38fd873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511907"
---
# <span data-ttu-id="755ee-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="755ee-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="755ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="755ee-102">SYNOPSIS</span></span>
<span data-ttu-id="755ee-103">Ottiene le impostazioni dell'estensione di diagnostica in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="755ee-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="755ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="755ee-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="755ee-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="755ee-105">DESCRIPTION</span></span>
<span data-ttu-id="755ee-106">Il cmdlet **Get-AzureRmVMDiagnosticsExtension** ottiene le impostazioni dell'estensione di diagnostica di Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="755ee-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="755ee-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="755ee-107">EXAMPLES</span></span>

### <span data-ttu-id="755ee-108">Esempio 1: ottenere l'estensione di diagnostica applicata a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="755ee-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="755ee-109">Questo comando consente di ottenere l'estensione di diagnostica applicata alla macchina virtuale denominata ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="755ee-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="755ee-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="755ee-110">PARAMETERS</span></span>

### <span data-ttu-id="755ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="755ee-111">-DefaultProfile</span></span>
<span data-ttu-id="755ee-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="755ee-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="755ee-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="755ee-113">-Name</span></span>
<span data-ttu-id="755ee-114">Specifica il nome dell'estensione di diagnostica per cui questo cmdlet ottiene le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="755ee-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="755ee-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="755ee-115">-ResourceGroupName</span></span>
<span data-ttu-id="755ee-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="755ee-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="755ee-117">-Stato</span><span class="sxs-lookup"><span data-stu-id="755ee-117">-Status</span></span>
<span data-ttu-id="755ee-118">Indica che questo cmdlet usa il valore di stato.</span><span class="sxs-lookup"><span data-stu-id="755ee-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="755ee-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="755ee-119">-VMName</span></span>
<span data-ttu-id="755ee-120">Specifica il nome della macchina virtuale da cui questo cmdlet ottiene l'estensione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="755ee-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="755ee-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755ee-121">CommonParameters</span></span>
<span data-ttu-id="755ee-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="755ee-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755ee-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="755ee-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755ee-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="755ee-124">INPUTS</span></span>

### <span data-ttu-id="755ee-125">System. String</span><span class="sxs-lookup"><span data-stu-id="755ee-125">System.String</span></span>

### <span data-ttu-id="755ee-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="755ee-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="755ee-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="755ee-127">OUTPUTS</span></span>

### <span data-ttu-id="755ee-128">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="755ee-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="755ee-129">Note</span><span class="sxs-lookup"><span data-stu-id="755ee-129">NOTES</span></span>

## <span data-ttu-id="755ee-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="755ee-130">RELATED LINKS</span></span>

[<span data-ttu-id="755ee-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="755ee-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="755ee-132">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="755ee-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


