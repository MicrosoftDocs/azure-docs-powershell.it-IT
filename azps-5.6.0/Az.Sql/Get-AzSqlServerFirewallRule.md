---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: 21c942a9a67fd263dd251fd66224858292759096
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997329"
---
# <span data-ttu-id="98221-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="98221-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="98221-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98221-102">SYNOPSIS</span></span>
<span data-ttu-id="98221-103">Recupera le regole del firewall per un SQL server di database.</span><span class="sxs-lookup"><span data-stu-id="98221-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="98221-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98221-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98221-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="98221-105">DESCRIPTION</span></span>
<span data-ttu-id="98221-106">Il cmdlet **Get-AzSqlServerFirewallRule** ottiene le regole del firewall per un server di database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="98221-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="98221-107">Se si specifica il nome di una regola del firewall, questo cmdlet ottiene informazioni su quella specifica regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="98221-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="98221-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98221-108">EXAMPLES</span></span>

### <span data-ttu-id="98221-109">Esempio 1: Ottenere tutte le regole per un server</span><span class="sxs-lookup"><span data-stu-id="98221-109">Example 1: Get all rules for a server</span></span>
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

<span data-ttu-id="98221-110">Questo comando recupera tutte le regole del firewall per il server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="98221-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="98221-111">Esempio 2: Ottenere tutte le regole per un server usando i filtri</span><span class="sxs-lookup"><span data-stu-id="98221-111">Example 2: Get all rules for a server using filtering</span></span>
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

<span data-ttu-id="98221-112">Questo comando recupera tutte le regole del firewall per il server denominato Server01 che iniziano con "Regola".</span><span class="sxs-lookup"><span data-stu-id="98221-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="98221-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98221-113">PARAMETERS</span></span>

### <span data-ttu-id="98221-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98221-114">-DefaultProfile</span></span>
<span data-ttu-id="98221-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="98221-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98221-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="98221-116">-FirewallRuleName</span></span>
<span data-ttu-id="98221-117">Specifica il nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="98221-117">Specifies the name of the firewall rule.</span></span>

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

### <span data-ttu-id="98221-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98221-118">-ResourceGroupName</span></span>
<span data-ttu-id="98221-119">Specifica il nome del gruppo di risorse a cui è SQL Server risorsa.</span><span class="sxs-lookup"><span data-stu-id="98221-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="98221-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="98221-120">-ServerName</span></span>
<span data-ttu-id="98221-121">Specifica il nome della SQL Server.</span><span class="sxs-lookup"><span data-stu-id="98221-121">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="98221-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98221-122">-Confirm</span></span>
<span data-ttu-id="98221-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98221-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98221-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98221-124">-WhatIf</span></span>
<span data-ttu-id="98221-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98221-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98221-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98221-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98221-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98221-127">CommonParameters</span></span>
<span data-ttu-id="98221-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98221-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98221-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="98221-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98221-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="98221-130">INPUTS</span></span>

### <span data-ttu-id="98221-131">System.String</span><span class="sxs-lookup"><span data-stu-id="98221-131">System.String</span></span>

## <span data-ttu-id="98221-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98221-132">OUTPUTS</span></span>

### <span data-ttu-id="98221-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="98221-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="98221-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="98221-134">NOTES</span></span>

## <span data-ttu-id="98221-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98221-135">RELATED LINKS</span></span>

[<span data-ttu-id="98221-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="98221-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="98221-137">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="98221-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="98221-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="98221-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="98221-139">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="98221-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


