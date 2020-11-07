---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 4093e236f84d7587586ba30c8bd4653c4ba7358f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863349"
---
# <span data-ttu-id="8b83b-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8b83b-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="8b83b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b83b-102">SYNOPSIS</span></span>
<span data-ttu-id="8b83b-103">Imposta l'estensione di Azure SQL Server in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b83b-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="8b83b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b83b-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b83b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b83b-105">DESCRIPTION</span></span>
<span data-ttu-id="8b83b-106">Il cmdlet **set-AzVMSqlServerExtension** imposta l'estensione del server AzureSQL in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b83b-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="8b83b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b83b-107">EXAMPLES</span></span>

### <span data-ttu-id="8b83b-108">Esempio 1: impostare le impostazioni di correzione automatica in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="8b83b-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="8b83b-109">Il primo comando crea un oggetto Configuration usando il cmdlet **New-AzureVMSqlServerAutoPatchingConfig** .</span><span class="sxs-lookup"><span data-stu-id="8b83b-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="8b83b-110">Il comando Archivia la configurazione nella variabile $AutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="8b83b-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="8b83b-111">Il secondo comando consente di ottenere la macchina virtuale denominata VirtualMachine11 nel servizio denominato Service02 usando il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8b83b-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="8b83b-112">Il comando passa l'oggetto al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="8b83b-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="8b83b-113">Il cmdlet corrente imposta le impostazioni di correzione automatica in $AutoPatchingConfig per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b83b-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="8b83b-114">Il comando passa la macchina virtuale al cmdlet Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8b83b-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="8b83b-115">Esempio 2: impostare le impostazioni di backup automatico in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="8b83b-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="8b83b-116">Il primo comando crea un oggetto Configuration usando il cmdlet **New-AzureVMSqlServerAutoBackupConfig** .</span><span class="sxs-lookup"><span data-stu-id="8b83b-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="8b83b-117">Il comando Archivia la configurazione nella variabile $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="8b83b-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="8b83b-118">Il secondo comando consente di ottenere la macchina virtuale denominata VirtualMachine11 nel servizio denominato Service02 e quindi di passarla al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="8b83b-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="8b83b-119">Il cmdlet Current imposta le impostazioni di backup automatico in $AutoBackupConfig per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b83b-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="8b83b-120">Il comando passa la macchina virtuale al cmdlet Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8b83b-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="8b83b-121">Esempio 3: disabilitare un'estensione di SQL Server in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="8b83b-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="8b83b-122">Questo comando consente di ottenere una macchina virtuale denominata VirtualMachine08 in Service03 e quindi di passarla al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="8b83b-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="8b83b-123">Il comando Disabilita l'estensione della macchina virtuale di SQL Server in quella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b83b-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="8b83b-124">Esempio 4: disinstallare un'estensione di SQL Server in una specifica macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="8b83b-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="8b83b-125">Questo comando consente di ottenere una macchina virtuale denominata VirtualMachine08 in Service03 e quindi di passarla al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="8b83b-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="8b83b-126">Il comando disinstalla un'estensione della macchina virtuale di SQL Server in quella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b83b-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="8b83b-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b83b-127">PARAMETERS</span></span>

### <span data-ttu-id="8b83b-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="8b83b-128">-AutoBackupSettings</span></span>
<span data-ttu-id="8b83b-129">Specifica le impostazioni di backup automatico di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8b83b-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="8b83b-130">Per creare un oggetto **AutoBackupSettings** , usa il cmdlet New-AzureVMSqlServerAutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="8b83b-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="8b83b-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="8b83b-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="8b83b-132">Specifica le impostazioni di correzione automatica di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8b83b-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="8b83b-133">Per creare un oggetto **AutoPatchingSettings** , usa il cmdlet New-AzureVMSqlServerAutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="8b83b-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="8b83b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b83b-134">-DefaultProfile</span></span>
<span data-ttu-id="8b83b-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b83b-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b83b-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="8b83b-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="8b83b-137">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8b83b-137">-Location</span></span>
<span data-ttu-id="8b83b-138">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b83b-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="8b83b-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b83b-139">-Name</span></span>
<span data-ttu-id="8b83b-140">Specifica il nome dell'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8b83b-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="8b83b-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b83b-141">-ResourceGroupName</span></span>
<span data-ttu-id="8b83b-142">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b83b-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8b83b-143">-Versione</span><span class="sxs-lookup"><span data-stu-id="8b83b-143">-Version</span></span>
<span data-ttu-id="8b83b-144">Specifica la versione dell'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8b83b-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="8b83b-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="8b83b-145">-VMName</span></span>
<span data-ttu-id="8b83b-146">Specifica il nome della macchina virtuale in cui questo cmdlet imposta l'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8b83b-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="8b83b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b83b-147">CommonParameters</span></span>
<span data-ttu-id="8b83b-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b83b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b83b-149">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b83b-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b83b-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b83b-150">INPUTS</span></span>

### <span data-ttu-id="8b83b-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8b83b-151">None</span></span>
<span data-ttu-id="8b83b-152">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8b83b-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8b83b-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b83b-153">OUTPUTS</span></span>

### <span data-ttu-id="8b83b-154">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8b83b-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8b83b-155">Note</span><span class="sxs-lookup"><span data-stu-id="8b83b-155">NOTES</span></span>

## <span data-ttu-id="8b83b-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b83b-156">RELATED LINKS</span></span>

[<span data-ttu-id="8b83b-157">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8b83b-157">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="8b83b-158">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8b83b-158">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="8b83b-159">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="8b83b-159">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="8b83b-160">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="8b83b-160">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="8b83b-161">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8b83b-161">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="8b83b-162">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8b83b-162">Update-AzVM</span></span>](./Update-AzVM.md)


