---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 97eae8c5c545297a7d6287a951ec02433d591168
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865249"
---
# <span data-ttu-id="0e6bf-101">Disable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="0e6bf-101">Disable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="0e6bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0e6bf-102">SYNOPSIS</span></span>
<span data-ttu-id="0e6bf-103">Disabilita il backup automatico per un elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-103">Disables auto backup for a protectable item.</span></span>

## <span data-ttu-id="0e6bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e6bf-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e6bf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e6bf-105">DESCRIPTION</span></span>
<span data-ttu-id="0e6bf-106">Il cmdlet **Disable-AzRecoveryServicesBackupAutoProtection Disabilita** la protezione su un elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-106">The **Disable-AzRecoveryServicesBackupAutoProtection** cmdlet disables protection on a protectable item.</span></span>

## <span data-ttu-id="0e6bf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e6bf-107">EXAMPLES</span></span>

### <span data-ttu-id="0e6bf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0e6bf-108">Example 1</span></span>
```
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Disable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL"
```

<span data-ttu-id="0e6bf-109">Il primo cmdlet Disabilita i criteri di protezione del backup.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-109">The first cmdlet disables the Backup protection policy.</span></span>

## <span data-ttu-id="0e6bf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0e6bf-110">PARAMETERS</span></span>

### <span data-ttu-id="0e6bf-111">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="0e6bf-111">-BackupManagementType</span></span>
<span data-ttu-id="0e6bf-112">Tipo di gestione di backup della risorsa (ad esempio: MAB, DPM).</span><span class="sxs-lookup"><span data-stu-id="0e6bf-112">Backup Management type of the resource (for example: MAB, DPM).</span></span>

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

### <span data-ttu-id="0e6bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e6bf-113">-DefaultProfile</span></span>
<span data-ttu-id="0e6bf-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e6bf-115">-InputItem</span><span class="sxs-lookup"><span data-stu-id="0e6bf-115">-InputItem</span></span>
<span data-ttu-id="0e6bf-116">ID elemento</span><span class="sxs-lookup"><span data-stu-id="0e6bf-116">Item Id</span></span>

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

### <span data-ttu-id="0e6bf-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e6bf-117">-PassThru</span></span>
<span data-ttu-id="0e6bf-118">Restituire il risultato per la protezione automatica.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-118">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="0e6bf-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0e6bf-119">-VaultId</span></span>
<span data-ttu-id="0e6bf-120">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0e6bf-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="0e6bf-121">-WorkloadType</span></span>
<span data-ttu-id="0e6bf-122">Tipo di carico di lavoro della risorsa (ad esempio: AzureVM, WindowsServer, AzureFiles).</span><span class="sxs-lookup"><span data-stu-id="0e6bf-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles).</span></span>

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

### <span data-ttu-id="0e6bf-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0e6bf-123">-Confirm</span></span>
<span data-ttu-id="0e6bf-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e6bf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e6bf-125">-WhatIf</span></span>
<span data-ttu-id="0e6bf-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e6bf-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e6bf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e6bf-128">CommonParameters</span></span>
<span data-ttu-id="0e6bf-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e6bf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e6bf-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e6bf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e6bf-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0e6bf-131">INPUTS</span></span>

### <span data-ttu-id="0e6bf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0e6bf-132">System.String</span></span>

## <span data-ttu-id="0e6bf-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e6bf-133">OUTPUTS</span></span>

### <span data-ttu-id="0e6bf-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e6bf-134">System.Boolean</span></span>

## <span data-ttu-id="0e6bf-135">Note</span><span class="sxs-lookup"><span data-stu-id="0e6bf-135">NOTES</span></span>

## <span data-ttu-id="0e6bf-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e6bf-136">RELATED LINKS</span></span>
