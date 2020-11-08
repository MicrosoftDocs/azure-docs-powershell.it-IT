---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A8F07D1-AC20-4950-9019-BDFB4FD3CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7569e203369bf1177b4eecc2bd689f3e20dcd48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029499"
---
# <span data-ttu-id="43f44-101">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="43f44-101">Set-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="43f44-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43f44-102">SYNOPSIS</span></span>
<span data-ttu-id="43f44-103">Imposta le informazioni per un'estensione di script personalizzata di Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="43f44-103">Sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="43f44-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43f44-104">SYNTAX</span></span>

### <span data-ttu-id="43f44-105">SetCustomScriptExtensionByContainerAndFileNames (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43f44-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-ContainerName] <String>
 [-FileName] <String[]> [[-StorageAccountName] <String>] [[-StorageEndpointSuffix] <String>]
 [[-StorageAccountKey] <String>] [[-Run] <String>] [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="43f44-106">DisableCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="43f44-106">DisableCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="43f44-107">UninstalleCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="43f44-107">UninstalleCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="43f44-108">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="43f44-108">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [[-FileUri] <String[]>]
 [-Run] <String> [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="43f44-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43f44-109">DESCRIPTION</span></span>
<span data-ttu-id="43f44-110">Il cmdlet **set-AzureVMCustomScriptExtension** imposta le informazioni per un'estensione di script personalizzata di Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="43f44-110">The **Set-AzureVMCustomScriptExtension** cmdlet sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="43f44-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43f44-111">EXAMPLES</span></span>

### <span data-ttu-id="43f44-112">Esempio 1: impostare le informazioni per un'estensione di script personalizzata della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="43f44-112">Example 1: Set information for a virtual machine custom script extension</span></span>
```
PS C:\> $VM = Set-AzureVMCustomScriptExtension -VM $VM -ContainerName "Container01" -FileName "script1.ps1","script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> New-AzureVM -Location "West US" -ServiceName $SVC -VM $VM;
```

<span data-ttu-id="43f44-113">Questo comando imposta le informazioni per un'estensione di script personalizzata della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43f44-113">This command sets information for a virtual machine custom script extension.</span></span>

### <span data-ttu-id="43f44-114">Esempio 2: impostare le informazioni per un'estensione di script personalizzata della macchina virtuale usando un percorso di file</span><span class="sxs-lookup"><span data-stu-id="43f44-114">Example 2: Set information for a virtual machine custom script extension using a file path</span></span>
```
PS C:\> Set-AzureVMCustomScriptExtension -VM $VM -FileUri "http://www.blob.core.contoso.net/bar/script1.ps1","http://www.blob.core.contoso.net/baz/script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> Update-AzureVM -ServiceName $SVC -Name $Name -VM VM;
```

<span data-ttu-id="43f44-115">Questo comando imposta le informazioni per un'estensione di script personalizzata della macchina virtuale usando più URL di file.</span><span class="sxs-lookup"><span data-stu-id="43f44-115">This command sets information for a virtual machine custom script extension using multiple file URLs.</span></span>

## <span data-ttu-id="43f44-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43f44-116">PARAMETERS</span></span>

### <span data-ttu-id="43f44-117">-Argomento</span><span class="sxs-lookup"><span data-stu-id="43f44-117">-Argument</span></span>
<span data-ttu-id="43f44-118">Specifica una stringa che fornisce un argomento che questo cmdlet viene eseguito nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43f44-118">Specifies a string that supplies an argument that this cmdlet runs on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames, SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f44-119">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="43f44-119">-ContainerName</span></span>
<span data-ttu-id="43f44-120">Specifica il nome del contenitore nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="43f44-120">Specifies the container name within the storage account.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f44-121">-Disable</span><span class="sxs-lookup"><span data-stu-id="43f44-121">-Disable</span></span>
<span data-ttu-id="43f44-122">Indica che questo cmdlet disabilita lo stato dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="43f44-122">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f44-123">-Nomefile</span><span class="sxs-lookup"><span data-stu-id="43f44-123">-FileName</span></span>
<span data-ttu-id="43f44-124">Specifica una matrice di stringhe contenente i nomi dei file BLOB nel contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="43f44-124">Specifies a string array that contains the names of the blob files in the specified container.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f44-125">-FileUri</span><span class="sxs-lookup"><span data-stu-id="43f44-125">-FileUri</span></span>
<span data-ttu-id="43f44-126">Specifica una matrice di stringhe che contiene gli URL dei file BLOB.</span><span class="sxs-lookup"><span data-stu-id="43f44-126">Specifies a string array that contains the URLs of the blob files.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f44-127">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="43f44-127">-ForceUpdate</span></span>
<span data-ttu-id="43f44-128">Indica che questo cmdlet applica nuovamente una configurazione a un'estensione quando la configurazione non è stata aggiornata.</span><span class="sxs-lookup"><span data-stu-id="43f44-128">Indicates that this cmdlet re-apply a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f44-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="43f44-129">-InformationAction</span></span>
<span data-ttu-id="43f44-130">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="43f44-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="43f44-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="43f44-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43f44-132">Continuare</span><span class="sxs-lookup"><span data-stu-id="43f44-132">Continue</span></span>
- <span data-ttu-id="43f44-133">Ignora</span><span class="sxs-lookup"><span data-stu-id="43f44-133">Ignore</span></span>
- <span data-ttu-id="43f44-134">Informarsi</span><span class="sxs-lookup"><span data-stu-id="43f44-134">Inquire</span></span>
- <span data-ttu-id="43f44-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="43f44-135">SilentlyContinue</span></span>
- <span data-ttu-id="43f44-136">Stop</span><span class="sxs-lookup"><span data-stu-id="43f44-136">Stop</span></span>
- <span data-ttu-id="43f44-137">Sospensione</span><span class="sxs-lookup"><span data-stu-id="43f44-137">Suspend</span></span>

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

### <span data-ttu-id="43f44-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="43f44-138">-InformationVariable</span></span>
<span data-ttu-id="43f44-139">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="43f44-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="43f44-140">-Profile</span><span class="sxs-lookup"><span data-stu-id="43f44-140">-Profile</span></span>
<span data-ttu-id="43f44-141">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43f44-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="43f44-142">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="43f44-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="43f44-143">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="43f44-143">-ReferenceName</span></span>
<span data-ttu-id="43f44-144">Specifica il nome di riferimento per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="43f44-144">Specifies the reference name for the extension.</span></span>

<span data-ttu-id="43f44-145">Questo parametro è una stringa definita dall'utente che può essere usata per fare riferimento a un'estensione.</span><span class="sxs-lookup"><span data-stu-id="43f44-145">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="43f44-146">Viene specificato quando l'estensione viene aggiunta alla macchina virtuale per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="43f44-146">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="43f44-147">Per gli aggiornamenti successivi, è necessario specificare il nome di riferimento usato in precedenza durante l'aggiornamento dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="43f44-147">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="43f44-148">Il *riferimento* assegnato a un'estensione viene restituito tramite il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="43f44-148">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f44-149">-Run</span><span class="sxs-lookup"><span data-stu-id="43f44-149">-Run</span></span>
<span data-ttu-id="43f44-150">Specifica il comando eseguito da questo cmdlet dall'estensione nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43f44-150">Specifies the command this cmdlet runs by the extension on the virtual machine.</span></span>
<span data-ttu-id="43f44-151">È supportato solo "powershell.exe".</span><span class="sxs-lookup"><span data-stu-id="43f44-151">Only "powershell.exe" is supported.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: RunFile, Command

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: RunFile, Command

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f44-152">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="43f44-152">-StorageAccountKey</span></span>
<span data-ttu-id="43f44-153">Specifica la chiave dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="43f44-153">Specifies the storage account key</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f44-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="43f44-154">-StorageAccountName</span></span>
<span data-ttu-id="43f44-155">Specifica il nome dell'account di archiviazione nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="43f44-155">Specifies the storage account name in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f44-156">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="43f44-156">-StorageEndpointSuffix</span></span>
<span data-ttu-id="43f44-157">Specifica l'endpoint del servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="43f44-157">Specifies the storage service endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f44-158">-Disinstalla</span><span class="sxs-lookup"><span data-stu-id="43f44-158">-Uninstall</span></span>
<span data-ttu-id="43f44-159">Indica che questo cmdlet Disinstalla l'estensione di script personalizzata dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43f44-159">Indicates that this cmdlet uninstalls the custom script extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstalleCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f44-160">-Versione</span><span class="sxs-lookup"><span data-stu-id="43f44-160">-Version</span></span>
<span data-ttu-id="43f44-161">Specifica la versione dell'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="43f44-161">Specifies the version of the custom script extension.</span></span>

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

### <span data-ttu-id="43f44-162">-VM</span><span class="sxs-lookup"><span data-stu-id="43f44-162">-VM</span></span>
<span data-ttu-id="43f44-163">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="43f44-163">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="43f44-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f44-164">CommonParameters</span></span>
<span data-ttu-id="43f44-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43f44-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f44-166">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43f44-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f44-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43f44-167">INPUTS</span></span>

## <span data-ttu-id="43f44-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43f44-168">OUTPUTS</span></span>

## <span data-ttu-id="43f44-169">Note</span><span class="sxs-lookup"><span data-stu-id="43f44-169">NOTES</span></span>

## <span data-ttu-id="43f44-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43f44-170">RELATED LINKS</span></span>

[<span data-ttu-id="43f44-171">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="43f44-171">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="43f44-172">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="43f44-172">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="43f44-173">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="43f44-173">Get-AzureVM</span></span>](./Get-AzureVM.md)


