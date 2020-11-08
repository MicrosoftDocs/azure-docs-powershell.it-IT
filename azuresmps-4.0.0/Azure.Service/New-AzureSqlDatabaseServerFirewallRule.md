---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023927"
---
# <span data-ttu-id="bcb2c-101">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bcb2c-101">New-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="bcb2c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bcb2c-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb2c-103">Crea una regola del firewall nel server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-103">Creates a firewall rule in Azure SQL Database Server.</span></span>

## <span data-ttu-id="bcb2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcb2c-104">SYNTAX</span></span>

### <span data-ttu-id="bcb2c-105">IpRange (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bcb2c-105">IpRange (Default)</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcb2c-106">AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="bcb2c-106">AllowAllAzureServices</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcb2c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcb2c-107">DESCRIPTION</span></span>
<span data-ttu-id="bcb2c-108">Il cmdlet **New-AzureSqlDatabaseServerFirewallRule** crea una regola del firewall nell'istanza specificata del server di database SQL di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-108">The **New-AzureSqlDatabaseServerFirewallRule** cmdlet creates a firewall rule in the specified instance of Azure SQL Database Server in the current subscription.</span></span>

<span data-ttu-id="bcb2c-109">USA i parametri *StartIpAddress* e *EndIpAddress* per specificare un intervallo di indirizzi IP che questa regola consente di connettersi al server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-109">Use the *StartIpAddress* and *EndIpAddress* parameters to specify a range of IP addresses that this rule allows to connect to the Azure SQL Database server.</span></span>

<span data-ttu-id="bcb2c-110">Specifica il parametro *AllowAllAzureServices* per creare una regola che consenta connessioni Azure al server.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-110">Specify the *AllowAllAzureServices* parameter to create a rule that allows Azure connections to the server.</span></span>
<span data-ttu-id="bcb2c-111">La regola include i valori degli indirizzi IP iniziali e finali di 0.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-111">The rule has starting and ending IP address values of 0.0.0.0.</span></span>
<span data-ttu-id="bcb2c-112">Se non specifichi un nome per la regola del firewall, questo cmdlet assegna il nome predefinito AllowAllAzureServices.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-112">If you do not specify a firewall rule name, this cmdlet assigns the default name AllowAllAzureServices.</span></span>

## <span data-ttu-id="bcb2c-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcb2c-113">EXAMPLES</span></span>

### <span data-ttu-id="bcb2c-114">Esempio 1: creare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="bcb2c-114">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

<span data-ttu-id="bcb2c-115">Questo comando crea una regola del firewall FirewallRule24 nel server di database SQL di Azure denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-115">This command creates a firewall rule FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="bcb2c-116">Il comando specifica un intervallo di indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-116">The command specifies an IP address range.</span></span>

### <span data-ttu-id="bcb2c-117">Esempio 2: creare una regola che consenta a tutti i servizi Azure</span><span class="sxs-lookup"><span data-stu-id="bcb2c-117">Example 2: Create a rule that allows all Azure services</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

<span data-ttu-id="bcb2c-118">Questo comando crea una regola del firewall denominata AzureConnections nel server denominata lpqd0zbr8y che consente le connessioni Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-118">This command creates a firewall rule named AzureConnections on the server named lpqd0zbr8y that allows Azure connections.</span></span>

### <span data-ttu-id="bcb2c-119">Esempio 3: creare una regola che consente a tutti i servizi Azure che usano il nome predefinito di creare una regola che consenta a tutti i servizi Azure che usano il nome predefinito</span><span class="sxs-lookup"><span data-stu-id="bcb2c-119">Example 3: Create a rule that allows all Azure services that uses the default name Create a rule that allows all Azure services that uses the default name</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

<span data-ttu-id="bcb2c-120">Questo comando crea una regola del firewall nel server specificato denominato lpqd0zbr8y che consente le connessioni Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-120">This command creates a firewall rule on the specified server named lpqd0zbr8y that allows Azure connections.</span></span>
<span data-ttu-id="bcb2c-121">Il comando assegna il nome di regola predefinito AllowAllAzureServices.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-121">The command assigns the default rule name AllowAllAzureServices.</span></span>

## <span data-ttu-id="bcb2c-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcb2c-122">PARAMETERS</span></span>

### <span data-ttu-id="bcb2c-123">-AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="bcb2c-123">-AllowAllAzureServices</span></span>
<span data-ttu-id="bcb2c-124">Indica che questa regola del firewall consente a tutti gli indirizzi IP di Azure di accedere al server.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-124">Indicates that this firewall rule enables all Azure IP addresses to access the server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb2c-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="bcb2c-125">-EndIpAddress</span></span>
<span data-ttu-id="bcb2c-126">Specifica il valore finale dell'intervallo di indirizzi IP per la regola.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-126">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb2c-127">-Force</span><span class="sxs-lookup"><span data-stu-id="bcb2c-127">-Force</span></span>
<span data-ttu-id="bcb2c-128">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bcb2c-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="bcb2c-129">-Profile</span></span>
<span data-ttu-id="bcb2c-130">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bcb2c-131">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bcb2c-132">-RuleName</span><span class="sxs-lookup"><span data-stu-id="bcb2c-132">-RuleName</span></span>
<span data-ttu-id="bcb2c-133">Specifica il nome della nuova regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-133">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb2c-134">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="bcb2c-134">-ServerName</span></span>
<span data-ttu-id="bcb2c-135">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-135">Specifies the name of a server.</span></span>
<span data-ttu-id="bcb2c-136">Questo cmdlet crea una regola del firewall nel server specificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-136">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="bcb2c-137">Specificare il nome del server e non il nome DNS completo.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-137">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="bcb2c-138">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="bcb2c-138">-StartIpAddress</span></span>
<span data-ttu-id="bcb2c-139">Specifica il valore iniziale dell'intervallo di indirizzi IP per la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-139">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb2c-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bcb2c-140">-Confirm</span></span>
<span data-ttu-id="bcb2c-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcb2c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcb2c-142">-WhatIf</span></span>
<span data-ttu-id="bcb2c-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcb2c-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcb2c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb2c-145">CommonParameters</span></span>
<span data-ttu-id="bcb2c-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcb2c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb2c-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcb2c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb2c-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bcb2c-148">INPUTS</span></span>

## <span data-ttu-id="bcb2c-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcb2c-149">OUTPUTS</span></span>

### <span data-ttu-id="bcb2c-150">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="bcb2c-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="bcb2c-151">Note</span><span class="sxs-lookup"><span data-stu-id="bcb2c-151">NOTES</span></span>

## <span data-ttu-id="bcb2c-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcb2c-152">RELATED LINKS</span></span>

[<span data-ttu-id="bcb2c-153">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="bcb2c-153">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="bcb2c-154">Creare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="bcb2c-154">Create Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[<span data-ttu-id="bcb2c-155">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="bcb2c-155">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="bcb2c-156">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bcb2c-156">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="bcb2c-157">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bcb2c-157">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="bcb2c-158">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bcb2c-158">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


