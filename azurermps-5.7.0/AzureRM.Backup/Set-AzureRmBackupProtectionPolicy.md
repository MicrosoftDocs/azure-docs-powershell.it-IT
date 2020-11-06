---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 7d41abd1d56bab4df0d716c3a9d11ea14140b784
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519905"
---
# <span data-ttu-id="73772-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="73772-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="73772-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73772-102">SYNOPSIS</span></span>
<span data-ttu-id="73772-103">Modifica i criteri di protezione esistenti.</span><span class="sxs-lookup"><span data-stu-id="73772-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73772-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73772-104">SYNTAX</span></span>

### <span data-ttu-id="73772-105">NoScheduleParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="73772-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73772-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="73772-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73772-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="73772-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73772-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73772-108">DESCRIPTION</span></span>
<span data-ttu-id="73772-109">Il cmdlet **set-AzureRmBackupProtectionPolicy** modifica i criteri di protezione esistenti in Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="73772-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="73772-110">È possibile modificare i seguenti componenti dei criteri di protezione:</span><span class="sxs-lookup"><span data-stu-id="73772-110">You can modify the following protection policy components:</span></span> 

- <span data-ttu-id="73772-111">Nome</span><span class="sxs-lookup"><span data-stu-id="73772-111">Name</span></span>
- <span data-ttu-id="73772-112">Pianificazione del backup</span><span class="sxs-lookup"><span data-stu-id="73772-112">Backup schedule</span></span>
- <span data-ttu-id="73772-113">Criteri di conservazione</span><span class="sxs-lookup"><span data-stu-id="73772-113">Retention policies</span></span>

<span data-ttu-id="73772-114">Qualsiasi modifica può influire sul backup e sulla conservazione degli elementi associati al criterio.</span><span class="sxs-lookup"><span data-stu-id="73772-114">Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="73772-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73772-115">EXAMPLES</span></span>

## <span data-ttu-id="73772-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73772-116">PARAMETERS</span></span>

### <span data-ttu-id="73772-117">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="73772-117">-BackupTime</span></span>
<span data-ttu-id="73772-118">Specifica la nuova ora di backup del giorno, come oggetto **DateTime** , per il criterio.</span><span class="sxs-lookup"><span data-stu-id="73772-118">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="73772-119">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="73772-119">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="73772-120">Per informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="73772-120">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73772-121">-Tutti i giorni</span><span class="sxs-lookup"><span data-stu-id="73772-121">-Daily</span></span>
<span data-ttu-id="73772-122">Indica che l'operazione di backup viene eseguita in una programmazione giornaliera.</span><span class="sxs-lookup"><span data-stu-id="73772-122">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73772-123">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="73772-123">-DaysOfWeek</span></span>
<span data-ttu-id="73772-124">Specifica una matrice di giorni della settimana.</span><span class="sxs-lookup"><span data-stu-id="73772-124">Specifies an array of days of the week.</span></span>
<span data-ttu-id="73772-125">Questo criterio esegue i backup nei giorni specificati da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="73772-125">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="73772-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="73772-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="73772-127">Lunedì</span><span class="sxs-lookup"><span data-stu-id="73772-127">Monday</span></span> 
- <span data-ttu-id="73772-128">Martedì</span><span class="sxs-lookup"><span data-stu-id="73772-128">Tuesday</span></span> 
- <span data-ttu-id="73772-129">Mercoledì</span><span class="sxs-lookup"><span data-stu-id="73772-129">Wednesday</span></span> 
- <span data-ttu-id="73772-130">Giovedì</span><span class="sxs-lookup"><span data-stu-id="73772-130">Thursday</span></span> 
- <span data-ttu-id="73772-131">Venerdì</span><span class="sxs-lookup"><span data-stu-id="73772-131">Friday</span></span> 
- <span data-ttu-id="73772-132">Sabato</span><span class="sxs-lookup"><span data-stu-id="73772-132">Saturday</span></span> 
- <span data-ttu-id="73772-133">Domenica</span><span class="sxs-lookup"><span data-stu-id="73772-133">Sunday</span></span>

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73772-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73772-134">-DefaultProfile</span></span>
<span data-ttu-id="73772-135">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="73772-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73772-136">-NewName</span><span class="sxs-lookup"><span data-stu-id="73772-136">-NewName</span></span>
<span data-ttu-id="73772-137">Specifica il nuovo nome per il criterio.</span><span class="sxs-lookup"><span data-stu-id="73772-137">Specifies the new name for the policy.</span></span>
<span data-ttu-id="73772-138">Questo nome deve essere univoco in un Vault.</span><span class="sxs-lookup"><span data-stu-id="73772-138">This name must be unique in a vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73772-139">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="73772-139">-ProtectionPolicy</span></span>
<span data-ttu-id="73772-140">Specifica i criteri di protezione modificati da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73772-140">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="73772-141">Per ottenere un oggetto **AzureRmBackupProtectionPolicy** , usa il cmdlet Get-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="73772-141">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73772-142">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="73772-142">-RetentionPolicy</span></span>
<span data-ttu-id="73772-143">Specifica una matrice di criteri di conservazione per i criteri di backup.</span><span class="sxs-lookup"><span data-stu-id="73772-143">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="73772-144">Per ottenere oggetti **AzureRmBackupRetentionPolicy** , usa il cmdlet New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="73772-144">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73772-145">-Settimanale</span><span class="sxs-lookup"><span data-stu-id="73772-145">-Weekly</span></span>
<span data-ttu-id="73772-146">Indica che l'operazione di backup viene eseguita in una programmazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="73772-146">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73772-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73772-147">CommonParameters</span></span>
<span data-ttu-id="73772-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73772-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73772-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73772-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73772-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73772-150">INPUTS</span></span>

### <span data-ttu-id="73772-151">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="73772-151">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="73772-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73772-152">OUTPUTS</span></span>

### <span data-ttu-id="73772-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="73772-153">None</span></span>

## <span data-ttu-id="73772-154">Note</span><span class="sxs-lookup"><span data-stu-id="73772-154">NOTES</span></span>

## <span data-ttu-id="73772-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73772-155">RELATED LINKS</span></span>

[<span data-ttu-id="73772-156">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="73772-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


