---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: b37ae31c1f0dc6360743a863f0305fd5823cbb3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521125"
---
# <span data-ttu-id="6fc41-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="6fc41-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="6fc41-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6fc41-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc41-103">Ottiene lo stato di spostamento dei database elastici.</span><span class="sxs-lookup"><span data-stu-id="6fc41-103">Gets the status of moving elastic databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fc41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6fc41-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> -ElasticPoolName <String> -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fc41-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fc41-105">DESCRIPTION</span></span>
<span data-ttu-id="6fc41-106">Il cmdlet **Get-AzureRmSqlDatabaseActivity** ottiene lo stato dei database elastici che si spostano all'interno o all'esterno di un pool di database elastico in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="6fc41-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of elastic databases moving into or out of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="6fc41-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6fc41-107">EXAMPLES</span></span>

### <span data-ttu-id="6fc41-108">Esempio 1: ottenere lo stato per tutte le istanze di database SQL</span><span class="sxs-lookup"><span data-stu-id="6fc41-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="6fc41-109">Questo comando restituisce lo stato dell'operazione di tutte le istanze di database SQL in un pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="6fc41-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="6fc41-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6fc41-110">PARAMETERS</span></span>

### <span data-ttu-id="6fc41-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6fc41-111">-DatabaseName</span></span>
<span data-ttu-id="6fc41-112">Specifica il nome del database per cui questo cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="6fc41-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="6fc41-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6fc41-113">-ElasticPoolName</span></span>
<span data-ttu-id="6fc41-114">Specifica il nome del pool di database elastici per cui questo cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="6fc41-114">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="6fc41-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="6fc41-115">-OperationId</span></span>
<span data-ttu-id="6fc41-116">Specifica l'ID dell'operazione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fc41-116">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fc41-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fc41-117">-ResourceGroupName</span></span>
<span data-ttu-id="6fc41-118">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="6fc41-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="6fc41-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="6fc41-119">-ServerName</span></span>
<span data-ttu-id="6fc41-120">Specifica il nome di Microsoft SQL Server che ospita il pool di database elastici.</span><span class="sxs-lookup"><span data-stu-id="6fc41-120">Specifies the name of the Microsoft SQL Server that hosts the elastic database pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fc41-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6fc41-121">-Confirm</span></span>
<span data-ttu-id="6fc41-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fc41-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fc41-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fc41-123">-WhatIf</span></span>
<span data-ttu-id="6fc41-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6fc41-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fc41-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6fc41-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fc41-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc41-126">-DefaultProfile</span></span>
<span data-ttu-id="6fc41-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6fc41-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fc41-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc41-128">CommonParameters</span></span>
<span data-ttu-id="6fc41-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fc41-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc41-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fc41-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc41-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6fc41-131">INPUTS</span></span>

## <span data-ttu-id="6fc41-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6fc41-132">OUTPUTS</span></span>

### <span data-ttu-id="6fc41-133">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="6fc41-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="6fc41-134">Note</span><span class="sxs-lookup"><span data-stu-id="6fc41-134">NOTES</span></span>

## <span data-ttu-id="6fc41-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6fc41-135">RELATED LINKS</span></span>

