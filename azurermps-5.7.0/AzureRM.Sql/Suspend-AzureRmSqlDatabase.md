---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/suspend-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: b4238ff85a35bcf6a48016a005af8a1f889332cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687405"
---
# <span data-ttu-id="651c6-101">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="651c6-101">Suspend-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="651c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="651c6-102">SYNOPSIS</span></span>
<span data-ttu-id="651c6-103">Sospende un database di SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="651c6-103">Suspends a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="651c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="651c6-104">SYNTAX</span></span>

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="651c6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="651c6-105">DESCRIPTION</span></span>
<span data-ttu-id="651c6-106">Il cmdlet **Suspend-AzureRmSqlDatabase** sospende un database di Azure SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="651c6-106">The **Suspend-AzureRmSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="651c6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="651c6-107">EXAMPLES</span></span>

### <span data-ttu-id="651c6-108">Esempio 1: sospendere un database di Azure SQL data warehouse</span><span class="sxs-lookup"><span data-stu-id="651c6-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="651c6-109">Questo comando sospende un database di SQL data warehouse Active Azure.</span><span class="sxs-lookup"><span data-stu-id="651c6-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="651c6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="651c6-110">PARAMETERS</span></span>

### <span data-ttu-id="651c6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="651c6-111">-AsJob</span></span>
<span data-ttu-id="651c6-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="651c6-112">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="651c6-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="651c6-113">-DatabaseName</span></span>
<span data-ttu-id="651c6-114">Specifica il nome del database sospeso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="651c6-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="651c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="651c6-115">-DefaultProfile</span></span>
<span data-ttu-id="651c6-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="651c6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="651c6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="651c6-117">-ResourceGroupName</span></span>
<span data-ttu-id="651c6-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="651c6-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="651c6-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="651c6-119">-ServerName</span></span>
<span data-ttu-id="651c6-120">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="651c6-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="651c6-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="651c6-121">-Confirm</span></span>
<span data-ttu-id="651c6-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="651c6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="651c6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="651c6-123">-WhatIf</span></span>
<span data-ttu-id="651c6-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="651c6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="651c6-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="651c6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="651c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="651c6-126">CommonParameters</span></span>
<span data-ttu-id="651c6-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="651c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="651c6-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="651c6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="651c6-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="651c6-129">INPUTS</span></span>

### <span data-ttu-id="651c6-130">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="651c6-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="651c6-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="651c6-131">OUTPUTS</span></span>

### <span data-ttu-id="651c6-132">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="651c6-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="651c6-133">Note</span><span class="sxs-lookup"><span data-stu-id="651c6-133">NOTES</span></span>
* <span data-ttu-id="651c6-134">Il cmdlet **Suspend-AzureRmSqlDatabase** funziona solo nei database di Azure SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="651c6-134">The **Suspend-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="651c6-135">Questa operazione non è supportata nelle edizioni Basic, standard e Premium di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="651c6-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="651c6-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="651c6-136">RELATED LINKS</span></span>

[<span data-ttu-id="651c6-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="651c6-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="651c6-138">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="651c6-138">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="651c6-139">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="651c6-139">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="651c6-140">Curriculum vitae-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="651c6-140">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="651c6-141">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="651c6-141">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="651c6-142">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="651c6-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


