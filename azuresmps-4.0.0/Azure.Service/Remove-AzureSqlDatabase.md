---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B3813F54-E5B7-4605-BB1C-67417FDDB076
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3f9817ebe556bc80364d012040387cca72c56c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029570"
---
# <span data-ttu-id="5018c-101">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5018c-101">Remove-AzureSqlDatabase</span></span>

## <span data-ttu-id="5018c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5018c-102">SYNOPSIS</span></span>
<span data-ttu-id="5018c-103">Elimina un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="5018c-103">Deletes an Azure SQL Database.</span></span>

## <span data-ttu-id="5018c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5018c-104">SYNTAX</span></span>

### <span data-ttu-id="5018c-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="5018c-105">ByNameWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5018c-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="5018c-106">ByObjectWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5018c-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="5018c-107">ByNameWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5018c-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="5018c-108">ByObjectWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -Database <Database> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5018c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5018c-109">DESCRIPTION</span></span>
<span data-ttu-id="5018c-110">Il cmdlet **Remove-AzureSqlDatabase** Elimina un database SQL di Azure per il contesto di connessione del server o il nome del server.</span><span class="sxs-lookup"><span data-stu-id="5018c-110">The **Remove-AzureSqlDatabase** cmdlet deletes an Azure SQL Database by server connection context or server name.</span></span>
<span data-ttu-id="5018c-111">È possibile creare un contesto di connessione del server di database SQL di Azure usando il cmdlet **New-AzureSqlDatabaseServerContext** e quindi usarlo con questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5018c-111">You can create an Azure SQL Database server connection context using the **New-AzureSqlDatabaseServerContext** cmdlet, and then use it with this cmdlet.</span></span>

<span data-ttu-id="5018c-112">Quando si elimina un database specificando un nome del server di database SQL di Azure, il cmdlet **Remove-AzureSqlDatabase** usa il nome e le informazioni di abbonamento di Azure correnti per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5018c-112">When you delete a database by specifying an Azure SQL Database server name, the **Remove-AzureSqlDatabase** cmdlet uses the name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="5018c-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5018c-113">EXAMPLES</span></span>

### <span data-ttu-id="5018c-114">Esempio 1: rimuovere un database</span><span class="sxs-lookup"><span data-stu-id="5018c-114">Example 1: Remove a database</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="5018c-115">Questo comando rimuove il database denominato Database01 dal contesto di connessione del server di database SQL di Azure $Context.</span><span class="sxs-lookup"><span data-stu-id="5018c-115">This command removes the database named Database01 from the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="5018c-116">Esempio 2: rimuovere un database usando un nome di server</span><span class="sxs-lookup"><span data-stu-id="5018c-116">Example 2: Remove a database by using a server name</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="5018c-117">Questo comando rimuove il database denominato Database01 dal server di database SQL di Azure denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="5018c-117">This command removes the database named Database01 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="5018c-118">Esempio 3: rimuovere un database tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="5018c-118">Example 3: Remove a database by using the pipeline</span></span>
```
PS C:\> $Database01 | Remove-AzureSqlDatabase -ConnectionContext $Context
PS C:\> $Database01 | Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="5018c-119">Questo esempio illustra il metodo alternativo per passare l'oggetto di database tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="5018c-119">This example demonstrates the alternative method of passing the database object through the pipeline.</span></span>

## <span data-ttu-id="5018c-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5018c-120">PARAMETERS</span></span>

### <span data-ttu-id="5018c-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="5018c-121">-ConnectionContext</span></span>
<span data-ttu-id="5018c-122">Specifica il contesto di connessione di un server da cui questo cmdlet rimuove un database.</span><span class="sxs-lookup"><span data-stu-id="5018c-122">Specifies the connection context of a server from which this cmdlet removes a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5018c-123">-Database</span><span class="sxs-lookup"><span data-stu-id="5018c-123">-Database</span></span>
<span data-ttu-id="5018c-124">Specifica un oggetto che rappresenta il database rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5018c-124">Specifies an object that represents the database that this cmdlet removes.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5018c-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5018c-125">-DatabaseName</span></span>
<span data-ttu-id="5018c-126">Specifica il nome del database rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5018c-126">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5018c-127">-Force</span><span class="sxs-lookup"><span data-stu-id="5018c-127">-Force</span></span>
<span data-ttu-id="5018c-128">Consente di completare l'azione senza richiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="5018c-128">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="5018c-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="5018c-129">-Profile</span></span>
<span data-ttu-id="5018c-130">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5018c-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5018c-131">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="5018c-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5018c-132">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5018c-132">-ServerName</span></span>
<span data-ttu-id="5018c-133">Specifica il nome del server in cui questo cmdlet elimina il database.</span><span class="sxs-lookup"><span data-stu-id="5018c-133">Specifies the name of the server on which this cmdlet deletes the database.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5018c-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5018c-134">-Confirm</span></span>
<span data-ttu-id="5018c-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5018c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5018c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5018c-136">-WhatIf</span></span>
<span data-ttu-id="5018c-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5018c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5018c-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5018c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5018c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5018c-139">CommonParameters</span></span>
<span data-ttu-id="5018c-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5018c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5018c-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5018c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5018c-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5018c-142">INPUTS</span></span>

### <span data-ttu-id="5018c-143">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database</span><span class="sxs-lookup"><span data-stu-id="5018c-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="5018c-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5018c-144">OUTPUTS</span></span>

## <span data-ttu-id="5018c-145">Note</span><span class="sxs-lookup"><span data-stu-id="5018c-145">NOTES</span></span>
* <span data-ttu-id="5018c-146">A causa della gravità dell'operazione, per impostazione predefinita, questo cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="5018c-146">Because of the severity of the operation, by default, this cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="5018c-147">Per ignorare la conferma, specificare il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="5018c-147">To skip confirmation, specify the *Force* parameter.</span></span>

## <span data-ttu-id="5018c-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5018c-148">RELATED LINKS</span></span>

[<span data-ttu-id="5018c-149">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="5018c-149">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="5018c-150">Eliminare un database</span><span class="sxs-lookup"><span data-stu-id="5018c-150">Delete Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505705.aspx)

[<span data-ttu-id="5018c-151">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="5018c-151">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="5018c-152">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5018c-152">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="5018c-153">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5018c-153">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="5018c-154">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="5018c-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="5018c-155">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5018c-155">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


