---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383DD041-78DC-4170-9529-1FD6F13BC178
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29cbf01629ef772fc41436f3916a2077c1535329
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029568"
---
# <span data-ttu-id="ebaab-101">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ebaab-101">Remove-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="ebaab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ebaab-102">SYNOPSIS</span></span>
<span data-ttu-id="ebaab-103">Rimuove una regola del firewall da un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ebaab-103">Removes a firewall rule from an Azure SQL Database server.</span></span>

## <span data-ttu-id="ebaab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ebaab-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebaab-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebaab-105">DESCRIPTION</span></span>
<span data-ttu-id="ebaab-106">Il cmdlet **Remove-AzureSqlDatabaseServerFirewallRule** rimuove una regola del firewall da un'istanza del server di database SQL di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="ebaab-106">The **Remove-AzureSqlDatabaseServerFirewallRule** cmdlet removes a firewall rule from an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="ebaab-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ebaab-107">EXAMPLES</span></span>

### <span data-ttu-id="ebaab-108">Esempio 1: rimuovere una regola</span><span class="sxs-lookup"><span data-stu-id="ebaab-108">Example 1: Remove a rule</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="ebaab-109">Questo comando rimuove la regola del firewall denominata FirewallRule24 dal server di database SQL di Azure denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="ebaab-109">This command removes the firewall rule named FirewallRule24 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="ebaab-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ebaab-110">PARAMETERS</span></span>

### <span data-ttu-id="ebaab-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ebaab-111">-Force</span></span>
<span data-ttu-id="ebaab-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ebaab-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ebaab-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="ebaab-113">-Profile</span></span>
<span data-ttu-id="ebaab-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebaab-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ebaab-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ebaab-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebaab-116">-RuleName</span><span class="sxs-lookup"><span data-stu-id="ebaab-116">-RuleName</span></span>
<span data-ttu-id="ebaab-117">Specifica il nome della regola del firewall rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebaab-117">Specifies the name of the firewall rule that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebaab-118">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ebaab-118">-ServerName</span></span>
<span data-ttu-id="ebaab-119">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="ebaab-119">Specifies the name of a server.</span></span>
<span data-ttu-id="ebaab-120">Questo cmdlet consente di rimuovere una regola del firewall dal server specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ebaab-120">This cmdlet removes a firewall rule from the server that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebaab-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ebaab-121">-Confirm</span></span>
<span data-ttu-id="ebaab-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebaab-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebaab-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebaab-123">-WhatIf</span></span>
<span data-ttu-id="ebaab-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ebaab-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebaab-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ebaab-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebaab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebaab-126">CommonParameters</span></span>
<span data-ttu-id="ebaab-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebaab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebaab-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebaab-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebaab-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ebaab-129">INPUTS</span></span>

### <span data-ttu-id="ebaab-130">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="ebaab-130">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="ebaab-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ebaab-131">OUTPUTS</span></span>

## <span data-ttu-id="ebaab-132">Note</span><span class="sxs-lookup"><span data-stu-id="ebaab-132">NOTES</span></span>

## <span data-ttu-id="ebaab-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ebaab-133">RELATED LINKS</span></span>

[<span data-ttu-id="ebaab-134">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="ebaab-134">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="ebaab-135">Eliminare la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="ebaab-135">Delete Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505706.aspx)

[<span data-ttu-id="ebaab-136">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="ebaab-136">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="ebaab-137">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ebaab-137">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="ebaab-138">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ebaab-138">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="ebaab-139">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ebaab-139">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


