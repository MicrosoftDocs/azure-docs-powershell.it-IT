---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: 12b44d2045574b1d787dd0b2bdb70ec44b616ae5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993241"
---
# <span data-ttu-id="3ae56-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="3ae56-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="3ae56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ae56-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae56-103">Ottiene lo stato delle operazioni di database.</span><span class="sxs-lookup"><span data-stu-id="3ae56-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="3ae56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ae56-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ae56-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3ae56-105">DESCRIPTION</span></span>
<span data-ttu-id="3ae56-106">Il cmdlet **Get-AzSqlDatabaseActivity** ottiene lo stato delle operazioni di database in Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3ae56-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="3ae56-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ae56-107">EXAMPLES</span></span>

### <span data-ttu-id="3ae56-108">Esempio 1: Ottenere lo stato per tutte le istanze SQL database</span><span class="sxs-lookup"><span data-stu-id="3ae56-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="3ae56-109">Questo comando restituisce lo stato dell'operazione di tutte SQL di database in un pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="3ae56-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="3ae56-110">Esempio 2: Ottenere lo stato per tutte le SQL di un database</span><span class="sxs-lookup"><span data-stu-id="3ae56-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="3ae56-111">Questo comando restituisce lo stato di tutte le SQL di un database.</span><span class="sxs-lookup"><span data-stu-id="3ae56-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="3ae56-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ae56-112">PARAMETERS</span></span>

### <span data-ttu-id="3ae56-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3ae56-113">-DatabaseName</span></span>
<span data-ttu-id="3ae56-114">Specifica il nome del database per cui il cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="3ae56-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="3ae56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae56-115">-DefaultProfile</span></span>
<span data-ttu-id="3ae56-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ae56-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ae56-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3ae56-117">-ElasticPoolName</span></span>
<span data-ttu-id="3ae56-118">Specifica il nome del pool di database elastico per cui il cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="3ae56-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="3ae56-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="3ae56-119">-OperationId</span></span>
<span data-ttu-id="3ae56-120">Specifica l'ID dell'operazione che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ae56-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3ae56-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ae56-121">-ResourceGroupName</span></span>
<span data-ttu-id="3ae56-122">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="3ae56-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="3ae56-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3ae56-123">-ServerName</span></span>
<span data-ttu-id="3ae56-124">Specifica il nome della cartella di Microsoft SQL Server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="3ae56-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="3ae56-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ae56-125">-Confirm</span></span>
<span data-ttu-id="3ae56-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ae56-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ae56-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ae56-127">-WhatIf</span></span>
<span data-ttu-id="3ae56-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ae56-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ae56-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ae56-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ae56-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae56-130">CommonParameters</span></span>
<span data-ttu-id="3ae56-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ae56-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae56-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3ae56-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae56-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="3ae56-133">INPUTS</span></span>

### <span data-ttu-id="3ae56-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3ae56-134">System.String</span></span>

### <span data-ttu-id="3ae56-135">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3ae56-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3ae56-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ae56-136">OUTPUTS</span></span>

### <span data-ttu-id="3ae56-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="3ae56-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="3ae56-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="3ae56-138">NOTES</span></span>

## <span data-ttu-id="3ae56-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ae56-139">RELATED LINKS</span></span>
