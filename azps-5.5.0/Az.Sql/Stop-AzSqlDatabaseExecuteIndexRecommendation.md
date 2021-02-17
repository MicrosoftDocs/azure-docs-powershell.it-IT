---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ca7aeed13627bba3c380b3f1062ee80fcc7c3ebf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207859"
---
# <span data-ttu-id="d1a5d-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="d1a5d-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="d1a5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1a5d-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a5d-103">Interrompe il flusso di lavoro che esegue un'operazione di indicizzazione consigliata.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="d1a5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1a5d-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1a5d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d1a5d-105">DESCRIPTION</span></span>
<span data-ttu-id="d1a5d-106">Il cmdlet **Stop-AzSqlDatabaseExecuteIndexRecommendation** interrompe il flusso di lavoro che esegue un'operazione di indice consigliata.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="d1a5d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1a5d-107">EXAMPLES</span></span>

### <span data-ttu-id="d1a5d-108">Esempio 1: Interrompere l'esecuzione di un suggerimento per l'indice</span><span class="sxs-lookup"><span data-stu-id="d1a5d-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="d1a5d-109">Questo comando interrompe l'esecuzione di un suggerimento per l'indice.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="d1a5d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1a5d-110">PARAMETERS</span></span>

### <span data-ttu-id="d1a5d-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d1a5d-111">-DatabaseName</span></span>
<span data-ttu-id="d1a5d-112">Specifica il nome del database per cui questo cmdlet interrompe il flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="d1a5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a5d-113">-DefaultProfile</span></span>
<span data-ttu-id="d1a5d-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d1a5d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1a5d-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="d1a5d-115">-IndexRecommendationName</span></span>
<span data-ttu-id="d1a5d-116">Specifica il nome del suggerimento per l'indice interrotto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d1a5d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1a5d-117">-ResourceGroupName</span></span>
<span data-ttu-id="d1a5d-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d1a5d-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d1a5d-119">-ServerName</span></span>
<span data-ttu-id="d1a5d-120">Specifica il server che ospita il database per cui questo cmdlet interrompe un flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="d1a5d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a5d-121">CommonParameters</span></span>
<span data-ttu-id="d1a5d-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a5d-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d1a5d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a5d-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="d1a5d-124">INPUTS</span></span>

### <span data-ttu-id="d1a5d-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d1a5d-125">System.String</span></span>

## <span data-ttu-id="d1a5d-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1a5d-126">OUTPUTS</span></span>

### <span data-ttu-id="d1a5d-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="d1a5d-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="d1a5d-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="d1a5d-128">NOTES</span></span>

## <span data-ttu-id="d1a5d-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1a5d-129">RELATED LINKS</span></span>

[<span data-ttu-id="d1a5d-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="d1a5d-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="d1a5d-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="d1a5d-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="d1a5d-132">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="d1a5d-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


