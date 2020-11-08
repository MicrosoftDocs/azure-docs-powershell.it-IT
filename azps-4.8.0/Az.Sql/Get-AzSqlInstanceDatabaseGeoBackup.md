---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: dd57b5d6e4301b1ab22b041367388d37986a946e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191211"
---
# <span data-ttu-id="a9df4-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="a9df4-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="a9df4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9df4-102">SYNOPSIS</span></span>
<span data-ttu-id="a9df4-103">Restituisce informazioni sul backup ridondante del database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a9df4-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="a9df4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9df4-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9df4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9df4-105">DESCRIPTION</span></span>
<span data-ttu-id="a9df4-106">Il cmdlet **Get-AzSqlInstanceDatabaseGeoBackup** ottiene uno o più database SQL di Azure Backup ridondanti da un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="a9df4-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="a9df4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9df4-107">EXAMPLES</span></span>

### <span data-ttu-id="a9df4-108">Esempio 1: ottenere tutti i backup ridondanti del database in un'istanza</span><span class="sxs-lookup"><span data-stu-id="a9df4-108">Example 1: Get all database redundant backups on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="a9df4-109">Questo comando consente di ottenere tutti i backup ridondanti del database nell'istanza denominata managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="a9df4-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="a9df4-110">Esempio 2: ottenere un backup ridondante del database per nome in un'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="a9df4-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="a9df4-111">Questo comando ottiene un backup ridondante di database denominato managedDatabase1 da un'istanza denominata managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="a9df4-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="a9df4-112">Esempio 3: ottenere tutti i backup ridondanti di database in un'istanza tramite filtro</span><span class="sxs-lookup"><span data-stu-id="a9df4-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="a9df4-113">Questo comando consente di ottenere tutti i backup ridondanti del database nell'istanza denominata managedInstance1 che iniziano con "managedDatabase".</span><span class="sxs-lookup"><span data-stu-id="a9df4-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="a9df4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9df4-114">PARAMETERS</span></span>

### <span data-ttu-id="a9df4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9df4-115">-DefaultProfile</span></span>
<span data-ttu-id="a9df4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9df4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9df4-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a9df4-117">-InstanceName</span></span>
<span data-ttu-id="a9df4-118">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a9df4-118">The name of the instance.</span></span>

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

### <span data-ttu-id="a9df4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9df4-119">-Name</span></span>
<span data-ttu-id="a9df4-120">Nome del database dell'istanza da recuperare.</span><span class="sxs-lookup"><span data-stu-id="a9df4-120">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RecoverableInstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9df4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9df4-121">-ResourceGroupName</span></span>
<span data-ttu-id="a9df4-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a9df4-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9df4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9df4-123">CommonParameters</span></span>
<span data-ttu-id="a9df4-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9df4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9df4-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9df4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9df4-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9df4-126">INPUTS</span></span>

### <span data-ttu-id="a9df4-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a9df4-127">None</span></span>

## <span data-ttu-id="a9df4-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9df4-128">OUTPUTS</span></span>

### <span data-ttu-id="a9df4-129">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a9df4-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="a9df4-130">Note</span><span class="sxs-lookup"><span data-stu-id="a9df4-130">NOTES</span></span>

## <span data-ttu-id="a9df4-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9df4-131">RELATED LINKS</span></span>
