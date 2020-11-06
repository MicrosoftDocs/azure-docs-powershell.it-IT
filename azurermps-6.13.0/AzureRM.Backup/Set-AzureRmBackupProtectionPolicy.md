---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: caf6394ce84b18bd8e36b4504173fe7f7bb07fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511952"
---
# <span data-ttu-id="c3409-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3409-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="c3409-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3409-102">SYNOPSIS</span></span>
<span data-ttu-id="c3409-103">Modifica i criteri di protezione esistenti.</span><span class="sxs-lookup"><span data-stu-id="c3409-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3409-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3409-104">SYNTAX</span></span>

### <span data-ttu-id="c3409-105">NoScheduleParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c3409-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3409-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="c3409-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3409-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="c3409-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3409-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3409-108">DESCRIPTION</span></span>
<span data-ttu-id="c3409-109">Il cmdlet **set-AzureRmBackupProtectionPolicy** modifica i criteri di protezione esistenti in Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="c3409-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="c3409-110">È possibile modificare i seguenti componenti dei criteri di protezione:</span><span class="sxs-lookup"><span data-stu-id="c3409-110">You can modify the following protection policy components:</span></span> 
- <span data-ttu-id="c3409-111">Nome</span><span class="sxs-lookup"><span data-stu-id="c3409-111">Name</span></span>
- <span data-ttu-id="c3409-112">Pianificazione del backup</span><span class="sxs-lookup"><span data-stu-id="c3409-112">Backup schedule</span></span>
- <span data-ttu-id="c3409-113">Criteri di conservazione qualsiasi modifica può influire sul backup e sulla conservazione degli elementi associati al criterio.</span><span class="sxs-lookup"><span data-stu-id="c3409-113">Retention policies Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="c3409-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3409-114">EXAMPLES</span></span>

## <span data-ttu-id="c3409-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3409-115">PARAMETERS</span></span>

### <span data-ttu-id="c3409-116">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="c3409-116">-BackupTime</span></span>
<span data-ttu-id="c3409-117">Specifica la nuova ora di backup del giorno, come oggetto **DateTime** , per il criterio.</span><span class="sxs-lookup"><span data-stu-id="c3409-117">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="c3409-118">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="c3409-118">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="c3409-119">Per informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="c3409-119">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3409-120">-Tutti i giorni</span><span class="sxs-lookup"><span data-stu-id="c3409-120">-Daily</span></span>
<span data-ttu-id="c3409-121">Indica che l'operazione di backup viene eseguita in una programmazione giornaliera.</span><span class="sxs-lookup"><span data-stu-id="c3409-121">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3409-122">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="c3409-122">-DaysOfWeek</span></span>
<span data-ttu-id="c3409-123">Specifica una matrice di giorni della settimana.</span><span class="sxs-lookup"><span data-stu-id="c3409-123">Specifies an array of days of the week.</span></span>
<span data-ttu-id="c3409-124">Questo criterio esegue i backup nei giorni specificati da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c3409-124">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="c3409-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3409-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c3409-126">Lunedì</span><span class="sxs-lookup"><span data-stu-id="c3409-126">Monday</span></span> 
- <span data-ttu-id="c3409-127">Martedì</span><span class="sxs-lookup"><span data-stu-id="c3409-127">Tuesday</span></span> 
- <span data-ttu-id="c3409-128">Mercoledì</span><span class="sxs-lookup"><span data-stu-id="c3409-128">Wednesday</span></span> 
- <span data-ttu-id="c3409-129">Giovedì</span><span class="sxs-lookup"><span data-stu-id="c3409-129">Thursday</span></span> 
- <span data-ttu-id="c3409-130">Venerdì</span><span class="sxs-lookup"><span data-stu-id="c3409-130">Friday</span></span> 
- <span data-ttu-id="c3409-131">Sabato</span><span class="sxs-lookup"><span data-stu-id="c3409-131">Saturday</span></span> 
- <span data-ttu-id="c3409-132">Domenica</span><span class="sxs-lookup"><span data-stu-id="c3409-132">Sunday</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3409-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3409-133">-DefaultProfile</span></span>
<span data-ttu-id="c3409-134">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c3409-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3409-135">-NewName</span><span class="sxs-lookup"><span data-stu-id="c3409-135">-NewName</span></span>
<span data-ttu-id="c3409-136">Specifica il nuovo nome per il criterio.</span><span class="sxs-lookup"><span data-stu-id="c3409-136">Specifies the new name for the policy.</span></span>
<span data-ttu-id="c3409-137">Questo nome deve essere univoco in un Vault.</span><span class="sxs-lookup"><span data-stu-id="c3409-137">This name must be unique in a vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3409-138">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3409-138">-ProtectionPolicy</span></span>
<span data-ttu-id="c3409-139">Specifica i criteri di protezione modificati da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3409-139">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="c3409-140">Per ottenere un oggetto **AzureRmBackupProtectionPolicy** , usa il cmdlet Get-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="c3409-140">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3409-141">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3409-141">-RetentionPolicy</span></span>
<span data-ttu-id="c3409-142">Specifica una matrice di criteri di conservazione per i criteri di backup.</span><span class="sxs-lookup"><span data-stu-id="c3409-142">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="c3409-143">Per ottenere oggetti **AzureRmBackupRetentionPolicy** , usa il cmdlet New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="c3409-143">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3409-144">-Settimanale</span><span class="sxs-lookup"><span data-stu-id="c3409-144">-Weekly</span></span>
<span data-ttu-id="c3409-145">Indica che l'operazione di backup viene eseguita in una programmazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="c3409-145">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3409-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3409-146">CommonParameters</span></span>
<span data-ttu-id="c3409-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3409-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3409-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3409-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3409-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3409-149">INPUTS</span></span>

### <span data-ttu-id="c3409-150">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3409-150">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>
<span data-ttu-id="c3409-151">Parametri: ProtectionPolicy (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c3409-151">Parameters: ProtectionPolicy (ByValue)</span></span>

## <span data-ttu-id="c3409-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3409-152">OUTPUTS</span></span>

### <span data-ttu-id="c3409-153">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="c3409-153">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="c3409-154">Note</span><span class="sxs-lookup"><span data-stu-id="c3409-154">NOTES</span></span>

## <span data-ttu-id="c3409-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3409-155">RELATED LINKS</span></span>

[<span data-ttu-id="c3409-156">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3409-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


