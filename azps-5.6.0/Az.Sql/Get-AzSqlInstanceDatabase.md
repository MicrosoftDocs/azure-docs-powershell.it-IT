---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 4385b231a5346af6b49ad3a74c6c984f2f94c416
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999501"
---
# <span data-ttu-id="49941-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="49941-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="49941-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49941-102">SYNOPSIS</span></span>
<span data-ttu-id="49941-103">Restituisce informazioni su Azure SQL database dell'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="49941-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="49941-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49941-104">SYNTAX</span></span>

### <span data-ttu-id="49941-105">GetInstanceDatabaseFromInputParameters (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="49941-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49941-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="49941-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49941-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="49941-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49941-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="49941-108">DESCRIPTION</span></span>
<span data-ttu-id="49941-109">Il cmdlet **Get-AzSqlInstanceDatabase** ottiene uno o più database SQL Azure da un'istanza gestita SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="49941-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="49941-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49941-110">EXAMPLES</span></span>

### <span data-ttu-id="49941-111">Esempio 1: Recuperare tutti i database in un'istanza</span><span class="sxs-lookup"><span data-stu-id="49941-111">Example 1: Get all databases on a instance</span></span>
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

<span data-ttu-id="49941-112">Questo comando recupera tutti i database nell'istanza denominata managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="49941-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="49941-113">Esempio 2: Ottenere un database in base al nome in un'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="49941-113">Example 2: Get a database by name on a Managed instance</span></span>
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

<span data-ttu-id="49941-114">Questo comando recupera un database denominato managedDatabase1 da un'istanza denominata managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="49941-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="49941-115">Esempio 3: Recuperare tutti i database di un'istanza usando i filtri</span><span class="sxs-lookup"><span data-stu-id="49941-115">Example 3: Get all databases on a instance using filtering</span></span>
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

<span data-ttu-id="49941-116">Questo comando recupera tutti i database nell'istanza denominata managedInstance1 che iniziano con "managedDatabase".</span><span class="sxs-lookup"><span data-stu-id="49941-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="49941-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49941-117">PARAMETERS</span></span>

### <span data-ttu-id="49941-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49941-118">-DefaultProfile</span></span>
<span data-ttu-id="49941-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49941-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49941-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="49941-120">-InstanceName</span></span>
<span data-ttu-id="49941-121">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="49941-121">The instance name.</span></span>

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

### <span data-ttu-id="49941-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="49941-122">-InstanceObject</span></span>
<span data-ttu-id="49941-123">L'oggetto istanza da usare per ottenere il database dell'istanza</span><span class="sxs-lookup"><span data-stu-id="49941-123">The instance object to use for getting instance database</span></span>

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

### <span data-ttu-id="49941-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="49941-124">-InstanceResourceId</span></span>
<span data-ttu-id="49941-125">ID risorsa dell'oggetto istanza da ottenere</span><span class="sxs-lookup"><span data-stu-id="49941-125">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="49941-126">-Name</span><span class="sxs-lookup"><span data-stu-id="49941-126">-Name</span></span>
<span data-ttu-id="49941-127">Nome del database delle istanze SQL Azure da recuperare.</span><span class="sxs-lookup"><span data-stu-id="49941-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

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

### <span data-ttu-id="49941-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49941-128">-ResourceGroupName</span></span>
<span data-ttu-id="49941-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="49941-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="49941-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49941-130">CommonParameters</span></span>
<span data-ttu-id="49941-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49941-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49941-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="49941-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49941-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="49941-133">INPUTS</span></span>

### <span data-ttu-id="49941-134">System.String</span><span class="sxs-lookup"><span data-stu-id="49941-134">System.String</span></span>

### <span data-ttu-id="49941-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="49941-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="49941-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49941-136">OUTPUTS</span></span>

### <span data-ttu-id="49941-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="49941-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="49941-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="49941-138">NOTES</span></span>

## <span data-ttu-id="49941-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49941-139">RELATED LINKS</span></span>
