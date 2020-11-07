---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 4dea3f8bf91bb4b9c0478c281e6ca9366c49744c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864949"
---
# <span data-ttu-id="04c49-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="04c49-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="04c49-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="04c49-102">SYNOPSIS</span></span>
<span data-ttu-id="04c49-103">Modifica una regola del firewall nel server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="04c49-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="04c49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04c49-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04c49-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04c49-105">DESCRIPTION</span></span>
<span data-ttu-id="04c49-106">Il cmdlet **set-AzSqlServerFirewallRule** modifica una regola del firewall in un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="04c49-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="04c49-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04c49-107">EXAMPLES</span></span>

### <span data-ttu-id="04c49-108">Esempio 1: modificare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="04c49-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="04c49-109">Questo comando consente di modificare una regola del firewall denominata Rule01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="04c49-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="04c49-110">Il comando modifica gli indirizzi IP di inizio e fine.</span><span class="sxs-lookup"><span data-stu-id="04c49-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="04c49-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04c49-111">PARAMETERS</span></span>

### <span data-ttu-id="04c49-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c49-112">-DefaultProfile</span></span>
<span data-ttu-id="04c49-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="04c49-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04c49-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="04c49-114">-EndIpAddress</span></span>
<span data-ttu-id="04c49-115">Specifica il valore finale dell'intervallo di indirizzi IP per la regola.</span><span class="sxs-lookup"><span data-stu-id="04c49-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="04c49-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="04c49-116">-FirewallRuleName</span></span>
<span data-ttu-id="04c49-117">Specifica il nome della regola del firewall che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="04c49-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="04c49-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04c49-118">-ResourceGroupName</span></span>
<span data-ttu-id="04c49-119">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="04c49-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="04c49-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="04c49-120">-ServerName</span></span>
<span data-ttu-id="04c49-121">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="04c49-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="04c49-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="04c49-122">-StartIpAddress</span></span>
<span data-ttu-id="04c49-123">Specifica il valore iniziale dell'intervallo di indirizzi IP per la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="04c49-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="04c49-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="04c49-124">-Confirm</span></span>
<span data-ttu-id="04c49-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04c49-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04c49-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04c49-126">-WhatIf</span></span>
<span data-ttu-id="04c49-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04c49-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04c49-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04c49-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04c49-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c49-129">CommonParameters</span></span>
<span data-ttu-id="04c49-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04c49-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c49-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04c49-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c49-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="04c49-132">INPUTS</span></span>

### <span data-ttu-id="04c49-133">System. String</span><span class="sxs-lookup"><span data-stu-id="04c49-133">System.String</span></span>

## <span data-ttu-id="04c49-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04c49-134">OUTPUTS</span></span>

### <span data-ttu-id="04c49-135">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="04c49-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="04c49-136">Note</span><span class="sxs-lookup"><span data-stu-id="04c49-136">NOTES</span></span>

## <span data-ttu-id="04c49-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04c49-137">RELATED LINKS</span></span>

[<span data-ttu-id="04c49-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="04c49-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="04c49-139">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="04c49-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="04c49-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="04c49-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="04c49-141">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="04c49-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


