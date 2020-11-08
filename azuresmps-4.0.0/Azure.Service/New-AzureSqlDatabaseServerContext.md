---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023928"
---
# <span data-ttu-id="87ebb-101">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="87ebb-101">New-AzureSqlDatabaseServerContext</span></span>

## <span data-ttu-id="87ebb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="87ebb-103">Crea un contesto di connessione al server.</span><span class="sxs-lookup"><span data-stu-id="87ebb-103">Creates a server connection context.</span></span>

## <span data-ttu-id="87ebb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87ebb-104">SYNTAX</span></span>

### <span data-ttu-id="87ebb-105">ByServerNameWithSqlAuth (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="87ebb-105">ByServerNameWithSqlAuth (Default)</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="87ebb-106">ByManageUrlWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="87ebb-106">ByManageUrlWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="87ebb-107">ByServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="87ebb-107">ByServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="87ebb-108">ByFullyQualifiedServerNameWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="87ebb-108">ByFullyQualifiedServerNameWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="87ebb-109">ByFullyQualifiedServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="87ebb-109">ByFullyQualifiedServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="87ebb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87ebb-110">DESCRIPTION</span></span>
<span data-ttu-id="87ebb-111">Il cmdlet **New-AzureSqlDatabaseServerContext** crea un contesto di connessione del server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="87ebb-111">The **New-AzureSqlDatabaseServerContext** cmdlet creates an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="87ebb-112">Usare l'autenticazione di SQL Server per creare un contesto di connessione a un server di database SQL utilizzando le credenziali specificate.</span><span class="sxs-lookup"><span data-stu-id="87ebb-112">Use SQL Server authentication to create a connection context to a SQL Database server by using the specified credentials.</span></span>
<span data-ttu-id="87ebb-113">È possibile specificare il server di database SQL per nome, per nome completo o per URL.</span><span class="sxs-lookup"><span data-stu-id="87ebb-113">You can specify the SQL Database server by name, by the fully qualified name, or by URL.</span></span>
<span data-ttu-id="87ebb-114">Per ottenere una credenziale, usare il cmdlet Get-Credential che chiede di specificare il nome utente e la password.</span><span class="sxs-lookup"><span data-stu-id="87ebb-114">To obtain a credential, use the Get-Credential cmdlet that prompts you to specify the user name and password.</span></span>

<span data-ttu-id="87ebb-115">Usa il cmdlet **New-AzureSqlDatabaseServerContext** con l'autenticazione basata su certificati per creare un contesto di connessione al server di database SQL specificato usando i dati di abbonamento di Azure specificati.</span><span class="sxs-lookup"><span data-stu-id="87ebb-115">Use the **New-AzureSqlDatabaseServerContext** cmdlet with certificate based authentication to create a connection context to the specified SQL Database server by using the specified Azure subscription data.</span></span>
<span data-ttu-id="87ebb-116">È possibile specificare il server di database SQL per nome o per il nome completo.</span><span class="sxs-lookup"><span data-stu-id="87ebb-116">You can specify SQL Database server by name or by the fully qualified name.</span></span>
<span data-ttu-id="87ebb-117">Puoi specificare i dati dell'abbonamento come parametro oppure può essere recuperato dall'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="87ebb-117">You can specify the subscription data as a parameter or it can be retrieved from the current Azure subscription.</span></span>
<span data-ttu-id="87ebb-118">Usare il cmdlet Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx per selezionare l'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="87ebb-118">Use the Select-AzureSubscriptionhttps://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet to select the current Azure subscription.</span></span>

## <span data-ttu-id="87ebb-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87ebb-119">EXAMPLES</span></span>

### <span data-ttu-id="87ebb-120">Esempio 1: creare un contesto usando l'autenticazione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="87ebb-120">Example 1: Create a context by using SQL Server authentication</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="87ebb-121">Questo esempio usa l'autenticazione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="87ebb-121">This example uses the SQL Server authentication.</span></span>

<span data-ttu-id="87ebb-122">Il primo comando richiede le credenziali di amministratore del server e archivia le credenziali nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="87ebb-122">The first command prompts you for server administrator credentials, and stores the credentials in the $Credential variable.</span></span>

<span data-ttu-id="87ebb-123">Il secondo comando si connette al server di database SQL denominato lpqd0zbr8y tramite $Credential.</span><span class="sxs-lookup"><span data-stu-id="87ebb-123">The second command connects to the SQL Database server named lpqd0zbr8y by using $Credential.</span></span>

<span data-ttu-id="87ebb-124">Il comando finale crea un database denominato Database17 nel server che fa parte del contesto in $Context.</span><span class="sxs-lookup"><span data-stu-id="87ebb-124">The final command creates a database named Database17 on the server that is part of the context in $Context.</span></span>

### <span data-ttu-id="87ebb-125">Esempio 2: creare un contesto usando l'autenticazione basata su certificati</span><span class="sxs-lookup"><span data-stu-id="87ebb-125">Example 2: Create a context by using certificate based authentication</span></span>
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

<span data-ttu-id="87ebb-126">Questo esempio usa l'autenticazione basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="87ebb-126">This example uses the certificate based authentication.</span></span>

<span data-ttu-id="87ebb-127">I primi due comandi assegnano valori alle variabili $SubscriptionId e $Thumbprint.</span><span class="sxs-lookup"><span data-stu-id="87ebb-127">The first two commands assign values to the $SubscriptionId and $Thumbprint variables.</span></span>

<span data-ttu-id="87ebb-128">Il terzo comando ottiene il certificato identificato dall'identificazione personale in $Thumbprint e lo archivia in $Certificate.</span><span class="sxs-lookup"><span data-stu-id="87ebb-128">The third command gets the certificate identified by the thumbprint in $Thumbprint, and stores it in $Certificate.</span></span>

<span data-ttu-id="87ebb-129">Il quarto comando imposta la sottoscrizione come Subscription07 e il quinto comando Seleziona l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="87ebb-129">The fourth command sets the subscription to be Subscription07, and the fifth command selects that subscription.</span></span>

<span data-ttu-id="87ebb-130">Il comando finale crea un contesto nell'abbonamento corrente per il server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="87ebb-130">The final command creates a context in the current subscription for the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="87ebb-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87ebb-131">PARAMETERS</span></span>

### <span data-ttu-id="87ebb-132">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="87ebb-132">-Credential</span></span>
<span data-ttu-id="87ebb-133">Specifica un oggetto Credential che fornisce l'autenticazione di SQL Server per l'accesso al server.</span><span class="sxs-lookup"><span data-stu-id="87ebb-133">Specifies a credential object that provides SQL Server authentication for you to access the server.</span></span>

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ebb-134">-FullyQualifiedServerName</span><span class="sxs-lookup"><span data-stu-id="87ebb-134">-FullyQualifiedServerName</span></span>
<span data-ttu-id="87ebb-135">Specifica il nome di dominio completo (FQDN) per il server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="87ebb-135">Specifies the fully qualified domain name (FQDN) name for the Azure SQL Database server.</span></span>
<span data-ttu-id="87ebb-136">Ad esempio, Server02.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="87ebb-136">For example, Server02.database.windows.net.</span></span>

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ebb-137">-ManageUrl</span><span class="sxs-lookup"><span data-stu-id="87ebb-137">-ManageUrl</span></span>
<span data-ttu-id="87ebb-138">Specifica l'URL usato da questo cmdlet per accedere al portale di Azure SQL DatabaseManagement per il server.</span><span class="sxs-lookup"><span data-stu-id="87ebb-138">Specifies the URL that this cmdlet uses to access the Azure SQL DatabaseManagement Portal for the server.</span></span>

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ebb-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="87ebb-139">-Profile</span></span>
<span data-ttu-id="87ebb-140">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87ebb-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="87ebb-141">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="87ebb-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="87ebb-142">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="87ebb-142">-ServerName</span></span>
<span data-ttu-id="87ebb-143">Specifica il nome del server di database.</span><span class="sxs-lookup"><span data-stu-id="87ebb-143">Specifies the name of the database server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87ebb-144">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="87ebb-144">-SubscriptionName</span></span>
<span data-ttu-id="87ebb-145">Specifica il nome dell'abbonamento Azure usato da questo cmdlet per creare il contesto di connessione.</span><span class="sxs-lookup"><span data-stu-id="87ebb-145">Specifies the name of the Azure subscription that this cmdlet uses to create the connection context.</span></span>
<span data-ttu-id="87ebb-146">Se non specifichi un valore per questo parametro, il cmdlet usa l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="87ebb-146">If you do not specify a value for this parameter, the cmdlet uses the current subscription.</span></span>
<span data-ttu-id="87ebb-147">Eseguire il cmdlet Select-AzureSubscription per cambiare l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="87ebb-147">Run the Select-AzureSubscription cmdlet to change the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87ebb-148">-UseSubscription</span><span class="sxs-lookup"><span data-stu-id="87ebb-148">-UseSubscription</span></span>
<span data-ttu-id="87ebb-149">Indica che questo cmdlet usa l'abbonamento Azure per creare il contesto di connessione.</span><span class="sxs-lookup"><span data-stu-id="87ebb-149">Indicates that this cmdlet uses Azure subscription for creating the connection context.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ebb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ebb-150">CommonParameters</span></span>
<span data-ttu-id="87ebb-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87ebb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ebb-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87ebb-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ebb-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87ebb-153">INPUTS</span></span>

## <span data-ttu-id="87ebb-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87ebb-154">OUTPUTS</span></span>

### <span data-ttu-id="87ebb-155">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. IServerDataServiceContext</span><span class="sxs-lookup"><span data-stu-id="87ebb-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span></span>

## <span data-ttu-id="87ebb-156">Note</span><span class="sxs-lookup"><span data-stu-id="87ebb-156">NOTES</span></span>
* <span data-ttu-id="87ebb-157">Se si effettua l'autenticazione senza specificare un dominio e se si usa Windows PowerShell 2,0, il cmdlet Get-Credential restituisce una barra rovesciata ( \\ ) anteposto al nome utente, ad esempio \User.</span><span class="sxs-lookup"><span data-stu-id="87ebb-157">If you authenticate without specifying a domain, and if you use Windows PowerShell 2.0, the Get-Credential cmdlet returns a backslash (\\) prepended to the username, for example, \user.</span></span> <span data-ttu-id="87ebb-158">Windows PowerShell 3,0 non aggiunge la barra rovesciata.</span><span class="sxs-lookup"><span data-stu-id="87ebb-158">Windows PowerShell 3.0 does not add the backslash.</span></span> <span data-ttu-id="87ebb-159">Questa barra rovesciata non viene riconosciuta dal parametro *Credential* del cmdlet **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="87ebb-159">This backslash is not recognized by the *Credential* parameter of the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span> <span data-ttu-id="87ebb-160">Per rimuoverlo, usare comandi simili ai seguenti:</span><span class="sxs-lookup"><span data-stu-id="87ebb-160">To remove it, use commands similar to the following:</span></span>

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## <span data-ttu-id="87ebb-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87ebb-161">RELATED LINKS</span></span>

[<span data-ttu-id="87ebb-162">Cmdlet di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="87ebb-162">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="87ebb-163">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="87ebb-163">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="87ebb-164">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="87ebb-164">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="87ebb-165">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="87ebb-165">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="87ebb-166">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="87ebb-166">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


