---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 81fa8a4ada2f2479d9aa2ecceb1de3c05c3f34c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005853"
---
# <span data-ttu-id="1fcea-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="1fcea-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="1fcea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fcea-102">SYNOPSIS</span></span>
<span data-ttu-id="1fcea-103">Il cmdlet **Enable-AzRecoveryServicesBackupAutoProtection** configura la protezione automatica delle asserzioni SQL correnti e future all'interno dell'istanza specificata con il criterio specificato.</span><span class="sxs-lookup"><span data-stu-id="1fcea-103">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets up automatic protection of current and any future SQL DBs within the given instance with the supplied policy.</span></span>

## <span data-ttu-id="1fcea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1fcea-104">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1fcea-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1fcea-105">DESCRIPTION</span></span>
<span data-ttu-id="1fcea-106">Questo comando consente agli utenti di proteggere automaticamente tutte le SQL db non protette esistenti e tutti i database che verranno aggiunti in un secondo momento con il criterio specificato.</span><span class="sxs-lookup"><span data-stu-id="1fcea-106">This command allows users to automatically protect all existing unprotected SQL DBs and any DB which will be added later with the given policy.</span></span>  <span data-ttu-id="1fcea-107">Poiché l'istruzione è di eseguire il backup di tutti i database dns futuri, l'operazione viene eseguita a livello di SQLInstance, il servizio di backup di Azure analizza periodicamente i contenitori protetti automaticamente alla ricerca di nuovi database e li protegge automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1fcea-107">Since the instruction is to back up all future DBs, the operation is done at a SQLInstance level, Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="1fcea-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1fcea-108">EXAMPLES</span></span>

### <span data-ttu-id="1fcea-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1fcea-109">Example 1</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultSQLPolicy"
PS C:\> $SQLInstance = Get-AzRecoveryServicesBackupProtectableItem -workloadType MSSQL -ItemType SQLInstance -VaultId $targetVault.ID -Name "MSSQLInstance" -ServerName "TestSQLServer" 
PS C:\> Enable-AzRecoveryServicesBackupAutoProtection -InputItem $SQLInstance -BackupManagementType AzureWorkload -WorkloadType MSSQL -Policy $Pol -VaultId $targetvault.ID 
```

<span data-ttu-id="1fcea-110">Il primo cmdlet ottiene un oggetto criterio predefinito, quindi lo archivia nella variabile $Pol predefinita.</span><span class="sxs-lookup"><span data-stu-id="1fcea-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="1fcea-111">Il secondo cmdlet recupera l'istanza SQL corrispondente, che è un elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="1fcea-111">The second cmdlet fetches the relevant SQLInstance which is a protectable item.</span></span> <span data-ttu-id="1fcea-112">Il terzo comando configura quindi la protezione automatica per questa istanza usando il criterio in $Pol.</span><span class="sxs-lookup"><span data-stu-id="1fcea-112">The 3rd command then sets up auto protection for this instance using the policy in $Pol.</span></span>

### <span data-ttu-id="1fcea-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1fcea-113">Example 2</span></span>

<span data-ttu-id="1fcea-114">Questo comando consente agli utenti di proteggere automaticamente tutti i database db non protetti esistenti e quelli che verranno aggiunti in un secondo momento con il criterio specificato.</span><span class="sxs-lookup"><span data-stu-id="1fcea-114">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="1fcea-115">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="1fcea-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType AzureVM -InputItem <ProtectableItemBase> -Policy $Pol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="1fcea-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fcea-116">PARAMETERS</span></span>

### <span data-ttu-id="1fcea-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="1fcea-117">-BackupManagementType</span></span>
<span data-ttu-id="1fcea-118">Classe di risorse protetta.</span><span class="sxs-lookup"><span data-stu-id="1fcea-118">The class of resources being protected.</span></span> <span data-ttu-id="1fcea-119">Attualmente i valori supportati per questo cmdlet sono MAB, AzureWorkload, AzureVM</span><span class="sxs-lookup"><span data-stu-id="1fcea-119">Currently the values supported for this cmdlet are MAB, AzureWorkload, AzureVM</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fcea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fcea-120">-DefaultProfile</span></span>
<span data-ttu-id="1fcea-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1fcea-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fcea-122">-InputItem</span><span class="sxs-lookup"><span data-stu-id="1fcea-122">-InputItem</span></span>
<span data-ttu-id="1fcea-123">Specifica l'oggetto elemento proteggibile che può essere passato come input.</span><span class="sxs-lookup"><span data-stu-id="1fcea-123">Specifies the protectable item object that can be passed as an input.</span></span> <span data-ttu-id="1fcea-124">Il valore corrente supportato è un oggetto protectableItem di tipo "SQLInstance".</span><span class="sxs-lookup"><span data-stu-id="1fcea-124">The current supported value is a protectableItem object of type "SQLInstance".</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fcea-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fcea-125">-PassThru</span></span>
<span data-ttu-id="1fcea-126">Restituire il risultato per la protezione automatica.</span><span class="sxs-lookup"><span data-stu-id="1fcea-126">Return the result for auto protection.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fcea-127">-Policy</span><span class="sxs-lookup"><span data-stu-id="1fcea-127">-Policy</span></span>
<span data-ttu-id="1fcea-128">Oggetto criterio di protezione.</span><span class="sxs-lookup"><span data-stu-id="1fcea-128">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fcea-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1fcea-129">-VaultId</span></span>
<span data-ttu-id="1fcea-130">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1fcea-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1fcea-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="1fcea-131">-WorkloadType</span></span>
<span data-ttu-id="1fcea-132">Tipo di carico di lavoro della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1fcea-132">Workload type of the resource.</span></span> <span data-ttu-id="1fcea-133">I valori correnti supportati sono AzureVM, WindowsServer, MSSQL</span><span class="sxs-lookup"><span data-stu-id="1fcea-133">The current supported values are AzureVM, WindowsServer, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fcea-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fcea-134">-Confirm</span></span>
<span data-ttu-id="1fcea-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fcea-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fcea-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fcea-136">-WhatIf</span></span>
<span data-ttu-id="1fcea-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fcea-137">Shows what would happen if the cmdlet runs.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fcea-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fcea-138">CommonParameters</span></span>
<span data-ttu-id="1fcea-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fcea-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fcea-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1fcea-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fcea-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="1fcea-141">INPUTS</span></span>

### <span data-ttu-id="1fcea-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1fcea-142">System.String</span></span>

## <span data-ttu-id="1fcea-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1fcea-143">OUTPUTS</span></span>

### <span data-ttu-id="1fcea-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="1fcea-144">System.Object</span></span>

## <span data-ttu-id="1fcea-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="1fcea-145">NOTES</span></span>

## <span data-ttu-id="1fcea-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1fcea-146">RELATED LINKS</span></span>
