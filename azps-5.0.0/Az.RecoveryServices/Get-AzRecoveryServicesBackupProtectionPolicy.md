---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 9595f3fc3062d6afdd5b5bbfab74f297b39b3f6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301219"
---
# <span data-ttu-id="592cb-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="592cb-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="592cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="592cb-102">SYNOPSIS</span></span>
<span data-ttu-id="592cb-103">Ottiene i criteri di protezione del backup per un Vault.</span><span class="sxs-lookup"><span data-stu-id="592cb-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="592cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="592cb-104">SYNTAX</span></span>

### <span data-ttu-id="592cb-105">NoParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="592cb-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="592cb-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="592cb-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="592cb-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="592cb-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="592cb-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="592cb-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="592cb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="592cb-109">DESCRIPTION</span></span>
<span data-ttu-id="592cb-110">Il cmdlet **Get-AzRecoveryServicesBackupProtectionPolicy** ottiene i criteri di protezione del backup di Azure per un Vault.</span><span class="sxs-lookup"><span data-stu-id="592cb-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="592cb-111">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="592cb-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="592cb-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="592cb-112">EXAMPLES</span></span>

### <span data-ttu-id="592cb-113">Esempio 1: ottenere tutti i criteri nel Vault</span><span class="sxs-lookup"><span data-stu-id="592cb-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="592cb-114">Questo comando consente di ottenere tutti i criteri di protezione creati nel Vault.</span><span class="sxs-lookup"><span data-stu-id="592cb-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="592cb-115">Esempio 2: ottenere un criterio specifico</span><span class="sxs-lookup"><span data-stu-id="592cb-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="592cb-116">Questo comando ottiene i criteri di protezione denominati DefaultPolicy e lo archivia nella variabile $Pol.</span><span class="sxs-lookup"><span data-stu-id="592cb-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="592cb-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="592cb-117">PARAMETERS</span></span>

### <span data-ttu-id="592cb-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="592cb-118">-BackupManagementType</span></span>
<span data-ttu-id="592cb-119">Classe di risorse protette.</span><span class="sxs-lookup"><span data-stu-id="592cb-119">The class of resources being protected.</span></span> <span data-ttu-id="592cb-120">Attualmente i valori supportati per questo cmdlet sono AzureVM, AzureStorage, AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="592cb-120">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload</span></span>

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

### <span data-ttu-id="592cb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592cb-121">-DefaultProfile</span></span>
<span data-ttu-id="592cb-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="592cb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="592cb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="592cb-123">-Name</span></span>
<span data-ttu-id="592cb-124">Specifica il nome del criterio.</span><span class="sxs-lookup"><span data-stu-id="592cb-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="592cb-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="592cb-125">-VaultId</span></span>
<span data-ttu-id="592cb-126">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="592cb-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="592cb-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="592cb-127">-WorkloadType</span></span>
<span data-ttu-id="592cb-128">Tipo di carico di lavoro della risorsa.</span><span class="sxs-lookup"><span data-stu-id="592cb-128">Workload type of the resource.</span></span> <span data-ttu-id="592cb-129">I valori supportati correnti sono AzureVM, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="592cb-129">The current supported values are AzureVM, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="592cb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592cb-130">CommonParameters</span></span>
<span data-ttu-id="592cb-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="592cb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592cb-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="592cb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592cb-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="592cb-133">INPUTS</span></span>

### <span data-ttu-id="592cb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="592cb-134">System.String</span></span>

## <span data-ttu-id="592cb-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="592cb-135">OUTPUTS</span></span>

### <span data-ttu-id="592cb-136">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="592cb-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="592cb-137">Note</span><span class="sxs-lookup"><span data-stu-id="592cb-137">NOTES</span></span>

## <span data-ttu-id="592cb-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="592cb-138">RELATED LINKS</span></span>

[<span data-ttu-id="592cb-139">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="592cb-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="592cb-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="592cb-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="592cb-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="592cb-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


