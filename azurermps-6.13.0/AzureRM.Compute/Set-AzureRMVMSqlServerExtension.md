---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: 61aa9673121f53f36d5c2994db348160eac55cd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687351"
---
# <span data-ttu-id="5a97a-101">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5a97a-101">Set-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="5a97a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a97a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a97a-103">Imposta l'estensione di Azure SQL Server in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5a97a-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a97a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a97a-104">SYNTAX</span></span>

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a97a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a97a-105">DESCRIPTION</span></span>
<span data-ttu-id="5a97a-106">Il cmdlet **set-AzureRmVMSqlServerExtension** imposta l'estensione del server AzureSQL in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5a97a-106">The **Set-AzureRmVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="5a97a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a97a-107">EXAMPLES</span></span>

### <span data-ttu-id="5a97a-108">Esempio 1: impostare le impostazioni di correzione automatica in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="5a97a-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

<span data-ttu-id="5a97a-109">Il primo comando crea un oggetto Configuration usando il cmdlet **New-AzureVMSqlServerAutoPatchingConfig** .</span><span class="sxs-lookup"><span data-stu-id="5a97a-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="5a97a-110">Il comando Archivia la configurazione nella variabile $AutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="5a97a-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="5a97a-111">Il secondo comando consente di ottenere la macchina virtuale denominata VirtualMachine11 nel servizio denominato Service02 usando il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="5a97a-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="5a97a-112">Il comando passa l'oggetto al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="5a97a-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5a97a-113">Il cmdlet corrente imposta le impostazioni di correzione automatica in $AutoPatchingConfig per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5a97a-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="5a97a-114">Il comando passa la macchina virtuale al cmdlet Update-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="5a97a-114">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="5a97a-115">Esempio 2: impostare le impostazioni di backup automatico in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="5a97a-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

<span data-ttu-id="5a97a-116">Il primo comando crea un oggetto Configuration usando il cmdlet **New-AzureVMSqlServerAutoBackupConfig** .</span><span class="sxs-lookup"><span data-stu-id="5a97a-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="5a97a-117">Il comando Archivia la configurazione nella variabile $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="5a97a-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="5a97a-118">Il secondo comando consente di ottenere la macchina virtuale denominata VirtualMachine11 nel servizio denominato Service02 e quindi di passarla al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="5a97a-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5a97a-119">Il cmdlet Current imposta le impostazioni di backup automatico in $AutoBackupConfig per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5a97a-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="5a97a-120">Il comando passa la macchina virtuale al cmdlet Update-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="5a97a-120">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="5a97a-121">Esempio 3: disabilitare un'estensione di SQL Server in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="5a97a-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

<span data-ttu-id="5a97a-122">Questo comando consente di ottenere una macchina virtuale denominata VirtualMachine08 in Service03 e quindi di passarla al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="5a97a-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5a97a-123">Il comando Disabilita l'estensione della macchina virtuale di SQL Server in quella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5a97a-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="5a97a-124">Esempio 4: disinstallare un'estensione di SQL Server in una specifica macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="5a97a-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
```

<span data-ttu-id="5a97a-125">Questo comando consente di ottenere una macchina virtuale denominata VirtualMachine08 in Service03 e quindi di passarla al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="5a97a-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5a97a-126">Il comando disinstalla un'estensione della macchina virtuale di SQL Server in quella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5a97a-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="5a97a-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a97a-127">PARAMETERS</span></span>

### <span data-ttu-id="5a97a-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="5a97a-128">-AutoBackupSettings</span></span>
<span data-ttu-id="5a97a-129">Specifica le impostazioni di backup automatico di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5a97a-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="5a97a-130">Per creare un oggetto **AutoBackupSettings** , usa il cmdlet New-AzureVMSqlServerAutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="5a97a-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="5a97a-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="5a97a-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="5a97a-132">Specifica le impostazioni di correzione automatica di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5a97a-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="5a97a-133">Per creare un oggetto **AutoPatchingSettings** , usa il cmdlet New-AzureVMSqlServerAutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="5a97a-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="5a97a-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a97a-134">-DefaultProfile</span></span>
<span data-ttu-id="5a97a-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a97a-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a97a-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="5a97a-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="5a97a-137">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5a97a-137">-Location</span></span>
<span data-ttu-id="5a97a-138">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5a97a-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="5a97a-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a97a-139">-Name</span></span>
<span data-ttu-id="5a97a-140">Specifica il nome dell'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5a97a-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="5a97a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a97a-141">-ResourceGroupName</span></span>
<span data-ttu-id="5a97a-142">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5a97a-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5a97a-143">-Versione</span><span class="sxs-lookup"><span data-stu-id="5a97a-143">-Version</span></span>
<span data-ttu-id="5a97a-144">Specifica la versione dell'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5a97a-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="5a97a-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="5a97a-145">-VMName</span></span>
<span data-ttu-id="5a97a-146">Specifica il nome della macchina virtuale in cui questo cmdlet imposta l'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5a97a-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="5a97a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a97a-147">CommonParameters</span></span>
<span data-ttu-id="5a97a-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a97a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a97a-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a97a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a97a-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a97a-150">INPUTS</span></span>

### <span data-ttu-id="5a97a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="5a97a-151">System.String</span></span>

### <span data-ttu-id="5a97a-152">Microsoft. Azure. Commands. Compute. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="5a97a-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="5a97a-153">Microsoft. Azure. Commands. Compute. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="5a97a-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="5a97a-154">Microsoft. Azure. Commands. Compute. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="5a97a-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="5a97a-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a97a-155">OUTPUTS</span></span>

### <span data-ttu-id="5a97a-156">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5a97a-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5a97a-157">Note</span><span class="sxs-lookup"><span data-stu-id="5a97a-157">NOTES</span></span>

## <span data-ttu-id="5a97a-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a97a-158">RELATED LINKS</span></span>

[<span data-ttu-id="5a97a-159">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a97a-159">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="5a97a-160">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5a97a-160">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="5a97a-161">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="5a97a-161">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="5a97a-162">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="5a97a-162">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="5a97a-163">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5a97a-163">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="5a97a-164">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a97a-164">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


