---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 0e28b5df77734645380316af6396f745469637df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518188"
---
# <span data-ttu-id="4dcb8-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4dcb8-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="4dcb8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4dcb8-102">SYNOPSIS</span></span>
<span data-ttu-id="4dcb8-103">Aggiunge un'estensione di diagnostica a VMSS.</span><span class="sxs-lookup"><span data-stu-id="4dcb8-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dcb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4dcb8-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4dcb8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4dcb8-105">DESCRIPTION</span></span>
<span data-ttu-id="4dcb8-106">Il cmdlet **Add-AzureRmVmssDiagnosticsExtension** aggiunge un'estensione di diagnostica all'istanza di Virtual Machine scale set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="4dcb8-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="4dcb8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4dcb8-107">EXAMPLES</span></span>

### <span data-ttu-id="4dcb8-108">Esempio 1: aggiungere un'estensione di diagnostica a VMSS</span><span class="sxs-lookup"><span data-stu-id="4dcb8-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="4dcb8-109">Questo comando aggiunge un'estensione di diagnostica a VMSS.</span><span class="sxs-lookup"><span data-stu-id="4dcb8-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="4dcb8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4dcb8-110">PARAMETERS</span></span>

### <span data-ttu-id="4dcb8-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="4dcb8-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="4dcb8-112">Indica se questo cmdlet consente all'agente guest Azure di aggiornare automaticamente l'estensione a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="4dcb8-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dcb8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4dcb8-113">-Force</span></span>
<span data-ttu-id="4dcb8-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4dcb8-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dcb8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4dcb8-115">-Name</span></span>
<span data-ttu-id="4dcb8-116">Specifica il nome di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="4dcb8-116">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dcb8-117">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="4dcb8-117">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="4dcb8-118">Specifica il percorso del file di configurazione privato.</span><span class="sxs-lookup"><span data-stu-id="4dcb8-118">Specifies the path of the private configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dcb8-119">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="4dcb8-119">-SettingFilePath</span></span>
<span data-ttu-id="4dcb8-120">Specifica il percorso del file di configurazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="4dcb8-120">Specifies the path of the public configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dcb8-121">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="4dcb8-121">-TypeHandlerVersion</span></span>
<span data-ttu-id="4dcb8-122">Specifica la versione dell'estensione da usare per questo VMSS.</span><span class="sxs-lookup"><span data-stu-id="4dcb8-122">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="4dcb8-123">Per ottenere la versione, eseguire il cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) con un valore di Microsoft. Azure. Diagnostics per il parametro *PublisherName* e IaaSDiagnostics per il parametro *Type* .</span><span class="sxs-lookup"><span data-stu-id="4dcb8-123">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dcb8-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4dcb8-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4dcb8-125">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="4dcb8-125">Specify the VMSS object.</span></span>
<span data-ttu-id="4dcb8-126">Puoi usare il cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4dcb8-126">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="4dcb8-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4dcb8-127">-Confirm</span></span>
<span data-ttu-id="4dcb8-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dcb8-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dcb8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dcb8-129">-WhatIf</span></span>
<span data-ttu-id="4dcb8-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4dcb8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dcb8-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4dcb8-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dcb8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dcb8-132">CommonParameters</span></span>
<span data-ttu-id="4dcb8-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dcb8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dcb8-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dcb8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dcb8-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4dcb8-135">INPUTS</span></span>

### <span data-ttu-id="4dcb8-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4dcb8-136">None</span></span>
<span data-ttu-id="4dcb8-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="4dcb8-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4dcb8-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4dcb8-138">OUTPUTS</span></span>

###  
<span data-ttu-id="4dcb8-139">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="4dcb8-139">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="4dcb8-140">Note</span><span class="sxs-lookup"><span data-stu-id="4dcb8-140">NOTES</span></span>

## <span data-ttu-id="4dcb8-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4dcb8-141">RELATED LINKS</span></span>

[<span data-ttu-id="4dcb8-142">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="4dcb8-142">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="4dcb8-143">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4dcb8-143">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="4dcb8-144">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4dcb8-144">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)