---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 1f7f039bb0bba1338fdcc4d5ceb3a403822fba71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510236"
---
# <span data-ttu-id="a42eb-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a42eb-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="a42eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a42eb-102">SYNOPSIS</span></span>
<span data-ttu-id="a42eb-103">Elimina una regola del firewall da un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="a42eb-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a42eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a42eb-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a42eb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a42eb-105">DESCRIPTION</span></span>
<span data-ttu-id="a42eb-106">Il cmdlet **Remove-AzureRmSqlServerFirewallRule** Elimina una regola del firewall dal server di database SQL di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="a42eb-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="a42eb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a42eb-107">EXAMPLES</span></span>

### <span data-ttu-id="a42eb-108">Esempio 1: eliminare una regola</span><span class="sxs-lookup"><span data-stu-id="a42eb-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "RresourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="a42eb-109">Questo comando Elimina una regola del firewall denominata Rule01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="a42eb-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="a42eb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a42eb-110">PARAMETERS</span></span>

### <span data-ttu-id="a42eb-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="a42eb-111">-FirewallRuleName</span></span>
<span data-ttu-id="a42eb-112">Specifica il nome della regola del firewall eliminata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a42eb-112">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="a42eb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a42eb-113">-Force</span></span>
<span data-ttu-id="a42eb-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a42eb-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a42eb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a42eb-115">-ResourceGroupName</span></span>
<span data-ttu-id="a42eb-116">Specifica il nome di un gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="a42eb-116">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a42eb-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a42eb-117">-ServerName</span></span>
<span data-ttu-id="a42eb-118">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="a42eb-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="a42eb-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a42eb-119">-Confirm</span></span>
<span data-ttu-id="a42eb-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a42eb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a42eb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a42eb-121">-WhatIf</span></span>
<span data-ttu-id="a42eb-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a42eb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a42eb-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a42eb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a42eb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a42eb-124">-DefaultProfile</span></span>
<span data-ttu-id="a42eb-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a42eb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a42eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a42eb-126">CommonParameters</span></span>
<span data-ttu-id="a42eb-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a42eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a42eb-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a42eb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a42eb-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a42eb-129">INPUTS</span></span>

### <span data-ttu-id="a42eb-130">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="a42eb-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="a42eb-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a42eb-131">OUTPUTS</span></span>

## <span data-ttu-id="a42eb-132">Note</span><span class="sxs-lookup"><span data-stu-id="a42eb-132">NOTES</span></span>

## <span data-ttu-id="a42eb-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a42eb-133">RELATED LINKS</span></span>

[<span data-ttu-id="a42eb-134">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a42eb-134">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a42eb-135">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a42eb-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a42eb-136">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a42eb-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="a42eb-137">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="a42eb-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


