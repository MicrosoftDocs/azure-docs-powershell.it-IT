---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
ms.openlocfilehash: 087ae12961d6bd9faf844221772b92c79362d13d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515799"
---
# <span data-ttu-id="5449b-101">Disable-AzureRmVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="5449b-101">Disable-AzureRmVMDiskEncryption</span></span>

## <span data-ttu-id="5449b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5449b-102">SYNOPSIS</span></span>
<span data-ttu-id="5449b-103">Disabilita la crittografia in una macchina virtuale IaaS.</span><span class="sxs-lookup"><span data-stu-id="5449b-103">Disables encryption on an IaaS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5449b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5449b-104">SYNTAX</span></span>

```
Disable-AzureRmVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5449b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5449b-105">DESCRIPTION</span></span>
<span data-ttu-id="5449b-106">Il cmdlet **Disable-AzureRmVMDiskEncryption Disabilita** la crittografia in una macchina virtuale dell'infrastruttura come servizio (IaaS).</span><span class="sxs-lookup"><span data-stu-id="5449b-106">The **Disable-AzureRmVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="5449b-107">Questo cmdlet è supportato solo in macchine virtuali Windows e non in macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="5449b-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="5449b-108">Questo cmdlet installa un'estensione nella macchina virtuale per disabilitare la crittografia.</span><span class="sxs-lookup"><span data-stu-id="5449b-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="5449b-109">Se il parametro *Name* non è specificato, viene creata un'estensione con il nome predefinito "AzureDiskEncryption per Windows VM".</span><span class="sxs-lookup"><span data-stu-id="5449b-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="5449b-110">Attenzione: questo cmdlet riavvia la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5449b-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="5449b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5449b-111">EXAMPLES</span></span>

### <span data-ttu-id="5449b-112">Esempio 1: disabilitare la crittografia per tutti i volumi in una macchina virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="5449b-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="5449b-113">Questo comando Disabilita la crittografia per i volumi di tipo all per la macchina virtuale denominata VM002 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="5449b-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="5449b-114">Dato che il parametro *VolumeType* non è specificato, il cmdlet imposta il valore su All.</span><span class="sxs-lookup"><span data-stu-id="5449b-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="5449b-115">Esempio 2: disabilitare la crittografia per i volumi di dati in una macchina virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="5449b-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="5449b-116">Questo comando Disabilita la crittografia per i volumi di dati di tipo per la macchina virtuale denominata VM004 che appartiene al gruppo di risorse denominato Group002.</span><span class="sxs-lookup"><span data-stu-id="5449b-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="5449b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5449b-117">PARAMETERS</span></span>

### <span data-ttu-id="5449b-118">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5449b-118">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="5449b-119">Indica che questo cmdlet disabilita l'aggiornamento automatico della versione secondaria dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="5449b-119">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5449b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5449b-120">-Force</span></span>
<span data-ttu-id="5449b-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5449b-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5449b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5449b-122">-Name</span></span>
<span data-ttu-id="5449b-123">Specifica il nome della risorsa di Azure Resource Manager (ARM) che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="5449b-123">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="5449b-124">Se questo parametro non viene specificato, questo cmdlet viene impostato su "AzureDiskEncryption for Windows VM".</span><span class="sxs-lookup"><span data-stu-id="5449b-124">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

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

### <span data-ttu-id="5449b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5449b-125">-ResourceGroupName</span></span>
<span data-ttu-id="5449b-126">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5449b-126">Specifies the resource group name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5449b-127">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5449b-127">-TypeHandlerVersion</span></span>
<span data-ttu-id="5449b-128">Specifica la versione dell'estensione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="5449b-128">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="5449b-129">Se non specifichi un valore per questo parametro, viene usata la versione più recente dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="5449b-129">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

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

### <span data-ttu-id="5449b-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="5449b-130">-VMName</span></span>
<span data-ttu-id="5449b-131">Specifica il nome della macchina virtuale in cui questo cmdlet disabilita la crittografia.</span><span class="sxs-lookup"><span data-stu-id="5449b-131">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5449b-132">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="5449b-132">-VolumeType</span></span>
<span data-ttu-id="5449b-133">Specifica il tipo di volumi della macchina virtuale per eseguire l'operazione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="5449b-133">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="5449b-134">Per le macchine virtuali Windows, i valori validi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5449b-134">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="5449b-135">Tutti</span><span class="sxs-lookup"><span data-stu-id="5449b-135">All</span></span>
- <span data-ttu-id="5449b-136">OS</span><span class="sxs-lookup"><span data-stu-id="5449b-136">OS</span></span>
- <span data-ttu-id="5449b-137">Dati.</span><span class="sxs-lookup"><span data-stu-id="5449b-137">Data.</span></span>
<span data-ttu-id="5449b-138">Se non specifichi un valore per questo parametro, il valore predefinito è all.</span><span class="sxs-lookup"><span data-stu-id="5449b-138">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="5449b-139">Disabilita la crittografia non è attualmente supportata per Linux.</span><span class="sxs-lookup"><span data-stu-id="5449b-139">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5449b-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5449b-140">-Confirm</span></span>
<span data-ttu-id="5449b-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5449b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5449b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5449b-142">-WhatIf</span></span>
<span data-ttu-id="5449b-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5449b-143">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5449b-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5449b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5449b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5449b-145">CommonParameters</span></span>
<span data-ttu-id="5449b-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5449b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5449b-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5449b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5449b-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5449b-148">INPUTS</span></span>

### <span data-ttu-id="5449b-149">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5449b-149">None</span></span>
<span data-ttu-id="5449b-150">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5449b-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5449b-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5449b-151">OUTPUTS</span></span>

### <span data-ttu-id="5449b-152">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="5449b-152">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="5449b-153">Note</span><span class="sxs-lookup"><span data-stu-id="5449b-153">NOTES</span></span>

## <span data-ttu-id="5449b-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5449b-154">RELATED LINKS</span></span>

[<span data-ttu-id="5449b-155">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="5449b-155">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="5449b-156">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="5449b-156">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="5449b-157">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="5449b-157">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


