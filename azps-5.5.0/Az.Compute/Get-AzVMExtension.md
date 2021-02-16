---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: ca9693f715d72366a6cc78030d0a8328bf0abc50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204906"
---
# <span data-ttu-id="0334a-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0334a-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="0334a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0334a-102">SYNOPSIS</span></span>
<span data-ttu-id="0334a-103">Ottiene le proprietà di Virtual Machine Extensions installate in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0334a-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="0334a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0334a-104">SYNTAX</span></span>

### <span data-ttu-id="0334a-105">GetExtensionParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0334a-105">GetExtensionParameterSet (Default)</span></span>
```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0334a-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="0334a-106">VMParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-VMObject <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0334a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0334a-107">ResourceIdParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-ResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0334a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0334a-108">DESCRIPTION</span></span>
<span data-ttu-id="0334a-109">Il cmdlet **Get-AzVMExtension** ottiene le proprietà delle estensioni delle macchine virtuali installate in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0334a-109">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="0334a-110">Specificare il nome di un'estensione per cui ottenere le proprietà.</span><span class="sxs-lookup"><span data-stu-id="0334a-110">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="0334a-111">Per ottenere solo la visualizzazione dell'istanza di un'estensione, specificare il parametro Status.</span><span class="sxs-lookup"><span data-stu-id="0334a-111">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="0334a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0334a-112">EXAMPLES</span></span>

### <span data-ttu-id="0334a-113">Esempio 1: Ottenere le proprietà di un'estensione</span><span class="sxs-lookup"><span data-stu-id="0334a-113">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="0334a-114">Questo comando recupera le proprietà per l'estensione denominata CustomScriptExtension nella macchina virtuale denominata VirtualMachine22 nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0334a-114">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="0334a-115">Esempio 2: Ottenere la visualizzazione istanza di un'estensione</span><span class="sxs-lookup"><span data-stu-id="0334a-115">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                : {Microsoft.Azure.Management.Compute.Models.InstanceViewStatus}
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="0334a-116">Questo comando ottiene la visualizzazione dell'istanza per l'estensione CustomScriptExtension nella macchina virtuale denominata VirtualMachine22 nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0334a-116">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="0334a-117">Esempio 3: Ottenere tutte le estensioni installate in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="0334a-117">Example 3: Get all extensions installed on a VM</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

### <span data-ttu-id="0334a-118">Esempio 4: Ottenere le proprietà di un'estensione usando il parametro della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="0334a-118">Example 4: Get properties of an extension using the VM parameter</span></span>
```
PS C:\> $vm = Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine22"
PS C:\> Get-AzVMExtension -VM $vm

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="0334a-119">Questo comando recupera l'elenco delle estensioni installate nella macchina virtuale denominata VirtualMachine22 nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0334a-119">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="0334a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0334a-120">PARAMETERS</span></span>

### <span data-ttu-id="0334a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0334a-121">-DefaultProfile</span></span>
<span data-ttu-id="0334a-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0334a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0334a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0334a-123">-Name</span></span>
<span data-ttu-id="0334a-124">Specifica il nome di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="0334a-124">Specifies the name of an extension.</span></span>
<span data-ttu-id="0334a-125">Questo cmdlet ottiene le proprietà per l'estensione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0334a-125">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0334a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0334a-126">-ResourceGroupName</span></span>
<span data-ttu-id="0334a-127">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0334a-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0334a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0334a-128">-ResourceId</span></span>
<span data-ttu-id="0334a-129">ID risorsa che specifica l'oggetto della macchina virtuale su cui è impostata l'estensione.</span><span class="sxs-lookup"><span data-stu-id="0334a-129">Resource Id specifying the virtual machine object the extension is on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0334a-130">-Stato</span><span class="sxs-lookup"><span data-stu-id="0334a-130">-Status</span></span>
<span data-ttu-id="0334a-131">Indica che questo cmdlet ottiene solo la visualizzazione dell'istanza di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="0334a-131">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="0334a-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="0334a-132">-VMName</span></span>
<span data-ttu-id="0334a-133">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0334a-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0334a-134">Questo cmdlet recupera le proprietà di un'estensione dalla macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0334a-134">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0334a-135">-VMObject</span><span class="sxs-lookup"><span data-stu-id="0334a-135">-VMObject</span></span>
<span data-ttu-id="0334a-136">Specifica l'oggetto della macchina virtuale su cui è impostata l'estensione.</span><span class="sxs-lookup"><span data-stu-id="0334a-136">Specifies the virtual machine object the extension is on.</span></span>

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

### <span data-ttu-id="0334a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0334a-137">CommonParameters</span></span>
<span data-ttu-id="0334a-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0334a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0334a-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0334a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0334a-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="0334a-140">INPUTS</span></span>

### <span data-ttu-id="0334a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0334a-141">System.String</span></span>

### <span data-ttu-id="0334a-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0334a-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0334a-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0334a-143">OUTPUTS</span></span>

### <span data-ttu-id="0334a-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="0334a-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="0334a-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="0334a-145">NOTES</span></span>

## <span data-ttu-id="0334a-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0334a-146">RELATED LINKS</span></span>

[<span data-ttu-id="0334a-147">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0334a-147">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="0334a-148">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0334a-148">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


