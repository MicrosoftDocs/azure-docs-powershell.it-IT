---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E9FB22-43A8-4D07-AF48-5884E4593CA9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f3baea7440d58812056999ea4f271acf80b8d4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023404"
---
# <span data-ttu-id="240b4-101">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="240b4-101">Set-AzureVMExtension</span></span>

## <span data-ttu-id="240b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="240b4-102">SYNOPSIS</span></span>
<span data-ttu-id="240b4-103">Imposta le estensioni delle risorse per le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="240b4-103">Sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="240b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="240b4-104">SYNTAX</span></span>

### <span data-ttu-id="240b4-105">SetByExtensionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="240b4-105">SetByExtensionName (Default)</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfiguration] <String>] [[-PrivateConfiguration] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="240b4-106">SetByExtensionNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="240b4-106">SetByExtensionNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="240b4-107">SetByReferenceName</span><span class="sxs-lookup"><span data-stu-id="240b4-107">SetByReferenceName</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfiguration] <String>]
 [[-PrivateConfiguration] <String>] [-Disable] [-Uninstall] [[-PublicConfigKey] <String>]
 [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="240b4-108">SetByReferenceNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="240b4-108">SetByReferenceNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>]
 [-Disable] [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="240b4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="240b4-109">DESCRIPTION</span></span>
<span data-ttu-id="240b4-110">Il cmdlet **set-AzureVMExtension** imposta le estensioni delle risorse per le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="240b4-110">The **Set-AzureVMExtension** cmdlet sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="240b4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="240b4-111">EXAMPLES</span></span>

### <span data-ttu-id="240b4-112">Esempio 1: creare una macchina virtuale con le estensioni delle risorse applicate</span><span class="sxs-lookup"><span data-stu-id="240b4-112">Example 1: Create a virtual machine with resource extensions applied</span></span>
```
PS C:\> $X = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $IMG;$X = Add-AzureProvisioningConfig -VM $X -Password $PWD -AdminUsername $USR -Windows;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext1 -Publisher $Publisher -Version $VER -PublicConfiguration $P1 -PrivateConfiguration $P2;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext2 -Publisher $Publisher -Version $VER -PublicConfiguration $P3 -PrivateConfiguration $P4;New-AzureVM -Location $LOC -ServiceName $SVC -VM $X;
```

<span data-ttu-id="240b4-113">Questo comando crea una macchina virtuale con le estensioni delle risorse applicate.</span><span class="sxs-lookup"><span data-stu-id="240b4-113">This command creates a virtual machine with resource extensions applied.</span></span>

## <span data-ttu-id="240b4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="240b4-114">PARAMETERS</span></span>

### <span data-ttu-id="240b4-115">-Disable</span><span class="sxs-lookup"><span data-stu-id="240b4-115">-Disable</span></span>
<span data-ttu-id="240b4-116">Indica che questo cmdlet disabilita lo stato dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="240b4-116">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240b4-117">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="240b4-117">-ExtensionName</span></span>
<span data-ttu-id="240b4-118">Specifica il nome dell'estensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="240b4-118">Specifies the extension name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240b4-119">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="240b4-119">-ForceUpdate</span></span>
<span data-ttu-id="240b4-120">Indica che questo cmdlet applica nuovamente una configurazione a un'estensione quando la configurazione non è stata aggiornata.</span><span class="sxs-lookup"><span data-stu-id="240b4-120">Indicates that this cmdlet re-applies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="240b4-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="240b4-121">-InformationAction</span></span>
<span data-ttu-id="240b4-122">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="240b4-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="240b4-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="240b4-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="240b4-124">Continuare</span><span class="sxs-lookup"><span data-stu-id="240b4-124">Continue</span></span>
- <span data-ttu-id="240b4-125">Ignora</span><span class="sxs-lookup"><span data-stu-id="240b4-125">Ignore</span></span>
- <span data-ttu-id="240b4-126">Informarsi</span><span class="sxs-lookup"><span data-stu-id="240b4-126">Inquire</span></span>
- <span data-ttu-id="240b4-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="240b4-127">SilentlyContinue</span></span>
- <span data-ttu-id="240b4-128">Stop</span><span class="sxs-lookup"><span data-stu-id="240b4-128">Stop</span></span>
- <span data-ttu-id="240b4-129">Sospensione</span><span class="sxs-lookup"><span data-stu-id="240b4-129">Suspend</span></span>

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

### <span data-ttu-id="240b4-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="240b4-130">-InformationVariable</span></span>
<span data-ttu-id="240b4-131">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="240b4-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="240b4-132">-PrivateConfigKey</span><span class="sxs-lookup"><span data-stu-id="240b4-132">-PrivateConfigKey</span></span>
<span data-ttu-id="240b4-133">Specifica una chiave di configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="240b4-133">Specifies a private configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240b4-134">-PrivateConfigPath</span><span class="sxs-lookup"><span data-stu-id="240b4-134">-PrivateConfigPath</span></span>
<span data-ttu-id="240b4-135">Specifica il percorso di configurazione privato.</span><span class="sxs-lookup"><span data-stu-id="240b4-135">Specifies the private configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240b4-136">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="240b4-136">-PrivateConfiguration</span></span>
<span data-ttu-id="240b4-137">Specifica il testo della configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="240b4-137">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240b4-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="240b4-138">-Profile</span></span>
<span data-ttu-id="240b4-139">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="240b4-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="240b4-140">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="240b4-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="240b4-141">-PublicConfigKey</span><span class="sxs-lookup"><span data-stu-id="240b4-141">-PublicConfigKey</span></span>
<span data-ttu-id="240b4-142">Specifica la chiave di configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="240b4-142">Specifies the public configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240b4-143">-PublicConfigPath</span><span class="sxs-lookup"><span data-stu-id="240b4-143">-PublicConfigPath</span></span>
<span data-ttu-id="240b4-144">Specifica il percorso di configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="240b4-144">Specifies the public configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240b4-145">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="240b4-145">-PublicConfiguration</span></span>
<span data-ttu-id="240b4-146">Specifica il testo della configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="240b4-146">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240b4-147">-Publisher</span><span class="sxs-lookup"><span data-stu-id="240b4-147">-Publisher</span></span>
<span data-ttu-id="240b4-148">Specifica l'editore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="240b4-148">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240b4-149">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="240b4-149">-ReferenceName</span></span>
<span data-ttu-id="240b4-150">Specifica il nome di riferimento dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="240b4-150">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="240b4-151">Si tratta di una stringa definita dall'utente che può essere usata per fare riferimento a un'estensione.</span><span class="sxs-lookup"><span data-stu-id="240b4-151">This is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="240b4-152">È necessario specificarlo quando l'estensione viene aggiunta alla macchina virtuale per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="240b4-152">You need to specify it when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="240b4-153">Per gli aggiornamenti successivi, è necessario specificare il nome di riferimento usato in precedenza durante l'aggiornamento dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="240b4-153">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="240b4-154">Il riferimento assegnato a un'estensione viene restituito tramite il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="240b4-154">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByReferenceName, SetByReferenceNameAndConfigFile
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240b4-155">-Disinstalla</span><span class="sxs-lookup"><span data-stu-id="240b4-155">-Uninstall</span></span>
<span data-ttu-id="240b4-156">Indica che questo cmdlet Disinstalla l'estensione della risorsa dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="240b4-156">Indicates that this cmdlet uninstalls the resource extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240b4-157">-Versione</span><span class="sxs-lookup"><span data-stu-id="240b4-157">-Version</span></span>
<span data-ttu-id="240b4-158">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="240b4-158">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240b4-159">-VM</span><span class="sxs-lookup"><span data-stu-id="240b4-159">-VM</span></span>
<span data-ttu-id="240b4-160">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="240b4-160">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="240b4-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="240b4-161">CommonParameters</span></span>
<span data-ttu-id="240b4-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="240b4-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="240b4-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="240b4-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="240b4-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="240b4-164">INPUTS</span></span>

## <span data-ttu-id="240b4-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="240b4-165">OUTPUTS</span></span>

## <span data-ttu-id="240b4-166">Note</span><span class="sxs-lookup"><span data-stu-id="240b4-166">NOTES</span></span>

## <span data-ttu-id="240b4-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="240b4-167">RELATED LINKS</span></span>

[<span data-ttu-id="240b4-168">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="240b4-168">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="240b4-169">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="240b4-169">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="240b4-170">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="240b4-170">Get-AzureVM</span></span>](./Get-AzureVM.md)


