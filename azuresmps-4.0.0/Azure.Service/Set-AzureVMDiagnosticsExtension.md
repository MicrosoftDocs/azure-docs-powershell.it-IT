---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A05B39BF-87EB-471E-9FCD-F7807CB46B4D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1aa7cff6d655bf33fa1a317516fda20237f6fc14
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029500"
---
# <span data-ttu-id="d4af5-101">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d4af5-101">Set-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="d4af5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4af5-102">SYNOPSIS</span></span>
<span data-ttu-id="d4af5-103">Configura l'estensione di diagnostica di Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d4af5-103">Configures the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="d4af5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4af5-104">SYNTAX</span></span>

### <span data-ttu-id="d4af5-105">SetDiagnosticsExtension (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d4af5-105">SetDiagnosticsExtension (Default)</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d4af5-106">SetDiagnosticsWithReferenceExtension</span><span class="sxs-lookup"><span data-stu-id="d4af5-106">SetDiagnosticsWithReferenceExtension</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d4af5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4af5-107">DESCRIPTION</span></span>
<span data-ttu-id="d4af5-108">Il cmdlet **set-AzureVMDiagnosticsExtension** configura l'estensione di diagnostica Microsoft Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d4af5-108">The **Set-AzureVMDiagnosticsExtension** cmdlet configures the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="d4af5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4af5-109">EXAMPLES</span></span>

### <span data-ttu-id="d4af5-110">Esempio 1: creare una macchina virtuale con estensione di diagnostica Azure applicata</span><span class="sxs-lookup"><span data-stu-id="d4af5-110">Example 1: Create a virtual machine with Azure Diagnostics extension applied</span></span>
```
PS C:\> $VM = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $VMImage
PS C:\> $VM = Add-AzureProvisioningConfig -VM $VM -AdminUsername $Username -Password $Password -Windows
PS C:\> $VM = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> New-AzureVM -Location $Location -ServiceName $Service_Name -VM $VM
```

<span data-ttu-id="d4af5-111">Questi comandi abilitano l'estensione di diagnostica di Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d4af5-111">These commands enable the Azure Diagnostics extension on a virtual machine.</span></span>

### <span data-ttu-id="d4af5-112">Esempio 2: abilitare un'estensione di diagnostica di Azure in una macchina virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="d4af5-112">Example 2: Enable an Azure Diagnostics extension on an existing virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName $Service_Name -Name $VM_Name
PS C:\> $VM_Update = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> Update-AzureVM -ServiceName $Service_Name -Name $VM_Name -VM $VM_Update.VM
```

<span data-ttu-id="d4af5-113">Il primo comando usa il cmdlet **Get-AzureVM** per ottenere una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d4af5-113">The first command uses the **Get-AzureVM** cmdlet to get a virtual machine.</span></span>

<span data-ttu-id="d4af5-114">Il secondo comando usa il cmdlet **set-AzureVMDiagnosticsExtension** per aggiornare la configurazione della macchina virtuale per includere l'estensione di diagnostica di Azure.</span><span class="sxs-lookup"><span data-stu-id="d4af5-114">The second command uses the **Set-AzureVMDiagnosticsExtension** cmdlet to update the virtual machine configuration to include the Azure Diagnostics extension.</span></span>

<span data-ttu-id="d4af5-115">Il comando finale applica la configurazione aggiornata alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d4af5-115">The final command applies the updated configuration to the virtual machine.</span></span>

## <span data-ttu-id="d4af5-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4af5-116">PARAMETERS</span></span>

### <span data-ttu-id="d4af5-117">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="d4af5-117">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="d4af5-118">Specifica un percorso per la configurazione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="d4af5-118">Specifies a path for the diagnostics configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4af5-119">-Disable</span><span class="sxs-lookup"><span data-stu-id="d4af5-119">-Disable</span></span>
<span data-ttu-id="d4af5-120">Indica che questo cmdlet disabilita l'estensione di diagnostica nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d4af5-120">Indicates that this cmdlet disables the diagnostics extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4af5-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d4af5-121">-InformationAction</span></span>
<span data-ttu-id="d4af5-122">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="d4af5-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d4af5-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d4af5-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4af5-124">Continuare</span><span class="sxs-lookup"><span data-stu-id="d4af5-124">Continue</span></span>
- <span data-ttu-id="d4af5-125">Ignora</span><span class="sxs-lookup"><span data-stu-id="d4af5-125">Ignore</span></span>
- <span data-ttu-id="d4af5-126">Informarsi</span><span class="sxs-lookup"><span data-stu-id="d4af5-126">Inquire</span></span>
- <span data-ttu-id="d4af5-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d4af5-127">SilentlyContinue</span></span>
- <span data-ttu-id="d4af5-128">Stop</span><span class="sxs-lookup"><span data-stu-id="d4af5-128">Stop</span></span>
- <span data-ttu-id="d4af5-129">Sospensione</span><span class="sxs-lookup"><span data-stu-id="d4af5-129">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4af5-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d4af5-130">-InformationVariable</span></span>
<span data-ttu-id="d4af5-131">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="d4af5-131">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4af5-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="d4af5-132">-Profile</span></span>
<span data-ttu-id="d4af5-133">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4af5-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d4af5-134">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d4af5-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4af5-135">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="d4af5-135">-ReferenceName</span></span>
<span data-ttu-id="d4af5-136">Specifica il nome di riferimento per l'estensione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="d4af5-136">Specifies the reference name for the diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: SetDiagnosticsWithReferenceExtension
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4af5-137">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4af5-137">-StorageAccountEndpoint</span></span>
<span data-ttu-id="d4af5-138">Specifica un endpoint dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d4af5-138">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4af5-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d4af5-139">-StorageAccountKey</span></span>
<span data-ttu-id="d4af5-140">Specifica una chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d4af5-140">Specifies a storage account key.</span></span>

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

### <span data-ttu-id="d4af5-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d4af5-141">-StorageAccountName</span></span>
<span data-ttu-id="d4af5-142">Specifica un nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d4af5-142">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4af5-143">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="d4af5-143">-StorageContext</span></span>
<span data-ttu-id="d4af5-144">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d4af5-144">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4af5-145">-Versione</span><span class="sxs-lookup"><span data-stu-id="d4af5-145">-Version</span></span>
<span data-ttu-id="d4af5-146">Specifica la versione dell'estensione come stringa.</span><span class="sxs-lookup"><span data-stu-id="d4af5-146">Specifies the extension version as a string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4af5-147">-VM</span><span class="sxs-lookup"><span data-stu-id="d4af5-147">-VM</span></span>
<span data-ttu-id="d4af5-148">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="d4af5-148">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4af5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4af5-149">CommonParameters</span></span>
<span data-ttu-id="d4af5-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4af5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4af5-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4af5-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4af5-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4af5-152">INPUTS</span></span>

## <span data-ttu-id="d4af5-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4af5-153">OUTPUTS</span></span>

## <span data-ttu-id="d4af5-154">Note</span><span class="sxs-lookup"><span data-stu-id="d4af5-154">NOTES</span></span>

## <span data-ttu-id="d4af5-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4af5-155">RELATED LINKS</span></span>

[<span data-ttu-id="d4af5-156">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d4af5-156">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="d4af5-157">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d4af5-157">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="d4af5-158">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d4af5-158">Update-AzureVM</span></span>](./Update-AzureVM.md)


