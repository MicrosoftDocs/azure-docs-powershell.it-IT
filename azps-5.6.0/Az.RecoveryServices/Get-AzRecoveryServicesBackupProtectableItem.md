---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 1d14a1559d62f00b4a513c6a25dad28b7816e2d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990862"
---
# <span data-ttu-id="57968-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="57968-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="57968-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57968-102">SYNOPSIS</span></span>
<span data-ttu-id="57968-103">Questo comando recupera tutti gli elementi proteggibili all'interno di un determinato contenitore o in tutti i contenitori registrati.</span><span class="sxs-lookup"><span data-stu-id="57968-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="57968-104">Sarà costituito da tutti gli elementi della gerarchia dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="57968-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="57968-105">Restituisce i database di database e le relative entità di livello superiore, ad esempio Istanza, AvailabilityGroup e così via.</span><span class="sxs-lookup"><span data-stu-id="57968-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="57968-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57968-106">SYNTAX</span></span>

### <span data-ttu-id="57968-107">NoFilterParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="57968-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57968-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="57968-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57968-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="57968-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57968-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="57968-110">DESCRIPTION</span></span>
<span data-ttu-id="57968-111">Il cmdlet **Get-AzRecoveryServicesBackupProtectableItem** ottiene l'elenco degli elementi proteggibili in un contenitore e lo stato di protezione degli elementi.</span><span class="sxs-lookup"><span data-stu-id="57968-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="57968-112">Un contenitore registrato in un vault di Servizi di ripristino di Azure può contenere uno o più elementi che possono essere protetti.</span><span class="sxs-lookup"><span data-stu-id="57968-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="57968-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57968-113">EXAMPLES</span></span>

### <span data-ttu-id="57968-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="57968-114">Example 1</span></span>
```
PS C:\> $Vault = Get-AzRecoveryServicesVault -Name "MyRecoveryVault"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer -Status Registered -VaultId $Vault.Id
PS C:\> $Item = Get-AzRecoveryServicesBackupProtectableItem -Container $Container -ItemType "SQLInstance" -WorkloadType "MSSQL" -VaultId $Vault.ID
```

<span data-ttu-id="57968-115">Il primo comando ottiene il contenitore di tipo MSSQL e quindi lo archivia nella $Container variabile.</span><span class="sxs-lookup"><span data-stu-id="57968-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="57968-116">Il secondo comando recupera l'elemento protetto da backup in $Container e quindi lo archivia nella $Item variabile.</span><span class="sxs-lookup"><span data-stu-id="57968-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="57968-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57968-117">PARAMETERS</span></span>

### <span data-ttu-id="57968-118">-Container</span><span class="sxs-lookup"><span data-stu-id="57968-118">-Container</span></span>
<span data-ttu-id="57968-119">Contenitore in cui si trova l'elemento</span><span class="sxs-lookup"><span data-stu-id="57968-119">Container where the item resides</span></span>

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

### <span data-ttu-id="57968-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57968-120">-DefaultProfile</span></span>
<span data-ttu-id="57968-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57968-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57968-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="57968-122">-ItemType</span></span>
<span data-ttu-id="57968-123">Specifica il tipo di elemento proteggibile.</span><span class="sxs-lookup"><span data-stu-id="57968-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="57968-124">Valori applicabili: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span><span class="sxs-lookup"><span data-stu-id="57968-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

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

### <span data-ttu-id="57968-125">-Name</span><span class="sxs-lookup"><span data-stu-id="57968-125">-Name</span></span>
<span data-ttu-id="57968-126">Specifica il nome del database, dell'istanza o del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="57968-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

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

### <span data-ttu-id="57968-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="57968-127">-ParentID</span></span>
<span data-ttu-id="57968-128">È stato specificato l ARM ID utente di un'istanza o di un gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="57968-128">Specified the ARM ID of an Instance or AG.</span></span>

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

### <span data-ttu-id="57968-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="57968-129">-ServerName</span></span>
<span data-ttu-id="57968-130">Specifica il nome del server a cui appartiene l'elemento.</span><span class="sxs-lookup"><span data-stu-id="57968-130">Specifies the name of the server to which the item belongs.</span></span>

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

### <span data-ttu-id="57968-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="57968-131">-VaultId</span></span>
<span data-ttu-id="57968-132">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="57968-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="57968-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="57968-133">-WorkloadType</span></span>
<span data-ttu-id="57968-134">Tipo di carico di lavoro della risorsa.</span><span class="sxs-lookup"><span data-stu-id="57968-134">Workload type of the resource.</span></span> <span data-ttu-id="57968-135">I valori correnti supportati sono AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="57968-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="57968-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57968-136">CommonParameters</span></span>
<span data-ttu-id="57968-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57968-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57968-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="57968-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57968-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="57968-139">INPUTS</span></span>

### <span data-ttu-id="57968-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="57968-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="57968-141">System.String</span><span class="sxs-lookup"><span data-stu-id="57968-141">System.String</span></span>

## <span data-ttu-id="57968-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57968-142">OUTPUTS</span></span>

### <span data-ttu-id="57968-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="57968-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="57968-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="57968-144">NOTES</span></span>

## <span data-ttu-id="57968-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57968-145">RELATED LINKS</span></span>
