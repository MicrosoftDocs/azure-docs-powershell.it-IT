---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: a31a77f4e0780b5100018962b3475a0dffa97d9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201407"
---
# <span data-ttu-id="065e2-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="065e2-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="065e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="065e2-102">SYNOPSIS</span></span>
<span data-ttu-id="065e2-103">Riprende un database SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="065e2-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="065e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="065e2-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="065e2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="065e2-105">DESCRIPTION</span></span>
<span data-ttu-id="065e2-106">Il cmdlet **Resume-AzSqlDatabase** riprende un database azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="065e2-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="065e2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="065e2-107">EXAMPLES</span></span>

### <span data-ttu-id="065e2-108">Esempio 1: riprende un database di Azure SQL Data Warehouse</span><span class="sxs-lookup"><span data-stu-id="065e2-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="065e2-109">Questo comando riprende un database Azure SQL Data Warehouse sospeso.</span><span class="sxs-lookup"><span data-stu-id="065e2-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="065e2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="065e2-110">PARAMETERS</span></span>

### <span data-ttu-id="065e2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="065e2-111">-AsJob</span></span>
<span data-ttu-id="065e2-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="065e2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="065e2-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="065e2-113">-DatabaseName</span></span>
<span data-ttu-id="065e2-114">Specifica il nome del database che il cmdlet riprende.</span><span class="sxs-lookup"><span data-stu-id="065e2-114">Specifies the name of the database that this cmdlet resumes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="065e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="065e2-115">-DefaultProfile</span></span>
<span data-ttu-id="065e2-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="065e2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="065e2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="065e2-117">-ResourceGroupName</span></span>
<span data-ttu-id="065e2-118">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="065e2-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="065e2-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="065e2-119">-ServerName</span></span>
<span data-ttu-id="065e2-120">Specifica il nome del server che ospita il database che il cmdlet riprende.</span><span class="sxs-lookup"><span data-stu-id="065e2-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="065e2-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="065e2-121">-Confirm</span></span>
<span data-ttu-id="065e2-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="065e2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="065e2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="065e2-123">-WhatIf</span></span>
<span data-ttu-id="065e2-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="065e2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="065e2-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="065e2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="065e2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="065e2-126">CommonParameters</span></span>
<span data-ttu-id="065e2-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="065e2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="065e2-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="065e2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="065e2-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="065e2-129">INPUTS</span></span>

### <span data-ttu-id="065e2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="065e2-130">System.String</span></span>

## <span data-ttu-id="065e2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="065e2-131">OUTPUTS</span></span>

### <span data-ttu-id="065e2-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="065e2-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="065e2-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="065e2-133">NOTES</span></span>
* <span data-ttu-id="065e2-134">Il cmdlet **Resume-AzSqlDatabase** funziona solo nei database di Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="065e2-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="065e2-135">Questa operazione non è supportata nelle edizioni Azure SQL Database Basic, Standard e Premium.</span><span class="sxs-lookup"><span data-stu-id="065e2-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="065e2-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="065e2-136">RELATED LINKS</span></span>

[<span data-ttu-id="065e2-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="065e2-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="065e2-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="065e2-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="065e2-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="065e2-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="065e2-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="065e2-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="065e2-141">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="065e2-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="065e2-142">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="065e2-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


