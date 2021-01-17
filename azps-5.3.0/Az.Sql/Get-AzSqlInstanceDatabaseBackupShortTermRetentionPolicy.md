---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 3666fd9c790f5445f83c3a068e7423b64a172c5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475662"
---
# <span data-ttu-id="23891-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="23891-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="23891-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23891-102">SYNOPSIS</span></span>
<span data-ttu-id="23891-103">Ottiene un criterio di conservazione a breve termine di backup.</span><span class="sxs-lookup"><span data-stu-id="23891-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="23891-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23891-104">SYNTAX</span></span>

### <span data-ttu-id="23891-105">PolicyByResourceInstanceDatabaseSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="23891-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23891-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="23891-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23891-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="23891-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23891-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23891-108">DESCRIPTION</span></span>
<span data-ttu-id="23891-109">Il cmdlet **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** ottiene i criteri di conservazione a breve termine registrati nel database.</span><span class="sxs-lookup"><span data-stu-id="23891-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="23891-110">Il criterio è il periodo di conservazione, in giorni, per i backup di ripristino temporizzato.</span><span class="sxs-lookup"><span data-stu-id="23891-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="23891-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23891-111">EXAMPLES</span></span>

### <span data-ttu-id="23891-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="23891-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="23891-113">Questo comando ottiene i criteri di conservazione a breve termine per Database01.</span><span class="sxs-lookup"><span data-stu-id="23891-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="23891-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="23891-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="23891-115">Questo comando consente di ottenere i criteri di conservazione a breve termine per Database01 tramite piping in un oggetto di database.</span><span class="sxs-lookup"><span data-stu-id="23891-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="23891-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="23891-116">Example 3</span></span>
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

<span data-ttu-id="23891-117">Questo comando consente di ottenere i criteri di conservazione a breve termine per tutti i database eliminati denominati Database01 tramite piping in un oggetto di database eliminato.</span><span class="sxs-lookup"><span data-stu-id="23891-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="23891-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23891-118">PARAMETERS</span></span>

### <span data-ttu-id="23891-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="23891-119">-DatabaseName</span></span>
<span data-ttu-id="23891-120">Nome del database dell'istanza SQL di Azure per cui recuperare i backup.</span><span class="sxs-lookup"><span data-stu-id="23891-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="23891-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23891-121">-DefaultProfile</span></span>
<span data-ttu-id="23891-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23891-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23891-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="23891-123">-DeletionDate</span></span>
<span data-ttu-id="23891-124">Data di eliminazione del database dell'istanza di Azure SQL per il recupero dei backup, con precisione in millisecondi (ad esempio 2016-02-23T00:21:22.847 Z)</span><span class="sxs-lookup"><span data-stu-id="23891-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="23891-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23891-125">-InputObject</span></span>
<span data-ttu-id="23891-126">L'oggetto di database Live o Deleted per ottenere o impostare i criteri per.</span><span class="sxs-lookup"><span data-stu-id="23891-126">The live or deleted database object to get/set the policy for.</span></span>

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

### <span data-ttu-id="23891-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="23891-127">-InstanceName</span></span>
<span data-ttu-id="23891-128">Nome dell'istanza gestita di Azure SQL in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="23891-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="23891-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23891-129">-ResourceGroupName</span></span>
<span data-ttu-id="23891-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="23891-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="23891-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23891-131">-ResourceId</span></span>
<span data-ttu-id="23891-132">ID risorsa dei criteri di conservazione a breve termine.</span><span class="sxs-lookup"><span data-stu-id="23891-132">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="23891-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23891-133">CommonParameters</span></span>
<span data-ttu-id="23891-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23891-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23891-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23891-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23891-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23891-136">INPUTS</span></span>

### <span data-ttu-id="23891-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="23891-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="23891-138">System. String</span><span class="sxs-lookup"><span data-stu-id="23891-138">System.String</span></span>

## <span data-ttu-id="23891-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23891-139">OUTPUTS</span></span>

### <span data-ttu-id="23891-140">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="23891-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="23891-141">Note</span><span class="sxs-lookup"><span data-stu-id="23891-141">NOTES</span></span>

## <span data-ttu-id="23891-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23891-142">RELATED LINKS</span></span>
