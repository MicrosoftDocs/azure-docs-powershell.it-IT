---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssadditionalunattendcontent
schema: 2.0.0
ms.openlocfilehash: c0ceb74c6880508f04fb0832c48d0752507f5a5b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866156"
---
# <span data-ttu-id="21180-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="21180-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="21180-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21180-102">SYNOPSIS</span></span>
<span data-ttu-id="21180-103">Aggiunge informazioni al file di risposte dell'installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="21180-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21180-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21180-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21180-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21180-105">DESCRIPTION</span></span>
<span data-ttu-id="21180-106">Il cmdlet **Add-AzureRmVmssAdditionalUnattendContent** aggiunge informazioni al file di risposte per l'installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="21180-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="21180-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21180-107">EXAMPLES</span></span>

### <span data-ttu-id="21180-108">Esempio 1: aggiungere informazioni al file di risposte dell'installazione automatica di Windows</span><span class="sxs-lookup"><span data-stu-id="21180-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="21180-109">Questo comando aggiunge informazioni al file di risposte per l'installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="21180-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="21180-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21180-110">PARAMETERS</span></span>

### <span data-ttu-id="21180-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="21180-111">-ComponentName</span></span>
<span data-ttu-id="21180-112">Specifica il nome del componente da configurare con il contenuto aggiunto.</span><span class="sxs-lookup"><span data-stu-id="21180-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="21180-113">L'unico valore consentito è Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="21180-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: ComponentNames
Parameter Sets: (All)
Aliases: 
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21180-114">-Contenuto</span><span class="sxs-lookup"><span data-stu-id="21180-114">-Content</span></span>
<span data-ttu-id="21180-115">Specifica il contenuto formattato XML aggiunto al file unattend.xml per il percorso e il componente specificati.</span><span class="sxs-lookup"><span data-stu-id="21180-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21180-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21180-116">-DefaultProfile</span></span>
<span data-ttu-id="21180-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21180-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21180-118">-Passname</span><span class="sxs-lookup"><span data-stu-id="21180-118">-PassName</span></span>
<span data-ttu-id="21180-119">Specifica il nome del passaggio a cui si applica il contenuto.</span><span class="sxs-lookup"><span data-stu-id="21180-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="21180-120">L'unico valore consentito è oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="21180-120">The only allowable value is oobeSystem.</span></span>

```yaml
Type: PassNames
Parameter Sets: (All)
Aliases: 
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21180-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="21180-121">-SettingName</span></span>
<span data-ttu-id="21180-122">Specifica il nome dell'impostazione a cui si applica il contenuto.</span><span class="sxs-lookup"><span data-stu-id="21180-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="21180-123">I valori accettabili per questo parametro sono::</span><span class="sxs-lookup"><span data-stu-id="21180-123">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="21180-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="21180-124">FirstLogonCommands</span></span>
- <span data-ttu-id="21180-125">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="21180-125">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21180-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="21180-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="21180-127">Specifica l'oggetto **set di scale** della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="21180-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="21180-128">Puoi usare il cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="21180-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21180-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="21180-129">-Confirm</span></span>
<span data-ttu-id="21180-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21180-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21180-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21180-131">-WhatIf</span></span>
<span data-ttu-id="21180-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21180-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21180-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21180-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21180-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21180-134">CommonParameters</span></span>
<span data-ttu-id="21180-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21180-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21180-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21180-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21180-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21180-137">INPUTS</span></span>

### <span data-ttu-id="21180-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="21180-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="21180-139">Il parametro ' VirtualMachineScaleSet ' accetta il valore di tipo ' VirtualMachineScaleSet ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="21180-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="21180-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21180-140">OUTPUTS</span></span>

### <span data-ttu-id="21180-141">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="21180-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="21180-142">Note</span><span class="sxs-lookup"><span data-stu-id="21180-142">NOTES</span></span>

## <span data-ttu-id="21180-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21180-143">RELATED LINKS</span></span>

[<span data-ttu-id="21180-144">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="21180-144">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
