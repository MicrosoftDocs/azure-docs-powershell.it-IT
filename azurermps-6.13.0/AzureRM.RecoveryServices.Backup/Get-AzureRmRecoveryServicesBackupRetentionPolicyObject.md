---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: 83eeeec861452407dae1a9d92e5bc900b98d6512
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517351"
---
# <span data-ttu-id="b06f7-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="b06f7-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="b06f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b06f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b06f7-103">Ottiene un oggetto Criteri di conservazione di base.</span><span class="sxs-lookup"><span data-stu-id="b06f7-103">Gets a base retention policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b06f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b06f7-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b06f7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b06f7-105">DESCRIPTION</span></span>
<span data-ttu-id="b06f7-106">Il cmdlet **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** ottiene un **AzureRMRecoveryServicesRetentionPolicyObject** di base.</span><span class="sxs-lookup"><span data-stu-id="b06f7-106">The **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="b06f7-107">Questo oggetto non viene mantenuto nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b06f7-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="b06f7-108">Si tratta di un oggetto temporaneo che può essere manipolato e usato con il cmdlet New-AzureRmRecoveryServicesBackupProtectionPolicy per creare un nuovo criterio di backup.</span><span class="sxs-lookup"><span data-stu-id="b06f7-108">It is a temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="b06f7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b06f7-109">EXAMPLES</span></span>

### <span data-ttu-id="b06f7-110">Esempio 1: creare un criterio di protezione del backup</span><span class="sxs-lookup"><span data-stu-id="b06f7-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="b06f7-111">Il primo comando ottiene l'oggetto Criteri di conservazione e lo archivia nella variabile $RetPol.</span><span class="sxs-lookup"><span data-stu-id="b06f7-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="b06f7-112">Il secondo comando imposta la durata dell'oggetto Criteri di conservazione su 365 giorni.</span><span class="sxs-lookup"><span data-stu-id="b06f7-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="b06f7-113">Il terzo comando ottiene l'oggetto Criteri di pianificazione e lo archivia nella variabile $SchPol.</span><span class="sxs-lookup"><span data-stu-id="b06f7-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="b06f7-114">L'ultimo comando crea un criterio di protezione del backup usando i criteri di conservazione e i criteri di pianificazione creati con i comandi precedenti.</span><span class="sxs-lookup"><span data-stu-id="b06f7-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="b06f7-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b06f7-115">PARAMETERS</span></span>

### <span data-ttu-id="b06f7-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="b06f7-116">-BackupManagementType</span></span>
<span data-ttu-id="b06f7-117">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="b06f7-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="b06f7-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b06f7-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b06f7-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b06f7-119">AzureVM</span></span> 
- <span data-ttu-id="b06f7-120">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="b06f7-120">AzureSQLDatabase</span></span>
- <span data-ttu-id="b06f7-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="b06f7-121">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b06f7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b06f7-122">-DefaultProfile</span></span>
<span data-ttu-id="b06f7-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b06f7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b06f7-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="b06f7-124">-WorkloadType</span></span>
<span data-ttu-id="b06f7-125">Specifica il tipo di carico di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b06f7-125">Specifies the workload type.</span></span>
<span data-ttu-id="b06f7-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b06f7-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b06f7-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b06f7-127">AzureVM</span></span> 
- <span data-ttu-id="b06f7-128">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="b06f7-128">AzureSQLDatabase</span></span>
- <span data-ttu-id="b06f7-129">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="b06f7-129">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b06f7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b06f7-130">CommonParameters</span></span>
<span data-ttu-id="b06f7-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b06f7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b06f7-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b06f7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b06f7-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b06f7-133">INPUTS</span></span>

### <span data-ttu-id="b06f7-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b06f7-134">None</span></span>

## <span data-ttu-id="b06f7-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b06f7-135">OUTPUTS</span></span>

### <span data-ttu-id="b06f7-136">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="b06f7-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="b06f7-137">Note</span><span class="sxs-lookup"><span data-stu-id="b06f7-137">NOTES</span></span>

## <span data-ttu-id="b06f7-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b06f7-138">RELATED LINKS</span></span>

[<span data-ttu-id="b06f7-139">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="b06f7-139">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="b06f7-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b06f7-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

