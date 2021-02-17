---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 7f13b1a1a5daad4e7c97de962943bb859f6a09df
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399482"
---
# <span data-ttu-id="d27f1-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="d27f1-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="d27f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d27f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d27f1-103">Interrompe il flusso di lavoro che esegue un'operazione di indicizzazione consigliata.</span><span class="sxs-lookup"><span data-stu-id="d27f1-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="d27f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d27f1-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d27f1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d27f1-105">DESCRIPTION</span></span>
<span data-ttu-id="d27f1-106">Il cmdlet **Stop-AzSqlDatabaseExecuteIndexRecommendation** interrompe il flusso di lavoro che esegue un'operazione di indice consigliata.</span><span class="sxs-lookup"><span data-stu-id="d27f1-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="d27f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d27f1-107">EXAMPLES</span></span>

### <span data-ttu-id="d27f1-108">Esempio 1: Interrompere l'esecuzione di un suggerimento per l'indice</span><span class="sxs-lookup"><span data-stu-id="d27f1-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="d27f1-109">Questo comando interrompe l'esecuzione di un suggerimento per l'indice.</span><span class="sxs-lookup"><span data-stu-id="d27f1-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="d27f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d27f1-110">PARAMETERS</span></span>

### <span data-ttu-id="d27f1-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d27f1-111">-DatabaseName</span></span>
<span data-ttu-id="d27f1-112">Specifica il nome del database per cui questo cmdlet interrompe il flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d27f1-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="d27f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d27f1-113">-DefaultProfile</span></span>
<span data-ttu-id="d27f1-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d27f1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d27f1-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="d27f1-115">-IndexRecommendationName</span></span>
<span data-ttu-id="d27f1-116">Specifica il nome del suggerimento per l'indice interrotto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d27f1-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d27f1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d27f1-117">-ResourceGroupName</span></span>
<span data-ttu-id="d27f1-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="d27f1-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d27f1-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d27f1-119">-ServerName</span></span>
<span data-ttu-id="d27f1-120">Specifica il server che ospita il database per cui questo cmdlet interrompe un flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d27f1-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="d27f1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d27f1-121">CommonParameters</span></span>
<span data-ttu-id="d27f1-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d27f1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d27f1-123">Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d27f1-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d27f1-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="d27f1-124">INPUTS</span></span>

### <span data-ttu-id="d27f1-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d27f1-125">System.String</span></span>

## <span data-ttu-id="d27f1-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d27f1-126">OUTPUTS</span></span>

### <span data-ttu-id="d27f1-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="d27f1-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="d27f1-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="d27f1-128">NOTES</span></span>

## <span data-ttu-id="d27f1-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d27f1-129">RELATED LINKS</span></span>


[<span data-ttu-id="d27f1-130">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="d27f1-130">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="d27f1-131">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="d27f1-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


