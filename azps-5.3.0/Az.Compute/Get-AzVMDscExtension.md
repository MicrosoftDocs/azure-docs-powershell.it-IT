---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: e487e86c26ec09d1335ee34dab56292b564169b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477803"
---
# <span data-ttu-id="a26b5-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="a26b5-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="a26b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a26b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a26b5-103">Ottiene le impostazioni dell'estensione DSC in una particolare macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a26b5-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="a26b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a26b5-104">SYNTAX</span></span>

### <span data-ttu-id="a26b5-105">GetDscExtension (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a26b5-105">GetDscExtension (Default)</span></span>
```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a26b5-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="a26b5-106">VMParameterSet</span></span>
```
Get-AzVMDscExtension [-Status] [-VM <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a26b5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a26b5-107">DESCRIPTION</span></span>
<span data-ttu-id="a26b5-108">Il cmdlet **Get-AzVMDscExtension** ottiene le impostazioni dell'estensione di configurazione dello stato desiderata in una determinata macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a26b5-108">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="a26b5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a26b5-109">EXAMPLES</span></span>

### <span data-ttu-id="a26b5-110">Esempio 1: ottenere le impostazioni di un'estensione DSC</span><span class="sxs-lookup"><span data-stu-id="a26b5-110">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="a26b5-111">Questo comando consente di ottenere le impostazioni di estensione denominate DSC nella macchina virtuale denominata VM07.</span><span class="sxs-lookup"><span data-stu-id="a26b5-111">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="a26b5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a26b5-112">PARAMETERS</span></span>

### <span data-ttu-id="a26b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a26b5-113">-DefaultProfile</span></span>
<span data-ttu-id="a26b5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a26b5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a26b5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a26b5-115">-Name</span></span>
<span data-ttu-id="a26b5-116">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="a26b5-116">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="a26b5-117">Il cmdlet Set-AzVMDscExtension imposta questo nome su Microsoft. PowerShell. DSC, che è lo stesso valore usato da **Get-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="a26b5-117">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="a26b5-118">Specifica questo parametro solo se il nome predefinito è stato modificato nel cmdlet **set-AzVMDscExtension** o si usa un nome di risorsa diverso in un modello di gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="a26b5-118">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a26b5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a26b5-119">-ResourceGroupName</span></span>
<span data-ttu-id="a26b5-120">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a26b5-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a26b5-121">-Stato</span><span class="sxs-lookup"><span data-stu-id="a26b5-121">-Status</span></span>
<span data-ttu-id="a26b5-122">Indica che questo cmdlet ottiene la visualizzazione dell'istanza dell'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="a26b5-122">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a26b5-123">-VM</span><span class="sxs-lookup"><span data-stu-id="a26b5-123">-VM</span></span>
<span data-ttu-id="a26b5-124">Specifica l'oggetto macchina virtuale in cui è attiva l'estensione.</span><span class="sxs-lookup"><span data-stu-id="a26b5-124">Specifies the virtual machine object the extension is on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a26b5-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="a26b5-125">-VMName</span></span>
<span data-ttu-id="a26b5-126">Specifica il nome di una macchina virtuale per cui questo cmdlet ottiene l'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="a26b5-126">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a26b5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a26b5-127">CommonParameters</span></span>
<span data-ttu-id="a26b5-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a26b5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a26b5-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a26b5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a26b5-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a26b5-130">INPUTS</span></span>

### <span data-ttu-id="a26b5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a26b5-131">System.String</span></span>

### <span data-ttu-id="a26b5-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a26b5-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a26b5-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a26b5-133">OUTPUTS</span></span>

### <span data-ttu-id="a26b5-134">Microsoft. Azure. Commands. Compute. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="a26b5-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="a26b5-135">Note</span><span class="sxs-lookup"><span data-stu-id="a26b5-135">NOTES</span></span>

## <span data-ttu-id="a26b5-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a26b5-136">RELATED LINKS</span></span>

[<span data-ttu-id="a26b5-137">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="a26b5-137">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="a26b5-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="a26b5-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


