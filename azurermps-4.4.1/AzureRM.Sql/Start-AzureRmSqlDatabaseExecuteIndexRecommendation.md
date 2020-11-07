---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ae4564b1f583b8057438ee631de6b13d38e008ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687672"
---
# <span data-ttu-id="ea42e-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ea42e-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="ea42e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea42e-102">SYNOPSIS</span></span>
<span data-ttu-id="ea42e-103">Avvia il flusso di lavoro che esegue un'operazione di indice consigliata.</span><span class="sxs-lookup"><span data-stu-id="ea42e-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea42e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea42e-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea42e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea42e-105">DESCRIPTION</span></span>
<span data-ttu-id="ea42e-106">Il cmdlet **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** avvia il flusso di lavoro che esegue un'operazione di indice consigliata per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ea42e-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="ea42e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea42e-107">EXAMPLES</span></span>

### <span data-ttu-id="ea42e-108">Esempio 1: eseguire una raccomandazione indice</span><span class="sxs-lookup"><span data-stu-id="ea42e-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="ea42e-109">Questo comando esegue una raccomandazione indice.</span><span class="sxs-lookup"><span data-stu-id="ea42e-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="ea42e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea42e-110">PARAMETERS</span></span>

### <span data-ttu-id="ea42e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ea42e-111">-DatabaseName</span></span>
<span data-ttu-id="ea42e-112">Specifica il nome del database per cui questo cmdlet avvia il flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ea42e-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="ea42e-113">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="ea42e-113">-IndexRecommendationName</span></span>
<span data-ttu-id="ea42e-114">Specifica il nome dell'indice consigliato per l'esecuzione di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea42e-114">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="ea42e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea42e-115">-ResourceGroupName</span></span>
<span data-ttu-id="ea42e-116">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="ea42e-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ea42e-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ea42e-117">-ServerName</span></span>
<span data-ttu-id="ea42e-118">Specifica il server che ospita il database per cui questo cmdlet avvia un flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ea42e-118">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="ea42e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea42e-119">-DefaultProfile</span></span>
<span data-ttu-id="ea42e-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea42e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea42e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea42e-121">CommonParameters</span></span>
<span data-ttu-id="ea42e-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea42e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea42e-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea42e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea42e-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea42e-124">INPUTS</span></span>

## <span data-ttu-id="ea42e-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea42e-125">OUTPUTS</span></span>

## <span data-ttu-id="ea42e-126">Note</span><span class="sxs-lookup"><span data-stu-id="ea42e-126">NOTES</span></span>

## <span data-ttu-id="ea42e-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea42e-127">RELATED LINKS</span></span>

[<span data-ttu-id="ea42e-128">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="ea42e-128">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="ea42e-129">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ea42e-129">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="ea42e-130">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="ea42e-130">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


