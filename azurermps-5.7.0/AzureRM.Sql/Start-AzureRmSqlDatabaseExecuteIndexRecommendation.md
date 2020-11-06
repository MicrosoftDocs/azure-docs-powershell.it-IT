---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ac5bf33bd87ff290784728fd0c4857d5278d3057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517843"
---
# <span data-ttu-id="565ef-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="565ef-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="565ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="565ef-102">SYNOPSIS</span></span>
<span data-ttu-id="565ef-103">Avvia il flusso di lavoro che esegue un'operazione di indice consigliata.</span><span class="sxs-lookup"><span data-stu-id="565ef-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="565ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="565ef-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="565ef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="565ef-105">DESCRIPTION</span></span>
<span data-ttu-id="565ef-106">Il cmdlet **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** avvia il flusso di lavoro che esegue un'operazione di indice consigliata per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="565ef-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="565ef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="565ef-107">EXAMPLES</span></span>

### <span data-ttu-id="565ef-108">Esempio 1: eseguire una raccomandazione indice</span><span class="sxs-lookup"><span data-stu-id="565ef-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="565ef-109">Questo comando esegue una raccomandazione indice.</span><span class="sxs-lookup"><span data-stu-id="565ef-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="565ef-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="565ef-110">PARAMETERS</span></span>

### <span data-ttu-id="565ef-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="565ef-111">-DatabaseName</span></span>
<span data-ttu-id="565ef-112">Specifica il nome del database per cui questo cmdlet avvia il flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="565ef-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="565ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="565ef-113">-DefaultProfile</span></span>
<span data-ttu-id="565ef-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="565ef-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="565ef-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="565ef-115">-IndexRecommendationName</span></span>
<span data-ttu-id="565ef-116">Specifica il nome dell'indice consigliato per l'esecuzione di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="565ef-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="565ef-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="565ef-117">-ResourceGroupName</span></span>
<span data-ttu-id="565ef-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="565ef-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="565ef-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="565ef-119">-ServerName</span></span>
<span data-ttu-id="565ef-120">Specifica il server che ospita il database per cui questo cmdlet avvia un flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="565ef-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="565ef-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="565ef-121">CommonParameters</span></span>
<span data-ttu-id="565ef-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="565ef-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="565ef-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="565ef-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="565ef-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="565ef-124">INPUTS</span></span>

### <span data-ttu-id="565ef-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="565ef-125">None</span></span>
<span data-ttu-id="565ef-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="565ef-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="565ef-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="565ef-127">OUTPUTS</span></span>

## <span data-ttu-id="565ef-128">Note</span><span class="sxs-lookup"><span data-stu-id="565ef-128">NOTES</span></span>

## <span data-ttu-id="565ef-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="565ef-129">RELATED LINKS</span></span>

[<span data-ttu-id="565ef-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="565ef-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="565ef-131">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="565ef-131">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="565ef-132">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="565ef-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


