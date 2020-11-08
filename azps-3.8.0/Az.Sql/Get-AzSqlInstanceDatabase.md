---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 8fb9b14dca32940911f0ef3bdae80a187c64b374
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022245"
---
# <span data-ttu-id="e8799-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e8799-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="e8799-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8799-102">SYNOPSIS</span></span>
<span data-ttu-id="e8799-103">Restituisce informazioni sul database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e8799-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="e8799-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8799-104">SYNTAX</span></span>

### <span data-ttu-id="e8799-105">GetInstanceDatabaseFromInputParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e8799-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8799-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="e8799-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8799-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="e8799-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8799-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8799-108">DESCRIPTION</span></span>
<span data-ttu-id="e8799-109">Il cmdlet **Get-AzSqlInstanceDatabase** ottiene uno o più database SQL di Azure da un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e8799-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="e8799-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8799-110">EXAMPLES</span></span>

### <span data-ttu-id="e8799-111">Esempio 1: ottenere tutti i database in un'istanza</span><span class="sxs-lookup"><span data-stu-id="e8799-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="e8799-112">Questo comando consente di ottenere tutti i database nell'istanza denominata managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="e8799-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="e8799-113">Esempio 2: ottenere un database per nome in un'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="e8799-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="e8799-114">Questo comando ottiene un database denominato managedDatabase1 da un'istanza denominata managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="e8799-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="e8799-115">Esempio 3: ottenere tutti i database in un'istanza usando il filtro</span><span class="sxs-lookup"><span data-stu-id="e8799-115">Example 3: Get all databases on a instance using filtering</span></span>
```
PS C:\> Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="e8799-116">Questo comando consente di ottenere tutti i database nell'istanza denominata managedInstance1 che iniziano con "managedDatabase".</span><span class="sxs-lookup"><span data-stu-id="e8799-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="e8799-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8799-117">PARAMETERS</span></span>

### <span data-ttu-id="e8799-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8799-118">-DefaultProfile</span></span>
<span data-ttu-id="e8799-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8799-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8799-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e8799-120">-InstanceName</span></span>
<span data-ttu-id="e8799-121">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="e8799-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8799-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="e8799-122">-InstanceObject</span></span>
<span data-ttu-id="e8799-123">Oggetto Instance da usare per ottenere il database dell'istanza</span><span class="sxs-lookup"><span data-stu-id="e8799-123">The instance object to use for getting instance database</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8799-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="e8799-124">-InstanceResourceId</span></span>
<span data-ttu-id="e8799-125">ID risorsa dell'oggetto Instance da ottenere</span><span class="sxs-lookup"><span data-stu-id="e8799-125">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8799-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8799-126">-Name</span></span>
<span data-ttu-id="e8799-127">Nome del database dell'istanza SQL di Azure da recuperare.</span><span class="sxs-lookup"><span data-stu-id="e8799-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8799-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8799-128">-ResourceGroupName</span></span>
<span data-ttu-id="e8799-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e8799-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8799-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8799-130">CommonParameters</span></span>
<span data-ttu-id="e8799-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8799-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8799-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8799-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8799-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8799-133">INPUTS</span></span>

### <span data-ttu-id="e8799-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e8799-134">System.String</span></span>

### <span data-ttu-id="e8799-135">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="e8799-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="e8799-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8799-136">OUTPUTS</span></span>

### <span data-ttu-id="e8799-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e8799-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e8799-138">Note</span><span class="sxs-lookup"><span data-stu-id="e8799-138">NOTES</span></span>

## <span data-ttu-id="e8799-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8799-139">RELATED LINKS</span></span>
