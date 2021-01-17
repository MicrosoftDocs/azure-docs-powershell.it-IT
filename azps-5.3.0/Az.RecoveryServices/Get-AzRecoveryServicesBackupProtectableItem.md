---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: add399ca208cdcd1f1b4395523f8df43875ff451
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475004"
---
# <span data-ttu-id="5c71b-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5c71b-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="5c71b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c71b-102">SYNOPSIS</span></span>
<span data-ttu-id="5c71b-103">Questo comando consente di recuperare tutti gli elementi protetti all'interno di un determinato contenitore o in tutti i contenitori registrati.</span><span class="sxs-lookup"><span data-stu-id="5c71b-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="5c71b-104">Sarà costituito da tutti gli elementi della gerarchia dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5c71b-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="5c71b-105">Restituisce DBs e le entità di livello superiore come instance, AvailabilityGroup e così via.</span><span class="sxs-lookup"><span data-stu-id="5c71b-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="5c71b-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c71b-106">SYNTAX</span></span>

### <span data-ttu-id="5c71b-107">NoFilterParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5c71b-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c71b-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="5c71b-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c71b-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="5c71b-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c71b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c71b-110">DESCRIPTION</span></span>
<span data-ttu-id="5c71b-111">Il cmdlet **Get-AzRecoveryServicesBackupProtectableItem** Ottiene l'elenco degli elementi protettivi in un contenitore e lo stato di protezione degli elementi.</span><span class="sxs-lookup"><span data-stu-id="5c71b-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="5c71b-112">Un contenitore registrato in un Vault di servizi di ripristino di Azure può avere uno o più elementi che possono essere protetti.</span><span class="sxs-lookup"><span data-stu-id="5c71b-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="5c71b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c71b-113">EXAMPLES</span></span>

### <span data-ttu-id="5c71b-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5c71b-114">Example 1</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType MSSQL -Status Registered
PS C:\> $Item = Get-AzRecoveryServicesProtectableItem -Container $Container -ItemType "SQLDatabase" -VaultId $vault.ID
```

<span data-ttu-id="5c71b-115">Il primo comando ottiene il contenitore di tipo MSSQL e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="5c71b-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="5c71b-116">Il secondo comando consente di ottenere l'elemento protettivo di backup in $Container e quindi di archiviarlo nella variabile $Item.</span><span class="sxs-lookup"><span data-stu-id="5c71b-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="5c71b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c71b-117">PARAMETERS</span></span>

### <span data-ttu-id="5c71b-118">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="5c71b-118">-Container</span></span>
<span data-ttu-id="5c71b-119">Contenitore in cui si trova l'elemento</span><span class="sxs-lookup"><span data-stu-id="5c71b-119">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c71b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c71b-120">-DefaultProfile</span></span>
<span data-ttu-id="5c71b-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c71b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c71b-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="5c71b-122">-ItemType</span></span>
<span data-ttu-id="5c71b-123">Specifica il tipo di elemento protettivo.</span><span class="sxs-lookup"><span data-stu-id="5c71b-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="5c71b-124">Valori applicabili: (SqlDatabase, SQLInstance, SQLAvailabilityGroup).</span><span class="sxs-lookup"><span data-stu-id="5c71b-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemType
Parameter Sets: FilterParamSet, IdParamSet
Aliases:
Accepted values: SQLDataBase, SQLInstance, SQLAvailabilityGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c71b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c71b-125">-Name</span></span>
<span data-ttu-id="5c71b-126">Specifica il nome del database, dell'istanza o di AvailabilityGroup.</span><span class="sxs-lookup"><span data-stu-id="5c71b-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c71b-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="5c71b-127">-ParentID</span></span>
<span data-ttu-id="5c71b-128">Specifica l'ID ARM di un'istanza o di un AG.</span><span class="sxs-lookup"><span data-stu-id="5c71b-128">Specified the ARM ID of an Instance or AG.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c71b-129">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5c71b-129">-ServerName</span></span>
<span data-ttu-id="5c71b-130">Specifica il nome del server a cui appartiene l'elemento.</span><span class="sxs-lookup"><span data-stu-id="5c71b-130">Specifies the name of the server to which the item belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c71b-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5c71b-131">-VaultId</span></span>
<span data-ttu-id="5c71b-132">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5c71b-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5c71b-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="5c71b-133">-WorkloadType</span></span>
<span data-ttu-id="5c71b-134">Tipo di carico di lavoro della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5c71b-134">Workload type of the resource.</span></span> <span data-ttu-id="5c71b-135">I valori supportati correnti sono AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="5c71b-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:
Accepted values: AzureVM, WindowsServer, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c71b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c71b-136">CommonParameters</span></span>
<span data-ttu-id="5c71b-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c71b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c71b-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c71b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c71b-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c71b-139">INPUTS</span></span>

### <span data-ttu-id="5c71b-140">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="5c71b-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="5c71b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5c71b-141">System.String</span></span>

## <span data-ttu-id="5c71b-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c71b-142">OUTPUTS</span></span>

### <span data-ttu-id="5c71b-143">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="5c71b-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="5c71b-144">Note</span><span class="sxs-lookup"><span data-stu-id="5c71b-144">NOTES</span></span>

## <span data-ttu-id="5c71b-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c71b-145">RELATED LINKS</span></span>
