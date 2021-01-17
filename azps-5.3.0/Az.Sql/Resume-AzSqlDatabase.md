---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: a31a77f4e0780b5100018962b3475a0dffa97d9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376487"
---
# <span data-ttu-id="577ca-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="577ca-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="577ca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="577ca-102">SYNOPSIS</span></span>
<span data-ttu-id="577ca-103">Riprende un database di SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="577ca-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="577ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="577ca-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="577ca-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="577ca-105">DESCRIPTION</span></span>
<span data-ttu-id="577ca-106">Il cmdlet **Resume-AzSqlDatabase** riprende un database di Azure SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="577ca-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="577ca-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="577ca-107">EXAMPLES</span></span>

### <span data-ttu-id="577ca-108">Esempio 1: riprende un database di Azure SQL data warehouse</span><span class="sxs-lookup"><span data-stu-id="577ca-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="577ca-109">Questo comando riprende un database SQL data warehouse di Azure sospesa.</span><span class="sxs-lookup"><span data-stu-id="577ca-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="577ca-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="577ca-110">PARAMETERS</span></span>

### <span data-ttu-id="577ca-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="577ca-111">-AsJob</span></span>
<span data-ttu-id="577ca-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="577ca-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="577ca-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="577ca-113">-DatabaseName</span></span>
<span data-ttu-id="577ca-114">Specifica il nome del database che questo cmdlet riprende.</span><span class="sxs-lookup"><span data-stu-id="577ca-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="577ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="577ca-115">-DefaultProfile</span></span>
<span data-ttu-id="577ca-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="577ca-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="577ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="577ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="577ca-118">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="577ca-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="577ca-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="577ca-119">-ServerName</span></span>
<span data-ttu-id="577ca-120">Specifica il nome del server che ospita il database che questo cmdlet riprende.</span><span class="sxs-lookup"><span data-stu-id="577ca-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="577ca-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="577ca-121">-Confirm</span></span>
<span data-ttu-id="577ca-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="577ca-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="577ca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="577ca-123">-WhatIf</span></span>
<span data-ttu-id="577ca-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="577ca-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="577ca-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="577ca-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="577ca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577ca-126">CommonParameters</span></span>
<span data-ttu-id="577ca-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="577ca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="577ca-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="577ca-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577ca-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="577ca-129">INPUTS</span></span>

### <span data-ttu-id="577ca-130">System. String</span><span class="sxs-lookup"><span data-stu-id="577ca-130">System.String</span></span>

## <span data-ttu-id="577ca-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="577ca-131">OUTPUTS</span></span>

### <span data-ttu-id="577ca-132">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="577ca-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="577ca-133">Note</span><span class="sxs-lookup"><span data-stu-id="577ca-133">NOTES</span></span>
* <span data-ttu-id="577ca-134">Il cmdlet **Resume-AzSqlDatabase** funziona solo nei database di Azure SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="577ca-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="577ca-135">Questa operazione non è supportata nelle edizioni Basic, standard e Premium di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="577ca-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="577ca-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="577ca-136">RELATED LINKS</span></span>

[<span data-ttu-id="577ca-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="577ca-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="577ca-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="577ca-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="577ca-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="577ca-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="577ca-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="577ca-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="577ca-141">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="577ca-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="577ca-142">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="577ca-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


