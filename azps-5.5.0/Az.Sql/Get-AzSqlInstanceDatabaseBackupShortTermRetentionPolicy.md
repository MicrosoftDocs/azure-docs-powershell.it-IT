---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 3666fd9c790f5445f83c3a068e7423b64a172c5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198567"
---
# <span data-ttu-id="40be5-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="40be5-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="40be5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40be5-102">SYNOPSIS</span></span>
<span data-ttu-id="40be5-103">Ottiene un criterio di conservazione a breve termine di backup.</span><span class="sxs-lookup"><span data-stu-id="40be5-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="40be5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40be5-104">SYNTAX</span></span>

### <span data-ttu-id="40be5-105">PolicyByResourceInstanceDatabaseSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="40be5-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40be5-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="40be5-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40be5-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="40be5-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40be5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="40be5-108">DESCRIPTION</span></span>
<span data-ttu-id="40be5-109">Il cmdlet **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** ottiene il criterio di conservazione a breve termine registrato nel database.</span><span class="sxs-lookup"><span data-stu-id="40be5-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="40be5-110">Il criterio è il periodo di conservazione, in giorni, per i backup di ripristino tempormente pianificati.</span><span class="sxs-lookup"><span data-stu-id="40be5-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="40be5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40be5-111">EXAMPLES</span></span>

### <span data-ttu-id="40be5-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="40be5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="40be5-113">Questo comando ottiene i criteri di conservazione a breve termine per database01.</span><span class="sxs-lookup"><span data-stu-id="40be5-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="40be5-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="40be5-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="40be5-115">Questo comando ottiene i criteri di conservazione a breve termine per database01 tramite piping in un oggetto di database.</span><span class="sxs-lookup"><span data-stu-id="40be5-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="40be5-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="40be5-116">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 7

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 7
```

<span data-ttu-id="40be5-117">Questo comando recupera i criteri di conservazione a breve termine per tutti i database eliminati denominati database01 tramite piping in un oggetto di database eliminato.</span><span class="sxs-lookup"><span data-stu-id="40be5-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="40be5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40be5-118">PARAMETERS</span></span>

### <span data-ttu-id="40be5-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="40be5-119">-DatabaseName</span></span>
<span data-ttu-id="40be5-120">Nome del database delle istanze SQL Azure per cui recuperare i backup.</span><span class="sxs-lookup"><span data-stu-id="40be5-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40be5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40be5-121">-DefaultProfile</span></span>
<span data-ttu-id="40be5-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40be5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40be5-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="40be5-123">-DeletionDate</span></span>
<span data-ttu-id="40be5-124">Data di eliminazione del database delle istanze di Azure SQL per cui recuperare i backup con precisione in millisecondi (ad esempio 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="40be5-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40be5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40be5-125">-InputObject</span></span>
<span data-ttu-id="40be5-126">Oggetto di database live o eliminato per cui ottenere/impostare i criteri.</span><span class="sxs-lookup"><span data-stu-id="40be5-126">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40be5-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="40be5-127">-InstanceName</span></span>
<span data-ttu-id="40be5-128">Il nome dell'istanza SQL gestita di Azure in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="40be5-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40be5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40be5-129">-ResourceGroupName</span></span>
<span data-ttu-id="40be5-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="40be5-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40be5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40be5-131">-ResourceId</span></span>
<span data-ttu-id="40be5-132">ID risorsa per i criteri di conservazione a breve termine.</span><span class="sxs-lookup"><span data-stu-id="40be5-132">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40be5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40be5-133">CommonParameters</span></span>
<span data-ttu-id="40be5-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40be5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40be5-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="40be5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40be5-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="40be5-136">INPUTS</span></span>

### <span data-ttu-id="40be5-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="40be5-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="40be5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="40be5-138">System.String</span></span>

## <span data-ttu-id="40be5-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40be5-139">OUTPUTS</span></span>

### <span data-ttu-id="40be5-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="40be5-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="40be5-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="40be5-141">NOTES</span></span>

## <span data-ttu-id="40be5-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40be5-142">RELATED LINKS</span></span>
