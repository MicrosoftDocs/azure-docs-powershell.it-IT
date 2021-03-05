---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: f64f7f7e16f18c9213c77df2903c17d8e7ea4ae1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999693"
---
# <span data-ttu-id="f78f5-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="f78f5-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="f78f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f78f5-102">SYNOPSIS</span></span>
<span data-ttu-id="f78f5-103">Recupera un database eliminato che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="f78f5-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="f78f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f78f5-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f78f5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f78f5-105">DESCRIPTION</span></span>
<span data-ttu-id="f78f5-106">Il cmdlet **Get-AzSqlDeletedDatabaseBackup** ottiene un backup del database SQL eliminato specificato che è possibile ripristinare o tutti i backup che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="f78f5-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="f78f5-107">Questo cmdlet è supportato anche dal servizio SQL Server stretch database in Azure.</span><span class="sxs-lookup"><span data-stu-id="f78f5-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f78f5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f78f5-108">EXAMPLES</span></span>

### <span data-ttu-id="f78f5-109">Esempio 1: Ottenere tutti i backup di database eliminati in un server</span><span class="sxs-lookup"><span data-stu-id="f78f5-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="f78f5-110">Questo comando recupera tutti i backup del database eliminati in un server.</span><span class="sxs-lookup"><span data-stu-id="f78f5-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="f78f5-111">Esempio 2: Ottenere un backup del database eliminato specificato</span><span class="sxs-lookup"><span data-stu-id="f78f5-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="f78f5-112">Questo comando recupera il backup del database eliminato per ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="f78f5-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="f78f5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f78f5-113">PARAMETERS</span></span>

### <span data-ttu-id="f78f5-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f78f5-114">-DatabaseName</span></span>
<span data-ttu-id="f78f5-115">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="f78f5-115">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f78f5-116">-DefaultProfile</span></span>
<span data-ttu-id="f78f5-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f78f5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f78f5-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="f78f5-118">-DeletionDate</span></span>
<span data-ttu-id="f78f5-119">Specifica la data, come oggetto **DateTime,** in cui il database è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="f78f5-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="f78f5-120">Per ottenere un **oggetto DateTime,** usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="f78f5-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78f5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f78f5-121">-ResourceGroupName</span></span>
<span data-ttu-id="f78f5-122">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="f78f5-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f78f5-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f78f5-123">-ServerName</span></span>
<span data-ttu-id="f78f5-124">Specifica il nome del server di database.</span><span class="sxs-lookup"><span data-stu-id="f78f5-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="f78f5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f78f5-125">-Confirm</span></span>
<span data-ttu-id="f78f5-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f78f5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f78f5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f78f5-127">-WhatIf</span></span>
<span data-ttu-id="f78f5-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f78f5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f78f5-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f78f5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f78f5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f78f5-130">CommonParameters</span></span>
<span data-ttu-id="f78f5-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f78f5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f78f5-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f78f5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f78f5-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="f78f5-133">INPUTS</span></span>

### <span data-ttu-id="f78f5-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f78f5-134">System.String</span></span>

### <span data-ttu-id="f78f5-135">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f78f5-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f78f5-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f78f5-136">OUTPUTS</span></span>

### <span data-ttu-id="f78f5-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="f78f5-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="f78f5-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="f78f5-138">NOTES</span></span>

## <span data-ttu-id="f78f5-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f78f5-139">RELATED LINKS</span></span>

[<span data-ttu-id="f78f5-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f78f5-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="f78f5-141">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="f78f5-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
