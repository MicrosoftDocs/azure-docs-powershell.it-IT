---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 566081ea78137c3816ecee58e76a4811c7f54f62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961373"
---
# <span data-ttu-id="e263b-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e263b-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="e263b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e263b-102">SYNOPSIS</span></span>
<span data-ttu-id="e263b-103">Termina la replica dei dati tra un database SQL dati e il database secondario specificato.</span><span class="sxs-lookup"><span data-stu-id="e263b-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="e263b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e263b-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e263b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e263b-105">DESCRIPTION</span></span>
<span data-ttu-id="e263b-106">Il cmdlet **Remove-AzSqlDatabaseSecondary forza** la terminazione di un collegamento di replica geografica.</span><span class="sxs-lookup"><span data-stu-id="e263b-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="e263b-107">Questo cmdlet sostituisce il Stop-AzSqlDatabaseCopy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e263b-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="e263b-108">Non esiste alcuna sincronizzazione della replica prima della terminazione.</span><span class="sxs-lookup"><span data-stu-id="e263b-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="e263b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e263b-109">EXAMPLES</span></span>

## <span data-ttu-id="e263b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e263b-110">PARAMETERS</span></span>

### <span data-ttu-id="e263b-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e263b-111">-DatabaseName</span></span>
<span data-ttu-id="e263b-112">Specifica il nome del database SQL Azure primario con il collegamento di replica rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e263b-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e263b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e263b-113">-DefaultProfile</span></span>
<span data-ttu-id="e263b-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e263b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e263b-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e263b-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="e263b-116">Specifica il nome del gruppo di risorse partner.</span><span class="sxs-lookup"><span data-stu-id="e263b-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="e263b-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="e263b-117">-PartnerServerName</span></span>
<span data-ttu-id="e263b-118">Specifica il nome del partner SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e263b-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="e263b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e263b-119">-ResourceGroupName</span></span>
<span data-ttu-id="e263b-120">Specifica il nome del gruppo di risorse associato al collegamento di replica da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e263b-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="e263b-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e263b-121">-ServerName</span></span>
<span data-ttu-id="e263b-122">Specifica il nome dell'SQL Server contenente il collegamento di replica da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e263b-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="e263b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e263b-123">-Confirm</span></span>
<span data-ttu-id="e263b-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e263b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e263b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e263b-125">-WhatIf</span></span>
<span data-ttu-id="e263b-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e263b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e263b-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e263b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e263b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e263b-128">CommonParameters</span></span>
<span data-ttu-id="e263b-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e263b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e263b-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e263b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e263b-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="e263b-131">INPUTS</span></span>

### <span data-ttu-id="e263b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e263b-132">System.String</span></span>

## <span data-ttu-id="e263b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e263b-133">OUTPUTS</span></span>

### <span data-ttu-id="e263b-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="e263b-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="e263b-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="e263b-135">NOTES</span></span>

## <span data-ttu-id="e263b-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e263b-136">RELATED LINKS</span></span>

[<span data-ttu-id="e263b-137">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e263b-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="e263b-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e263b-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="e263b-139">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="e263b-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
