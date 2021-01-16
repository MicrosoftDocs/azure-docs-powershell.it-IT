---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: d66b8515c6b2c3782c6f6c2b49d462dbb7bd1660
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476719"
---
# <span data-ttu-id="eb8a5-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="eb8a5-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="eb8a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb8a5-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8a5-103">Ottiene un oggetto Criteri di pianificazione di base.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="eb8a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb8a5-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb8a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb8a5-105">DESCRIPTION</span></span>
<span data-ttu-id="eb8a5-106">Il cmdlet **Get-AzRecoveryServicesBackupSchedulePolicyObject** ottiene un **AzureRMRecoveryServicesSchedulePolicyObject** di base.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="eb8a5-107">Questo oggetto non viene mantenuto nel sistema.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="eb8a5-108">È un oggetto temporaneo che puoi modificare e usare con il cmdlet New-AzRecoveryServicesBackupProtectionPolicy per creare un nuovo criterio di protezione del backup.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="eb8a5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb8a5-109">EXAMPLES</span></span>

### <span data-ttu-id="eb8a5-110">Esempio 1: impostare la frequenza di programmazione su settimanale</span><span class="sxs-lookup"><span data-stu-id="eb8a5-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="eb8a5-111">Il primo comando ottiene l'oggetto Criteri di conservazione e lo archivia nella variabile $RetPol.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="eb8a5-112">Il secondo comando ottiene l'oggetto Criteri di pianificazione e lo archivia nella variabile $SchPol.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="eb8a5-113">Il terzo comando cambia la frequenza per i criteri di pianificazione su Weekly.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="eb8a5-114">L'ultimo comando crea un criterio di protezione del backup con la pianificazione aggiornata.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="eb8a5-115">Esempio 2: impostare il tempo di backup</span><span class="sxs-lookup"><span data-stu-id="eb8a5-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="eb8a5-116">Il primo comando ottiene l'oggetto Criteri di pianificazione e lo archivia nella variabile $SchPol.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="eb8a5-117">Il secondo comando rimuove tutti i tempi di esecuzione pianificati da $SchPol.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="eb8a5-118">Il terzo comando ottiene la data e l'ora correnti e lo archivia nella variabile $DT.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="eb8a5-119">Il quarto comando sostituisce gli orari di esecuzione pianificati con l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="eb8a5-120">È possibile eseguire il backup solo AzureVM una volta al giorno, quindi per reimpostare il tempo di backup è necessario sostituire la pianificazione originale.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="eb8a5-121">L'ultimo comando crea un criterio di protezione del backup usando la nuova pianificazione.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="eb8a5-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb8a5-122">PARAMETERS</span></span>

### <span data-ttu-id="eb8a5-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="eb8a5-123">-BackupManagementType</span></span>
<span data-ttu-id="eb8a5-124">Classe di risorse protette.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-124">The class of resources being protected.</span></span> <span data-ttu-id="eb8a5-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="eb8a5-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb8a5-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="eb8a5-126">AzureVM</span></span> 
- <span data-ttu-id="eb8a5-127">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="eb8a5-127">AzureStorage</span></span>
- <span data-ttu-id="eb8a5-128">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="eb8a5-128">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8a5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb8a5-129">-DefaultProfile</span></span>
<span data-ttu-id="eb8a5-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb8a5-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="eb8a5-131">-WorkloadType</span></span>
<span data-ttu-id="eb8a5-132">Tipo di carico di lavoro della risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-132">Workload type of the resource.</span></span> <span data-ttu-id="eb8a5-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="eb8a5-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb8a5-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="eb8a5-134">AzureVM</span></span> 
- <span data-ttu-id="eb8a5-135">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="eb8a5-135">AzureFiles</span></span>
- <span data-ttu-id="eb8a5-136">MSSQL</span><span class="sxs-lookup"><span data-stu-id="eb8a5-136">MSSQL</span></span>


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8a5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8a5-137">CommonParameters</span></span>
<span data-ttu-id="eb8a5-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb8a5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8a5-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb8a5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8a5-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb8a5-140">INPUTS</span></span>

### <span data-ttu-id="eb8a5-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="eb8a5-141">None</span></span>

## <span data-ttu-id="eb8a5-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb8a5-142">OUTPUTS</span></span>

### <span data-ttu-id="eb8a5-143">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="eb8a5-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="eb8a5-144">Note</span><span class="sxs-lookup"><span data-stu-id="eb8a5-144">NOTES</span></span>

## <span data-ttu-id="eb8a5-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb8a5-145">RELATED LINKS</span></span>

[<span data-ttu-id="eb8a5-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="eb8a5-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="eb8a5-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="eb8a5-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


