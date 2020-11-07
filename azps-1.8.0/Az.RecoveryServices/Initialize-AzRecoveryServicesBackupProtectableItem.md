---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 0fd0473cccdf8fbef3d3bab941ab6b3ce7813a63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677635"
---
# <span data-ttu-id="7f08b-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7f08b-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="7f08b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f08b-102">SYNOPSIS</span></span>
<span data-ttu-id="7f08b-103">Questo comando attiva l'individuazione di eventuali elementi non protetti del tipo di carico di lavoro specifico nel contenitore indicato.</span><span class="sxs-lookup"><span data-stu-id="7f08b-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="7f08b-104">Se l'applicazione DB non è protetta automaticamente, usare questo comando per scoprire le nuove DBs ogni volta che vengono aggiunte e procedere alla loro protezione.</span><span class="sxs-lookup"><span data-stu-id="7f08b-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="7f08b-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f08b-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f08b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f08b-106">DESCRIPTION</span></span>
<span data-ttu-id="7f08b-107">il cmdlet richiede carichi di lavoro specifici all'interno di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="7f08b-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="7f08b-108">In questo modo viene attivata un'operazione che crea elementi protettivi.</span><span class="sxs-lookup"><span data-stu-id="7f08b-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="7f08b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f08b-109">EXAMPLES</span></span>

### <span data-ttu-id="7f08b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7f08b-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container –WorkloadType “MSSQL”
```

<span data-ttu-id="7f08b-111">Il cmdlet esegue un'operazione di individuazione per nuovi elementi protettivi.</span><span class="sxs-lookup"><span data-stu-id="7f08b-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="7f08b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f08b-112">PARAMETERS</span></span>

### <span data-ttu-id="7f08b-113">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="7f08b-113">-Container</span></span>
<span data-ttu-id="7f08b-114">Contenitore in cui si trova l'elemento</span><span class="sxs-lookup"><span data-stu-id="7f08b-114">Container where the item resides</span></span>

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

### <span data-ttu-id="7f08b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f08b-115">-DefaultProfile</span></span>
<span data-ttu-id="7f08b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f08b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f08b-117">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7f08b-117">-VaultId</span></span>
<span data-ttu-id="7f08b-118">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7f08b-118">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7f08b-119">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="7f08b-119">-WorkloadType</span></span>
<span data-ttu-id="7f08b-120">Tipo di carico di lavoro della risorsa (ad esempio: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="7f08b-120">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="7f08b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f08b-121">CommonParameters</span></span>
<span data-ttu-id="7f08b-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f08b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f08b-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f08b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f08b-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f08b-124">INPUTS</span></span>

### <span data-ttu-id="7f08b-125">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="7f08b-125">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="7f08b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7f08b-126">System.String</span></span>

## <span data-ttu-id="7f08b-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f08b-127">OUTPUTS</span></span>

### <span data-ttu-id="7f08b-128">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="7f08b-128">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="7f08b-129">Note</span><span class="sxs-lookup"><span data-stu-id="7f08b-129">NOTES</span></span>

## <span data-ttu-id="7f08b-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f08b-130">RELATED LINKS</span></span>