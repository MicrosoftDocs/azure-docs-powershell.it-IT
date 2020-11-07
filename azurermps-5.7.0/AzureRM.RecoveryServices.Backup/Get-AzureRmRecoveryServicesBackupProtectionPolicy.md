---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 3220ef801ff86a3fb95a4595efd8c94330bfcba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685610"
---
# <span data-ttu-id="55e05-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="55e05-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="55e05-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55e05-102">SYNOPSIS</span></span>
<span data-ttu-id="55e05-103">Ottiene i criteri di protezione del backup per un Vault.</span><span class="sxs-lookup"><span data-stu-id="55e05-103">Gets Backup protection policies for a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55e05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55e05-104">SYNTAX</span></span>

### <span data-ttu-id="55e05-105">NoParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="55e05-105">NoParamSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55e05-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="55e05-106">PolicyNameParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55e05-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="55e05-107">WorkloadParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55e05-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="55e05-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55e05-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55e05-109">DESCRIPTION</span></span>
<span data-ttu-id="55e05-110">Il cmdlet **Get-AzureRmRecoveryServicesBackupProtectionPolicy** ottiene i criteri di protezione del backup di Azure per un Vault.</span><span class="sxs-lookup"><span data-stu-id="55e05-110">The **Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>

<span data-ttu-id="55e05-111">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="55e05-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="55e05-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55e05-112">EXAMPLES</span></span>

### <span data-ttu-id="55e05-113">Esempio 1: ottenere tutti i criteri nel Vault</span><span class="sxs-lookup"><span data-stu-id="55e05-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="55e05-114">Questo comando consente di ottenere tutti i criteri di protezione creati nel Vault.</span><span class="sxs-lookup"><span data-stu-id="55e05-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="55e05-115">Esempio 2: ottenere un criterio specifico</span><span class="sxs-lookup"><span data-stu-id="55e05-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="55e05-116">Questo comando ottiene i criteri di protezione denominati DefaultPolicy e lo archivia nella variabile $Pol.</span><span class="sxs-lookup"><span data-stu-id="55e05-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="55e05-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55e05-117">PARAMETERS</span></span>

### <span data-ttu-id="55e05-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="55e05-118">-BackupManagementType</span></span>
<span data-ttu-id="55e05-119">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="55e05-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="55e05-120">Attualmente è supportato solo AzureVM.</span><span class="sxs-lookup"><span data-stu-id="55e05-120">Currently, only AzureVM is supported.</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e05-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e05-121">-DefaultProfile</span></span>
<span data-ttu-id="55e05-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55e05-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55e05-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="55e05-123">-Name</span></span>
<span data-ttu-id="55e05-124">Specifica il nome del criterio.</span><span class="sxs-lookup"><span data-stu-id="55e05-124">Specifies the name of the policy.</span></span>

```yaml
Type: String
Parameter Sets: PolicyNameParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e05-125">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="55e05-125">-WorkloadType</span></span>
<span data-ttu-id="55e05-126">Specifica il tipo di carico di lavoro.</span><span class="sxs-lookup"><span data-stu-id="55e05-126">Specifies the workload type.</span></span>
<span data-ttu-id="55e05-127">Attualmente è supportato solo AzureVM.</span><span class="sxs-lookup"><span data-stu-id="55e05-127">Currently, only AzureVM is supported.</span></span>

```yaml
Type: WorkloadType
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e05-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e05-128">CommonParameters</span></span>
<span data-ttu-id="55e05-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55e05-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e05-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55e05-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e05-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55e05-131">INPUTS</span></span>

### <span data-ttu-id="55e05-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="55e05-132">None</span></span>
<span data-ttu-id="55e05-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="55e05-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55e05-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55e05-134">OUTPUTS</span></span>

### <span data-ttu-id="55e05-135">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="55e05-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="55e05-136">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. PolicyBase]</span><span class="sxs-lookup"><span data-stu-id="55e05-136">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase]</span></span>

## <span data-ttu-id="55e05-137">Note</span><span class="sxs-lookup"><span data-stu-id="55e05-137">NOTES</span></span>

## <span data-ttu-id="55e05-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55e05-138">RELATED LINKS</span></span>

[<span data-ttu-id="55e05-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="55e05-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="55e05-140">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="55e05-140">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="55e05-141">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="55e05-141">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


