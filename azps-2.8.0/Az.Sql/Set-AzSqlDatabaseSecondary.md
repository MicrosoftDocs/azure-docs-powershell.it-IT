---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 7c500ba5ea2494109a99e7c66e084efefc48d2e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857149"
---
# <span data-ttu-id="60f77-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="60f77-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="60f77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60f77-102">SYNOPSIS</span></span>
<span data-ttu-id="60f77-103">Commuta un database secondario come primario per avviare il failover.</span><span class="sxs-lookup"><span data-stu-id="60f77-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="60f77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60f77-104">SYNTAX</span></span>

### <span data-ttu-id="60f77-105">NoOptionsSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60f77-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60f77-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="60f77-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60f77-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60f77-107">DESCRIPTION</span></span>
<span data-ttu-id="60f77-108">Il cmdlet **set-AzSqlDatabaseSecondary** passa un database secondario come primario per avviare il failover.</span><span class="sxs-lookup"><span data-stu-id="60f77-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="60f77-109">Questo cmdlet è progettato come comando di configurazione generale, ma attualmente è limitato all'avvio del failover.</span><span class="sxs-lookup"><span data-stu-id="60f77-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="60f77-110">Specifica il parametro *AllowDataLoss* per avviare un failover della forza durante un'interruzione.</span><span class="sxs-lookup"><span data-stu-id="60f77-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="60f77-111">Non è necessario specificare questo parametro quando si esegue un'operazione pianificata, ad esempio esercitazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="60f77-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="60f77-112">In quest'ultimo caso, il database secondario viene sincronizzato con il principale prima che venga attivato.</span><span class="sxs-lookup"><span data-stu-id="60f77-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="60f77-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60f77-113">EXAMPLES</span></span>

### <span data-ttu-id="60f77-114">1: avviare un failover pianificato</span><span class="sxs-lookup"><span data-stu-id="60f77-114">1: Initiate a planned failover</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="60f77-115">2: avviare un failover forzato (con potenziale perdita di dati)</span><span class="sxs-lookup"><span data-stu-id="60f77-115">2: Initiate a forced failover (with potential data loss)</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="60f77-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60f77-116">PARAMETERS</span></span>

### <span data-ttu-id="60f77-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="60f77-117">-AllowDataLoss</span></span>
<span data-ttu-id="60f77-118">Indica che questa operazione di failover consente la perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="60f77-118">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f77-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60f77-119">-AsJob</span></span>
<span data-ttu-id="60f77-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="60f77-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f77-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="60f77-121">-DatabaseName</span></span>
<span data-ttu-id="60f77-122">Specifica il nome del database SQL di Azure secondario.</span><span class="sxs-lookup"><span data-stu-id="60f77-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="60f77-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f77-123">-DefaultProfile</span></span>
<span data-ttu-id="60f77-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="60f77-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60f77-125">-Failover</span><span class="sxs-lookup"><span data-stu-id="60f77-125">-Failover</span></span>
<span data-ttu-id="60f77-126">Indica che questa operazione è un failover.</span><span class="sxs-lookup"><span data-stu-id="60f77-126">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f77-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60f77-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="60f77-128">Specifica il nome del gruppo di risorse a cui è assegnato il database SQL di Azure partner.</span><span class="sxs-lookup"><span data-stu-id="60f77-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="60f77-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60f77-129">-ResourceGroupName</span></span>
<span data-ttu-id="60f77-130">Specifica il nome del gruppo di risorse a cui è assegnato il database SQL di Azure secondario.</span><span class="sxs-lookup"><span data-stu-id="60f77-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="60f77-131">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="60f77-131">-ServerName</span></span>
<span data-ttu-id="60f77-132">Specifica il nome di SQL Server che ospita il database SQL di Azure secondario.</span><span class="sxs-lookup"><span data-stu-id="60f77-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="60f77-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="60f77-133">-Confirm</span></span>
<span data-ttu-id="60f77-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60f77-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60f77-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60f77-135">-WhatIf</span></span>
<span data-ttu-id="60f77-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60f77-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60f77-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60f77-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60f77-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f77-138">CommonParameters</span></span>
<span data-ttu-id="60f77-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60f77-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f77-140">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60f77-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f77-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60f77-141">INPUTS</span></span>

### <span data-ttu-id="60f77-142">System. String</span><span class="sxs-lookup"><span data-stu-id="60f77-142">System.String</span></span>

## <span data-ttu-id="60f77-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60f77-143">OUTPUTS</span></span>

### <span data-ttu-id="60f77-144">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="60f77-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="60f77-145">Note</span><span class="sxs-lookup"><span data-stu-id="60f77-145">NOTES</span></span>

## <span data-ttu-id="60f77-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60f77-146">RELATED LINKS</span></span>

[<span data-ttu-id="60f77-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="60f77-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="60f77-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="60f77-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="60f77-149">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="60f77-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
