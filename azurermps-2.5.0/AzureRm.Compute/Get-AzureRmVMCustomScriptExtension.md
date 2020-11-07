---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: b6ce3afb8b280b9ca07746979f0bb5ba425afd82
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867154"
---
# <span data-ttu-id="0e241-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="0e241-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="0e241-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0e241-102">SYNOPSIS</span></span>
<span data-ttu-id="0e241-103">Ottiene informazioni su un'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0e241-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e241-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e241-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e241-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e241-105">DESCRIPTION</span></span>
<span data-ttu-id="0e241-106">Il cmdlet **Get-AzureRmVMCustomScriptExtension** ottiene informazioni su un'estensione di una macchina virtuale script personalizzata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0e241-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="0e241-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e241-107">EXAMPLES</span></span>

### <span data-ttu-id="0e241-108">Esempio 1: ottenere un'estensione di script personalizzata</span><span class="sxs-lookup"><span data-stu-id="0e241-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="0e241-109">Questo comando consente di ottenere l'estensione di script personalizzata denominata ContosoCustomScript per la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="0e241-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="0e241-110">Esempio 2: ottenere la visualizzazione dell'istanza di un'estensione di script personalizzata</span><span class="sxs-lookup"><span data-stu-id="0e241-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="0e241-111">Questo comando consente di ottenere la visualizzazione dell'istanza dell'estensione di script personalizzata denominata ContosoCustomScript per la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="0e241-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="0e241-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0e241-112">PARAMETERS</span></span>

### <span data-ttu-id="0e241-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e241-113">-DefaultProfile</span></span>
<span data-ttu-id="0e241-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0e241-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e241-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e241-115">-Name</span></span>
<span data-ttu-id="0e241-116">Specifica il nome dell'estensione di script personalizzata su cui questo cmdlet ottiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="0e241-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e241-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e241-117">-ResourceGroupName</span></span>
<span data-ttu-id="0e241-118">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0e241-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0e241-119">-Stato</span><span class="sxs-lookup"><span data-stu-id="0e241-119">-Status</span></span>
<span data-ttu-id="0e241-120">Indica che questo cmdlet ottiene la visualizzazione dell'istanza dell'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0e241-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="0e241-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="0e241-121">-VMName</span></span>
<span data-ttu-id="0e241-122">Specifica il nome di una macchina virtuale per cui questo cmdlet ottiene l'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0e241-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="0e241-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e241-123">CommonParameters</span></span>
<span data-ttu-id="0e241-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e241-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e241-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e241-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e241-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0e241-126">INPUTS</span></span>

### <span data-ttu-id="0e241-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0e241-127">None</span></span>
<span data-ttu-id="0e241-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0e241-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0e241-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e241-129">OUTPUTS</span></span>

### <span data-ttu-id="0e241-130">Microsoft. Azure. Commands. Compute. Models. VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="0e241-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="0e241-131">Note</span><span class="sxs-lookup"><span data-stu-id="0e241-131">NOTES</span></span>

## <span data-ttu-id="0e241-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e241-132">RELATED LINKS</span></span>

[<span data-ttu-id="0e241-133">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="0e241-133">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="0e241-134">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="0e241-134">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="0e241-135">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="0e241-135">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


