---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 6f79d85fd09848f1b6f43e4907565b4989197183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512211"
---
# <span data-ttu-id="06991-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="06991-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="06991-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06991-102">SYNOPSIS</span></span>
<span data-ttu-id="06991-103">Elimina una regola del firewall da un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="06991-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06991-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06991-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06991-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06991-105">DESCRIPTION</span></span>
<span data-ttu-id="06991-106">Il cmdlet **Remove-AzureRmSqlServerFirewallRule** Elimina una regola del firewall dal server di database SQL di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="06991-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="06991-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06991-107">EXAMPLES</span></span>

### <span data-ttu-id="06991-108">Esempio 1: eliminare una regola</span><span class="sxs-lookup"><span data-stu-id="06991-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "RresourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="06991-109">Questo comando Elimina una regola del firewall denominata Rule01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="06991-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="06991-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06991-110">PARAMETERS</span></span>

### <span data-ttu-id="06991-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06991-111">-DefaultProfile</span></span>
<span data-ttu-id="06991-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="06991-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06991-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="06991-113">-FirewallRuleName</span></span>
<span data-ttu-id="06991-114">Specifica il nome della regola del firewall eliminata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06991-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06991-115">-Force</span><span class="sxs-lookup"><span data-stu-id="06991-115">-Force</span></span>
<span data-ttu-id="06991-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="06991-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06991-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06991-117">-ResourceGroupName</span></span>
<span data-ttu-id="06991-118">Specifica il nome di un gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="06991-118">Specifies the name of a resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06991-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="06991-119">-ServerName</span></span>
<span data-ttu-id="06991-120">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="06991-120">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06991-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06991-121">-Confirm</span></span>
<span data-ttu-id="06991-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06991-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06991-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06991-123">-WhatIf</span></span>
<span data-ttu-id="06991-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06991-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06991-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06991-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06991-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06991-126">CommonParameters</span></span>
<span data-ttu-id="06991-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06991-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06991-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06991-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06991-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06991-129">INPUTS</span></span>

### <span data-ttu-id="06991-130">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="06991-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="06991-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06991-131">OUTPUTS</span></span>

## <span data-ttu-id="06991-132">Note</span><span class="sxs-lookup"><span data-stu-id="06991-132">NOTES</span></span>

## <span data-ttu-id="06991-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06991-133">RELATED LINKS</span></span>

[<span data-ttu-id="06991-134">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="06991-134">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="06991-135">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="06991-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="06991-136">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="06991-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="06991-137">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="06991-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


