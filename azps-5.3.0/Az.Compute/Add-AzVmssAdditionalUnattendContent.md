---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 051228464b2f1e9770507ceacd4eaabfce5236b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477880"
---
# <span data-ttu-id="6af55-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="6af55-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="6af55-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6af55-102">SYNOPSIS</span></span>
<span data-ttu-id="6af55-103">Aggiunge informazioni al file di risposte dell'installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="6af55-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="6af55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6af55-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6af55-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6af55-105">DESCRIPTION</span></span>
<span data-ttu-id="6af55-106">Il cmdlet **Add-AzVmssAdditionalUnattendContent** aggiunge informazioni al file di risposte per l'installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="6af55-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="6af55-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6af55-107">EXAMPLES</span></span>

### <span data-ttu-id="6af55-108">Esempio 1: aggiungere informazioni al file di risposte dell'installazione automatica di Windows</span><span class="sxs-lookup"><span data-stu-id="6af55-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="6af55-109">Questo comando aggiunge informazioni al file di risposte per l'installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="6af55-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="6af55-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6af55-110">PARAMETERS</span></span>

### <span data-ttu-id="6af55-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="6af55-111">-ComponentName</span></span>
<span data-ttu-id="6af55-112">Specifica il nome del componente da configurare con il contenuto aggiunto.</span><span class="sxs-lookup"><span data-stu-id="6af55-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="6af55-113">L'unico valore consentito è Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="6af55-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ComponentNames]
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6af55-114">-Contenuto</span><span class="sxs-lookup"><span data-stu-id="6af55-114">-Content</span></span>
<span data-ttu-id="6af55-115">Specifica il contenuto formattato XML aggiunto al file unattend.xml per il percorso e il componente specificati.</span><span class="sxs-lookup"><span data-stu-id="6af55-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6af55-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6af55-116">-DefaultProfile</span></span>
<span data-ttu-id="6af55-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6af55-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6af55-118">-Passname</span><span class="sxs-lookup"><span data-stu-id="6af55-118">-PassName</span></span>
<span data-ttu-id="6af55-119">Specifica il nome del passaggio a cui si applica il contenuto.</span><span class="sxs-lookup"><span data-stu-id="6af55-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="6af55-120">L'unico valore consentito è oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="6af55-120">The only allowable value is oobeSystem.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.PassNames]
Parameter Sets: (All)
Aliases:
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6af55-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="6af55-121">-SettingName</span></span>
<span data-ttu-id="6af55-122">Specifica il nome dell'impostazione a cui si applica il contenuto.</span><span class="sxs-lookup"><span data-stu-id="6af55-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="6af55-123">I valori accettabili per questo parametro sono::</span><span class="sxs-lookup"><span data-stu-id="6af55-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="6af55-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="6af55-124">FirstLogonCommands</span></span>
- <span data-ttu-id="6af55-125">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="6af55-125">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6af55-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6af55-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6af55-127">Specifica l'oggetto **set di scale** della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6af55-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="6af55-128">Puoi usare il cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6af55-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="6af55-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6af55-129">-Confirm</span></span>
<span data-ttu-id="6af55-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6af55-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af55-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6af55-131">-WhatIf</span></span>
<span data-ttu-id="6af55-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6af55-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6af55-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6af55-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af55-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6af55-134">CommonParameters</span></span>
<span data-ttu-id="6af55-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6af55-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6af55-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6af55-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6af55-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6af55-137">INPUTS</span></span>

### <span data-ttu-id="6af55-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6af55-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="6af55-139">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. PassNames, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6af55-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6af55-140">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ComponentNames, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6af55-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6af55-141">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. SettingNames, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6af55-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6af55-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6af55-142">System.String</span></span>

## <span data-ttu-id="6af55-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6af55-143">OUTPUTS</span></span>

### <span data-ttu-id="6af55-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6af55-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6af55-145">Note</span><span class="sxs-lookup"><span data-stu-id="6af55-145">NOTES</span></span>

## <span data-ttu-id="6af55-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6af55-146">RELATED LINKS</span></span>

[<span data-ttu-id="6af55-147">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6af55-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
