---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: d426cd18aaf3382939e55668b1c19938319a3c51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192967"
---
# <span data-ttu-id="94d49-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="94d49-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="94d49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94d49-102">SYNOPSIS</span></span>
<span data-ttu-id="94d49-103">Ottiene un oggetto criterio di conservazione di base.</span><span class="sxs-lookup"><span data-stu-id="94d49-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="94d49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94d49-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94d49-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="94d49-105">DESCRIPTION</span></span>
<span data-ttu-id="94d49-106">Il cmdlet **Get-AzRecoveryServicesBackupRetentionPolicyObject** ottiene un oggetto **Base AzureRMRecoveryServicesRetentionPolicyObject.**</span><span class="sxs-lookup"><span data-stu-id="94d49-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="94d49-107">Questo oggetto non viene mantenuto nel sistema.</span><span class="sxs-lookup"><span data-stu-id="94d49-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="94d49-108">Si tratta di un oggetto temporaneo che è possibile modificare e usare con il cmdlet New-AzRecoveryServicesBackupProtectionPolicy per creare un nuovo criterio di backup.</span><span class="sxs-lookup"><span data-stu-id="94d49-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="94d49-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94d49-109">EXAMPLES</span></span>

### <span data-ttu-id="94d49-110">Esempio 1: Creare criteri di protezione per il backup</span><span class="sxs-lookup"><span data-stu-id="94d49-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="94d49-111">Il primo comando ottiene l'oggetto criterio di conservazione e quindi lo archivia nella variabile $RetPol conservazione.</span><span class="sxs-lookup"><span data-stu-id="94d49-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="94d49-112">Il secondo comando imposta la durata per l'oggetto criterio di conservazione su 365 giorni.</span><span class="sxs-lookup"><span data-stu-id="94d49-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="94d49-113">Il terzo comando ottiene l'oggetto criterio di pianificazione e quindi lo archivia nella $SchPol variabile.</span><span class="sxs-lookup"><span data-stu-id="94d49-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="94d49-114">L'ultimo comando crea un criterio di protezione del backup usando i criteri di conservazione e i criteri di pianificazione creati con i comandi precedenti.</span><span class="sxs-lookup"><span data-stu-id="94d49-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="94d49-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94d49-115">PARAMETERS</span></span>

### <span data-ttu-id="94d49-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="94d49-116">-BackupManagementType</span></span>
<span data-ttu-id="94d49-117">Classe di risorse protetta.</span><span class="sxs-lookup"><span data-stu-id="94d49-117">The class of resources being protected.</span></span> <span data-ttu-id="94d49-118">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="94d49-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="94d49-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="94d49-119">AzureVM</span></span> 
- <span data-ttu-id="94d49-120">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="94d49-120">AzureWorkload</span></span>
- <span data-ttu-id="94d49-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="94d49-121">AzureStorage</span></span>

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

### <span data-ttu-id="94d49-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d49-122">-DefaultProfile</span></span>
<span data-ttu-id="94d49-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94d49-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94d49-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="94d49-124">-WorkloadType</span></span>
<span data-ttu-id="94d49-125">Tipo di carico di lavoro della risorsa.</span><span class="sxs-lookup"><span data-stu-id="94d49-125">Workload type of the resource.</span></span> <span data-ttu-id="94d49-126">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="94d49-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="94d49-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="94d49-127">AzureVM</span></span> 
- <span data-ttu-id="94d49-128">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="94d49-128">AzureFiles</span></span>
- <span data-ttu-id="94d49-129">MSSQL</span><span class="sxs-lookup"><span data-stu-id="94d49-129">MSSQL</span></span>

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

### <span data-ttu-id="94d49-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d49-130">CommonParameters</span></span>
<span data-ttu-id="94d49-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94d49-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d49-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="94d49-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d49-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="94d49-133">INPUTS</span></span>

### <span data-ttu-id="94d49-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="94d49-134">None</span></span>

## <span data-ttu-id="94d49-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94d49-135">OUTPUTS</span></span>

### <span data-ttu-id="94d49-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="94d49-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="94d49-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="94d49-137">NOTES</span></span>

## <span data-ttu-id="94d49-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94d49-138">RELATED LINKS</span></span>

[<span data-ttu-id="94d49-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="94d49-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="94d49-140">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="94d49-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)


