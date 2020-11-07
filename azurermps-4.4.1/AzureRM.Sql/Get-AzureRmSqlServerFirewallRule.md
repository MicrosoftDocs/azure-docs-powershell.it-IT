---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 27715ee03871c08c53380861e2cd54d843b2ba51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687066"
---
# <span data-ttu-id="ffa21-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ffa21-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="ffa21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ffa21-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa21-103">Ottiene le regole del firewall per un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="ffa21-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffa21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ffa21-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ffa21-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ffa21-105">DESCRIPTION</span></span>
<span data-ttu-id="ffa21-106">Il cmdlet **Get-AzureRmSqlServerFirewallRule** ottiene le regole del firewall per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa21-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="ffa21-107">Se specifichi il nome di una regola del firewall, questo cmdlet ottiene le informazioni relative alla specifica regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="ffa21-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="ffa21-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ffa21-108">EXAMPLES</span></span>

### <span data-ttu-id="ffa21-109">Esempio 1: ottenere tutte le regole per un server</span><span class="sxs-lookup"><span data-stu-id="ffa21-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="ffa21-110">Questo comando consente di ottenere tutte le regole del firewall per il server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="ffa21-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="ffa21-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ffa21-111">PARAMETERS</span></span>

### <span data-ttu-id="ffa21-112">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="ffa21-112">-FirewallRuleName</span></span>
<span data-ttu-id="ffa21-113">Specifica il nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="ffa21-113">Specifies the name of the firewall rule.</span></span>

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

### <span data-ttu-id="ffa21-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa21-114">-ResourceGroupName</span></span>
<span data-ttu-id="ffa21-115">Specifica il nome del gruppo di risorse a cui è assegnato SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ffa21-115">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="ffa21-116">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ffa21-116">-ServerName</span></span>
<span data-ttu-id="ffa21-117">Specifica il nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ffa21-117">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="ffa21-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ffa21-118">-Confirm</span></span>
<span data-ttu-id="ffa21-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffa21-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa21-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa21-120">-WhatIf</span></span>
<span data-ttu-id="ffa21-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ffa21-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffa21-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ffa21-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa21-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa21-123">-DefaultProfile</span></span>
<span data-ttu-id="ffa21-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa21-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffa21-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa21-125">CommonParameters</span></span>
<span data-ttu-id="ffa21-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffa21-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa21-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffa21-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa21-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ffa21-128">INPUTS</span></span>

## <span data-ttu-id="ffa21-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ffa21-129">OUTPUTS</span></span>

### <span data-ttu-id="ffa21-130">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="ffa21-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="ffa21-131">Note</span><span class="sxs-lookup"><span data-stu-id="ffa21-131">NOTES</span></span>

## <span data-ttu-id="ffa21-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ffa21-132">RELATED LINKS</span></span>

[<span data-ttu-id="ffa21-133">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ffa21-133">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="ffa21-134">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ffa21-134">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="ffa21-135">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ffa21-135">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="ffa21-136">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="ffa21-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


