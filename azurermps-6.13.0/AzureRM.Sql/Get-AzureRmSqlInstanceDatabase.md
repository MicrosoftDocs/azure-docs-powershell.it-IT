---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: fe6779c64a3cbc5a484dd4a3ee3662bcdaf59059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514772"
---
# <span data-ttu-id="7620d-101">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7620d-101">Get-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="7620d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7620d-102">SYNOPSIS</span></span>
<span data-ttu-id="7620d-103">Restituisce informazioni sul database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7620d-103">Returns information about Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7620d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7620d-104">SYNTAX</span></span>

### <span data-ttu-id="7620d-105">GetInstanceDatabaseFromInputParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7620d-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7620d-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="7620d-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7620d-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="7620d-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7620d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7620d-108">DESCRIPTION</span></span>
<span data-ttu-id="7620d-109">Il cmdlet **Get-AzureRmSqlInstanceDatabase** ottiene uno o più database SQL di Azure da un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="7620d-109">The **Get-AzureRmSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="7620d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7620d-110">EXAMPLES</span></span>

### <span data-ttu-id="7620d-111">Esempio 1: ottenere tutti i database in un'istanza</span><span class="sxs-lookup"><span data-stu-id="7620d-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
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

<span data-ttu-id="7620d-112">Questo comando consente di ottenere tutti i database nell'istanza denominata managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="7620d-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="7620d-113">Esempio 2: ottenere un database per nome in un'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="7620d-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="7620d-114">Questo comando ottiene un database denominato managedDatabase1 da un'istanza denominata managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="7620d-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

## <span data-ttu-id="7620d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7620d-115">PARAMETERS</span></span>

### <span data-ttu-id="7620d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7620d-116">-DefaultProfile</span></span>
<span data-ttu-id="7620d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7620d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7620d-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7620d-118">-InstanceName</span></span>
<span data-ttu-id="7620d-119">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7620d-119">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7620d-120">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="7620d-120">-InstanceObject</span></span>
<span data-ttu-id="7620d-121">Oggetto Instance da usare per ottenere il database dell'istanza</span><span class="sxs-lookup"><span data-stu-id="7620d-121">The instance object to use for getting instance database</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7620d-122">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="7620d-122">-InstanceResourceId</span></span>
<span data-ttu-id="7620d-123">ID risorsa dell'oggetto Instance da ottenere</span><span class="sxs-lookup"><span data-stu-id="7620d-123">The resource id of instance object to get</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7620d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7620d-124">-Name</span></span>
<span data-ttu-id="7620d-125">Nome del database dell'istanza SQL di Azure da recuperare.</span><span class="sxs-lookup"><span data-stu-id="7620d-125">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7620d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7620d-126">-ResourceGroupName</span></span>
<span data-ttu-id="7620d-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7620d-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7620d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7620d-128">CommonParameters</span></span>
<span data-ttu-id="7620d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7620d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7620d-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7620d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7620d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7620d-131">INPUTS</span></span>

### <span data-ttu-id="7620d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7620d-132">System.String</span></span>
<span data-ttu-id="7620d-133">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="7620d-133">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="7620d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7620d-134">OUTPUTS</span></span>

### <span data-ttu-id="7620d-135">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7620d-135">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="7620d-136">Note</span><span class="sxs-lookup"><span data-stu-id="7620d-136">NOTES</span></span>

## <span data-ttu-id="7620d-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7620d-137">RELATED LINKS</span></span>
