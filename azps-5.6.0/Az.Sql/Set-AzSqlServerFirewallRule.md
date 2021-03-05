---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 2365cb4f6dedeb0620a2bdb1c1549eb0cd25d0c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992401"
---
# <span data-ttu-id="e8769-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e8769-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="e8769-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8769-102">SYNOPSIS</span></span>
<span data-ttu-id="e8769-103">Modifica una regola del firewall in Azure SQL server di database.</span><span class="sxs-lookup"><span data-stu-id="e8769-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="e8769-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8769-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8769-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e8769-105">DESCRIPTION</span></span>
<span data-ttu-id="e8769-106">Il cmdlet **Set-AzSqlServerFirewallRule** modifica una regola del firewall in un server di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e8769-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="e8769-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8769-107">EXAMPLES</span></span>

### <span data-ttu-id="e8769-108">Esempio 1: Modificare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="e8769-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="e8769-109">Questo comando modifica una regola del firewall denominata Rule01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="e8769-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="e8769-110">Il comando modifica gli indirizzi IP di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="e8769-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="e8769-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8769-111">PARAMETERS</span></span>

### <span data-ttu-id="e8769-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8769-112">-DefaultProfile</span></span>
<span data-ttu-id="e8769-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e8769-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8769-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="e8769-114">-EndIpAddress</span></span>
<span data-ttu-id="e8769-115">Specifica il valore finale dell'intervallo di indirizzi IP per la regola.</span><span class="sxs-lookup"><span data-stu-id="e8769-115">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8769-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="e8769-116">-FirewallRuleName</span></span>
<span data-ttu-id="e8769-117">Specifica il nome della regola del firewall modificata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8769-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8769-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8769-118">-ResourceGroupName</span></span>
<span data-ttu-id="e8769-119">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="e8769-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e8769-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e8769-120">-ServerName</span></span>
<span data-ttu-id="e8769-121">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="e8769-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e8769-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="e8769-122">-StartIpAddress</span></span>
<span data-ttu-id="e8769-123">Specifica il valore iniziale dell'intervallo di indirizzi IP per la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="e8769-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8769-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8769-124">-Confirm</span></span>
<span data-ttu-id="e8769-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8769-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8769-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8769-126">-WhatIf</span></span>
<span data-ttu-id="e8769-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8769-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8769-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8769-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8769-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8769-129">CommonParameters</span></span>
<span data-ttu-id="e8769-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8769-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8769-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e8769-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8769-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="e8769-132">INPUTS</span></span>

### <span data-ttu-id="e8769-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e8769-133">System.String</span></span>

## <span data-ttu-id="e8769-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8769-134">OUTPUTS</span></span>

### <span data-ttu-id="e8769-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="e8769-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="e8769-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="e8769-136">NOTES</span></span>

## <span data-ttu-id="e8769-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8769-137">RELATED LINKS</span></span>

[<span data-ttu-id="e8769-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e8769-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="e8769-139">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e8769-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="e8769-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e8769-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="e8769-141">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="e8769-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


