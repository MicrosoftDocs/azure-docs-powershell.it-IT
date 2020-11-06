---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 4ea286ae6e3aec7f3eca961b5dc1452c717f3c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519919"
---
# <span data-ttu-id="7ab28-101">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ab28-101">New-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="7ab28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ab28-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab28-103">Crea un criterio di backup.</span><span class="sxs-lookup"><span data-stu-id="7ab28-103">Creates a Backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ab28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ab28-104">SYNTAX</span></span>

### <span data-ttu-id="7ab28-105">NoScheduleParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7ab28-105">NoScheduleParamSet (Default)</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ab28-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="7ab28-106">DailyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ab28-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="7ab28-107">WeeklyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ab28-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ab28-108">DESCRIPTION</span></span>
<span data-ttu-id="7ab28-109">Il cmdlet **New-AzureRmBackupProtectionPolicy** crea un criterio di backup di Azure come oggetto PowerShell di Azure.</span><span class="sxs-lookup"><span data-stu-id="7ab28-109">The **New-AzureRmBackupProtectionPolicy** cmdlet creates an Azure Backup policy as an Azure PowerShell object.</span></span>

<span data-ttu-id="7ab28-110">Un criterio di backup definisce quando e con quale frequenza viene eseguito il backup di un elemento.</span><span class="sxs-lookup"><span data-stu-id="7ab28-110">A backup policy defines when and how often Backup backs up an item.</span></span>
<span data-ttu-id="7ab28-111">Il cmdlet Enable-AzureRmBackupProtection usa un criterio di backup.</span><span class="sxs-lookup"><span data-stu-id="7ab28-111">The Enable-AzureRmBackupProtection cmdlet uses a backup policy.</span></span>

## <span data-ttu-id="7ab28-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ab28-112">EXAMPLES</span></span>

### <span data-ttu-id="7ab28-113">Esempio 1: creare criteri di backup giornalieri con la conservazione giornaliera e mensile</span><span class="sxs-lookup"><span data-stu-id="7ab28-113">Example 1: Create a daily backup policy with daily and monthly retention</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="7ab28-114">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="7ab28-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="7ab28-115">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="7ab28-115">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="7ab28-116">Il secondo comando crea un criterio di conservazione per 30 giorni di conservazione giornaliera e lo archivia nella variabile $Daily.</span><span class="sxs-lookup"><span data-stu-id="7ab28-116">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="7ab28-117">Il terzo comando crea un criterio di conservazione che mantiene il backup il decimo e il ventesimo di ogni mese per dodici mesi.</span><span class="sxs-lookup"><span data-stu-id="7ab28-117">The third command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="7ab28-118">Il comando Archivia i criteri di conservazione nella variabile $Monthly.</span><span class="sxs-lookup"><span data-stu-id="7ab28-118">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="7ab28-119">Il comando finale crea un criterio di backup per il Vault in $Vault che ha un tempo di backup giornaliero di 3:00 PM.</span><span class="sxs-lookup"><span data-stu-id="7ab28-119">The final command creates a backup policy for the vault in $Vault that has a daily backup time of 3:00 PM.</span></span>
<span data-ttu-id="7ab28-120">Il comando assegna i criteri di conservazione archiviati in $Daily e $Monthly.</span><span class="sxs-lookup"><span data-stu-id="7ab28-120">The command assigns the retention policies stored in $Daily and $Monthly.</span></span>
<span data-ttu-id="7ab28-121">Il comando Archivia il risultato nella variabile $ProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="7ab28-121">The command stores the result in the $ProtectionPolicy variable.</span></span>

## <span data-ttu-id="7ab28-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ab28-122">PARAMETERS</span></span>

### <span data-ttu-id="7ab28-123">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="7ab28-123">-BackupTime</span></span>
<span data-ttu-id="7ab28-124">Specifica l'ora del giorno, come oggetto **DateTime** , per l'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="7ab28-124">Specifies the time of day, as a **DateTime** object, for the backup operation.</span></span>
<span data-ttu-id="7ab28-125">Per ottenere un valore **DateTime** , usa il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="7ab28-125">To obtain a **DateTime** , use the Get-Date cmdlet.</span></span>
<span data-ttu-id="7ab28-126">Per informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="7ab28-126">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab28-127">-Tutti i giorni</span><span class="sxs-lookup"><span data-stu-id="7ab28-127">-Daily</span></span>
<span data-ttu-id="7ab28-128">Indica che l'operazione di backup viene eseguita in una programmazione giornaliera.</span><span class="sxs-lookup"><span data-stu-id="7ab28-128">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab28-129">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="7ab28-129">-DaysOfWeek</span></span>
<span data-ttu-id="7ab28-130">Specifica una matrice di giorni della settimana.</span><span class="sxs-lookup"><span data-stu-id="7ab28-130">Specifies an array of days of the week.</span></span>
<span data-ttu-id="7ab28-131">Questo criterio esegue i backup nei giorni specificati da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7ab28-131">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="7ab28-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ab28-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7ab28-133">Lunedì</span><span class="sxs-lookup"><span data-stu-id="7ab28-133">Monday</span></span> 
- <span data-ttu-id="7ab28-134">Martedì</span><span class="sxs-lookup"><span data-stu-id="7ab28-134">Tuesday</span></span> 
- <span data-ttu-id="7ab28-135">Mercoledì</span><span class="sxs-lookup"><span data-stu-id="7ab28-135">Wednesday</span></span> 
- <span data-ttu-id="7ab28-136">Giovedì</span><span class="sxs-lookup"><span data-stu-id="7ab28-136">Thursday</span></span> 
- <span data-ttu-id="7ab28-137">Venerdì</span><span class="sxs-lookup"><span data-stu-id="7ab28-137">Friday</span></span> 
- <span data-ttu-id="7ab28-138">Sabato</span><span class="sxs-lookup"><span data-stu-id="7ab28-138">Saturday</span></span> 
- <span data-ttu-id="7ab28-139">Domenica</span><span class="sxs-lookup"><span data-stu-id="7ab28-139">Sunday</span></span>

<span data-ttu-id="7ab28-140">Se si specifica il parametro *Weekly* , specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7ab28-140">If you specify the *Weekly* parameter, specify this parameter.</span></span>

```yaml
Type: String[]
Parameter Sets: NoScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab28-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab28-141">-DefaultProfile</span></span>
<span data-ttu-id="7ab28-142">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7ab28-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ab28-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ab28-143">-Name</span></span>
<span data-ttu-id="7ab28-144">Specifica un nome per i criteri di backup.</span><span class="sxs-lookup"><span data-stu-id="7ab28-144">Specifies a name for the backup policy.</span></span>
<span data-ttu-id="7ab28-145">Selezionare un nome univoco nel Vault.</span><span class="sxs-lookup"><span data-stu-id="7ab28-145">Select a name that is unique in the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab28-146">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ab28-146">-RetentionPolicy</span></span>
<span data-ttu-id="7ab28-147">Specifica una matrice di criteri di conservazione per i criteri di backup.</span><span class="sxs-lookup"><span data-stu-id="7ab28-147">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="7ab28-148">Per ottenere un **AzureRmBackupRetentionPolicy** , usare il cmdlet New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="7ab28-148">To obtain an **AzureRmBackupRetentionPolicy** , use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab28-149">-Digitare</span><span class="sxs-lookup"><span data-stu-id="7ab28-149">-Type</span></span>
<span data-ttu-id="7ab28-150">Specifica il tipo di elemento di backup a cui si applicano i criteri.</span><span class="sxs-lookup"><span data-stu-id="7ab28-150">Specifies the type of backup item to which the policy applies.</span></span>
<span data-ttu-id="7ab28-151">Attualmente, l'unico valore supportato è AzureVM.</span><span class="sxs-lookup"><span data-stu-id="7ab28-151">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab28-152">-Vault</span><span class="sxs-lookup"><span data-stu-id="7ab28-152">-Vault</span></span>
<span data-ttu-id="7ab28-153">Specifica il Vault di backup di Azure a cui appartiene il criterio di backup.</span><span class="sxs-lookup"><span data-stu-id="7ab28-153">Specifies the Azure Backup vault to which the backup policy belongs.</span></span>
<span data-ttu-id="7ab28-154">Per ottenere un oggetto **AzureRmBackupVault** , usa il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="7ab28-154">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab28-155">-Settimanale</span><span class="sxs-lookup"><span data-stu-id="7ab28-155">-Weekly</span></span>
<span data-ttu-id="7ab28-156">Indica che i criteri di backup vengono attivati settimanalmente in uno o più giorni della settimana.</span><span class="sxs-lookup"><span data-stu-id="7ab28-156">Indicates that the backup policy is triggered weekly on one or more days of the week.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab28-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab28-157">CommonParameters</span></span>
<span data-ttu-id="7ab28-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab28-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab28-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ab28-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab28-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ab28-160">INPUTS</span></span>

### <span data-ttu-id="7ab28-161">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7ab28-161">None</span></span>

## <span data-ttu-id="7ab28-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ab28-162">OUTPUTS</span></span>

### <span data-ttu-id="7ab28-163">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ab28-163">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="7ab28-164">Note</span><span class="sxs-lookup"><span data-stu-id="7ab28-164">NOTES</span></span>
* <span data-ttu-id="7ab28-165">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7ab28-165">None</span></span>

## <span data-ttu-id="7ab28-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ab28-166">RELATED LINKS</span></span>

[<span data-ttu-id="7ab28-167">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="7ab28-167">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="7ab28-168">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ab28-168">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="7ab28-169">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7ab28-169">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="7ab28-170">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="7ab28-170">New-AzureRmBackupRetentionPolicyObject</span></span>](./New-AzureRmBackupRetentionPolicyObject.md)

[<span data-ttu-id="7ab28-171">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ab28-171">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="7ab28-172">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ab28-172">Set-AzureRmBackupProtectionPolicy</span></span>](./Set-AzureRmBackupProtectionPolicy.md)


