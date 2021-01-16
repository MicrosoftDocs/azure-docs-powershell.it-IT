---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 2e24dc80b93d72722d05a7dced05cbea02751a05
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355132"
---
# <span data-ttu-id="174af-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="174af-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="174af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="174af-102">SYNOPSIS</span></span>
<span data-ttu-id="174af-103">Ottiene i database elastici in un pool elastico e i relativi valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="174af-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="174af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="174af-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="174af-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="174af-105">DESCRIPTION</span></span>
<span data-ttu-id="174af-106">Il cmdlet **Get-AzSqlElasticPoolDatabase** ottiene i database elastici in un pool elastico e i relativi valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="174af-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="174af-107">Puoi specificare il nome di un database elastico in Azure SQL database per visualizzare i valori delle proprietà solo per il database.</span><span class="sxs-lookup"><span data-stu-id="174af-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="174af-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="174af-108">EXAMPLES</span></span>

### <span data-ttu-id="174af-109">Esempio 1: ottenere tutti i database in un pool elastico</span><span class="sxs-lookup"><span data-stu-id="174af-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="174af-110">Questo comando consente di ottenere tutti i database in un pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="174af-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="174af-111">Esempio 2: ottenere tutti i database in un pool elastico usando il filtro</span><span class="sxs-lookup"><span data-stu-id="174af-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="174af-112">Questo comando consente di ottenere tutti i database in un pool elastico denominato ElasticPool01 che iniziano con "database".</span><span class="sxs-lookup"><span data-stu-id="174af-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="174af-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="174af-113">PARAMETERS</span></span>

### <span data-ttu-id="174af-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="174af-114">-DatabaseName</span></span>
<span data-ttu-id="174af-115">Specifica il nome del database SQL ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="174af-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="174af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="174af-116">-DefaultProfile</span></span>
<span data-ttu-id="174af-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="174af-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="174af-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="174af-118">-ElasticPoolName</span></span>
<span data-ttu-id="174af-119">Specifica il nome di un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="174af-119">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="174af-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="174af-120">-ResourceGroupName</span></span>
<span data-ttu-id="174af-121">Specifica il nome di un gruppo di risorse a cui è assegnato il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="174af-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="174af-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="174af-122">-ServerName</span></span>
<span data-ttu-id="174af-123">Specifica il nome di un server che contiene un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="174af-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="174af-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="174af-124">-Confirm</span></span>
<span data-ttu-id="174af-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="174af-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="174af-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="174af-126">-WhatIf</span></span>
<span data-ttu-id="174af-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="174af-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="174af-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="174af-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="174af-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="174af-129">CommonParameters</span></span>
<span data-ttu-id="174af-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="174af-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="174af-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="174af-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="174af-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="174af-132">INPUTS</span></span>

### <span data-ttu-id="174af-133">System. String</span><span class="sxs-lookup"><span data-stu-id="174af-133">System.String</span></span>

## <span data-ttu-id="174af-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="174af-134">OUTPUTS</span></span>

### <span data-ttu-id="174af-135">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="174af-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="174af-136">Note</span><span class="sxs-lookup"><span data-stu-id="174af-136">NOTES</span></span>

## <span data-ttu-id="174af-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="174af-137">RELATED LINKS</span></span>

[<span data-ttu-id="174af-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="174af-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="174af-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="174af-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="174af-140">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="174af-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="174af-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="174af-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="174af-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="174af-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

