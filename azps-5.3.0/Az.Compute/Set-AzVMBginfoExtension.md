---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: a98a2f5cbc8034e8cec4d324bb7ecaa28297e772
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477664"
---
# <span data-ttu-id="7e95c-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="7e95c-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="7e95c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e95c-102">SYNOPSIS</span></span>
<span data-ttu-id="7e95c-103">Aggiunge l'estensione BGInfo a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e95c-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="7e95c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e95c-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e95c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e95c-105">DESCRIPTION</span></span>
<span data-ttu-id="7e95c-106">Il cmdlet **set-AzVMBGInfoExtension** aggiunge l'estensione BGInfo a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e95c-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="7e95c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e95c-107">EXAMPLES</span></span>

### <span data-ttu-id="7e95c-108">Esempio 1: aggiungere l'estensione BGInfo per una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="7e95c-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="7e95c-109">Questo comando aggiunge l'estensione BGInfo alla macchina virtuale denominata ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="7e95c-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="7e95c-110">Il comando specifica il gruppo di risorse e la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e95c-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="7e95c-111">Il comando specifica il nome e la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="7e95c-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="7e95c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e95c-112">PARAMETERS</span></span>

### <span data-ttu-id="7e95c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e95c-113">-DefaultProfile</span></span>
<span data-ttu-id="7e95c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e95c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e95c-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="7e95c-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="7e95c-116">Indica che questo cmdlet impedisce all'agente guest Azure di aggiornare automaticamente l'estensione a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="7e95c-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="7e95c-117">Per impostazione predefinita, questo cmdlet consente all'agente guest di aggiornare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="7e95c-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="7e95c-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="7e95c-118">-ForceRerun</span></span>
<span data-ttu-id="7e95c-119">Specifica che l'estensione deve essere eseguita di nuovo con le stesse impostazioni pubbliche o protette.</span><span class="sxs-lookup"><span data-stu-id="7e95c-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="7e95c-120">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="7e95c-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="7e95c-121">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="7e95c-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e95c-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7e95c-122">-Location</span></span>
<span data-ttu-id="7e95c-123">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e95c-123">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e95c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e95c-124">-Name</span></span>
<span data-ttu-id="7e95c-125">Specifica il nome dell'estensione BGInfo che questo cmdlet aggiunge a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e95c-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e95c-126">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="7e95c-126">-NoWait</span></span>
<span data-ttu-id="7e95c-127">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7e95c-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="7e95c-128">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="7e95c-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="7e95c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e95c-129">-ResourceGroupName</span></span>
<span data-ttu-id="7e95c-130">Specifica il nome del gruppo di risorse della macchina virtuale a cui questo cmdlet aggiunge un'estensione.</span><span class="sxs-lookup"><span data-stu-id="7e95c-130">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="7e95c-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="7e95c-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="7e95c-132">Specifica la versione dell'estensione aggiunta da questo cmdlet alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e95c-132">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e95c-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="7e95c-133">-VMName</span></span>
<span data-ttu-id="7e95c-134">Specifica il nome della macchina virtuale a cui questo cmdlet aggiunge l'estensione BGInfo.</span><span class="sxs-lookup"><span data-stu-id="7e95c-134">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="7e95c-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7e95c-135">-Confirm</span></span>
<span data-ttu-id="7e95c-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e95c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e95c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e95c-137">-WhatIf</span></span>
<span data-ttu-id="7e95c-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e95c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e95c-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e95c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e95c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e95c-140">CommonParameters</span></span>
<span data-ttu-id="7e95c-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e95c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e95c-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e95c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e95c-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e95c-143">INPUTS</span></span>

### <span data-ttu-id="7e95c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7e95c-144">System.String</span></span>

### <span data-ttu-id="7e95c-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7e95c-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7e95c-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e95c-146">OUTPUTS</span></span>

### <span data-ttu-id="7e95c-147">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7e95c-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7e95c-148">Note</span><span class="sxs-lookup"><span data-stu-id="7e95c-148">NOTES</span></span>

## <span data-ttu-id="7e95c-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e95c-149">RELATED LINKS</span></span>
