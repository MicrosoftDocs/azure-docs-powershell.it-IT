---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: 08c5778002a80bb4fb2effdd977f134079f3aa0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518543"
---
# <span data-ttu-id="39228-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="39228-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="39228-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39228-102">SYNOPSIS</span></span>
<span data-ttu-id="39228-103">Ottiene lo stato delle operazioni del database.</span><span class="sxs-lookup"><span data-stu-id="39228-103">Gets the status of database operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39228-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39228-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39228-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39228-105">DESCRIPTION</span></span>
<span data-ttu-id="39228-106">Il cmdlet **Get-AzureRmSqlDatabaseActivity** ottiene lo stato delle operazioni di database in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="39228-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="39228-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39228-107">EXAMPLES</span></span>

### <span data-ttu-id="39228-108">Esempio 1: ottenere lo stato per tutte le istanze di database SQL</span><span class="sxs-lookup"><span data-stu-id="39228-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="39228-109">Questo comando restituisce lo stato dell'operazione di tutte le istanze di database SQL in un pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="39228-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="39228-110">Esempio 2: ottenere lo stato per tutte le operazioni di database SQL</span><span class="sxs-lookup"><span data-stu-id="39228-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="39228-111">Questo comando restituisce lo stato di tutte le operazioni di database SQL in un database.</span><span class="sxs-lookup"><span data-stu-id="39228-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="39228-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39228-112">PARAMETERS</span></span>

### <span data-ttu-id="39228-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="39228-113">-DatabaseName</span></span>
<span data-ttu-id="39228-114">Specifica il nome del database per cui questo cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="39228-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="39228-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39228-115">-DefaultProfile</span></span>
<span data-ttu-id="39228-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39228-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39228-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="39228-117">-ElasticPoolName</span></span>
<span data-ttu-id="39228-118">Specifica il nome del pool di database elastici per cui questo cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="39228-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="39228-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="39228-119">-OperationId</span></span>
<span data-ttu-id="39228-120">Specifica l'ID dell'operazione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39228-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="39228-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39228-121">-ResourceGroupName</span></span>
<span data-ttu-id="39228-122">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="39228-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="39228-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="39228-123">-ServerName</span></span>
<span data-ttu-id="39228-124">Specifica il nome di Microsoft SQL Server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="39228-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="39228-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="39228-125">-Confirm</span></span>
<span data-ttu-id="39228-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39228-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39228-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39228-127">-WhatIf</span></span>
<span data-ttu-id="39228-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39228-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39228-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39228-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39228-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39228-130">CommonParameters</span></span>
<span data-ttu-id="39228-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39228-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39228-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39228-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39228-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39228-133">INPUTS</span></span>

### <span data-ttu-id="39228-134">System. String</span><span class="sxs-lookup"><span data-stu-id="39228-134">System.String</span></span>

### <span data-ttu-id="39228-135">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="39228-135">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="39228-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39228-136">OUTPUTS</span></span>

### <span data-ttu-id="39228-137">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="39228-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="39228-138">Note</span><span class="sxs-lookup"><span data-stu-id="39228-138">NOTES</span></span>

## <span data-ttu-id="39228-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39228-139">RELATED LINKS</span></span>
