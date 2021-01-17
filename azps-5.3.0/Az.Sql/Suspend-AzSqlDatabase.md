---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: a2bfaa0b6cd6d0731bceab7f05a59216e80bd135
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473728"
---
# <span data-ttu-id="fd81f-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fd81f-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="fd81f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd81f-102">SYNOPSIS</span></span>
<span data-ttu-id="fd81f-103">Sospende un database di SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="fd81f-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="fd81f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd81f-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd81f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd81f-105">DESCRIPTION</span></span>
<span data-ttu-id="fd81f-106">Il cmdlet **Suspend-AzSqlDatabase** sospende un database di Azure SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="fd81f-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="fd81f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd81f-107">EXAMPLES</span></span>

### <span data-ttu-id="fd81f-108">Esempio 1: sospendere un database di Azure SQL data warehouse</span><span class="sxs-lookup"><span data-stu-id="fd81f-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="fd81f-109">Questo comando sospende un database di SQL data warehouse Active Azure.</span><span class="sxs-lookup"><span data-stu-id="fd81f-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="fd81f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd81f-110">PARAMETERS</span></span>

### <span data-ttu-id="fd81f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd81f-111">-AsJob</span></span>
<span data-ttu-id="fd81f-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fd81f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd81f-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fd81f-113">-DatabaseName</span></span>
<span data-ttu-id="fd81f-114">Specifica il nome del database sospeso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd81f-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="fd81f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd81f-115">-DefaultProfile</span></span>
<span data-ttu-id="fd81f-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fd81f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd81f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd81f-117">-ResourceGroupName</span></span>
<span data-ttu-id="fd81f-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="fd81f-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fd81f-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="fd81f-119">-ServerName</span></span>
<span data-ttu-id="fd81f-120">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="fd81f-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="fd81f-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fd81f-121">-Confirm</span></span>
<span data-ttu-id="fd81f-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd81f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd81f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd81f-123">-WhatIf</span></span>
<span data-ttu-id="fd81f-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd81f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd81f-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd81f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd81f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd81f-126">CommonParameters</span></span>
<span data-ttu-id="fd81f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd81f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd81f-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd81f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd81f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd81f-129">INPUTS</span></span>

### <span data-ttu-id="fd81f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fd81f-130">System.String</span></span>

## <span data-ttu-id="fd81f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd81f-131">OUTPUTS</span></span>

### <span data-ttu-id="fd81f-132">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fd81f-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="fd81f-133">Note</span><span class="sxs-lookup"><span data-stu-id="fd81f-133">NOTES</span></span>
* <span data-ttu-id="fd81f-134">Il cmdlet **Suspend-AzSqlDatabase** funziona solo nei database di Azure SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="fd81f-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="fd81f-135">Questa operazione non è supportata nelle edizioni Basic, standard e Premium di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fd81f-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="fd81f-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd81f-136">RELATED LINKS</span></span>

[<span data-ttu-id="fd81f-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fd81f-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="fd81f-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fd81f-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="fd81f-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fd81f-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="fd81f-140">Curriculum vitae-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fd81f-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="fd81f-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fd81f-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="fd81f-142">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="fd81f-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


