---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: b0f3f657caea0da29ecf78baff15fe0afb7008ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967518"
---
# <span data-ttu-id="3581e-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3581e-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="3581e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3581e-102">SYNOPSIS</span></span>
<span data-ttu-id="3581e-103">Ottiene i criteri di conservazione a lungo termine del database.</span><span class="sxs-lookup"><span data-stu-id="3581e-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="3581e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3581e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3581e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3581e-105">DESCRIPTION</span></span>
<span data-ttu-id="3581e-106">Il cmdlet **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** ottiene i criteri di conservazione a lungo termine registrati nel database.</span><span class="sxs-lookup"><span data-stu-id="3581e-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="3581e-107">Il criterio è una risorsa di backup di Azure usata per definire i criteri di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="3581e-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="3581e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3581e-108">EXAMPLES</span></span>

### <span data-ttu-id="3581e-109">Esempio 1: Ottenere la versione corrente dei criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="3581e-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="3581e-110">Questo comando recupera la versione corrente dei criteri di conservazione a lungo termine per database01</span><span class="sxs-lookup"><span data-stu-id="3581e-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="3581e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3581e-111">PARAMETERS</span></span>

### <span data-ttu-id="3581e-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3581e-112">-DatabaseName</span></span>
<span data-ttu-id="3581e-113">Il nome del database SQL Azure da usare.</span><span class="sxs-lookup"><span data-stu-id="3581e-113">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3581e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3581e-114">-DefaultProfile</span></span>
<span data-ttu-id="3581e-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3581e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3581e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3581e-116">-ResourceGroupName</span></span>
<span data-ttu-id="3581e-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3581e-117">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3581e-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3581e-118">-ServerName</span></span>
<span data-ttu-id="3581e-119">Nome della cartella di SQL Server Azure in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="3581e-119">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3581e-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3581e-120">-Confirm</span></span>
<span data-ttu-id="3581e-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3581e-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3581e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3581e-122">-WhatIf</span></span>
<span data-ttu-id="3581e-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3581e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3581e-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3581e-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3581e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3581e-125">CommonParameters</span></span>
<span data-ttu-id="3581e-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3581e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3581e-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3581e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3581e-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="3581e-128">INPUTS</span></span>

### <span data-ttu-id="3581e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3581e-129">System.String</span></span>

## <span data-ttu-id="3581e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3581e-130">OUTPUTS</span></span>

### <span data-ttu-id="3581e-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="3581e-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="3581e-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="3581e-132">NOTES</span></span>

## <span data-ttu-id="3581e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3581e-133">RELATED LINKS</span></span>

[<span data-ttu-id="3581e-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3581e-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="3581e-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3581e-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="3581e-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3581e-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="3581e-137">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="3581e-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)