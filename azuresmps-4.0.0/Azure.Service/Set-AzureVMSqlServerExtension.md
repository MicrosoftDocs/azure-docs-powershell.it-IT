---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 56C7B6F5-C2AC-4C5A-8930-645374694CC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 053bb1bfb31b90a91d69e50b77ac6411321014f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023748"
---
# <span data-ttu-id="5031e-101">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5031e-101">Set-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="5031e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5031e-102">SYNOPSIS</span></span>
<span data-ttu-id="5031e-103">Imposta l'estensione di Azure SQL Server in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5031e-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="5031e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5031e-104">SYNTAX</span></span>

### <span data-ttu-id="5031e-105">EnableSqlServerExtension (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5031e-105">EnableSqlServerExtension (Default)</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>]
 [[-AutoPatchingSettings] <AutoPatchingSettings>] [[-AutoBackupSettings] <AutoBackupSettings>]
 [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5031e-106">DisableSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5031e-106">DisableSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5031e-107">UninstallSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5031e-107">UninstallSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5031e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5031e-108">DESCRIPTION</span></span>
<span data-ttu-id="5031e-109">Il cmdlet **set-AzureVMSqlServerExtension** imposta l'estensione di Azure SQL Server in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5031e-109">The **Set-AzureVMSqlServerExtension** cmdlet sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="5031e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5031e-110">EXAMPLES</span></span>

### <span data-ttu-id="5031e-111">Esempio 1: impostare le impostazioni di correzione automatica in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="5031e-111">Example 1: Set auto-patching settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoPatchingSettings $APS | Update-AzureVM
```

<span data-ttu-id="5031e-112">Questo comando imposta le impostazioni di correzione automatica in una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="5031e-112">This command sets auto-patching settings on an Azure virtual machine.</span></span>

### <span data-ttu-id="5031e-113">Esempio 2: impostare le impostazioni di backup automatico in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="5031e-113">Example 2: Set auto-backup settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoBackupSettings $ABS | Update-AzureVM
```

<span data-ttu-id="5031e-114">Questo comando imposta le impostazioni di backup automatico in Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="5031e-114">This command sets auto-backup settings on Azure virtual machine.</span></span>

### <span data-ttu-id="5031e-115">Esempio 3: disabilitare un'estensione di SQL Server in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="5031e-115">Example 3: Disable an SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Disable
```

<span data-ttu-id="5031e-116">Questo comando Disabilita l'estensione della macchina virtuale di SQL Server in una determinata macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5031e-116">This command disables SQL Server virtual machine extension on a given virtual machine.</span></span>

### <span data-ttu-id="5031e-117">Esempio 4: disinstallare un'estensione di SQL Server in una specifica macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="5031e-117">Example 4: Uninstall an SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Uninstall
```

<span data-ttu-id="5031e-118">Questo comando disinstalla un'estensione della macchina virtuale di SQL Server nella macchina virtuale denominata VMName.</span><span class="sxs-lookup"><span data-stu-id="5031e-118">This command uninstalls a SQL Server virtual machine extension on the virtual machine named VMName.</span></span>

## <span data-ttu-id="5031e-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5031e-119">PARAMETERS</span></span>

### <span data-ttu-id="5031e-120">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="5031e-120">-AutoBackupSettings</span></span>
<span data-ttu-id="5031e-121">Specifica le impostazioni di backup automatico di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5031e-121">Specifies the automatic SQL Server backup settings.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5031e-122">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="5031e-122">-AutoPatchingSettings</span></span>
<span data-ttu-id="5031e-123">Specifica le impostazioni di correzione automatica di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5031e-123">Specifies the automatic SQL Server patching settings.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5031e-124">-Disable</span><span class="sxs-lookup"><span data-stu-id="5031e-124">-Disable</span></span>
<span data-ttu-id="5031e-125">Indica che questo cmdlet disabilita lo stato dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="5031e-125">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5031e-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5031e-126">-InformationAction</span></span>
<span data-ttu-id="5031e-127">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="5031e-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5031e-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5031e-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5031e-129">Continuare</span><span class="sxs-lookup"><span data-stu-id="5031e-129">Continue</span></span>
- <span data-ttu-id="5031e-130">Ignora</span><span class="sxs-lookup"><span data-stu-id="5031e-130">Ignore</span></span>
- <span data-ttu-id="5031e-131">Informarsi</span><span class="sxs-lookup"><span data-stu-id="5031e-131">Inquire</span></span>
- <span data-ttu-id="5031e-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5031e-132">SilentlyContinue</span></span>
- <span data-ttu-id="5031e-133">Stop</span><span class="sxs-lookup"><span data-stu-id="5031e-133">Stop</span></span>
- <span data-ttu-id="5031e-134">Sospensione</span><span class="sxs-lookup"><span data-stu-id="5031e-134">Suspend</span></span>

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

### <span data-ttu-id="5031e-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5031e-135">-InformationVariable</span></span>
<span data-ttu-id="5031e-136">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="5031e-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5031e-137">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="5031e-137">-KeyVaultCredentialSettings</span></span>
<span data-ttu-id="5031e-138">Specifica le impostazioni delle credenziali del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="5031e-138">Specifies key vault credential settings.</span></span>

```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5031e-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="5031e-139">-Profile</span></span>
<span data-ttu-id="5031e-140">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5031e-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5031e-141">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="5031e-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5031e-142">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="5031e-142">-ReferenceName</span></span>
<span data-ttu-id="5031e-143">Specifica il nome di riferimento dell'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5031e-143">Specifies the reference name of the SQL Server extension.</span></span>

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

### <span data-ttu-id="5031e-144">-Disinstalla</span><span class="sxs-lookup"><span data-stu-id="5031e-144">-Uninstall</span></span>
<span data-ttu-id="5031e-145">Indica che questo cmdlet Disinstalla l'estensione di SQL Server dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5031e-145">Indicates that this cmdlet uninstalls the SQL Server extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5031e-146">-Versione</span><span class="sxs-lookup"><span data-stu-id="5031e-146">-Version</span></span>
<span data-ttu-id="5031e-147">Specifica la versione dell'estensione di SQL Server da cui Get-AzureVMSqlServerExtension recupera le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="5031e-147">Specifies the version of the SQL Server extension that Get-AzureVMSqlServerExtension retrieves settings from.</span></span>

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

### <span data-ttu-id="5031e-148">-VM</span><span class="sxs-lookup"><span data-stu-id="5031e-148">-VM</span></span>
<span data-ttu-id="5031e-149">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="5031e-149">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="5031e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5031e-150">CommonParameters</span></span>
<span data-ttu-id="5031e-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5031e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5031e-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5031e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5031e-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5031e-153">INPUTS</span></span>

## <span data-ttu-id="5031e-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5031e-154">OUTPUTS</span></span>

## <span data-ttu-id="5031e-155">Note</span><span class="sxs-lookup"><span data-stu-id="5031e-155">NOTES</span></span>

## <span data-ttu-id="5031e-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5031e-156">RELATED LINKS</span></span>

[<span data-ttu-id="5031e-157">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5031e-157">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="5031e-158">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5031e-158">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)


