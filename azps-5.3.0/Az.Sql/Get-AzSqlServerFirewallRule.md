---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: c2157521614375bbdeb06aac9a62320ec1e08c70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476651"
---
# <span data-ttu-id="5f409-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5f409-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="5f409-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f409-102">SYNOPSIS</span></span>
<span data-ttu-id="5f409-103">Ottiene le regole del firewall per un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="5f409-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="5f409-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f409-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f409-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f409-105">DESCRIPTION</span></span>
<span data-ttu-id="5f409-106">Il cmdlet **Get-AzSqlServerFirewallRule** ottiene le regole del firewall per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="5f409-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="5f409-107">Se specifichi il nome di una regola del firewall, questo cmdlet ottiene le informazioni relative alla specifica regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="5f409-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="5f409-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f409-108">EXAMPLES</span></span>

### <span data-ttu-id="5f409-109">Esempio 1: ottenere tutte le regole per un server</span><span class="sxs-lookup"><span data-stu-id="5f409-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="5f409-110">Questo comando consente di ottenere tutte le regole del firewall per il server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="5f409-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="5f409-111">Esempio 2: ottenere tutte le regole per un server tramite filtro</span><span class="sxs-lookup"><span data-stu-id="5f409-111">Example 2: Get all rules for a server using filtering</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule*"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : Rule01

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule02
```

<span data-ttu-id="5f409-112">Questo comando consente di ottenere tutte le regole del firewall per il server denominato Server01 che iniziano con "Rule".</span><span class="sxs-lookup"><span data-stu-id="5f409-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="5f409-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f409-113">PARAMETERS</span></span>

### <span data-ttu-id="5f409-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f409-114">-DefaultProfile</span></span>
<span data-ttu-id="5f409-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5f409-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f409-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="5f409-116">-FirewallRuleName</span></span>
<span data-ttu-id="5f409-117">Specifica il nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="5f409-117">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f409-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f409-118">-ResourceGroupName</span></span>
<span data-ttu-id="5f409-119">Specifica il nome del gruppo di risorse a cui è assegnato SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5f409-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="5f409-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5f409-120">-ServerName</span></span>
<span data-ttu-id="5f409-121">Specifica il nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5f409-121">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="5f409-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5f409-122">-Confirm</span></span>
<span data-ttu-id="5f409-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f409-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f409-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f409-124">-WhatIf</span></span>
<span data-ttu-id="5f409-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f409-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f409-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f409-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f409-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f409-127">CommonParameters</span></span>
<span data-ttu-id="5f409-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f409-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f409-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f409-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f409-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f409-130">INPUTS</span></span>

### <span data-ttu-id="5f409-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5f409-131">System.String</span></span>

## <span data-ttu-id="5f409-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f409-132">OUTPUTS</span></span>

### <span data-ttu-id="5f409-133">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="5f409-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="5f409-134">Note</span><span class="sxs-lookup"><span data-stu-id="5f409-134">NOTES</span></span>

## <span data-ttu-id="5f409-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f409-135">RELATED LINKS</span></span>

[<span data-ttu-id="5f409-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5f409-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5f409-137">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5f409-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5f409-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5f409-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5f409-139">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="5f409-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


