---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: 64d8dae1b12630c6ef0086ab2648fcd424c0389d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519850"
---
# <span data-ttu-id="71472-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="71472-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="71472-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71472-102">SYNOPSIS</span></span>
<span data-ttu-id="71472-103">Ottiene lo stato delle operazioni del database.</span><span class="sxs-lookup"><span data-stu-id="71472-103">Gets the status of database operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71472-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71472-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71472-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71472-105">DESCRIPTION</span></span>
<span data-ttu-id="71472-106">Il cmdlet **Get-AzureRmSqlDatabaseActivity** ottiene lo stato delle operazioni di database in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="71472-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="71472-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71472-107">EXAMPLES</span></span>

### <span data-ttu-id="71472-108">Esempio 1: ottenere lo stato per tutte le istanze di database SQL</span><span class="sxs-lookup"><span data-stu-id="71472-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="71472-109">Questo comando restituisce lo stato dell'operazione di tutte le istanze di database SQL in un pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="71472-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="71472-110">Esempio 2: ottenere lo stato per tutte le operazioni di database SQL</span><span class="sxs-lookup"><span data-stu-id="71472-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="71472-111">Questo comando restituisce lo stato di tutte le operazioni di database SQL in un database.</span><span class="sxs-lookup"><span data-stu-id="71472-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="71472-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71472-112">PARAMETERS</span></span>

### <span data-ttu-id="71472-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="71472-113">-DatabaseName</span></span>
<span data-ttu-id="71472-114">Specifica il nome del database per cui questo cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="71472-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="71472-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71472-115">-DefaultProfile</span></span>
<span data-ttu-id="71472-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71472-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71472-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="71472-117">-ElasticPoolName</span></span>
<span data-ttu-id="71472-118">Specifica il nome del pool di database elastici per cui questo cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="71472-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71472-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="71472-119">-OperationId</span></span>
<span data-ttu-id="71472-120">Specifica l'ID dell'operazione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71472-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71472-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71472-121">-ResourceGroupName</span></span>
<span data-ttu-id="71472-122">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="71472-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="71472-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="71472-123">-ServerName</span></span>
<span data-ttu-id="71472-124">Specifica il nome di Microsoft SQL Server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="71472-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="71472-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="71472-125">-Confirm</span></span>
<span data-ttu-id="71472-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71472-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71472-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71472-127">-WhatIf</span></span>
<span data-ttu-id="71472-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71472-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71472-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71472-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71472-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71472-130">CommonParameters</span></span>
<span data-ttu-id="71472-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71472-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71472-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71472-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71472-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71472-133">INPUTS</span></span>

### <span data-ttu-id="71472-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="71472-134">None</span></span>
<span data-ttu-id="71472-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="71472-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71472-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71472-136">OUTPUTS</span></span>

### <span data-ttu-id="71472-137">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="71472-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="71472-138">Note</span><span class="sxs-lookup"><span data-stu-id="71472-138">NOTES</span></span>

## <span data-ttu-id="71472-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71472-139">RELATED LINKS</span></span>
