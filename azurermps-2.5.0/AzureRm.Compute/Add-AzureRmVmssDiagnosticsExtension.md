---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 8e6a0ec7002f211e660c3ca71d190faf719bbd6c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865956"
---
# <span data-ttu-id="df007-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="df007-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="df007-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df007-102">SYNOPSIS</span></span>
<span data-ttu-id="df007-103">Aggiunge un'estensione di diagnostica a VMSS.</span><span class="sxs-lookup"><span data-stu-id="df007-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df007-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df007-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df007-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df007-105">DESCRIPTION</span></span>
<span data-ttu-id="df007-106">Il cmdlet **Add-AzureRmVmssDiagnosticsExtension** aggiunge un'estensione di diagnostica all'istanza di Virtual Machine scale set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="df007-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="df007-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df007-107">EXAMPLES</span></span>

### <span data-ttu-id="df007-108">Esempio 1: aggiungere un'estensione di diagnostica a VMSS</span><span class="sxs-lookup"><span data-stu-id="df007-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="df007-109">Questo comando aggiunge un'estensione di diagnostica a VMSS.</span><span class="sxs-lookup"><span data-stu-id="df007-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="df007-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df007-110">PARAMETERS</span></span>

### <span data-ttu-id="df007-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="df007-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="df007-112">Indica se questo cmdlet consente all'agente guest Azure di aggiornare automaticamente l'estensione a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="df007-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="df007-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df007-113">-DefaultProfile</span></span>
<span data-ttu-id="df007-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="df007-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df007-115">-Force</span><span class="sxs-lookup"><span data-stu-id="df007-115">-Force</span></span>
<span data-ttu-id="df007-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="df007-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="df007-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="df007-117">-Name</span></span>
<span data-ttu-id="df007-118">Specifica il nome di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="df007-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="df007-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="df007-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="df007-120">Specifica il percorso del file di configurazione privato.</span><span class="sxs-lookup"><span data-stu-id="df007-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="df007-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="df007-121">-SettingFilePath</span></span>
<span data-ttu-id="df007-122">Specifica il percorso del file di configurazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="df007-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="df007-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="df007-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="df007-124">Specifica la versione dell'estensione da usare per questo VMSS.</span><span class="sxs-lookup"><span data-stu-id="df007-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="df007-125">Per ottenere la versione, eseguire il cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) con un valore di Microsoft. Azure. Diagnostics per il parametro *PublisherName* e IaaSDiagnostics per il parametro *Type* .</span><span class="sxs-lookup"><span data-stu-id="df007-125">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="df007-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="df007-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="df007-127">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="df007-127">Specify the VMSS object.</span></span>
<span data-ttu-id="df007-128">Puoi usare il cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="df007-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="df007-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="df007-129">-Confirm</span></span>
<span data-ttu-id="df007-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df007-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df007-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df007-131">-WhatIf</span></span>
<span data-ttu-id="df007-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df007-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df007-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df007-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df007-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df007-134">CommonParameters</span></span>
<span data-ttu-id="df007-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df007-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df007-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df007-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df007-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df007-137">INPUTS</span></span>

### <span data-ttu-id="df007-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="df007-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="df007-139">Il parametro ' VirtualMachineScaleSet ' accetta il valore di tipo ' VirtualMachineScaleSet ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="df007-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="df007-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df007-140">OUTPUTS</span></span>

###  
<span data-ttu-id="df007-141">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="df007-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="df007-142">Note</span><span class="sxs-lookup"><span data-stu-id="df007-142">NOTES</span></span>

## <span data-ttu-id="df007-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df007-143">RELATED LINKS</span></span>

[<span data-ttu-id="df007-144">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="df007-144">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="df007-145">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="df007-145">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="df007-146">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="df007-146">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)
