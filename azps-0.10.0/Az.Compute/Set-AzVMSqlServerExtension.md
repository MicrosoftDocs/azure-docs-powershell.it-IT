---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 1795216cbc18da2d503a1e0056d614337cd12785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398241"
---
# <span data-ttu-id="9ae82-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9ae82-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="9ae82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ae82-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae82-103">Imposta l'estensione SQL Server azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9ae82-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="9ae82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ae82-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ae82-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9ae82-105">DESCRIPTION</span></span>
<span data-ttu-id="9ae82-106">Il cmdlet **Set-AzVMSqlServerExtension** imposta l'estensione del server AzureSQL in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9ae82-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="9ae82-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ae82-107">EXAMPLES</span></span>

### <span data-ttu-id="9ae82-108">Esempio 1: Configurare le impostazioni automatiche di applicazione delle patch in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="9ae82-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="9ae82-109">Il primo comando crea un oggetto configurazione usando il cmdlet **New-AzureVMSqlServerAutoPatchingConfig.**</span><span class="sxs-lookup"><span data-stu-id="9ae82-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="9ae82-110">Il comando archivia la configurazione nella $AutoPatchingConfig variabile.</span><span class="sxs-lookup"><span data-stu-id="9ae82-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="9ae82-111">Il secondo comando recupera la macchina virtuale denominata VirtualMachine11 nel servizio denominato Service02 usando il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="9ae82-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="9ae82-112">Il comando passa l'oggetto al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="9ae82-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="9ae82-113">Il cmdlet corrente configura le impostazioni di applicazione automatica delle patch in $AutoPatchingConfig per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9ae82-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="9ae82-114">Il comando passa la macchina virtuale al cmdlet Update-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ae82-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="9ae82-115">Esempio 2: Configurare le impostazioni di backup automatico in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="9ae82-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="9ae82-116">Il primo comando crea un oggetto configurazione usando il cmdlet **New-AzureVMSqlServerAutoBackupConfig.**</span><span class="sxs-lookup"><span data-stu-id="9ae82-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="9ae82-117">Il comando archivia la configurazione nella $AutoBackupConfig variabile.</span><span class="sxs-lookup"><span data-stu-id="9ae82-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="9ae82-118">Il secondo comando recupera la macchina virtuale denominata VirtualMachine11 nel servizio denominato Service02 e quindi la passa al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="9ae82-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="9ae82-119">Il cmdlet corrente configura le impostazioni di backup automatico in $AutoBackupConfig per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9ae82-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="9ae82-120">Il comando passa la macchina virtuale al cmdlet Update-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ae82-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="9ae82-121">Esempio 3: Disabilitare un'estensione SQL Server in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="9ae82-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="9ae82-122">Questo comando ottiene una macchina virtuale denominata VirtualMachine08 in Service03 e la passa al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="9ae82-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="9ae82-123">Il comando disabilita SQL Server'estensione della macchina virtuale in tale macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9ae82-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="9ae82-124">Esempio 4: Disinstallare un'estensione SQL Server in una macchina virtuale specifica</span><span class="sxs-lookup"><span data-stu-id="9ae82-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="9ae82-125">Questo comando ottiene una macchina virtuale denominata VirtualMachine08 in Service03 e la passa al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="9ae82-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="9ae82-126">Il comando disinstalla un'SQL Server di macchina virtuale specifica in tale macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9ae82-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="9ae82-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ae82-127">PARAMETERS</span></span>

### <span data-ttu-id="9ae82-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="9ae82-128">-AutoBackupSettings</span></span>
<span data-ttu-id="9ae82-129">Specifica le impostazioni di SQL Server di backup automatico.</span><span class="sxs-lookup"><span data-stu-id="9ae82-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="9ae82-130">Per creare un **oggetto AutoBackupSettings,** usare il cmdlet New-AzureVMSqlServerAutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="9ae82-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="9ae82-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="9ae82-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="9ae82-132">Specifica le impostazioni di SQL Server di distribuzione automatica delle patch.</span><span class="sxs-lookup"><span data-stu-id="9ae82-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="9ae82-133">Per creare un **oggetto AutoPatchingSettings,** usare il cmdlet New-AzureVMSqlServerAutoPatchingConfig AutoPatchingSettings.</span><span class="sxs-lookup"><span data-stu-id="9ae82-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="9ae82-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ae82-134">-DefaultProfile</span></span>
<span data-ttu-id="9ae82-135">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae82-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ae82-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="9ae82-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="9ae82-137">-Location</span><span class="sxs-lookup"><span data-stu-id="9ae82-137">-Location</span></span>
<span data-ttu-id="9ae82-138">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9ae82-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="9ae82-139">-Name</span><span class="sxs-lookup"><span data-stu-id="9ae82-139">-Name</span></span>
<span data-ttu-id="9ae82-140">Specifica il nome della SQL Server'estensione.</span><span class="sxs-lookup"><span data-stu-id="9ae82-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="9ae82-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ae82-141">-ResourceGroupName</span></span>
<span data-ttu-id="9ae82-142">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9ae82-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9ae82-143">-Version</span><span class="sxs-lookup"><span data-stu-id="9ae82-143">-Version</span></span>
<span data-ttu-id="9ae82-144">Specifica la versione dell'estensione SQL Server versione.</span><span class="sxs-lookup"><span data-stu-id="9ae82-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="9ae82-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="9ae82-145">-VMName</span></span>
<span data-ttu-id="9ae82-146">Specifica il nome della macchina virtuale in cui questo cmdlet imposta l SQL Server estensione.</span><span class="sxs-lookup"><span data-stu-id="9ae82-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="9ae82-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae82-147">CommonParameters</span></span>
<span data-ttu-id="9ae82-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ae82-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae82-149">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ae82-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae82-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="9ae82-150">INPUTS</span></span>

### <span data-ttu-id="9ae82-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9ae82-151">None</span></span>
<span data-ttu-id="9ae82-152">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="9ae82-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9ae82-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ae82-153">OUTPUTS</span></span>

### <span data-ttu-id="9ae82-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9ae82-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9ae82-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="9ae82-155">NOTES</span></span>

## <span data-ttu-id="9ae82-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ae82-156">RELATED LINKS</span></span>

[<span data-ttu-id="9ae82-157">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="9ae82-157">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="9ae82-158">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9ae82-158">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="9ae82-159">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="9ae82-159">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="9ae82-160">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="9ae82-160">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="9ae82-161">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9ae82-161">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="9ae82-162">Update-AZVM</span><span class="sxs-lookup"><span data-stu-id="9ae82-162">Update-AzVM</span></span>](./Update-AzVM.md)


