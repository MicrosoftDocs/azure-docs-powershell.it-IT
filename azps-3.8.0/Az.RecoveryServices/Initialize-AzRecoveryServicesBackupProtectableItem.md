---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 8bc2286cf6df736ee54390447e83f0337c031001
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022666"
---
# <span data-ttu-id="e8ba0-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e8ba0-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="e8ba0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ba0-103">Questo comando attiva l'individuazione di eventuali elementi non protetti del tipo di carico di lavoro specifico nel contenitore indicato.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="e8ba0-104">Se l'applicazione DB non è protetta automaticamente, usare questo comando per scoprire le nuove DBs ogni volta che vengono aggiunte e procedere alla loro protezione.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="e8ba0-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8ba0-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8ba0-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8ba0-106">DESCRIPTION</span></span>
<span data-ttu-id="e8ba0-107">il cmdlet richiede carichi di lavoro specifici all'interno di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="e8ba0-108">In questo modo viene attivata un'operazione che crea elementi protettivi.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="e8ba0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8ba0-109">EXAMPLES</span></span>

### <span data-ttu-id="e8ba0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e8ba0-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container -WorkloadType "MSSQL"
```

<span data-ttu-id="e8ba0-111">Il cmdlet esegue un'operazione di individuazione per nuovi elementi protettivi.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="e8ba0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8ba0-112">PARAMETERS</span></span>

### <span data-ttu-id="e8ba0-113">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="e8ba0-113">-Container</span></span>
<span data-ttu-id="e8ba0-114">Contenitore in cui si trova l'elemento</span><span class="sxs-lookup"><span data-stu-id="e8ba0-114">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ba0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ba0-115">-DefaultProfile</span></span>
<span data-ttu-id="e8ba0-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8ba0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8ba0-117">-PassThru</span></span>
<span data-ttu-id="e8ba0-118">Restituire il contenitore da eliminare.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-118">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="e8ba0-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e8ba0-119">-VaultId</span></span>
<span data-ttu-id="e8ba0-120">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e8ba0-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="e8ba0-121">-WorkloadType</span></span>
<span data-ttu-id="e8ba0-122">Tipo di carico di lavoro della risorsa (ad esempio: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="e8ba0-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ba0-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e8ba0-123">-Confirm</span></span>
<span data-ttu-id="e8ba0-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8ba0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ba0-125">-WhatIf</span></span>
<span data-ttu-id="e8ba0-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8ba0-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8ba0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ba0-128">CommonParameters</span></span>
<span data-ttu-id="e8ba0-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8ba0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ba0-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8ba0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ba0-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8ba0-131">INPUTS</span></span>

### <span data-ttu-id="e8ba0-132">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="e8ba0-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="e8ba0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e8ba0-133">System.String</span></span>

## <span data-ttu-id="e8ba0-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8ba0-134">OUTPUTS</span></span>

### <span data-ttu-id="e8ba0-135">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="e8ba0-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="e8ba0-136">Note</span><span class="sxs-lookup"><span data-stu-id="e8ba0-136">NOTES</span></span>

## <span data-ttu-id="e8ba0-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8ba0-137">RELATED LINKS</span></span>
