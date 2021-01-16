---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 4353a61efd0141947879ad6795c321f5ed43e1d3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363310"
---
# <span data-ttu-id="ab628-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ab628-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="ab628-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab628-102">SYNOPSIS</span></span>
<span data-ttu-id="ab628-103">Termina la replicazione dei dati tra un database SQL e il database secondario specificato.</span><span class="sxs-lookup"><span data-stu-id="ab628-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="ab628-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab628-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab628-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab628-105">DESCRIPTION</span></span>
<span data-ttu-id="ab628-106">Il cmdlet **Remove-AzSqlDatabaseSecondary** forza la terminazione di un collegamento di Geo-replica.</span><span class="sxs-lookup"><span data-stu-id="ab628-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="ab628-107">Questo cmdlet sostituisce il cmdlet Stop-AzSqlDatabaseCopy.</span><span class="sxs-lookup"><span data-stu-id="ab628-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="ab628-108">Non c'è sincronizzazione della replica prima della terminazione.</span><span class="sxs-lookup"><span data-stu-id="ab628-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="ab628-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab628-109">EXAMPLES</span></span>

## <span data-ttu-id="ab628-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab628-110">PARAMETERS</span></span>

### <span data-ttu-id="ab628-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ab628-111">-DatabaseName</span></span>
<span data-ttu-id="ab628-112">Specifica il nome del database SQL primario di Azure che contiene il collegamento di replica rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab628-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ab628-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab628-113">-DefaultProfile</span></span>
<span data-ttu-id="ab628-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ab628-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab628-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab628-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ab628-116">Specifica il nome del gruppo di risorse partner.</span><span class="sxs-lookup"><span data-stu-id="ab628-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="ab628-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="ab628-117">-PartnerServerName</span></span>
<span data-ttu-id="ab628-118">Specifica il nome del partner SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ab628-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="ab628-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab628-119">-ResourceGroupName</span></span>
<span data-ttu-id="ab628-120">Specifica il nome del gruppo di risorse associato al collegamento di replica da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ab628-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="ab628-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ab628-121">-ServerName</span></span>
<span data-ttu-id="ab628-122">Specifica il nome di SQL Server che contiene il collegamento di replica da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ab628-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="ab628-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ab628-123">-Confirm</span></span>
<span data-ttu-id="ab628-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab628-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab628-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab628-125">-WhatIf</span></span>
<span data-ttu-id="ab628-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab628-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab628-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab628-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab628-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab628-128">CommonParameters</span></span>
<span data-ttu-id="ab628-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab628-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab628-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab628-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab628-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab628-131">INPUTS</span></span>

### <span data-ttu-id="ab628-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ab628-132">System.String</span></span>

## <span data-ttu-id="ab628-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab628-133">OUTPUTS</span></span>

### <span data-ttu-id="ab628-134">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="ab628-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="ab628-135">Note</span><span class="sxs-lookup"><span data-stu-id="ab628-135">NOTES</span></span>

## <span data-ttu-id="ab628-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab628-136">RELATED LINKS</span></span>

[<span data-ttu-id="ab628-137">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ab628-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="ab628-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ab628-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="ab628-139">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="ab628-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
