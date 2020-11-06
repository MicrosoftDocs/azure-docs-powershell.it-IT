---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/resume-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
ms.openlocfilehash: eef0b5d4b74f6390044453ec318b5f3de6846814
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512188"
---
# <span data-ttu-id="79ab6-101">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="79ab6-101">Resume-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="79ab6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79ab6-102">SYNOPSIS</span></span>
<span data-ttu-id="79ab6-103">Riprende un database di SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="79ab6-103">Resumes a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79ab6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79ab6-104">SYNTAX</span></span>

```
Resume-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79ab6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79ab6-105">DESCRIPTION</span></span>
<span data-ttu-id="79ab6-106">Il cmdlet **Resume-AzureRmSqlDatabase** riprende un database di Azure SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="79ab6-106">The **Resume-AzureRmSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="79ab6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79ab6-107">EXAMPLES</span></span>

### <span data-ttu-id="79ab6-108">Esempio 1: riprende un database di Azure SQL data warehouse</span><span class="sxs-lookup"><span data-stu-id="79ab6-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="79ab6-109">Questo comando riprende un database SQL data warehouse di Azure sospesa.</span><span class="sxs-lookup"><span data-stu-id="79ab6-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="79ab6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79ab6-110">PARAMETERS</span></span>

### <span data-ttu-id="79ab6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79ab6-111">-AsJob</span></span>
<span data-ttu-id="79ab6-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="79ab6-112">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79ab6-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="79ab6-113">-DatabaseName</span></span>
<span data-ttu-id="79ab6-114">Specifica il nome del database che questo cmdlet riprende.</span><span class="sxs-lookup"><span data-stu-id="79ab6-114">Specifies the name of the database that this cmdlet resumes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79ab6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79ab6-115">-DefaultProfile</span></span>
<span data-ttu-id="79ab6-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="79ab6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79ab6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79ab6-117">-ResourceGroupName</span></span>
<span data-ttu-id="79ab6-118">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="79ab6-118">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79ab6-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="79ab6-119">-ServerName</span></span>
<span data-ttu-id="79ab6-120">Specifica il nome del server che ospita il database che questo cmdlet riprende.</span><span class="sxs-lookup"><span data-stu-id="79ab6-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79ab6-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="79ab6-121">-Confirm</span></span>
<span data-ttu-id="79ab6-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79ab6-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79ab6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79ab6-123">-WhatIf</span></span>
<span data-ttu-id="79ab6-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79ab6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79ab6-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79ab6-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79ab6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ab6-126">CommonParameters</span></span>
<span data-ttu-id="79ab6-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79ab6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ab6-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79ab6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ab6-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79ab6-129">INPUTS</span></span>

### <span data-ttu-id="79ab6-130">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="79ab6-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="79ab6-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79ab6-131">OUTPUTS</span></span>

### <span data-ttu-id="79ab6-132">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="79ab6-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="79ab6-133">Note</span><span class="sxs-lookup"><span data-stu-id="79ab6-133">NOTES</span></span>
* <span data-ttu-id="79ab6-134">Il cmdlet **Resume-AzureRmSqlDatabase** funziona solo nei database di Azure SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="79ab6-134">The **Resume-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="79ab6-135">Questa operazione non è supportata nelle edizioni Basic, standard e Premium di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="79ab6-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="79ab6-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79ab6-136">RELATED LINKS</span></span>

[<span data-ttu-id="79ab6-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="79ab6-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="79ab6-138">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="79ab6-138">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="79ab6-139">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="79ab6-139">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="79ab6-140">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="79ab6-140">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="79ab6-141">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="79ab6-141">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="79ab6-142">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="79ab6-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


