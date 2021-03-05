---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 0b76faf383e8cd3c70d6ff1e7e38de367850ac8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967357"
---
# <span data-ttu-id="bb829-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bb829-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="bb829-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb829-102">SYNOPSIS</span></span>
<span data-ttu-id="bb829-103">Elimina una regola del firewall da un server SQL database.</span><span class="sxs-lookup"><span data-stu-id="bb829-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="bb829-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb829-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb829-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bb829-105">DESCRIPTION</span></span>
<span data-ttu-id="bb829-106">Il cmdlet **Remove-AzSqlServerFirewallRule** elimina una regola del firewall dal server di database SQL Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="bb829-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="bb829-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb829-107">EXAMPLES</span></span>

### <span data-ttu-id="bb829-108">Esempio 1: Eliminare una regola</span><span class="sxs-lookup"><span data-stu-id="bb829-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="bb829-109">Questo comando elimina una regola del firewall denominata Rule01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="bb829-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="bb829-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb829-110">PARAMETERS</span></span>

### <span data-ttu-id="bb829-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb829-111">-DefaultProfile</span></span>
<span data-ttu-id="bb829-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bb829-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb829-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="bb829-113">-FirewallRuleName</span></span>
<span data-ttu-id="bb829-114">Specifica il nome della regola del firewall che il cmdlet elimina.</span><span class="sxs-lookup"><span data-stu-id="bb829-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="bb829-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bb829-115">-Force</span></span>
<span data-ttu-id="bb829-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="bb829-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bb829-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb829-117">-ResourceGroupName</span></span>
<span data-ttu-id="bb829-118">Specifica il nome di un gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="bb829-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="bb829-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bb829-119">-ServerName</span></span>
<span data-ttu-id="bb829-120">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="bb829-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="bb829-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb829-121">-Confirm</span></span>
<span data-ttu-id="bb829-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb829-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb829-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb829-123">-WhatIf</span></span>
<span data-ttu-id="bb829-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb829-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb829-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb829-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb829-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb829-126">CommonParameters</span></span>
<span data-ttu-id="bb829-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb829-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb829-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bb829-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb829-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="bb829-129">INPUTS</span></span>

### <span data-ttu-id="bb829-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bb829-130">System.String</span></span>

## <span data-ttu-id="bb829-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb829-131">OUTPUTS</span></span>

### <span data-ttu-id="bb829-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="bb829-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="bb829-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="bb829-133">NOTES</span></span>

## <span data-ttu-id="bb829-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb829-134">RELATED LINKS</span></span>

[<span data-ttu-id="bb829-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bb829-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="bb829-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bb829-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="bb829-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bb829-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="bb829-138">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="bb829-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


