---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeletedinstancedatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
ms.openlocfilehash: bee6bd373c6b9c67afa8c70385c397d9334b733e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188793"
---
# <span data-ttu-id="aac8b-101">Get-AzSqlDeletedInstanceDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="aac8b-101">Get-AzSqlDeletedInstanceDatabaseBackup</span></span>

## <span data-ttu-id="aac8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aac8b-102">SYNOPSIS</span></span>
<span data-ttu-id="aac8b-103">Ottiene un database eliminato che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="aac8b-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="aac8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aac8b-104">SYNTAX</span></span>

### <span data-ttu-id="aac8b-105">DeletedDatabaseList (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aac8b-105">DeletedDatabaseList (Default)</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aac8b-106">DeletedDatabaseByNameAndDeletedTime</span><span class="sxs-lookup"><span data-stu-id="aac8b-106">DeletedDatabaseByNameAndDeletedTime</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 -DatabaseName <String> [-DeletionDate] <DateTime> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aac8b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aac8b-107">DESCRIPTION</span></span>
<span data-ttu-id="aac8b-108">Il cmdlet **Get-AzSqlDeletedInstanceDatabaseBackup** ottiene un backup di database di istanza SQL eliminato specificato che è possibile ripristinare o tutti i backup eliminati che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="aac8b-108">The **Get-AzSqlDeletedInstanceDatabaseBackup** cmdlet gets a specified deleted SQL Instance database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="aac8b-109">Questo cmdlet è supportato anche dal servizio database stretch dell'istanza SQL in Azure.</span><span class="sxs-lookup"><span data-stu-id="aac8b-109">This cmdlet is also supported by the SQL Instance Stretch Database service on Azure.</span></span>

## <span data-ttu-id="aac8b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aac8b-110">EXAMPLES</span></span>

### <span data-ttu-id="aac8b-111">Esempio 1: ottenere tutti i backup di database eliminati in un server</span><span class="sxs-lookup"><span data-stu-id="aac8b-111">Example 1: Get all deleted database backups on a server</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000

DeletionDate         : 2019-03-04 04:00:08 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB3
CreationDate         : 2019-03-04 03:00:31 AM
EarliestRestorePoint : 2019-03-04 03:05:23 AM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB3,13196145
                       6082100000
```

<span data-ttu-id="aac8b-112">Questo comando ottiene tutti i backup del database eliminati in un server.</span><span class="sxs-lookup"><span data-stu-id="aac8b-112">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="aac8b-113">Esempio 2: ottenere un backup del database eliminato specificato</span><span class="sxs-lookup"><span data-stu-id="aac8b-113">Example 2: Get a specified deleted database backup</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000
```

## <span data-ttu-id="aac8b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aac8b-114">PARAMETERS</span></span>

### <span data-ttu-id="aac8b-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aac8b-115">-DatabaseName</span></span>
<span data-ttu-id="aac8b-116">Nome del database dell'istanza SQL di Azure per cui recuperare i backup.</span><span class="sxs-lookup"><span data-stu-id="aac8b-116">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac8b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac8b-117">-DefaultProfile</span></span>
<span data-ttu-id="aac8b-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aac8b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aac8b-119">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="aac8b-119">-DeletionDate</span></span>
<span data-ttu-id="aac8b-120">Data di eliminazione del database dell'istanza di Azure SQL per il recupero dei backup, con precisione in millisecondi (ad esempio 2016-02-23T00:21:22.847 Z)</span><span class="sxs-lookup"><span data-stu-id="aac8b-120">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac8b-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="aac8b-121">-InstanceName</span></span>
<span data-ttu-id="aac8b-122">Nome dell'istanza gestita di Azure SQL in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="aac8b-122">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac8b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aac8b-123">-ResourceGroupName</span></span>
<span data-ttu-id="aac8b-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aac8b-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac8b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac8b-125">CommonParameters</span></span>
<span data-ttu-id="aac8b-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aac8b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac8b-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aac8b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac8b-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aac8b-128">INPUTS</span></span>

### <span data-ttu-id="aac8b-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="aac8b-129">None</span></span>

## <span data-ttu-id="aac8b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aac8b-130">OUTPUTS</span></span>

### <span data-ttu-id="aac8b-131">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlDeletedManagedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="aac8b-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span></span>

## <span data-ttu-id="aac8b-132">Note</span><span class="sxs-lookup"><span data-stu-id="aac8b-132">NOTES</span></span>

## <span data-ttu-id="aac8b-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aac8b-133">RELATED LINKS</span></span>
