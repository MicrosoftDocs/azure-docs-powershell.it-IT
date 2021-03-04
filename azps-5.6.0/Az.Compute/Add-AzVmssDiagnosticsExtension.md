---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 93e9f660b0667286e5ce8c799b5404caae0ba0c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969565"
---
# <span data-ttu-id="b4186-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b4186-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="b4186-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4186-102">SYNOPSIS</span></span>
<span data-ttu-id="b4186-103">Aggiunge un'estensione di diagnostica al sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="b4186-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="b4186-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4186-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4186-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b4186-105">DESCRIPTION</span></span>
<span data-ttu-id="b4186-106">Il cmdlet **Add-AzVmssDiagnosticsExtension** aggiunge un'estensione di diagnostica all'istanza VMSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="b4186-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="b4186-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4186-107">EXAMPLES</span></span>

### <span data-ttu-id="b4186-108">Esempio 1: Aggiungere un'estensione di diagnostica a VMSS</span><span class="sxs-lookup"><span data-stu-id="b4186-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="b4186-109">Questo comando aggiunge un'estensione di diagnostica al sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="b4186-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="b4186-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4186-110">PARAMETERS</span></span>

### <span data-ttu-id="b4186-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b4186-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="b4186-112">Indica se questo cmdlet consente all'agente guest di Azure di aggiornare automaticamente l'estensione a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="b4186-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4186-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4186-113">-DefaultProfile</span></span>
<span data-ttu-id="b4186-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4186-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4186-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b4186-115">-Force</span></span>
<span data-ttu-id="b4186-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="b4186-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4186-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b4186-117">-Name</span></span>
<span data-ttu-id="b4186-118">Specifica il nome di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="b4186-118">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4186-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="b4186-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="b4186-120">Specifica il percorso del file di configurazione privato.</span><span class="sxs-lookup"><span data-stu-id="b4186-120">Specifies the path of the private configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4186-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="b4186-121">-SettingFilePath</span></span>
<span data-ttu-id="b4186-122">Specifica il percorso del file di configurazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="b4186-122">Specifies the path of the public configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4186-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b4186-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="b4186-124">Specifica la versione dell'estensione da usare per questo VMSS.</span><span class="sxs-lookup"><span data-stu-id="b4186-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="b4186-125">Per ottenere la versione, eseguire il cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) con un valore Microsoft.Azure.Diagnostics per il parametro *PublisherName* e IaaSDiagnostics per il parametro *Type.*</span><span class="sxs-lookup"><span data-stu-id="b4186-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4186-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b4186-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b4186-127">Specificare l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="b4186-127">Specify the VMSS object.</span></span>
<span data-ttu-id="b4186-128">È possibile usare il cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b4186-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4186-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4186-129">-Confirm</span></span>
<span data-ttu-id="b4186-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4186-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4186-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4186-131">-WhatIf</span></span>
<span data-ttu-id="b4186-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4186-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4186-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4186-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4186-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4186-134">CommonParameters</span></span>
<span data-ttu-id="b4186-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4186-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4186-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b4186-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4186-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="b4186-137">INPUTS</span></span>

### <span data-ttu-id="b4186-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b4186-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="b4186-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b4186-139">System.String</span></span>

### <span data-ttu-id="b4186-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4186-140">System.Boolean</span></span>

## <span data-ttu-id="b4186-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4186-141">OUTPUTS</span></span>

### <span data-ttu-id="b4186-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b4186-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="b4186-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="b4186-143">NOTES</span></span>

## <span data-ttu-id="b4186-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4186-144">RELATED LINKS</span></span>

[<span data-ttu-id="b4186-145">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b4186-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="b4186-146">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b4186-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="b4186-147">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b4186-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
