---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 2205c241625f0bfdc2be21cda34c5bc3d6d07c12
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014813"
---
# <span data-ttu-id="62935-101">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="62935-101">Get-AzSqlDatabaseIndexRecommendation</span></span>

## <span data-ttu-id="62935-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62935-102">SYNOPSIS</span></span>
<span data-ttu-id="62935-103">Recupera le operazioni di indice consigliate per un server o un database.</span><span class="sxs-lookup"><span data-stu-id="62935-103">Gets the recommended index operations for a server or database.</span></span>

## <span data-ttu-id="62935-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62935-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62935-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="62935-105">DESCRIPTION</span></span>
<span data-ttu-id="62935-106">Il cmdlet **Get-AzSqlDatabaseIndexRecommendation** ottiene le operazioni di indice consigliate per un database o un server di SQL azure.</span><span class="sxs-lookup"><span data-stu-id="62935-106">The **Get-AzSqlDatabaseIndexRecommendation** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="62935-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62935-107">EXAMPLES</span></span>

### <span data-ttu-id="62935-108">Esempio 1: Ottenere consigli sugli indici per tutti i database sul server</span><span class="sxs-lookup"><span data-stu-id="62935-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="62935-109">Questo comando restituisce gli indici consigliati per tutti i database sul server server01.</span><span class="sxs-lookup"><span data-stu-id="62935-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="62935-110">Esempio 2: Ottenere consigli sull'indice per un database specifico</span><span class="sxs-lookup"><span data-stu-id="62935-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="62935-111">Questo comando restituisce gli indici consigliati per un database specifico.</span><span class="sxs-lookup"><span data-stu-id="62935-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="62935-112">Esempio 3: Ottenere un singolo suggerimento per l'indice in base al nome</span><span class="sxs-lookup"><span data-stu-id="62935-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="62935-113">Questo comando restituisce un singolo suggerimento per l'indice in base al nome.</span><span class="sxs-lookup"><span data-stu-id="62935-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="62935-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62935-114">PARAMETERS</span></span>

### <span data-ttu-id="62935-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="62935-115">-DatabaseName</span></span>
<span data-ttu-id="62935-116">Specifica il nome del database per cui il cmdlet riceve consigli per l'indice.</span><span class="sxs-lookup"><span data-stu-id="62935-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="62935-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62935-117">-DefaultProfile</span></span>
<span data-ttu-id="62935-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="62935-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62935-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="62935-119">-IndexRecommendationName</span></span>
<span data-ttu-id="62935-120">Specifica il nome dell'consiglio per l'indice che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62935-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="62935-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62935-121">-ResourceGroupName</span></span>
<span data-ttu-id="62935-122">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="62935-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="62935-123">Questo cmdlet riceve i suggerimenti per l'indicizzazione per un database ospitato da questo server.</span><span class="sxs-lookup"><span data-stu-id="62935-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="62935-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="62935-124">-ServerName</span></span>
<span data-ttu-id="62935-125">Specifica il server che ospita il database per cui questo cmdlet riceve consigli per l'indice.</span><span class="sxs-lookup"><span data-stu-id="62935-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="62935-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="62935-126">-TableName</span></span>
<span data-ttu-id="62935-127">Specifica il nome di una tabella SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="62935-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="62935-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62935-128">-Confirm</span></span>
<span data-ttu-id="62935-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62935-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62935-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62935-130">-WhatIf</span></span>
<span data-ttu-id="62935-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62935-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62935-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62935-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62935-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62935-133">CommonParameters</span></span>
<span data-ttu-id="62935-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62935-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62935-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="62935-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62935-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="62935-136">INPUTS</span></span>

### <span data-ttu-id="62935-137">System.String</span><span class="sxs-lookup"><span data-stu-id="62935-137">System.String</span></span>

## <span data-ttu-id="62935-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62935-138">OUTPUTS</span></span>

### <span data-ttu-id="62935-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="62935-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="62935-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="62935-140">NOTES</span></span>

## <span data-ttu-id="62935-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62935-141">RELATED LINKS</span></span>

[<span data-ttu-id="62935-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="62935-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="62935-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="62935-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
