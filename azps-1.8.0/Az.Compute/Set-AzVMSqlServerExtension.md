---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 25fdd6eaf7271a48e65b871d10d5264d75d3fe23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684685"
---
# <span data-ttu-id="43c68-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="43c68-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="43c68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43c68-102">SYNOPSIS</span></span>
<span data-ttu-id="43c68-103">Imposta l'estensione di Azure SQL Server in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43c68-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="43c68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43c68-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43c68-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43c68-105">DESCRIPTION</span></span>
<span data-ttu-id="43c68-106">Il cmdlet **set-AzVMSqlServerExtension** imposta l'estensione del server AzureSQL in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43c68-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="43c68-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43c68-107">EXAMPLES</span></span>

### <span data-ttu-id="43c68-108">Esempio 1: impostare le impostazioni di correzione automatica in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="43c68-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="43c68-109">Il primo comando crea un oggetto Configuration usando il cmdlet **New-AzVMSqlServerAutoPatchingConfig** .</span><span class="sxs-lookup"><span data-stu-id="43c68-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="43c68-110">Il comando Archivia la configurazione nella variabile $AutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="43c68-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="43c68-111">Il secondo comando consente di ottenere la macchina virtuale denominata VirtualMachine11 nel servizio denominato Service02 usando il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="43c68-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="43c68-112">Il comando passa l'oggetto al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="43c68-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="43c68-113">Il cmdlet corrente imposta le impostazioni di correzione automatica in $AutoPatchingConfig per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43c68-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="43c68-114">Il comando passa la macchina virtuale al cmdlet Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="43c68-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="43c68-115">Esempio 2: impostare le impostazioni di backup automatico in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="43c68-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="43c68-116">Il primo comando crea un oggetto Configuration usando il cmdlet **New-AzVMSqlServerAutoBackupConfig** .</span><span class="sxs-lookup"><span data-stu-id="43c68-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="43c68-117">Il comando Archivia la configurazione nella variabile $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="43c68-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="43c68-118">Il secondo comando consente di ottenere la macchina virtuale denominata VirtualMachine11 nel servizio denominato Service02 e quindi di passarla al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="43c68-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="43c68-119">Il cmdlet Current imposta le impostazioni di backup automatico in $AutoBackupConfig per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43c68-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="43c68-120">Il comando passa la macchina virtuale al cmdlet Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="43c68-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="43c68-121">Esempio 3: disabilitare un'estensione di SQL Server in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="43c68-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="43c68-122">Questo comando consente di ottenere una macchina virtuale denominata VirtualMachine08 in Service03 e quindi di passarla al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="43c68-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="43c68-123">Il comando Disabilita l'estensione della macchina virtuale di SQL Server in quella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43c68-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="43c68-124">Esempio 4: disinstallare un'estensione di SQL Server in una specifica macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="43c68-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="43c68-125">Questo comando consente di ottenere una macchina virtuale denominata VirtualMachine08 in Service03 e quindi di passarla al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="43c68-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="43c68-126">Il comando disinstalla un'estensione della macchina virtuale di SQL Server in quella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43c68-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="43c68-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43c68-127">PARAMETERS</span></span>

### <span data-ttu-id="43c68-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="43c68-128">-AutoBackupSettings</span></span>
<span data-ttu-id="43c68-129">Specifica le impostazioni di backup automatico di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="43c68-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="43c68-130">Per creare un oggetto **AutoBackupSettings** , usa il cmdlet New-AzVMSqlServerAutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="43c68-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c68-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="43c68-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="43c68-132">Specifica le impostazioni di correzione automatica di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="43c68-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="43c68-133">Per creare un oggetto **AutoPatchingSettings** , usa il cmdlet New-AzVMSqlServerAutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="43c68-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c68-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c68-134">-DefaultProfile</span></span>
<span data-ttu-id="43c68-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43c68-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c68-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="43c68-136">-KeyVaultCredentialSettings</span></span>
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c68-137">-Posizione</span><span class="sxs-lookup"><span data-stu-id="43c68-137">-Location</span></span>
<span data-ttu-id="43c68-138">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43c68-138">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c68-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="43c68-139">-Name</span></span>
<span data-ttu-id="43c68-140">Specifica il nome dell'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="43c68-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="43c68-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43c68-141">-ResourceGroupName</span></span>
<span data-ttu-id="43c68-142">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43c68-142">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c68-143">-Versione</span><span class="sxs-lookup"><span data-stu-id="43c68-143">-Version</span></span>
<span data-ttu-id="43c68-144">Specifica la versione dell'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="43c68-144">Specifies the version of the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c68-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="43c68-145">-VMName</span></span>
<span data-ttu-id="43c68-146">Specifica il nome della macchina virtuale in cui questo cmdlet imposta l'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="43c68-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c68-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c68-147">CommonParameters</span></span>
<span data-ttu-id="43c68-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43c68-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c68-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43c68-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c68-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43c68-150">INPUTS</span></span>

### <span data-ttu-id="43c68-151">System. String</span><span class="sxs-lookup"><span data-stu-id="43c68-151">System.String</span></span>

### <span data-ttu-id="43c68-152">Microsoft. Azure. Commands. Compute. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="43c68-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="43c68-153">Microsoft. Azure. Commands. Compute. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="43c68-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="43c68-154">Microsoft. Azure. Commands. Compute. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="43c68-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="43c68-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43c68-155">OUTPUTS</span></span>

### <span data-ttu-id="43c68-156">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="43c68-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="43c68-157">Note</span><span class="sxs-lookup"><span data-stu-id="43c68-157">NOTES</span></span>

## <span data-ttu-id="43c68-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43c68-158">RELATED LINKS</span></span>

[<span data-ttu-id="43c68-159">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="43c68-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="43c68-160">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="43c68-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="43c68-161">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="43c68-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="43c68-162">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="43c68-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="43c68-163">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="43c68-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="43c68-164">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="43c68-164">Update-AzVM</span></span>](./Update-AzVM.md)


