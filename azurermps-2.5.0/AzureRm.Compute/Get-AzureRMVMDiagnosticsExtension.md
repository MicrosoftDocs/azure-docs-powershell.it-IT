---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: e02c86407326d9ea5b12a5a589e5860c9dfb5c19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867158"
---
# <span data-ttu-id="d9969-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d9969-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="d9969-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9969-102">SYNOPSIS</span></span>
<span data-ttu-id="d9969-103">Ottiene le impostazioni dell'estensione di diagnostica in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9969-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9969-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9969-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9969-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9969-105">DESCRIPTION</span></span>
<span data-ttu-id="d9969-106">Il cmdlet **Get-AzureRmVMDiagnosticsExtension** ottiene le impostazioni dell'estensione di diagnostica di Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9969-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="d9969-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9969-107">EXAMPLES</span></span>

### <span data-ttu-id="d9969-108">Esempio 1: ottenere l'estensione di diagnostica applicata a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="d9969-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="d9969-109">Questo comando consente di ottenere l'estensione di diagnostica applicata alla macchina virtuale denominata ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="d9969-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="d9969-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9969-110">PARAMETERS</span></span>

### <span data-ttu-id="d9969-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9969-111">-DefaultProfile</span></span>
<span data-ttu-id="d9969-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9969-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9969-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9969-113">-Name</span></span>
<span data-ttu-id="d9969-114">Specifica il nome dell'estensione di diagnostica per cui questo cmdlet ottiene le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="d9969-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="d9969-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9969-115">-ResourceGroupName</span></span>
<span data-ttu-id="d9969-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9969-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d9969-117">-Stato</span><span class="sxs-lookup"><span data-stu-id="d9969-117">-Status</span></span>
<span data-ttu-id="d9969-118">Indica che questo cmdlet usa il valore di stato.</span><span class="sxs-lookup"><span data-stu-id="d9969-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="d9969-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="d9969-119">-VMName</span></span>
<span data-ttu-id="d9969-120">Specifica il nome della macchina virtuale da cui questo cmdlet ottiene l'estensione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="d9969-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="d9969-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9969-121">CommonParameters</span></span>
<span data-ttu-id="d9969-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9969-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9969-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9969-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9969-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9969-124">INPUTS</span></span>

### <span data-ttu-id="d9969-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d9969-125">None</span></span>
<span data-ttu-id="d9969-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d9969-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9969-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9969-127">OUTPUTS</span></span>

### <span data-ttu-id="d9969-128">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d9969-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="d9969-129">Note</span><span class="sxs-lookup"><span data-stu-id="d9969-129">NOTES</span></span>

## <span data-ttu-id="d9969-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9969-130">RELATED LINKS</span></span>

[<span data-ttu-id="d9969-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d9969-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="d9969-132">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d9969-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


