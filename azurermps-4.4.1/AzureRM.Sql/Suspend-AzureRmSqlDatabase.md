---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: 23affeb81159da5a9f1212f5190f927dc1689e44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520739"
---
# <span data-ttu-id="5db41-101">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5db41-101">Suspend-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="5db41-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5db41-102">SYNOPSIS</span></span>
<span data-ttu-id="5db41-103">Sospende un database di SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="5db41-103">Suspends a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5db41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5db41-104">SYNTAX</span></span>

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5db41-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5db41-105">DESCRIPTION</span></span>
<span data-ttu-id="5db41-106">Il cmdlet **Suspend-AzureRmSqlDatabase** sospende un database di Azure SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="5db41-106">The **Suspend-AzureRmSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="5db41-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5db41-107">EXAMPLES</span></span>

### <span data-ttu-id="5db41-108">Esempio 1: sospendere un database di Azure SQL data warehouse</span><span class="sxs-lookup"><span data-stu-id="5db41-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="5db41-109">Questo comando sospende un database di SQL data warehouse Active Azure.</span><span class="sxs-lookup"><span data-stu-id="5db41-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="5db41-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5db41-110">PARAMETERS</span></span>

### <span data-ttu-id="5db41-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5db41-111">-DatabaseName</span></span>
<span data-ttu-id="5db41-112">Specifica il nome del database sospeso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5db41-112">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="5db41-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5db41-113">-ResourceGroupName</span></span>
<span data-ttu-id="5db41-114">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="5db41-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5db41-115">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5db41-115">-ServerName</span></span>
<span data-ttu-id="5db41-116">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="5db41-116">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="5db41-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5db41-117">-Confirm</span></span>
<span data-ttu-id="5db41-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5db41-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5db41-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5db41-119">-WhatIf</span></span>
<span data-ttu-id="5db41-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5db41-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5db41-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5db41-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5db41-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db41-122">-DefaultProfile</span></span>
<span data-ttu-id="5db41-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5db41-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db41-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db41-124">CommonParameters</span></span>
<span data-ttu-id="5db41-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5db41-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db41-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5db41-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db41-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5db41-127">INPUTS</span></span>

### <span data-ttu-id="5db41-128">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5db41-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5db41-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5db41-129">OUTPUTS</span></span>

### <span data-ttu-id="5db41-130">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5db41-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5db41-131">Note</span><span class="sxs-lookup"><span data-stu-id="5db41-131">NOTES</span></span>
* <span data-ttu-id="5db41-132">Il cmdlet **Suspend-AzureRmSqlDatabase** funziona solo nei database di Azure SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="5db41-132">The **Suspend-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="5db41-133">Questa operazione non è supportata nelle edizioni Basic, standard e Premium di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="5db41-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="5db41-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5db41-134">RELATED LINKS</span></span>

[<span data-ttu-id="5db41-135">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5db41-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="5db41-136">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5db41-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="5db41-137">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5db41-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="5db41-138">Curriculum vitae-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5db41-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="5db41-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5db41-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="5db41-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="5db41-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


