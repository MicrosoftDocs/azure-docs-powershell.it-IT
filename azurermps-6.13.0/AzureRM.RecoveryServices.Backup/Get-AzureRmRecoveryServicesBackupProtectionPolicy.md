---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: d08bd0a02878b1b99b3243e80512df30eca6e1c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514923"
---
# <span data-ttu-id="bf136-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bf136-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="bf136-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bf136-102">SYNOPSIS</span></span>
<span data-ttu-id="bf136-103">Ottiene i criteri di protezione del backup per un Vault.</span><span class="sxs-lookup"><span data-stu-id="bf136-103">Gets Backup protection policies for a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf136-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf136-104">SYNTAX</span></span>

### <span data-ttu-id="bf136-105">NoParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bf136-105">NoParamSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf136-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="bf136-106">PolicyNameParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf136-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="bf136-107">WorkloadParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf136-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="bf136-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf136-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf136-109">DESCRIPTION</span></span>
<span data-ttu-id="bf136-110">Il cmdlet **Get-AzureRmRecoveryServicesBackupProtectionPolicy** ottiene i criteri di protezione del backup di Azure per un Vault.</span><span class="sxs-lookup"><span data-stu-id="bf136-110">The **Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="bf136-111">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="bf136-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="bf136-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf136-112">EXAMPLES</span></span>

### <span data-ttu-id="bf136-113">Esempio 1: ottenere tutti i criteri nel Vault</span><span class="sxs-lookup"><span data-stu-id="bf136-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="bf136-114">Questo comando consente di ottenere tutti i criteri di protezione creati nel Vault.</span><span class="sxs-lookup"><span data-stu-id="bf136-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="bf136-115">Esempio 2: ottenere un criterio specifico</span><span class="sxs-lookup"><span data-stu-id="bf136-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="bf136-116">Questo comando ottiene i criteri di protezione denominati DefaultPolicy e lo archivia nella variabile $Pol.</span><span class="sxs-lookup"><span data-stu-id="bf136-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="bf136-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bf136-117">PARAMETERS</span></span>

### <span data-ttu-id="bf136-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="bf136-118">-BackupManagementType</span></span>
<span data-ttu-id="bf136-119">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="bf136-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="bf136-120">Attualmente è supportato solo AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="bf136-120">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf136-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf136-121">-DefaultProfile</span></span>
<span data-ttu-id="bf136-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bf136-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf136-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf136-123">-Name</span></span>
<span data-ttu-id="bf136-124">Specifica il nome del criterio.</span><span class="sxs-lookup"><span data-stu-id="bf136-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="bf136-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="bf136-125">-VaultId</span></span>
<span data-ttu-id="bf136-126">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="bf136-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="bf136-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="bf136-127">-WorkloadType</span></span>
<span data-ttu-id="bf136-128">Specifica il tipo di carico di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bf136-128">Specifies the workload type.</span></span>
<span data-ttu-id="bf136-129">Attualmente è supportato solo AzureVM, AzureFiles.</span><span class="sxs-lookup"><span data-stu-id="bf136-129">Currently, only AzureVM, AzureFiles is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf136-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf136-130">CommonParameters</span></span>
<span data-ttu-id="bf136-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf136-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf136-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf136-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf136-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bf136-133">INPUTS</span></span>

### <span data-ttu-id="bf136-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bf136-134">System.String</span></span>
<span data-ttu-id="bf136-135">Parametri: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bf136-135">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="bf136-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf136-136">OUTPUTS</span></span>

### <span data-ttu-id="bf136-137">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="bf136-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="bf136-138">Note</span><span class="sxs-lookup"><span data-stu-id="bf136-138">NOTES</span></span>

## <span data-ttu-id="bf136-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf136-139">RELATED LINKS</span></span>

[<span data-ttu-id="bf136-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bf136-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="bf136-141">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bf136-141">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="bf136-142">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bf136-142">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


