---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 6dfff295981ab341d05790e18ed6e4d5c5b0e822
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865179"
---
# <span data-ttu-id="bed1a-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="bed1a-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="bed1a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bed1a-102">SYNOPSIS</span></span>
<span data-ttu-id="bed1a-103">Questo comando consente agli utenti di proteggere automaticamente tutte le DBs non protette esistenti e qualsiasi DB che verrà aggiunto in seguito con il criterio specificato.</span><span class="sxs-lookup"><span data-stu-id="bed1a-103">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="bed1a-104">Il servizio di backup di Azure analizzerà periodicamente contenitori protetti automaticamente per qualsiasi nuova DBs e li proteggerà automaticamente.</span><span class="sxs-lookup"><span data-stu-id="bed1a-104">Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="bed1a-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bed1a-105">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bed1a-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bed1a-106">DESCRIPTION</span></span>
<span data-ttu-id="bed1a-107">Il cmdlet **Enable-AzRecoveryServicesBackupAutoProtection** imposta i criteri di protezione del backup di Azure auto su un elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="bed1a-107">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets Azure auto Backup protection policy on an protectable item.</span></span>

## <span data-ttu-id="bed1a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bed1a-108">EXAMPLES</span></span>

### <span data-ttu-id="bed1a-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bed1a-109">Example 1</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL" -Policy $Pol
```

<span data-ttu-id="bed1a-110">Il primo cmdlet ottiene un oggetto criteri predefinito e lo archivia nella variabile $Pol.</span><span class="sxs-lookup"><span data-stu-id="bed1a-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="bed1a-111">Il secondo cmdlet imposta i criteri di protezione del backup per AzureWorkload usando i criteri in $Pol.</span><span class="sxs-lookup"><span data-stu-id="bed1a-111">The second cmdlet sets the Backup protection policy for the AzureWorkload using the policy in $Pol.</span></span>

## <span data-ttu-id="bed1a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bed1a-112">PARAMETERS</span></span>

### <span data-ttu-id="bed1a-113">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="bed1a-113">-BackupManagementType</span></span>
<span data-ttu-id="bed1a-114">Tipo di gestione di backup della risorsa (ad esempio: MAB, DPM, AzureWorkload).</span><span class="sxs-lookup"><span data-stu-id="bed1a-114">Backup Management type of the resource (for example: MAB, DPM, AzureWorkload).</span></span>

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

### <span data-ttu-id="bed1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bed1a-115">-DefaultProfile</span></span>
<span data-ttu-id="bed1a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bed1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bed1a-117">-InputItem</span><span class="sxs-lookup"><span data-stu-id="bed1a-117">-InputItem</span></span>
<span data-ttu-id="bed1a-118">Specifica l'oggetto elemento protetto che può essere passato come input.</span><span class="sxs-lookup"><span data-stu-id="bed1a-118">Specifies the protectable item object that can be passed as an input.</span></span>

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

### <span data-ttu-id="bed1a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bed1a-119">-PassThru</span></span>
<span data-ttu-id="bed1a-120">Restituire il risultato per la protezione automatica.</span><span class="sxs-lookup"><span data-stu-id="bed1a-120">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="bed1a-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="bed1a-121">-Policy</span></span>
<span data-ttu-id="bed1a-122">Oggetto Criteri di protezione.</span><span class="sxs-lookup"><span data-stu-id="bed1a-122">Protection policy object.</span></span>

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

### <span data-ttu-id="bed1a-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="bed1a-123">-VaultId</span></span>
<span data-ttu-id="bed1a-124">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="bed1a-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="bed1a-125">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="bed1a-125">-WorkloadType</span></span>
<span data-ttu-id="bed1a-126">Tipo di carico di lavoro della risorsa (ad esempio: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="bed1a-126">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="bed1a-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bed1a-127">-Confirm</span></span>
<span data-ttu-id="bed1a-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bed1a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bed1a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bed1a-129">-WhatIf</span></span>
<span data-ttu-id="bed1a-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bed1a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bed1a-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bed1a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bed1a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bed1a-132">CommonParameters</span></span>
<span data-ttu-id="bed1a-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bed1a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bed1a-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bed1a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bed1a-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bed1a-135">INPUTS</span></span>

### <span data-ttu-id="bed1a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bed1a-136">System.String</span></span>

## <span data-ttu-id="bed1a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bed1a-137">OUTPUTS</span></span>

### <span data-ttu-id="bed1a-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="bed1a-138">System.Object</span></span>

## <span data-ttu-id="bed1a-139">Note</span><span class="sxs-lookup"><span data-stu-id="bed1a-139">NOTES</span></span>

## <span data-ttu-id="bed1a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bed1a-140">RELATED LINKS</span></span>
