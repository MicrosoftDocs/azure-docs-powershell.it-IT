---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 9aa895245f491e7b7ee077d083f052cd7e4e46e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985206"
---
# <span data-ttu-id="fde80-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fde80-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="fde80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fde80-102">SYNOPSIS</span></span>
<span data-ttu-id="fde80-103">Imposta l'estensione SQL Server azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fde80-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="fde80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fde80-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fde80-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fde80-105">DESCRIPTION</span></span>
<span data-ttu-id="fde80-106">Il cmdlet **Set-AzVMSqlServerExtension** imposta l'estensione del server AzureSQL in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fde80-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="fde80-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fde80-107">EXAMPLES</span></span>

### <span data-ttu-id="fde80-108">Esempio 1: Configurare le impostazioni automatiche di applicazione delle patch in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="fde80-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="fde80-109">Il primo comando crea un oggetto configurazione usando il cmdlet **New-AzVMSqlServerAutoPatchingConfig.**</span><span class="sxs-lookup"><span data-stu-id="fde80-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="fde80-110">Il comando archivia la configurazione nella $AutoPatchingConfig variabile.</span><span class="sxs-lookup"><span data-stu-id="fde80-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="fde80-111">Il secondo comando recupera la macchina virtuale denominata VirtualMachine11 nel servizio denominato Service02 usando il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="fde80-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="fde80-112">Il comando passa l'oggetto al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="fde80-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fde80-113">Il cmdlet corrente configura le impostazioni di applicazione automatica delle patch in $AutoPatchingConfig per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fde80-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="fde80-114">Il comando passa la macchina virtuale al cmdlet Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="fde80-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="fde80-115">Esempio 2: Configurare le impostazioni di backup automatico in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="fde80-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="fde80-116">Il primo comando crea un oggetto configurazione usando il cmdlet **New-AzVMSqlServerAutoBackupConfig.**</span><span class="sxs-lookup"><span data-stu-id="fde80-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="fde80-117">Il comando archivia la configurazione nella $AutoBackupConfig variabile.</span><span class="sxs-lookup"><span data-stu-id="fde80-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="fde80-118">Il secondo comando recupera la macchina virtuale denominata VirtualMachine11 nel servizio denominato Service02 e quindi la passa al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="fde80-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="fde80-119">Il cmdlet corrente configura le impostazioni di backup automatico in $AutoBackupConfig per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fde80-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="fde80-120">Il comando passa la macchina virtuale al cmdlet Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="fde80-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="fde80-121">Esempio 3: Disabilitare un'estensione SQL Server in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="fde80-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="fde80-122">Questo comando ottiene una macchina virtuale denominata VirtualMachine08 in Service03 e la passa al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="fde80-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="fde80-123">Il comando disabilita SQL Server'estensione della macchina virtuale nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fde80-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="fde80-124">Esempio 4: Disinstallare un'estensione SQL Server in una macchina virtuale specifica</span><span class="sxs-lookup"><span data-stu-id="fde80-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="fde80-125">Questo comando ottiene una macchina virtuale denominata VirtualMachine08 in Service03 e la passa al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="fde80-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="fde80-126">Il comando disinstalla un'SQL Server di macchina virtuale specifica in tale macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fde80-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="fde80-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fde80-127">PARAMETERS</span></span>

### <span data-ttu-id="fde80-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="fde80-128">-AutoBackupSettings</span></span>
<span data-ttu-id="fde80-129">Specifica le impostazioni di SQL Server di backup automatico.</span><span class="sxs-lookup"><span data-stu-id="fde80-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="fde80-130">Per creare un **oggetto AutoBackupSettings,** usare il cmdlet New-AzVMSqlServerAutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="fde80-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="fde80-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="fde80-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="fde80-132">Specifica le impostazioni di SQL Server di distribuzione automatica delle patch.</span><span class="sxs-lookup"><span data-stu-id="fde80-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="fde80-133">Per creare un **oggetto AutoPatchingSettings,** usare il cmdlet New-AzVMSqlServerAutoPatchingConfig AutoPatchingSettings.</span><span class="sxs-lookup"><span data-stu-id="fde80-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="fde80-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde80-134">-DefaultProfile</span></span>
<span data-ttu-id="fde80-135">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fde80-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fde80-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="fde80-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="fde80-137">-Location</span><span class="sxs-lookup"><span data-stu-id="fde80-137">-Location</span></span>
<span data-ttu-id="fde80-138">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fde80-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="fde80-139">-Name</span><span class="sxs-lookup"><span data-stu-id="fde80-139">-Name</span></span>
<span data-ttu-id="fde80-140">Specifica il nome della SQL Server'estensione.</span><span class="sxs-lookup"><span data-stu-id="fde80-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="fde80-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fde80-141">-ResourceGroupName</span></span>
<span data-ttu-id="fde80-142">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fde80-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fde80-143">-Version</span><span class="sxs-lookup"><span data-stu-id="fde80-143">-Version</span></span>
<span data-ttu-id="fde80-144">Specifica la versione dell'estensione SQL Server versione.</span><span class="sxs-lookup"><span data-stu-id="fde80-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="fde80-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="fde80-145">-VMName</span></span>
<span data-ttu-id="fde80-146">Specifica il nome della macchina virtuale in cui questo cmdlet imposta l SQL Server estensione.</span><span class="sxs-lookup"><span data-stu-id="fde80-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="fde80-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde80-147">CommonParameters</span></span>
<span data-ttu-id="fde80-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fde80-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde80-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fde80-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde80-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="fde80-150">INPUTS</span></span>

### <span data-ttu-id="fde80-151">System.String</span><span class="sxs-lookup"><span data-stu-id="fde80-151">System.String</span></span>

### <span data-ttu-id="fde80-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="fde80-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="fde80-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="fde80-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="fde80-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="fde80-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="fde80-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fde80-155">OUTPUTS</span></span>

### <span data-ttu-id="fde80-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fde80-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fde80-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="fde80-157">NOTES</span></span>

## <span data-ttu-id="fde80-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fde80-158">RELATED LINKS</span></span>

[<span data-ttu-id="fde80-159">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="fde80-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="fde80-160">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fde80-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="fde80-161">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="fde80-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="fde80-162">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="fde80-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="fde80-163">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fde80-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="fde80-164">Update-AZVM</span><span class="sxs-lookup"><span data-stu-id="fde80-164">Update-AzVM</span></span>](./Update-AzVM.md)


