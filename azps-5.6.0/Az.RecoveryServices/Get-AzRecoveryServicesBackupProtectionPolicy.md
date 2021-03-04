---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c29ff9d1fbe4a34f17a491dd1cb3c86c16f3ce75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958062"
---
# <span data-ttu-id="61829-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="61829-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="61829-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61829-102">SYNOPSIS</span></span>
<span data-ttu-id="61829-103">Recupera i criteri di protezione del backup per un vault.</span><span class="sxs-lookup"><span data-stu-id="61829-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="61829-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61829-104">SYNTAX</span></span>

### <span data-ttu-id="61829-105">NoParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61829-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61829-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="61829-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61829-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="61829-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61829-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="61829-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61829-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="61829-109">DESCRIPTION</span></span>
<span data-ttu-id="61829-110">Il cmdlet **Get-AzRecoveryServicesBackupProtectionPolicy** ottiene i criteri di protezione di Azure Backup per un vault.</span><span class="sxs-lookup"><span data-stu-id="61829-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="61829-111">Impostare il contesto del vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="61829-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="61829-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61829-112">EXAMPLES</span></span>

### <span data-ttu-id="61829-113">Esempio 1: Ottenere tutti i criteri nel Vault</span><span class="sxs-lookup"><span data-stu-id="61829-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="61829-114">Questo comando recupera tutti i criteri di protezione creati nel Vault.</span><span class="sxs-lookup"><span data-stu-id="61829-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="61829-115">Esempio 2: Ottenere un criterio specifico</span><span class="sxs-lookup"><span data-stu-id="61829-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="61829-116">Questo comando recupera il criterio di protezione denominato DefaultPolicy e quindi lo archivia nella $Pol variabile.</span><span class="sxs-lookup"><span data-stu-id="61829-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="61829-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61829-117">PARAMETERS</span></span>

### <span data-ttu-id="61829-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="61829-118">-BackupManagementType</span></span>
<span data-ttu-id="61829-119">Classe di risorse protetta.</span><span class="sxs-lookup"><span data-stu-id="61829-119">The class of resources being protected.</span></span> <span data-ttu-id="61829-120">Attualmente i valori supportati per questo cmdlet sono AzureVM, AzureStorage, AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="61829-120">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureStorage, AzureWorkload, MAB

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61829-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61829-121">-DefaultProfile</span></span>
<span data-ttu-id="61829-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61829-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61829-123">-Name</span><span class="sxs-lookup"><span data-stu-id="61829-123">-Name</span></span>
<span data-ttu-id="61829-124">Specifica il nome del criterio.</span><span class="sxs-lookup"><span data-stu-id="61829-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="61829-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="61829-125">-VaultId</span></span>
<span data-ttu-id="61829-126">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="61829-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="61829-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="61829-127">-WorkloadType</span></span>
<span data-ttu-id="61829-128">Tipo di carico di lavoro della risorsa.</span><span class="sxs-lookup"><span data-stu-id="61829-128">Workload type of the resource.</span></span> <span data-ttu-id="61829-129">I valori correnti supportati sono AzureVM, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="61829-129">The current supported values are AzureVM, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="61829-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61829-130">CommonParameters</span></span>
<span data-ttu-id="61829-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61829-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61829-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61829-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61829-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="61829-133">INPUTS</span></span>

### <span data-ttu-id="61829-134">System.String</span><span class="sxs-lookup"><span data-stu-id="61829-134">System.String</span></span>

## <span data-ttu-id="61829-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61829-135">OUTPUTS</span></span>

### <span data-ttu-id="61829-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="61829-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="61829-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="61829-137">NOTES</span></span>

## <span data-ttu-id="61829-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61829-138">RELATED LINKS</span></span>

[<span data-ttu-id="61829-139">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="61829-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="61829-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="61829-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="61829-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="61829-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


