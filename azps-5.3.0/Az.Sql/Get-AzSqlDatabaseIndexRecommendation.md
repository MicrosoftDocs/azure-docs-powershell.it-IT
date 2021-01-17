---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 9dd14e1f8b61978575501700346157d7c22c0111
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374961"
---
# <span data-ttu-id="27c26-101">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="27c26-101">Get-AzSqlDatabaseIndexRecommendation</span></span>

## <span data-ttu-id="27c26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27c26-102">SYNOPSIS</span></span>
<span data-ttu-id="27c26-103">Ottiene le operazioni di indice consigliate per un server o un database.</span><span class="sxs-lookup"><span data-stu-id="27c26-103">Gets the recommended index operations for a server or database.</span></span>

## <span data-ttu-id="27c26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27c26-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27c26-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27c26-105">DESCRIPTION</span></span>
<span data-ttu-id="27c26-106">Il cmdlet **Get-AzSqlDatabaseIndexRecommendation** ottiene le operazioni di indice consigliate per un database o un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="27c26-106">The **Get-AzSqlDatabaseIndexRecommendation** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="27c26-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27c26-107">EXAMPLES</span></span>

### <span data-ttu-id="27c26-108">Esempio 1: ottenere indicazioni sull'indice per tutti i database nel server</span><span class="sxs-lookup"><span data-stu-id="27c26-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="27c26-109">Questo comando restituisce i consigli sull'indice per tutti i database nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="27c26-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="27c26-110">Esempio 2: ottenere suggerimenti per l'indice per un database specifico</span><span class="sxs-lookup"><span data-stu-id="27c26-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="27c26-111">Questo comando restituisce i suggerimenti per l'indice per database specifico.</span><span class="sxs-lookup"><span data-stu-id="27c26-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="27c26-112">Esempio 3: ottenere una singola raccomandazione indice per nome</span><span class="sxs-lookup"><span data-stu-id="27c26-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="27c26-113">Questo comando restituisce la raccomandazione Single index per nome.</span><span class="sxs-lookup"><span data-stu-id="27c26-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="27c26-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27c26-114">PARAMETERS</span></span>

### <span data-ttu-id="27c26-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="27c26-115">-DatabaseName</span></span>
<span data-ttu-id="27c26-116">Specifica il nome del database per cui questo cmdlet ottiene le indicazioni per l'indice.</span><span class="sxs-lookup"><span data-stu-id="27c26-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="27c26-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27c26-117">-DefaultProfile</span></span>
<span data-ttu-id="27c26-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="27c26-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27c26-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="27c26-119">-IndexRecommendationName</span></span>
<span data-ttu-id="27c26-120">Specifica il nome dell'indice consigliato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27c26-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="27c26-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27c26-121">-ResourceGroupName</span></span>
<span data-ttu-id="27c26-122">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="27c26-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="27c26-123">Questo cmdlet ottiene suggerimenti per l'indice per un database ospitato da questo server.</span><span class="sxs-lookup"><span data-stu-id="27c26-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="27c26-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="27c26-124">-ServerName</span></span>
<span data-ttu-id="27c26-125">Specifica il server che ospita il database per il quale questo cmdlet ottiene i suggerimenti per l'indice.</span><span class="sxs-lookup"><span data-stu-id="27c26-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="27c26-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="27c26-126">-TableName</span></span>
<span data-ttu-id="27c26-127">Specifica il nome di una tabella SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="27c26-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="27c26-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="27c26-128">-Confirm</span></span>
<span data-ttu-id="27c26-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27c26-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27c26-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27c26-130">-WhatIf</span></span>
<span data-ttu-id="27c26-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27c26-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27c26-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27c26-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27c26-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c26-133">CommonParameters</span></span>
<span data-ttu-id="27c26-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27c26-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c26-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27c26-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c26-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27c26-136">INPUTS</span></span>

### <span data-ttu-id="27c26-137">System. String</span><span class="sxs-lookup"><span data-stu-id="27c26-137">System.String</span></span>

## <span data-ttu-id="27c26-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27c26-138">OUTPUTS</span></span>

### <span data-ttu-id="27c26-139">Microsoft. Azure. Commands. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="27c26-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="27c26-140">Note</span><span class="sxs-lookup"><span data-stu-id="27c26-140">NOTES</span></span>

## <span data-ttu-id="27c26-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27c26-141">RELATED LINKS</span></span>

[<span data-ttu-id="27c26-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="27c26-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="27c26-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="27c26-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
