---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
ms.openlocfilehash: d99e54439b2e8b4474c4b0123634ddd7c286ea9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508744"
---
# <span data-ttu-id="ac85b-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="ac85b-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="ac85b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac85b-102">SYNOPSIS</span></span>
<span data-ttu-id="ac85b-103">Aggiunge informazioni al file di risposte dell'installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="ac85b-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac85b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac85b-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac85b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac85b-105">DESCRIPTION</span></span>
<span data-ttu-id="ac85b-106">Il cmdlet **Add-AzureRmVmssAdditionalUnattendContent** aggiunge informazioni al file di risposte per l'installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="ac85b-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="ac85b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac85b-107">EXAMPLES</span></span>

### <span data-ttu-id="ac85b-108">Esempio 1: aggiungere informazioni al file di risposte dell'installazione automatica di Windows</span><span class="sxs-lookup"><span data-stu-id="ac85b-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="ac85b-109">Questo comando aggiunge informazioni al file di risposte per l'installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="ac85b-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="ac85b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac85b-110">PARAMETERS</span></span>

### <span data-ttu-id="ac85b-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="ac85b-111">-ComponentName</span></span>
<span data-ttu-id="ac85b-112">Specifica il nome del componente da configurare con il contenuto aggiunto.</span><span class="sxs-lookup"><span data-stu-id="ac85b-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="ac85b-113">L'unico valore consentito è Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="ac85b-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="ac85b-114">-Contenuto</span><span class="sxs-lookup"><span data-stu-id="ac85b-114">-Content</span></span>
<span data-ttu-id="ac85b-115">Specifica il contenuto formattato XML aggiunto al file unattend.xml per il percorso e il componente specificati.</span><span class="sxs-lookup"><span data-stu-id="ac85b-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="ac85b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac85b-116">-DefaultProfile</span></span>
<span data-ttu-id="ac85b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac85b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac85b-118">-Passname</span><span class="sxs-lookup"><span data-stu-id="ac85b-118">-PassName</span></span>
<span data-ttu-id="ac85b-119">Specifica il nome del passaggio a cui si applica il contenuto.</span><span class="sxs-lookup"><span data-stu-id="ac85b-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="ac85b-120">L'unico valore consentito è oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="ac85b-120">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="ac85b-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="ac85b-121">-SettingName</span></span>
<span data-ttu-id="ac85b-122">Specifica il nome dell'impostazione a cui si applica il contenuto.</span><span class="sxs-lookup"><span data-stu-id="ac85b-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="ac85b-123">I valori accettabili per questo parametro sono::</span><span class="sxs-lookup"><span data-stu-id="ac85b-123">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="ac85b-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="ac85b-124">FirstLogonCommands</span></span>
- <span data-ttu-id="ac85b-125">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="ac85b-125">AutoLogon</span></span>

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

### <span data-ttu-id="ac85b-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ac85b-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ac85b-127">Specifica l'oggetto **set di scale** della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ac85b-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="ac85b-128">Puoi usare il cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ac85b-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="ac85b-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ac85b-129">-Confirm</span></span>
<span data-ttu-id="ac85b-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac85b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac85b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac85b-131">-WhatIf</span></span>
<span data-ttu-id="ac85b-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac85b-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac85b-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac85b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac85b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac85b-134">CommonParameters</span></span>
<span data-ttu-id="ac85b-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac85b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac85b-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac85b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac85b-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac85b-137">INPUTS</span></span>

## <span data-ttu-id="ac85b-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac85b-138">OUTPUTS</span></span>

## <span data-ttu-id="ac85b-139">Note</span><span class="sxs-lookup"><span data-stu-id="ac85b-139">NOTES</span></span>

## <span data-ttu-id="ac85b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac85b-140">RELATED LINKS</span></span>

[<span data-ttu-id="ac85b-141">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ac85b-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
