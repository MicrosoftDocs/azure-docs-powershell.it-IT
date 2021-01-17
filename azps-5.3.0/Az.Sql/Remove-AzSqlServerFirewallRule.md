---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 83a68863b3dce71a091dc5de11377bade7bdc638
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473772"
---
# <span data-ttu-id="c71b7-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c71b7-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="c71b7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c71b7-102">SYNOPSIS</span></span>
<span data-ttu-id="c71b7-103">Elimina una regola del firewall da un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="c71b7-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="c71b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c71b7-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c71b7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c71b7-105">DESCRIPTION</span></span>
<span data-ttu-id="c71b7-106">Il cmdlet **Remove-AzSqlServerFirewallRule** Elimina una regola del firewall dal server di database SQL di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="c71b7-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="c71b7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c71b7-107">EXAMPLES</span></span>

### <span data-ttu-id="c71b7-108">Esempio 1: eliminare una regola</span><span class="sxs-lookup"><span data-stu-id="c71b7-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="c71b7-109">Questo comando Elimina una regola del firewall denominata Rule01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="c71b7-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="c71b7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c71b7-110">PARAMETERS</span></span>

### <span data-ttu-id="c71b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c71b7-111">-DefaultProfile</span></span>
<span data-ttu-id="c71b7-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c71b7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c71b7-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="c71b7-113">-FirewallRuleName</span></span>
<span data-ttu-id="c71b7-114">Specifica il nome della regola del firewall eliminata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c71b7-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="c71b7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c71b7-115">-Force</span></span>
<span data-ttu-id="c71b7-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c71b7-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c71b7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c71b7-117">-ResourceGroupName</span></span>
<span data-ttu-id="c71b7-118">Specifica il nome di un gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="c71b7-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c71b7-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="c71b7-119">-ServerName</span></span>
<span data-ttu-id="c71b7-120">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="c71b7-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="c71b7-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c71b7-121">-Confirm</span></span>
<span data-ttu-id="c71b7-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c71b7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c71b7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c71b7-123">-WhatIf</span></span>
<span data-ttu-id="c71b7-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c71b7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c71b7-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c71b7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c71b7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c71b7-126">CommonParameters</span></span>
<span data-ttu-id="c71b7-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c71b7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c71b7-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c71b7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c71b7-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c71b7-129">INPUTS</span></span>

### <span data-ttu-id="c71b7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c71b7-130">System.String</span></span>

## <span data-ttu-id="c71b7-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c71b7-131">OUTPUTS</span></span>

### <span data-ttu-id="c71b7-132">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="c71b7-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="c71b7-133">Note</span><span class="sxs-lookup"><span data-stu-id="c71b7-133">NOTES</span></span>

## <span data-ttu-id="c71b7-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c71b7-134">RELATED LINKS</span></span>

[<span data-ttu-id="c71b7-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c71b7-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="c71b7-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c71b7-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="c71b7-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c71b7-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="c71b7-138">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="c71b7-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


