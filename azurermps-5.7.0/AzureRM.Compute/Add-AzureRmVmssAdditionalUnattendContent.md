---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
ms.openlocfilehash: de61efcbabb2e5acd7d82bf7a1cec8341fe06433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512724"
---
# <span data-ttu-id="3bd9c-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="3bd9c-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="3bd9c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3bd9c-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd9c-103">Aggiunge informazioni al file di risposte dell'installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="3bd9c-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bd9c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3bd9c-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bd9c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bd9c-105">DESCRIPTION</span></span>
<span data-ttu-id="3bd9c-106">Il cmdlet **Add-AzureRmVmssAdditionalUnattendContent** aggiunge informazioni al file di risposte per l'installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="3bd9c-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="3bd9c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3bd9c-107">EXAMPLES</span></span>

### <span data-ttu-id="3bd9c-108">Esempio 1: aggiungere informazioni al file di risposte dell'installazione automatica di Windows</span><span class="sxs-lookup"><span data-stu-id="3bd9c-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="3bd9c-109">Questo comando aggiunge informazioni al file di risposte per l'installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="3bd9c-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="3bd9c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3bd9c-110">PARAMETERS</span></span>

### <span data-ttu-id="3bd9c-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="3bd9c-111">-ComponentName</span></span>
<span data-ttu-id="3bd9c-112">Specifica il nome del componente da configurare con il contenuto aggiunto.</span><span class="sxs-lookup"><span data-stu-id="3bd9c-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="3bd9c-113">L'unico valore consentito è Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="3bd9c-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="3bd9c-114">-Contenuto</span><span class="sxs-lookup"><span data-stu-id="3bd9c-114">-Content</span></span>
<span data-ttu-id="3bd9c-115">Specifica il contenuto formattato XML aggiunto al file unattend.xml per il percorso e il componente specificati.</span><span class="sxs-lookup"><span data-stu-id="3bd9c-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="3bd9c-116">-Passname</span><span class="sxs-lookup"><span data-stu-id="3bd9c-116">-PassName</span></span>
<span data-ttu-id="3bd9c-117">Specifica il nome del passaggio a cui si applica il contenuto.</span><span class="sxs-lookup"><span data-stu-id="3bd9c-117">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="3bd9c-118">L'unico valore consentito è oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="3bd9c-118">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="3bd9c-119">-SettingName</span><span class="sxs-lookup"><span data-stu-id="3bd9c-119">-SettingName</span></span>
<span data-ttu-id="3bd9c-120">Specifica il nome dell'impostazione a cui si applica il contenuto.</span><span class="sxs-lookup"><span data-stu-id="3bd9c-120">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="3bd9c-121">I valori accettabili per questo parametro sono::</span><span class="sxs-lookup"><span data-stu-id="3bd9c-121">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="3bd9c-122">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="3bd9c-122">FirstLogonCommands</span></span>
- <span data-ttu-id="3bd9c-123">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="3bd9c-123">AutoLogon</span></span>

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

### <span data-ttu-id="3bd9c-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3bd9c-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3bd9c-125">Specifica l'oggetto **set di scale** della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3bd9c-125">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="3bd9c-126">Puoi usare il cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3bd9c-126">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd9c-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3bd9c-127">-Confirm</span></span>
<span data-ttu-id="3bd9c-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bd9c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bd9c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd9c-129">-WhatIf</span></span>
<span data-ttu-id="3bd9c-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bd9c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bd9c-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bd9c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bd9c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd9c-132">CommonParameters</span></span>
<span data-ttu-id="3bd9c-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bd9c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd9c-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bd9c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd9c-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3bd9c-135">INPUTS</span></span>

### <span data-ttu-id="3bd9c-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3bd9c-136">None</span></span>
<span data-ttu-id="3bd9c-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3bd9c-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3bd9c-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3bd9c-138">OUTPUTS</span></span>

## <span data-ttu-id="3bd9c-139">Note</span><span class="sxs-lookup"><span data-stu-id="3bd9c-139">NOTES</span></span>

## <span data-ttu-id="3bd9c-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3bd9c-140">RELATED LINKS</span></span>

[<span data-ttu-id="3bd9c-141">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3bd9c-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
