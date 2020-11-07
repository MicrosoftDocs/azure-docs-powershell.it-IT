---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: f03d172db1a4e8952fea989499f1689d9e0b6a83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857161"
---
# <span data-ttu-id="08877-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="08877-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="08877-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08877-102">SYNOPSIS</span></span>
<span data-ttu-id="08877-103">Ottiene i database elastici in un pool elastico e i relativi valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="08877-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="08877-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08877-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08877-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08877-105">DESCRIPTION</span></span>
<span data-ttu-id="08877-106">Il cmdlet **Get-AzSqlElasticPoolDatabase** ottiene i database elastici in un pool elastico e i relativi valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="08877-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="08877-107">Puoi specificare il nome di un database elastico in Azure SQL database per visualizzare i valori delle proprietà solo per il database.</span><span class="sxs-lookup"><span data-stu-id="08877-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="08877-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08877-108">EXAMPLES</span></span>

### <span data-ttu-id="08877-109">Esempio 1: ottenere tutti i database in un pool elastico</span><span class="sxs-lookup"><span data-stu-id="08877-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="08877-110">Questo comando consente di ottenere tutti i database in un pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="08877-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="08877-111">Esempio 2: ottenere tutti i database in un pool elastico usando il filtro</span><span class="sxs-lookup"><span data-stu-id="08877-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="08877-112">Questo comando consente di ottenere tutti i database in un pool elastico denominato ElasticPool01 che iniziano con "database".</span><span class="sxs-lookup"><span data-stu-id="08877-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="08877-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08877-113">PARAMETERS</span></span>

### <span data-ttu-id="08877-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="08877-114">-DatabaseName</span></span>
<span data-ttu-id="08877-115">Specifica il nome del database SQL ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08877-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="08877-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08877-116">-DefaultProfile</span></span>
<span data-ttu-id="08877-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="08877-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08877-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="08877-118">-ElasticPoolName</span></span>
<span data-ttu-id="08877-119">Specifica il nome di un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="08877-119">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="08877-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08877-120">-ResourceGroupName</span></span>
<span data-ttu-id="08877-121">Specifica il nome di un gruppo di risorse a cui è assegnato il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="08877-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="08877-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="08877-122">-ServerName</span></span>
<span data-ttu-id="08877-123">Specifica il nome di un server che contiene un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="08877-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="08877-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="08877-124">-Confirm</span></span>
<span data-ttu-id="08877-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08877-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08877-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08877-126">-WhatIf</span></span>
<span data-ttu-id="08877-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08877-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08877-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08877-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08877-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08877-129">CommonParameters</span></span>
<span data-ttu-id="08877-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08877-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08877-131">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08877-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08877-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08877-132">INPUTS</span></span>

### <span data-ttu-id="08877-133">System. String</span><span class="sxs-lookup"><span data-stu-id="08877-133">System.String</span></span>

## <span data-ttu-id="08877-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08877-134">OUTPUTS</span></span>

### <span data-ttu-id="08877-135">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="08877-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="08877-136">Note</span><span class="sxs-lookup"><span data-stu-id="08877-136">NOTES</span></span>

## <span data-ttu-id="08877-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08877-137">RELATED LINKS</span></span>

[<span data-ttu-id="08877-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="08877-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="08877-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="08877-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="08877-140">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="08877-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="08877-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="08877-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="08877-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="08877-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

