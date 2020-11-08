---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: a0c2b1dbad943a690ae2965a9ea9520063909b9c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193692"
---
# <span data-ttu-id="63eab-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="63eab-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="63eab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63eab-102">SYNOPSIS</span></span>
<span data-ttu-id="63eab-103">Aggiunge un'estensione di diagnostica a VMSS.</span><span class="sxs-lookup"><span data-stu-id="63eab-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="63eab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63eab-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63eab-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63eab-105">DESCRIPTION</span></span>
<span data-ttu-id="63eab-106">Il cmdlet **Add-AzVmssDiagnosticsExtension** aggiunge un'estensione di diagnostica all'istanza di Virtual Machine scale set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="63eab-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="63eab-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63eab-107">EXAMPLES</span></span>

### <span data-ttu-id="63eab-108">Esempio 1: aggiungere un'estensione di diagnostica a VMSS</span><span class="sxs-lookup"><span data-stu-id="63eab-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="63eab-109">Questo comando aggiunge un'estensione di diagnostica a VMSS.</span><span class="sxs-lookup"><span data-stu-id="63eab-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="63eab-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63eab-110">PARAMETERS</span></span>

### <span data-ttu-id="63eab-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="63eab-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="63eab-112">Indica se questo cmdlet consente all'agente guest Azure di aggiornare automaticamente l'estensione a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="63eab-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="63eab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63eab-113">-DefaultProfile</span></span>
<span data-ttu-id="63eab-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="63eab-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63eab-115">-Force</span><span class="sxs-lookup"><span data-stu-id="63eab-115">-Force</span></span>
<span data-ttu-id="63eab-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="63eab-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="63eab-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="63eab-117">-Name</span></span>
<span data-ttu-id="63eab-118">Specifica il nome di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="63eab-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="63eab-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="63eab-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="63eab-120">Specifica il percorso del file di configurazione privato.</span><span class="sxs-lookup"><span data-stu-id="63eab-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="63eab-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="63eab-121">-SettingFilePath</span></span>
<span data-ttu-id="63eab-122">Specifica il percorso del file di configurazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="63eab-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="63eab-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="63eab-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="63eab-124">Specifica la versione dell'estensione da usare per questo VMSS.</span><span class="sxs-lookup"><span data-stu-id="63eab-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="63eab-125">Per ottenere la versione, eseguire il cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) con un valore di Microsoft. Azure. Diagnostics per il parametro *PublisherName* e IaaSDiagnostics per il parametro *Type* .</span><span class="sxs-lookup"><span data-stu-id="63eab-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="63eab-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="63eab-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="63eab-127">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="63eab-127">Specify the VMSS object.</span></span>
<span data-ttu-id="63eab-128">Puoi usare il cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="63eab-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="63eab-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="63eab-129">-Confirm</span></span>
<span data-ttu-id="63eab-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63eab-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63eab-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63eab-131">-WhatIf</span></span>
<span data-ttu-id="63eab-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63eab-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63eab-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63eab-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63eab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63eab-134">CommonParameters</span></span>
<span data-ttu-id="63eab-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63eab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63eab-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63eab-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63eab-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63eab-137">INPUTS</span></span>

### <span data-ttu-id="63eab-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="63eab-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="63eab-139">System. String</span><span class="sxs-lookup"><span data-stu-id="63eab-139">System.String</span></span>

### <span data-ttu-id="63eab-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="63eab-140">System.Boolean</span></span>

## <span data-ttu-id="63eab-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63eab-141">OUTPUTS</span></span>

### <span data-ttu-id="63eab-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="63eab-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="63eab-143">Note</span><span class="sxs-lookup"><span data-stu-id="63eab-143">NOTES</span></span>

## <span data-ttu-id="63eab-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63eab-144">RELATED LINKS</span></span>

[<span data-ttu-id="63eab-145">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="63eab-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="63eab-146">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="63eab-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="63eab-147">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="63eab-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)