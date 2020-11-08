---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: df4ad0ea9f0e1990fa3c71915b1882baf1d3a762
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019530"
---
# <span data-ttu-id="dacaa-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="dacaa-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="dacaa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dacaa-102">SYNOPSIS</span></span>
<span data-ttu-id="dacaa-103">Ottiene lo stato delle operazioni del database.</span><span class="sxs-lookup"><span data-stu-id="dacaa-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="dacaa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dacaa-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dacaa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dacaa-105">DESCRIPTION</span></span>
<span data-ttu-id="dacaa-106">Il cmdlet **Get-AzSqlDatabaseActivity** ottiene lo stato delle operazioni di database in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="dacaa-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="dacaa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dacaa-107">EXAMPLES</span></span>

### <span data-ttu-id="dacaa-108">Esempio 1: ottenere lo stato per tutte le istanze di database SQL</span><span class="sxs-lookup"><span data-stu-id="dacaa-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="dacaa-109">Questo comando restituisce lo stato dell'operazione di tutte le istanze di database SQL in un pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="dacaa-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="dacaa-110">Esempio 2: ottenere lo stato per tutte le operazioni di database SQL</span><span class="sxs-lookup"><span data-stu-id="dacaa-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="dacaa-111">Questo comando restituisce lo stato di tutte le operazioni di database SQL in un database.</span><span class="sxs-lookup"><span data-stu-id="dacaa-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="dacaa-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dacaa-112">PARAMETERS</span></span>

### <span data-ttu-id="dacaa-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dacaa-113">-DatabaseName</span></span>
<span data-ttu-id="dacaa-114">Specifica il nome del database per cui questo cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="dacaa-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="dacaa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dacaa-115">-DefaultProfile</span></span>
<span data-ttu-id="dacaa-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dacaa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dacaa-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="dacaa-117">-ElasticPoolName</span></span>
<span data-ttu-id="dacaa-118">Specifica il nome del pool di database elastici per cui questo cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="dacaa-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dacaa-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="dacaa-119">-OperationId</span></span>
<span data-ttu-id="dacaa-120">Specifica l'ID dell'operazione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dacaa-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dacaa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dacaa-121">-ResourceGroupName</span></span>
<span data-ttu-id="dacaa-122">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="dacaa-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="dacaa-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="dacaa-123">-ServerName</span></span>
<span data-ttu-id="dacaa-124">Specifica il nome di Microsoft SQL Server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="dacaa-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="dacaa-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dacaa-125">-Confirm</span></span>
<span data-ttu-id="dacaa-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dacaa-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dacaa-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dacaa-127">-WhatIf</span></span>
<span data-ttu-id="dacaa-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dacaa-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dacaa-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dacaa-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dacaa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dacaa-130">CommonParameters</span></span>
<span data-ttu-id="dacaa-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dacaa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dacaa-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dacaa-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dacaa-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dacaa-133">INPUTS</span></span>

### <span data-ttu-id="dacaa-134">System. String</span><span class="sxs-lookup"><span data-stu-id="dacaa-134">System.String</span></span>

### <span data-ttu-id="dacaa-135">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dacaa-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="dacaa-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dacaa-136">OUTPUTS</span></span>

### <span data-ttu-id="dacaa-137">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="dacaa-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="dacaa-138">Note</span><span class="sxs-lookup"><span data-stu-id="dacaa-138">NOTES</span></span>

## <span data-ttu-id="dacaa-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dacaa-139">RELATED LINKS</span></span>
