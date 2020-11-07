---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: 0639907999b3e84f5f609a3f0c6f1063204438ca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863774"
---
# <span data-ttu-id="aedef-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="aedef-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="aedef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aedef-102">SYNOPSIS</span></span>
<span data-ttu-id="aedef-103">Ottiene informazioni su un'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="aedef-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="aedef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aedef-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aedef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aedef-105">DESCRIPTION</span></span>
<span data-ttu-id="aedef-106">Il cmdlet **Get-AzVMCustomScriptExtension** ottiene informazioni su un'estensione di una macchina virtuale script personalizzata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="aedef-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="aedef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aedef-107">EXAMPLES</span></span>

### <span data-ttu-id="aedef-108">Esempio 1: ottenere un'estensione di script personalizzata</span><span class="sxs-lookup"><span data-stu-id="aedef-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="aedef-109">Questo comando consente di ottenere l'estensione di script personalizzata denominata ContosoCustomScript per la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="aedef-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="aedef-110">Esempio 2: ottenere la visualizzazione dell'istanza di un'estensione di script personalizzata</span><span class="sxs-lookup"><span data-stu-id="aedef-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="aedef-111">Questo comando consente di ottenere la visualizzazione dell'istanza dell'estensione di script personalizzata denominata ContosoCustomScript per la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="aedef-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="aedef-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aedef-112">PARAMETERS</span></span>

### <span data-ttu-id="aedef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aedef-113">-DefaultProfile</span></span>
<span data-ttu-id="aedef-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aedef-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aedef-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="aedef-115">-Name</span></span>
<span data-ttu-id="aedef-116">Specifica il nome dell'estensione di script personalizzata su cui questo cmdlet ottiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="aedef-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="aedef-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aedef-117">-ResourceGroupName</span></span>
<span data-ttu-id="aedef-118">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="aedef-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="aedef-119">-Stato</span><span class="sxs-lookup"><span data-stu-id="aedef-119">-Status</span></span>
<span data-ttu-id="aedef-120">Indica che questo cmdlet ottiene la visualizzazione dell'istanza dell'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="aedef-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="aedef-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="aedef-121">-VMName</span></span>
<span data-ttu-id="aedef-122">Specifica il nome di una macchina virtuale per cui questo cmdlet ottiene l'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="aedef-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="aedef-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aedef-123">CommonParameters</span></span>
<span data-ttu-id="aedef-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aedef-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aedef-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aedef-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aedef-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aedef-126">INPUTS</span></span>

### <span data-ttu-id="aedef-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="aedef-127">None</span></span>
<span data-ttu-id="aedef-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="aedef-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aedef-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aedef-129">OUTPUTS</span></span>

### <span data-ttu-id="aedef-130">Microsoft. Azure. Commands. Compute. Models. VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="aedef-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="aedef-131">Note</span><span class="sxs-lookup"><span data-stu-id="aedef-131">NOTES</span></span>

## <span data-ttu-id="aedef-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aedef-132">RELATED LINKS</span></span>

[<span data-ttu-id="aedef-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="aedef-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="aedef-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="aedef-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="aedef-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="aedef-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


