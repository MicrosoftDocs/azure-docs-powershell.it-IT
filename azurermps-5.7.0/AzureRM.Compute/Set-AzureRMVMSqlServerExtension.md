---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: c3a146b99119ab94bf98176d202cda52e1dc5704
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518176"
---
# <span data-ttu-id="92c96-101">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="92c96-101">Set-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="92c96-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92c96-102">SYNOPSIS</span></span>
<span data-ttu-id="92c96-103">Imposta l'estensione di Azure SQL Server in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="92c96-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92c96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92c96-104">SYNTAX</span></span>

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="92c96-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92c96-105">DESCRIPTION</span></span>
<span data-ttu-id="92c96-106">Il cmdlet **set-AzureRmVMSqlServerExtension** imposta l'estensione del server AzureSQL in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="92c96-106">The **Set-AzureRmVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="92c96-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92c96-107">EXAMPLES</span></span>

### <span data-ttu-id="92c96-108">Esempio 1: impostare le impostazioni di correzione automatica in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="92c96-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

<span data-ttu-id="92c96-109">Il primo comando crea un oggetto Configuration usando il cmdlet **New-AzureVMSqlServerAutoPatchingConfig** .</span><span class="sxs-lookup"><span data-stu-id="92c96-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="92c96-110">Il comando Archivia la configurazione nella variabile $AutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="92c96-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="92c96-111">Il secondo comando consente di ottenere la macchina virtuale denominata VirtualMachine11 nel servizio denominato Service02 usando il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="92c96-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="92c96-112">Il comando passa l'oggetto al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="92c96-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="92c96-113">Il cmdlet corrente imposta le impostazioni di correzione automatica in $AutoPatchingConfig per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="92c96-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="92c96-114">Il comando passa la macchina virtuale al cmdlet Update-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="92c96-114">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="92c96-115">Esempio 2: impostare le impostazioni di backup automatico in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="92c96-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

<span data-ttu-id="92c96-116">Il primo comando crea un oggetto Configuration usando il cmdlet **New-AzureVMSqlServerAutoBackupConfig** .</span><span class="sxs-lookup"><span data-stu-id="92c96-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="92c96-117">Il comando Archivia la configurazione nella variabile $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="92c96-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="92c96-118">Il secondo comando consente di ottenere la macchina virtuale denominata VirtualMachine11 nel servizio denominato Service02 e quindi di passarla al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="92c96-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="92c96-119">Il cmdlet Current imposta le impostazioni di backup automatico in $AutoBackupConfig per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="92c96-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="92c96-120">Il comando passa la macchina virtuale al cmdlet Update-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="92c96-120">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="92c96-121">Esempio 3: disabilitare un'estensione di SQL Server in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="92c96-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

<span data-ttu-id="92c96-122">Questo comando consente di ottenere una macchina virtuale denominata VirtualMachine08 in Service03 e quindi di passarla al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="92c96-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="92c96-123">Il comando Disabilita l'estensione della macchina virtuale di SQL Server in quella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="92c96-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="92c96-124">Esempio 4: disinstallare un'estensione di SQL Server in una specifica macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="92c96-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
```

<span data-ttu-id="92c96-125">Questo comando consente di ottenere una macchina virtuale denominata VirtualMachine08 in Service03 e quindi di passarla al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="92c96-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="92c96-126">Il comando disinstalla un'estensione della macchina virtuale di SQL Server in quella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="92c96-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="92c96-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92c96-127">PARAMETERS</span></span>

### <span data-ttu-id="92c96-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="92c96-128">-AutoBackupSettings</span></span>
<span data-ttu-id="92c96-129">Specifica le impostazioni di backup automatico di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="92c96-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="92c96-130">Per creare un oggetto **AutoBackupSettings** , usa il cmdlet New-AzureVMSqlServerAutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="92c96-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92c96-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="92c96-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="92c96-132">Specifica le impostazioni di correzione automatica di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="92c96-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="92c96-133">Per creare un oggetto **AutoPatchingSettings** , usa il cmdlet New-AzureVMSqlServerAutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="92c96-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92c96-134">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="92c96-134">-KeyVaultCredentialSettings</span></span>
```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92c96-135">-Posizione</span><span class="sxs-lookup"><span data-stu-id="92c96-135">-Location</span></span>
<span data-ttu-id="92c96-136">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="92c96-136">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92c96-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="92c96-137">-Name</span></span>
<span data-ttu-id="92c96-138">Specifica il nome dell'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="92c96-138">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="92c96-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92c96-139">-ResourceGroupName</span></span>
<span data-ttu-id="92c96-140">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="92c96-140">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92c96-141">-Versione</span><span class="sxs-lookup"><span data-stu-id="92c96-141">-Version</span></span>
<span data-ttu-id="92c96-142">Specifica la versione dell'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="92c96-142">Specifies the version of the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92c96-143">-VMName</span><span class="sxs-lookup"><span data-stu-id="92c96-143">-VMName</span></span>
<span data-ttu-id="92c96-144">Specifica il nome della macchina virtuale in cui questo cmdlet imposta l'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="92c96-144">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92c96-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92c96-145">CommonParameters</span></span>
<span data-ttu-id="92c96-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92c96-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92c96-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92c96-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92c96-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92c96-148">INPUTS</span></span>

### <span data-ttu-id="92c96-149">Nessuno</span><span class="sxs-lookup"><span data-stu-id="92c96-149">None</span></span>
<span data-ttu-id="92c96-150">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="92c96-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="92c96-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92c96-151">OUTPUTS</span></span>

## <span data-ttu-id="92c96-152">Note</span><span class="sxs-lookup"><span data-stu-id="92c96-152">NOTES</span></span>

## <span data-ttu-id="92c96-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92c96-153">RELATED LINKS</span></span>

[<span data-ttu-id="92c96-154">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="92c96-154">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="92c96-155">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="92c96-155">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="92c96-156">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="92c96-156">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="92c96-157">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="92c96-157">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="92c96-158">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="92c96-158">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="92c96-159">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="92c96-159">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


