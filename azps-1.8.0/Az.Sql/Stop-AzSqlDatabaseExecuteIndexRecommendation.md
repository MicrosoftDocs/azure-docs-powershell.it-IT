---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 9b21c290b2d5e5b6056297bba7d4196dd68d68d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676693"
---
# <span data-ttu-id="08dae-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="08dae-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="08dae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08dae-102">SYNOPSIS</span></span>
<span data-ttu-id="08dae-103">Interrompe il flusso di lavoro che esegue un'operazione di indice consigliata.</span><span class="sxs-lookup"><span data-stu-id="08dae-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="08dae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08dae-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08dae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08dae-105">DESCRIPTION</span></span>
<span data-ttu-id="08dae-106">Il cmdlet **Stop-AzSqlDatabaseExecuteIndexRecommendation** interrompe il flusso di lavoro che esegue un'operazione di indice consigliata.</span><span class="sxs-lookup"><span data-stu-id="08dae-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="08dae-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08dae-107">EXAMPLES</span></span>

### <span data-ttu-id="08dae-108">Esempio 1: interrompere l'uso di una raccomandazione indice</span><span class="sxs-lookup"><span data-stu-id="08dae-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="08dae-109">Questo comando interrompe l'uso di una raccomandazione indice.</span><span class="sxs-lookup"><span data-stu-id="08dae-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="08dae-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08dae-110">PARAMETERS</span></span>

### <span data-ttu-id="08dae-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="08dae-111">-DatabaseName</span></span>
<span data-ttu-id="08dae-112">Specifica il nome del database per cui questo cmdlet arresta il flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="08dae-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="08dae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08dae-113">-DefaultProfile</span></span>
<span data-ttu-id="08dae-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="08dae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08dae-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="08dae-115">-IndexRecommendationName</span></span>
<span data-ttu-id="08dae-116">Specifica il nome del suggerimento relativo all'indice che questo cmdlet si arresta.</span><span class="sxs-lookup"><span data-stu-id="08dae-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="08dae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08dae-117">-ResourceGroupName</span></span>
<span data-ttu-id="08dae-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="08dae-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="08dae-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="08dae-119">-ServerName</span></span>
<span data-ttu-id="08dae-120">Specifica il server che ospita il database per cui questo cmdlet arresta un flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="08dae-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="08dae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08dae-121">CommonParameters</span></span>
<span data-ttu-id="08dae-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08dae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08dae-123">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08dae-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08dae-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08dae-124">INPUTS</span></span>

### <span data-ttu-id="08dae-125">System. String</span><span class="sxs-lookup"><span data-stu-id="08dae-125">System.String</span></span>

## <span data-ttu-id="08dae-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08dae-126">OUTPUTS</span></span>

### <span data-ttu-id="08dae-127">Microsoft. Azure. Commands. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="08dae-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="08dae-128">Note</span><span class="sxs-lookup"><span data-stu-id="08dae-128">NOTES</span></span>

## <span data-ttu-id="08dae-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08dae-129">RELATED LINKS</span></span>

[<span data-ttu-id="08dae-130">Get-AzSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="08dae-130">Get-AzSqlDatabaseIndexRecommendations</span></span>](./Get-AzSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="08dae-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="08dae-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="08dae-132">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="08dae-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


