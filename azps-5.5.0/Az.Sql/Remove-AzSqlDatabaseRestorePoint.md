---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 2e98f832bd13509a853d85037a413b6fd5895695
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196038"
---
# <span data-ttu-id="710f4-101">Remove-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="710f4-101">Remove-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="710f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="710f4-102">SYNOPSIS</span></span>
<span data-ttu-id="710f4-103">Rimuove un determinato punto di ripristino da un SQL database.</span><span class="sxs-lookup"><span data-stu-id="710f4-103">Removes given restore point from a SQL Database.</span></span>

## <span data-ttu-id="710f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="710f4-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="710f4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="710f4-105">DESCRIPTION</span></span>
<span data-ttu-id="710f4-106">Il cmdlet **Remove-AzSqlDatabaseRestorePoint** rimuove il punto di ripristino specificato da Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="710f4-106">The **Remove-AzSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="710f4-107">Questo cmdlet è attualmente supportato dal servizio Datawarehouse SQL Server Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="710f4-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="710f4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="710f4-108">EXAMPLES</span></span>

### <span data-ttu-id="710f4-109">Esempio 1: Rimuovere un punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="710f4-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="710f4-110">Questo comando rimuove un punto di ripristino per il database SQL Azure in base alla data di creazione.</span><span class="sxs-lookup"><span data-stu-id="710f4-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="710f4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="710f4-111">PARAMETERS</span></span>

### <span data-ttu-id="710f4-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="710f4-112">-DatabaseName</span></span>
<span data-ttu-id="710f4-113">Specifica il nome dell'SQL database.</span><span class="sxs-lookup"><span data-stu-id="710f4-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="710f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="710f4-114">-DefaultProfile</span></span>
<span data-ttu-id="710f4-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="710f4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="710f4-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="710f4-116">-PassThru</span></span>
<span data-ttu-id="710f4-117">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="710f4-117">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="710f4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="710f4-118">-ResourceGroupName</span></span>
<span data-ttu-id="710f4-119">Specifica il nome del gruppo di risorse a cui è assegnato SQL database.</span><span class="sxs-lookup"><span data-stu-id="710f4-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="710f4-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="710f4-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="710f4-121">Specifica la data di creazione del punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="710f4-121">Specifies the restore point creation date.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="710f4-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="710f4-122">-ServerName</span></span>
<span data-ttu-id="710f4-123">Specifica il nome del server AzureSQL che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="710f4-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="710f4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="710f4-124">-Confirm</span></span>
<span data-ttu-id="710f4-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="710f4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="710f4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="710f4-126">-WhatIf</span></span>
<span data-ttu-id="710f4-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="710f4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="710f4-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="710f4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="710f4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="710f4-129">CommonParameters</span></span>
<span data-ttu-id="710f4-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="710f4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="710f4-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="710f4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="710f4-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="710f4-132">INPUTS</span></span>

### <span data-ttu-id="710f4-133">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="710f4-133">System.DateTime</span></span>

### <span data-ttu-id="710f4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="710f4-134">System.String</span></span>

## <span data-ttu-id="710f4-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="710f4-135">OUTPUTS</span></span>

### <span data-ttu-id="710f4-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="710f4-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="710f4-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="710f4-137">NOTES</span></span>

## <span data-ttu-id="710f4-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="710f4-138">RELATED LINKS</span></span>
