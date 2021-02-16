---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: e487e86c26ec09d1335ee34dab56292b564169b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199319"
---
# <span data-ttu-id="18821-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="18821-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="18821-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18821-102">SYNOPSIS</span></span>
<span data-ttu-id="18821-103">Ottiene le impostazioni dell'estensione DSC in una particolare macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18821-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="18821-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18821-104">SYNTAX</span></span>

### <span data-ttu-id="18821-105">GetDscExtension (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="18821-105">GetDscExtension (Default)</span></span>
```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18821-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="18821-106">VMParameterSet</span></span>
```
Get-AzVMDscExtension [-Status] [-VM <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18821-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="18821-107">DESCRIPTION</span></span>
<span data-ttu-id="18821-108">Il cmdlet **Get-AzVMDscExtension** ottiene le impostazioni dell'estensione DSC (Desired State Configuration) in una particolare macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18821-108">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="18821-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18821-109">EXAMPLES</span></span>

### <span data-ttu-id="18821-110">Esempio 1: Ottenere le impostazioni di un'estensione DSC</span><span class="sxs-lookup"><span data-stu-id="18821-110">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="18821-111">Questo comando ottiene le impostazioni dell'estensione DSC nella macchina virtuale denominata VM07.</span><span class="sxs-lookup"><span data-stu-id="18821-111">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="18821-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18821-112">PARAMETERS</span></span>

### <span data-ttu-id="18821-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18821-113">-DefaultProfile</span></span>
<span data-ttu-id="18821-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18821-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18821-115">-Name</span><span class="sxs-lookup"><span data-stu-id="18821-115">-Name</span></span>
<span data-ttu-id="18821-116">Specifica il nome della risorsa Gestione risorse di Azure che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="18821-116">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="18821-117">Il cmdlet Set-AzVMDscExtension imposta questo nome su Microsoft.Powershell.DSC, che è lo stesso valore usato da **Get-AzVMDscExtension.**</span><span class="sxs-lookup"><span data-stu-id="18821-117">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="18821-118">Specificare questo parametro solo se è stato modificato il nome predefinito nel cmdlet **Set-AzVMDscExtension** o se è stato usato un nome di risorsa diverso in un modello di Gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="18821-118">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="18821-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18821-119">-ResourceGroupName</span></span>
<span data-ttu-id="18821-120">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18821-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="18821-121">-Stato</span><span class="sxs-lookup"><span data-stu-id="18821-121">-Status</span></span>
<span data-ttu-id="18821-122">Indica che questo cmdlet ottiene la visualizzazione dell'istanza dell'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="18821-122">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="18821-123">-VM</span><span class="sxs-lookup"><span data-stu-id="18821-123">-VM</span></span>
<span data-ttu-id="18821-124">Specifica l'oggetto della macchina virtuale su cui è impostata l'estensione.</span><span class="sxs-lookup"><span data-stu-id="18821-124">Specifies the virtual machine object the extension is on.</span></span>

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

### <span data-ttu-id="18821-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="18821-125">-VMName</span></span>
<span data-ttu-id="18821-126">Specifica il nome di una macchina virtuale per cui questo cmdlet ottiene l'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="18821-126">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="18821-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18821-127">CommonParameters</span></span>
<span data-ttu-id="18821-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18821-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18821-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="18821-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18821-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="18821-130">INPUTS</span></span>

### <span data-ttu-id="18821-131">System.String</span><span class="sxs-lookup"><span data-stu-id="18821-131">System.String</span></span>

### <span data-ttu-id="18821-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="18821-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="18821-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18821-133">OUTPUTS</span></span>

### <span data-ttu-id="18821-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="18821-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="18821-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="18821-135">NOTES</span></span>

## <span data-ttu-id="18821-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18821-136">RELATED LINKS</span></span>

[<span data-ttu-id="18821-137">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="18821-137">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="18821-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="18821-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


