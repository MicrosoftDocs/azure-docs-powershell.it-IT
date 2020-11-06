---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: 83ed9062c5ad4beb0dff9c9c89b79a443cc68a52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509735"
---
# <span data-ttu-id="0f492-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="0f492-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="0f492-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f492-102">SYNOPSIS</span></span>
<span data-ttu-id="0f492-103">Ottiene un oggetto Criteri di conservazione di base.</span><span class="sxs-lookup"><span data-stu-id="0f492-103">Gets a base retention policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f492-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f492-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f492-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f492-105">DESCRIPTION</span></span>
<span data-ttu-id="0f492-106">Il cmdlet **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** ottiene un **AzureRMRecoveryServicesRetentionPolicyObject** di base.</span><span class="sxs-lookup"><span data-stu-id="0f492-106">The **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="0f492-107">Questo oggetto non viene mantenuto nel sistema.</span><span class="sxs-lookup"><span data-stu-id="0f492-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="0f492-108">Si tratta di un oggetto temporaneo che può essere manipolato e usato con il cmdlet New-AzureRmRecoveryServicesBackupProtectionPolicy per creare un nuovo criterio di backup.</span><span class="sxs-lookup"><span data-stu-id="0f492-108">It is a temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="0f492-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f492-109">EXAMPLES</span></span>

### <span data-ttu-id="0f492-110">Esempio 1: creare un criterio di protezione del backup</span><span class="sxs-lookup"><span data-stu-id="0f492-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="0f492-111">Il primo comando ottiene l'oggetto Criteri di conservazione e lo archivia nella variabile $RetPol.</span><span class="sxs-lookup"><span data-stu-id="0f492-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="0f492-112">Il secondo comando imposta la durata dell'oggetto Criteri di conservazione su 365 giorni.</span><span class="sxs-lookup"><span data-stu-id="0f492-112">The second command sets the duration for the retention policy object to 365 days.</span></span>

<span data-ttu-id="0f492-113">Il terzo comando ottiene l'oggetto Criteri di pianificazione e lo archivia nella variabile $SchPol.</span><span class="sxs-lookup"><span data-stu-id="0f492-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="0f492-114">L'ultimo comando crea un criterio di protezione del backup usando i criteri di conservazione e i criteri di pianificazione creati con i comandi precedenti.</span><span class="sxs-lookup"><span data-stu-id="0f492-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="0f492-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f492-115">PARAMETERS</span></span>

### <span data-ttu-id="0f492-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="0f492-116">-BackupManagementType</span></span>
<span data-ttu-id="0f492-117">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="0f492-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="0f492-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0f492-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f492-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="0f492-119">AzureVM</span></span> 
- <span data-ttu-id="0f492-120">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="0f492-120">AzureSQLDatabase</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f492-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f492-121">-DefaultProfile</span></span>
<span data-ttu-id="0f492-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f492-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f492-123">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="0f492-123">-WorkloadType</span></span>
<span data-ttu-id="0f492-124">Specifica il tipo di carico di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0f492-124">Specifies the workload type.</span></span>
<span data-ttu-id="0f492-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0f492-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f492-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="0f492-126">AzureVM</span></span> 
- <span data-ttu-id="0f492-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="0f492-127">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f492-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f492-128">CommonParameters</span></span>
<span data-ttu-id="0f492-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f492-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f492-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f492-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f492-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f492-131">INPUTS</span></span>

### <span data-ttu-id="0f492-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0f492-132">None</span></span>
<span data-ttu-id="0f492-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0f492-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0f492-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f492-134">OUTPUTS</span></span>

### <span data-ttu-id="0f492-135">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="0f492-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="0f492-136">Note</span><span class="sxs-lookup"><span data-stu-id="0f492-136">NOTES</span></span>

## <span data-ttu-id="0f492-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f492-137">RELATED LINKS</span></span>

[<span data-ttu-id="0f492-138">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="0f492-138">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="0f492-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0f492-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)


