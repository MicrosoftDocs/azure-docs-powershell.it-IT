---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 1ab1e223ec173cf5727011956f52979026159594
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402253"
---
# <span data-ttu-id="72907-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="72907-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="72907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72907-102">SYNOPSIS</span></span>
<span data-ttu-id="72907-103">Avvia il flusso di lavoro che esegue un'operazione di indicizzazione consigliata.</span><span class="sxs-lookup"><span data-stu-id="72907-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="72907-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72907-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72907-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="72907-105">DESCRIPTION</span></span>
<span data-ttu-id="72907-106">Il cmdlet **Start-AzSqlDatabaseExecuteIndexRecommendation** avvia il flusso di lavoro che esegue un'operazione di indice consigliata per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="72907-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="72907-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72907-107">EXAMPLES</span></span>

### <span data-ttu-id="72907-108">Esempio 1: Eseguire un suggerimento per l'indice</span><span class="sxs-lookup"><span data-stu-id="72907-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="72907-109">Questo comando esegue un suggerimento per l'indice.</span><span class="sxs-lookup"><span data-stu-id="72907-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="72907-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72907-110">PARAMETERS</span></span>

### <span data-ttu-id="72907-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="72907-111">-DatabaseName</span></span>
<span data-ttu-id="72907-112">Specifica il nome del database per cui questo cmdlet avvia il flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="72907-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="72907-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72907-113">-DefaultProfile</span></span>
<span data-ttu-id="72907-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="72907-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72907-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="72907-115">-IndexRecommendationName</span></span>
<span data-ttu-id="72907-116">Specifica il nome dell'consiglio per l'indice eseguito da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72907-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="72907-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72907-117">-ResourceGroupName</span></span>
<span data-ttu-id="72907-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="72907-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="72907-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72907-119">-ServerName</span></span>
<span data-ttu-id="72907-120">Specifica il server che ospita il database per cui questo cmdlet avvia un flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="72907-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="72907-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72907-121">CommonParameters</span></span>
<span data-ttu-id="72907-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72907-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72907-123">Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="72907-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72907-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="72907-124">INPUTS</span></span>

### <span data-ttu-id="72907-125">System.String</span><span class="sxs-lookup"><span data-stu-id="72907-125">System.String</span></span>

## <span data-ttu-id="72907-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72907-126">OUTPUTS</span></span>

### <span data-ttu-id="72907-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="72907-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="72907-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="72907-128">NOTES</span></span>

## <span data-ttu-id="72907-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72907-129">RELATED LINKS</span></span>


[<span data-ttu-id="72907-130">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="72907-130">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="72907-131">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="72907-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


