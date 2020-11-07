---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 71650d36c319536db5ad96aa142e2712e229d712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677643"
---
# <span data-ttu-id="d2749-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="d2749-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="d2749-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2749-102">SYNOPSIS</span></span>
<span data-ttu-id="d2749-103">Ottiene un oggetto Criteri di pianificazione di base.</span><span class="sxs-lookup"><span data-stu-id="d2749-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="d2749-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2749-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2749-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2749-105">DESCRIPTION</span></span>
<span data-ttu-id="d2749-106">Il cmdlet **Get-AzRecoveryServicesBackupSchedulePolicyObject** ottiene un **AzureRMRecoveryServicesSchedulePolicyObject** di base.</span><span class="sxs-lookup"><span data-stu-id="d2749-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="d2749-107">Questo oggetto non viene mantenuto nel sistema.</span><span class="sxs-lookup"><span data-stu-id="d2749-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="d2749-108">È un oggetto temporaneo che puoi modificare e usare con il cmdlet New-AzRecoveryServicesBackupProtectionPolicy per creare un nuovo criterio di protezione del backup.</span><span class="sxs-lookup"><span data-stu-id="d2749-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="d2749-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2749-109">EXAMPLES</span></span>

### <span data-ttu-id="d2749-110">Esempio 1: impostare la frequenza di programmazione su settimanale</span><span class="sxs-lookup"><span data-stu-id="d2749-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="d2749-111">Il primo comando ottiene l'oggetto Criteri di conservazione e lo archivia nella variabile $RetPol.</span><span class="sxs-lookup"><span data-stu-id="d2749-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="d2749-112">Il secondo comando ottiene l'oggetto Criteri di pianificazione e lo archivia nella variabile $SchPol.</span><span class="sxs-lookup"><span data-stu-id="d2749-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="d2749-113">Il terzo comando cambia la frequenza per i criteri di pianificazione su Weekly.</span><span class="sxs-lookup"><span data-stu-id="d2749-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="d2749-114">L'ultimo comando crea un criterio di protezione del backup con la pianificazione aggiornata.</span><span class="sxs-lookup"><span data-stu-id="d2749-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="d2749-115">Esempio 2: impostare il tempo di backup</span><span class="sxs-lookup"><span data-stu-id="d2749-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="d2749-116">Il primo comando ottiene l'oggetto Criteri di pianificazione e lo archivia nella variabile $SchPol.</span><span class="sxs-lookup"><span data-stu-id="d2749-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="d2749-117">Il secondo comando rimuove tutti i tempi di esecuzione pianificati da $SchPol.</span><span class="sxs-lookup"><span data-stu-id="d2749-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="d2749-118">Il terzo comando ottiene la data e l'ora correnti e lo archivia nella variabile $DT.</span><span class="sxs-lookup"><span data-stu-id="d2749-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="d2749-119">Il quarto comando sostituisce gli orari di esecuzione pianificati con l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="d2749-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="d2749-120">È possibile eseguire il backup solo AzureVM una volta al giorno, quindi per reimpostare il tempo di backup è necessario sostituire la pianificazione originale.</span><span class="sxs-lookup"><span data-stu-id="d2749-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="d2749-121">L'ultimo comando crea un criterio di protezione del backup usando la nuova pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d2749-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="d2749-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2749-122">PARAMETERS</span></span>

### <span data-ttu-id="d2749-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d2749-123">-BackupManagementType</span></span>
<span data-ttu-id="d2749-124">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="d2749-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="d2749-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d2749-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d2749-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="d2749-126">AzureVM</span></span> 
- <span data-ttu-id="d2749-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="d2749-127">AzureSQLDatabase</span></span>
- <span data-ttu-id="d2749-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="d2749-128">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2749-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2749-129">-DefaultProfile</span></span>
<span data-ttu-id="d2749-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2749-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2749-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d2749-131">-WorkloadType</span></span>
<span data-ttu-id="d2749-132">Specifica il tipo di carico di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d2749-132">Specifies the workload type.</span></span>
<span data-ttu-id="d2749-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d2749-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d2749-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="d2749-134">AzureVM</span></span> 
- <span data-ttu-id="d2749-135">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="d2749-135">AzureSQLDatabase</span></span>
- <span data-ttu-id="d2749-136">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="d2749-136">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2749-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2749-137">CommonParameters</span></span>
<span data-ttu-id="d2749-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2749-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2749-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2749-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2749-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2749-140">INPUTS</span></span>

### <span data-ttu-id="d2749-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d2749-141">None</span></span>

## <span data-ttu-id="d2749-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2749-142">OUTPUTS</span></span>

### <span data-ttu-id="d2749-143">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="d2749-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="d2749-144">Note</span><span class="sxs-lookup"><span data-stu-id="d2749-144">NOTES</span></span>

## <span data-ttu-id="d2749-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2749-145">RELATED LINKS</span></span>

[<span data-ttu-id="d2749-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d2749-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="d2749-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d2749-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


