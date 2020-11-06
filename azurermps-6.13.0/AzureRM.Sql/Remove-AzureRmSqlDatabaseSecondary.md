---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: f1bc8fcc019f25b4337dc88ac55965b8d988e753
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518480"
---
# <span data-ttu-id="1e8f0-101">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1e8f0-101">Remove-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="1e8f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e8f0-102">SYNOPSIS</span></span>
<span data-ttu-id="1e8f0-103">Termina la replicazione dei dati tra un database SQL e il database secondario specificato.</span><span class="sxs-lookup"><span data-stu-id="1e8f0-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e8f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e8f0-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e8f0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e8f0-105">DESCRIPTION</span></span>
<span data-ttu-id="1e8f0-106">Il cmdlet **Remove-AzureRmSqlDatabaseSecondary** forza la terminazione di un collegamento di Geo-replica.</span><span class="sxs-lookup"><span data-stu-id="1e8f0-106">The **Remove-AzureRmSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="1e8f0-107">Questo cmdlet sostituisce il cmdlet Stop-AzureSqlDatabaseCopy.</span><span class="sxs-lookup"><span data-stu-id="1e8f0-107">This cmdlet replaces the Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="1e8f0-108">Non c'è sincronizzazione della replica prima della terminazione.</span><span class="sxs-lookup"><span data-stu-id="1e8f0-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="1e8f0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e8f0-109">EXAMPLES</span></span>

## <span data-ttu-id="1e8f0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e8f0-110">PARAMETERS</span></span>

### <span data-ttu-id="1e8f0-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1e8f0-111">-DatabaseName</span></span>
<span data-ttu-id="1e8f0-112">Specifica il nome del database SQL primario di Azure che contiene il collegamento di replica rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e8f0-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e8f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e8f0-113">-DefaultProfile</span></span>
<span data-ttu-id="1e8f0-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1e8f0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e8f0-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e8f0-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="1e8f0-116">Specifica il nome del gruppo di risorse partner.</span><span class="sxs-lookup"><span data-stu-id="1e8f0-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="1e8f0-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="1e8f0-117">-PartnerServerName</span></span>
<span data-ttu-id="1e8f0-118">Specifica il nome del partner SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1e8f0-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="1e8f0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e8f0-119">-ResourceGroupName</span></span>
<span data-ttu-id="1e8f0-120">Specifica il nome del gruppo di risorse associato al collegamento di replica da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1e8f0-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="1e8f0-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="1e8f0-121">-ServerName</span></span>
<span data-ttu-id="1e8f0-122">Specifica il nome di SQL Server che contiene il collegamento di replica da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1e8f0-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="1e8f0-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1e8f0-123">-Confirm</span></span>
<span data-ttu-id="1e8f0-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e8f0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e8f0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e8f0-125">-WhatIf</span></span>
<span data-ttu-id="1e8f0-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e8f0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e8f0-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e8f0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e8f0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e8f0-128">CommonParameters</span></span>
<span data-ttu-id="1e8f0-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e8f0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e8f0-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e8f0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e8f0-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e8f0-131">INPUTS</span></span>

### <span data-ttu-id="1e8f0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1e8f0-132">System.String</span></span>

## <span data-ttu-id="1e8f0-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e8f0-133">OUTPUTS</span></span>

### <span data-ttu-id="1e8f0-134">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="1e8f0-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="1e8f0-135">Note</span><span class="sxs-lookup"><span data-stu-id="1e8f0-135">NOTES</span></span>

## <span data-ttu-id="1e8f0-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e8f0-136">RELATED LINKS</span></span>

[<span data-ttu-id="1e8f0-137">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1e8f0-137">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="1e8f0-138">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1e8f0-138">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="1e8f0-139">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="1e8f0-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
