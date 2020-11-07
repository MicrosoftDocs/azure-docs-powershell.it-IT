---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 295cb5bad09584c16e1217e68d3fc80c5ebf8598
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677656"
---
# <span data-ttu-id="18f83-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="18f83-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="18f83-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18f83-102">SYNOPSIS</span></span>
<span data-ttu-id="18f83-103">Ottiene i criteri di protezione del backup per un Vault.</span><span class="sxs-lookup"><span data-stu-id="18f83-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="18f83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18f83-104">SYNTAX</span></span>

### <span data-ttu-id="18f83-105">NoParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="18f83-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18f83-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="18f83-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18f83-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="18f83-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18f83-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="18f83-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18f83-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18f83-109">DESCRIPTION</span></span>
<span data-ttu-id="18f83-110">Il cmdlet **Get-AzRecoveryServicesBackupProtectionPolicy** ottiene i criteri di protezione del backup di Azure per un Vault.</span><span class="sxs-lookup"><span data-stu-id="18f83-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="18f83-111">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="18f83-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="18f83-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18f83-112">EXAMPLES</span></span>

### <span data-ttu-id="18f83-113">Esempio 1: ottenere tutti i criteri nel Vault</span><span class="sxs-lookup"><span data-stu-id="18f83-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="18f83-114">Questo comando consente di ottenere tutti i criteri di protezione creati nel Vault.</span><span class="sxs-lookup"><span data-stu-id="18f83-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="18f83-115">Esempio 2: ottenere un criterio specifico</span><span class="sxs-lookup"><span data-stu-id="18f83-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="18f83-116">Questo comando ottiene i criteri di protezione denominati DefaultPolicy e lo archivia nella variabile $Pol.</span><span class="sxs-lookup"><span data-stu-id="18f83-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="18f83-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18f83-117">PARAMETERS</span></span>

### <span data-ttu-id="18f83-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="18f83-118">-BackupManagementType</span></span>
<span data-ttu-id="18f83-119">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="18f83-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="18f83-120">Attualmente è supportato solo AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="18f83-120">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f83-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18f83-121">-DefaultProfile</span></span>
<span data-ttu-id="18f83-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18f83-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18f83-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="18f83-123">-Name</span></span>
<span data-ttu-id="18f83-124">Specifica il nome del criterio.</span><span class="sxs-lookup"><span data-stu-id="18f83-124">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f83-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="18f83-125">-VaultId</span></span>
<span data-ttu-id="18f83-126">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="18f83-126">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18f83-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="18f83-127">-WorkloadType</span></span>
<span data-ttu-id="18f83-128">Specifica il tipo di carico di lavoro.</span><span class="sxs-lookup"><span data-stu-id="18f83-128">Specifies the workload type.</span></span>
<span data-ttu-id="18f83-129">Attualmente è supportato solo AzureVM, AzureFiles.</span><span class="sxs-lookup"><span data-stu-id="18f83-129">Currently, only AzureVM, AzureFiles is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f83-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f83-130">CommonParameters</span></span>
<span data-ttu-id="18f83-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18f83-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f83-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18f83-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f83-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18f83-133">INPUTS</span></span>

### <span data-ttu-id="18f83-134">System. String</span><span class="sxs-lookup"><span data-stu-id="18f83-134">System.String</span></span>

## <span data-ttu-id="18f83-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18f83-135">OUTPUTS</span></span>

### <span data-ttu-id="18f83-136">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="18f83-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="18f83-137">Note</span><span class="sxs-lookup"><span data-stu-id="18f83-137">NOTES</span></span>

## <span data-ttu-id="18f83-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18f83-138">RELATED LINKS</span></span>

[<span data-ttu-id="18f83-139">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="18f83-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="18f83-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="18f83-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="18f83-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="18f83-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)

