---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: fcf5bec22dffc18d6c4f9950d8dfb3e5b37332a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687990"
---
# <span data-ttu-id="c327e-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="c327e-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="c327e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c327e-102">SYNOPSIS</span></span>
<span data-ttu-id="c327e-103">Ottiene un oggetto Criteri di pianificazione di base.</span><span class="sxs-lookup"><span data-stu-id="c327e-103">Gets a base schedule policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c327e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c327e-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c327e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c327e-105">DESCRIPTION</span></span>
<span data-ttu-id="c327e-106">Il cmdlet **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** ottiene un **AzureRMRecoveryServicesSchedulePolicyObject** di base.</span><span class="sxs-lookup"><span data-stu-id="c327e-106">The **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="c327e-107">Questo oggetto non viene mantenuto nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c327e-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="c327e-108">È un oggetto temporaneo che puoi modificare e usare con il cmdlet New-AzureRmRecoveryServicesBackupProtectionPolicy per creare un nuovo criterio di protezione del backup.</span><span class="sxs-lookup"><span data-stu-id="c327e-108">It is temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="c327e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c327e-109">EXAMPLES</span></span>

### <span data-ttu-id="c327e-110">Esempio 1: impostare la frequenza di programmazione su settimanale</span><span class="sxs-lookup"><span data-stu-id="c327e-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="c327e-111">Il primo comando ottiene l'oggetto Criteri di conservazione e lo archivia nella variabile $RetPol.</span><span class="sxs-lookup"><span data-stu-id="c327e-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="c327e-112">Il secondo comando ottiene l'oggetto Criteri di pianificazione e lo archivia nella variabile $SchPol.</span><span class="sxs-lookup"><span data-stu-id="c327e-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="c327e-113">Il terzo comando cambia la frequenza per i criteri di pianificazione su Weekly.</span><span class="sxs-lookup"><span data-stu-id="c327e-113">The third command changes the frequency for the schedule policy to weekly.</span></span>

<span data-ttu-id="c327e-114">L'ultimo comando crea un criterio di protezione del backup con la pianificazione aggiornata.</span><span class="sxs-lookup"><span data-stu-id="c327e-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="c327e-115">Esempio 2: impostare il tempo di backup</span><span class="sxs-lookup"><span data-stu-id="c327e-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="c327e-116">Il primo comando ottiene l'oggetto Criteri di pianificazione e lo archivia nella variabile $SchPol.</span><span class="sxs-lookup"><span data-stu-id="c327e-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="c327e-117">Il secondo comando rimuove tutti i tempi di esecuzione pianificati da $SchPol.</span><span class="sxs-lookup"><span data-stu-id="c327e-117">The second command removes all scheduled run times from $SchPol.</span></span>

<span data-ttu-id="c327e-118">Il terzo comando ottiene la data e l'ora correnti e lo archivia nella variabile $DT.</span><span class="sxs-lookup"><span data-stu-id="c327e-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>

<span data-ttu-id="c327e-119">Il quarto comando sostituisce gli orari di esecuzione pianificati con l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="c327e-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="c327e-120">È possibile eseguire il backup solo AzureVM una volta al giorno, quindi per reimpostare il tempo di backup è necessario sostituire la pianificazione originale.</span><span class="sxs-lookup"><span data-stu-id="c327e-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>

<span data-ttu-id="c327e-121">L'ultimo comando crea un criterio di protezione del backup usando la nuova pianificazione.</span><span class="sxs-lookup"><span data-stu-id="c327e-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="c327e-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c327e-122">PARAMETERS</span></span>

### <span data-ttu-id="c327e-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="c327e-123">-BackupManagementType</span></span>
<span data-ttu-id="c327e-124">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="c327e-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="c327e-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c327e-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c327e-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="c327e-126">AzureVM</span></span> 
- <span data-ttu-id="c327e-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="c327e-127">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c327e-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="c327e-128">-WorkloadType</span></span>
<span data-ttu-id="c327e-129">Specifica il tipo di carico di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c327e-129">Specifies the workload type.</span></span>
<span data-ttu-id="c327e-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c327e-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c327e-131">AzureVM</span><span class="sxs-lookup"><span data-stu-id="c327e-131">AzureVM</span></span> 
- <span data-ttu-id="c327e-132">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="c327e-132">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c327e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c327e-133">-DefaultProfile</span></span>
<span data-ttu-id="c327e-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c327e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c327e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c327e-135">CommonParameters</span></span>
<span data-ttu-id="c327e-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c327e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c327e-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c327e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c327e-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c327e-138">INPUTS</span></span>

## <span data-ttu-id="c327e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c327e-139">OUTPUTS</span></span>

### <span data-ttu-id="c327e-140">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="c327e-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="c327e-141">Note</span><span class="sxs-lookup"><span data-stu-id="c327e-141">NOTES</span></span>

## <span data-ttu-id="c327e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c327e-142">RELATED LINKS</span></span>

[<span data-ttu-id="c327e-143">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c327e-143">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="c327e-144">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c327e-144">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


