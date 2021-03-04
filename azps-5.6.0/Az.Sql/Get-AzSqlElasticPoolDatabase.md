---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 4a9e128fb8c67c44329dd2b99da8ce4722835323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999533"
---
# <span data-ttu-id="fba6c-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="fba6c-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="fba6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fba6c-102">SYNOPSIS</span></span>
<span data-ttu-id="fba6c-103">Recupera i database elastici in un pool flessibile e i relativi valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="fba6c-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="fba6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fba6c-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fba6c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fba6c-105">DESCRIPTION</span></span>
<span data-ttu-id="fba6c-106">Il cmdlet **Get-AzSqlElasticPoolDatabase** ottiene database elastici in un pool flessibile e i relativi valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="fba6c-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="fba6c-107">È possibile specificare il nome di un database elastico in Azure SQL database per visualizzare i valori delle proprietà solo per tale database.</span><span class="sxs-lookup"><span data-stu-id="fba6c-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="fba6c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fba6c-108">EXAMPLES</span></span>

### <span data-ttu-id="fba6c-109">Esempio 1: Recuperare tutti i database in un pool flessibile</span><span class="sxs-lookup"><span data-stu-id="fba6c-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="fba6c-110">Questo comando recupera tutti i database in un pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="fba6c-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="fba6c-111">Esempio 2: Recuperare tutti i database in un pool flessibile usando i filtri</span><span class="sxs-lookup"><span data-stu-id="fba6c-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="fba6c-112">Questo comando recupera tutti i database di un pool elastico denominato ElasticPool01 che iniziano con "Database".</span><span class="sxs-lookup"><span data-stu-id="fba6c-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="fba6c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fba6c-113">PARAMETERS</span></span>

### <span data-ttu-id="fba6c-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fba6c-114">-DatabaseName</span></span>
<span data-ttu-id="fba6c-115">Specifica il nome del SQL database predefinito che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fba6c-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fba6c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba6c-116">-DefaultProfile</span></span>
<span data-ttu-id="fba6c-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fba6c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fba6c-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="fba6c-118">-ElasticPoolName</span></span>
<span data-ttu-id="fba6c-119">Specifica il nome di un pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="fba6c-119">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="fba6c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fba6c-120">-ResourceGroupName</span></span>
<span data-ttu-id="fba6c-121">Specifica il nome di un gruppo di risorse a cui è assegnato il pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="fba6c-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="fba6c-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fba6c-122">-ServerName</span></span>
<span data-ttu-id="fba6c-123">Specifica il nome di un server che contiene un pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="fba6c-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="fba6c-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fba6c-124">-Confirm</span></span>
<span data-ttu-id="fba6c-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fba6c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fba6c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fba6c-126">-WhatIf</span></span>
<span data-ttu-id="fba6c-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fba6c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fba6c-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fba6c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fba6c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba6c-129">CommonParameters</span></span>
<span data-ttu-id="fba6c-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fba6c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba6c-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fba6c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba6c-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="fba6c-132">INPUTS</span></span>

### <span data-ttu-id="fba6c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fba6c-133">System.String</span></span>

## <span data-ttu-id="fba6c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fba6c-134">OUTPUTS</span></span>

### <span data-ttu-id="fba6c-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fba6c-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="fba6c-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="fba6c-136">NOTES</span></span>

## <span data-ttu-id="fba6c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fba6c-137">RELATED LINKS</span></span>

[<span data-ttu-id="fba6c-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fba6c-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="fba6c-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="fba6c-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="fba6c-140">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fba6c-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="fba6c-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fba6c-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="fba6c-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fba6c-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

