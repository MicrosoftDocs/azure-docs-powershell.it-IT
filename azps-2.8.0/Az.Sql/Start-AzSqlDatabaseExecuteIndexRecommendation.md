---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: c432b3a23c4495abebda013b5dd3943132827a30
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857713"
---
# <span data-ttu-id="fad00-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="fad00-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="fad00-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fad00-102">SYNOPSIS</span></span>
<span data-ttu-id="fad00-103">Avvia il flusso di lavoro che esegue un'operazione di indice consigliata.</span><span class="sxs-lookup"><span data-stu-id="fad00-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="fad00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fad00-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fad00-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fad00-105">DESCRIPTION</span></span>
<span data-ttu-id="fad00-106">Il cmdlet **Start-AzSqlDatabaseExecuteIndexRecommendation** avvia il flusso di lavoro che esegue un'operazione di indice consigliata per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="fad00-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="fad00-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fad00-107">EXAMPLES</span></span>

### <span data-ttu-id="fad00-108">Esempio 1: eseguire una raccomandazione indice</span><span class="sxs-lookup"><span data-stu-id="fad00-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="fad00-109">Questo comando esegue una raccomandazione indice.</span><span class="sxs-lookup"><span data-stu-id="fad00-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="fad00-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fad00-110">PARAMETERS</span></span>

### <span data-ttu-id="fad00-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fad00-111">-DatabaseName</span></span>
<span data-ttu-id="fad00-112">Specifica il nome del database per cui questo cmdlet avvia il flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="fad00-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="fad00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fad00-113">-DefaultProfile</span></span>
<span data-ttu-id="fad00-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fad00-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fad00-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="fad00-115">-IndexRecommendationName</span></span>
<span data-ttu-id="fad00-116">Specifica il nome dell'indice consigliato per l'esecuzione di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fad00-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="fad00-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fad00-117">-ResourceGroupName</span></span>
<span data-ttu-id="fad00-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="fad00-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fad00-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="fad00-119">-ServerName</span></span>
<span data-ttu-id="fad00-120">Specifica il server che ospita il database per cui questo cmdlet avvia un flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="fad00-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="fad00-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad00-121">CommonParameters</span></span>
<span data-ttu-id="fad00-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fad00-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad00-123">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fad00-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad00-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fad00-124">INPUTS</span></span>

### <span data-ttu-id="fad00-125">System. String</span><span class="sxs-lookup"><span data-stu-id="fad00-125">System.String</span></span>

## <span data-ttu-id="fad00-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fad00-126">OUTPUTS</span></span>

### <span data-ttu-id="fad00-127">Microsoft. Azure. Commands. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="fad00-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="fad00-128">Note</span><span class="sxs-lookup"><span data-stu-id="fad00-128">NOTES</span></span>

## <span data-ttu-id="fad00-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fad00-129">RELATED LINKS</span></span>

[<span data-ttu-id="fad00-130">Get-AzSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="fad00-130">Get-AzSqlDatabaseIndexRecommendations</span></span>](./Get-AzSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="fad00-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="fad00-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="fad00-132">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="fad00-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


