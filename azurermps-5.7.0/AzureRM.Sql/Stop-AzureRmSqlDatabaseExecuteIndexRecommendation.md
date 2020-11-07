---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: d4cb344f63b871f55668c4de7205ada80ff04f35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686669"
---
# <span data-ttu-id="4a5df-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="4a5df-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="4a5df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a5df-102">SYNOPSIS</span></span>
<span data-ttu-id="4a5df-103">Interrompe il flusso di lavoro che esegue un'operazione di indice consigliata.</span><span class="sxs-lookup"><span data-stu-id="4a5df-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a5df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a5df-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a5df-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a5df-105">DESCRIPTION</span></span>
<span data-ttu-id="4a5df-106">Il cmdlet **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** interrompe il flusso di lavoro che esegue un'operazione di indice consigliata.</span><span class="sxs-lookup"><span data-stu-id="4a5df-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="4a5df-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a5df-107">EXAMPLES</span></span>

### <span data-ttu-id="4a5df-108">Esempio 1: interrompere l'uso di una raccomandazione indice</span><span class="sxs-lookup"><span data-stu-id="4a5df-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="4a5df-109">Questo comando interrompe l'uso di una raccomandazione indice.</span><span class="sxs-lookup"><span data-stu-id="4a5df-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="4a5df-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a5df-110">PARAMETERS</span></span>

### <span data-ttu-id="4a5df-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a5df-111">-DatabaseName</span></span>
<span data-ttu-id="4a5df-112">Specifica il nome del database per cui questo cmdlet arresta il flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="4a5df-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="4a5df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a5df-113">-DefaultProfile</span></span>
<span data-ttu-id="4a5df-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4a5df-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a5df-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="4a5df-115">-IndexRecommendationName</span></span>
<span data-ttu-id="4a5df-116">Specifica il nome del suggerimento relativo all'indice che questo cmdlet si arresta.</span><span class="sxs-lookup"><span data-stu-id="4a5df-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="4a5df-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a5df-117">-ResourceGroupName</span></span>
<span data-ttu-id="4a5df-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="4a5df-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="4a5df-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4a5df-119">-ServerName</span></span>
<span data-ttu-id="4a5df-120">Specifica il server che ospita il database per cui questo cmdlet arresta un flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="4a5df-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="4a5df-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a5df-121">CommonParameters</span></span>
<span data-ttu-id="4a5df-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a5df-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a5df-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a5df-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a5df-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a5df-124">INPUTS</span></span>

### <span data-ttu-id="4a5df-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4a5df-125">None</span></span>
<span data-ttu-id="4a5df-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="4a5df-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4a5df-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a5df-127">OUTPUTS</span></span>

## <span data-ttu-id="4a5df-128">Note</span><span class="sxs-lookup"><span data-stu-id="4a5df-128">NOTES</span></span>

## <span data-ttu-id="4a5df-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a5df-129">RELATED LINKS</span></span>

[<span data-ttu-id="4a5df-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="4a5df-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="4a5df-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="4a5df-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="4a5df-132">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="4a5df-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


