---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5312556cb49d02ea901b4cb2526a36f7237f66d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404174"
---
# <span data-ttu-id="4c1bd-101">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="4c1bd-101">New-AzureSqlDatabaseServerContext</span></span>

## <span data-ttu-id="4c1bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="4c1bd-103">Crea un contesto di connessione al server.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-103">Creates a server connection context.</span></span>

## <span data-ttu-id="4c1bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c1bd-104">SYNTAX</span></span>

### <span data-ttu-id="4c1bd-105">ByServerNameWithSqlAuth (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4c1bd-105">ByServerNameWithSqlAuth (Default)</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c1bd-106">ByManageUrlWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="4c1bd-106">ByManageUrlWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4c1bd-107">ByServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="4c1bd-107">ByServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4c1bd-108">ByFullyQualifiedServerNameWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="4c1bd-108">ByFullyQualifiedServerNameWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4c1bd-109">ByFullyQualifiedServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="4c1bd-109">ByFullyQualifiedServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4c1bd-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4c1bd-110">DESCRIPTION</span></span>
<span data-ttu-id="4c1bd-111">Il cmdlet **New-AzureSqlDatabaseServerContext** crea un contesto di connessione del server SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-111">The **New-AzureSqlDatabaseServerContext** cmdlet creates an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="4c1bd-112">Usare SQL Server di autenticazione per creare un contesto di connessione a un server SQL database usando le credenziali specificate.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-112">Use SQL Server authentication to create a connection context to a SQL Database server by using the specified credentials.</span></span>
<span data-ttu-id="4c1bd-113">È possibile specificare il SQL server di database in base al nome, al nome completo o all'URL.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-113">You can specify the SQL Database server by name, by the fully qualified name, or by URL.</span></span>
<span data-ttu-id="4c1bd-114">Per ottenere le credenziali, usare Get-Credential cmdlet di configurazione che richiede di specificare il nome utente e la password.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-114">To obtain a credential, use the Get-Credential cmdlet that prompts you to specify the user name and password.</span></span>

<span data-ttu-id="4c1bd-115">Usare il cmdlet **New-AzureSqlDatabaseServerContext** con l'autenticazione basata su certificato per creare un contesto di connessione al server di database SQL specificato usando i dati di sottoscrizione di Azure specificati.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-115">Use the **New-AzureSqlDatabaseServerContext** cmdlet with certificate based authentication to create a connection context to the specified SQL Database server by using the specified Azure subscription data.</span></span>
<span data-ttu-id="4c1bd-116">È possibile specificare SQL server di database in base al nome o al nome completo.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-116">You can specify SQL Database server by name or by the fully qualified name.</span></span>
<span data-ttu-id="4c1bd-117">È possibile specificare i dati della sottoscrizione come parametro oppure possono essere recuperati dalla sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-117">You can specify the subscription data as a parameter or it can be retrieved from the current Azure subscription.</span></span>
<span data-ttu-id="4c1bd-118">Usare il cmdlet Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx per selezionare la sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-118">Use the Select-AzureSubscriptionhttps://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet to select the current Azure subscription.</span></span>

## <span data-ttu-id="4c1bd-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c1bd-119">EXAMPLES</span></span>

### <span data-ttu-id="4c1bd-120">Esempio 1: Creare un contesto usando l'SQL Server autenticazione</span><span class="sxs-lookup"><span data-stu-id="4c1bd-120">Example 1: Create a context by using SQL Server authentication</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="4c1bd-121">Questo esempio usa l'SQL Server autenticazione a più fattori.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-121">This example uses the SQL Server authentication.</span></span>

<span data-ttu-id="4c1bd-122">Il primo comando richiede le credenziali di amministratore del server e le archivia nella variabile $Credential locale.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-122">The first command prompts you for server administrator credentials, and stores the credentials in the $Credential variable.</span></span>

<span data-ttu-id="4c1bd-123">Il secondo comando si connette al server SQL database denominato lpqd0zbr8y usando $Credential.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-123">The second command connects to the SQL Database server named lpqd0zbr8y by using $Credential.</span></span>

<span data-ttu-id="4c1bd-124">Il comando finale crea un database denominato Database17 nel server che fa parte del contesto in $Context.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-124">The final command creates a database named Database17 on the server that is part of the context in $Context.</span></span>

### <span data-ttu-id="4c1bd-125">Esempio 2: Creare un contesto usando l'autenticazione basata su certificato</span><span class="sxs-lookup"><span data-stu-id="4c1bd-125">Example 2: Create a context by using certificate based authentication</span></span>
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

<span data-ttu-id="4c1bd-126">Questo esempio usa l'autenticazione basata su certificato.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-126">This example uses the certificate based authentication.</span></span>

<span data-ttu-id="4c1bd-127">I primi due comandi assegnano valori alle variabili $SubscriptionId e $Thumbprint variabili.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-127">The first two commands assign values to the $SubscriptionId and $Thumbprint variables.</span></span>

<span data-ttu-id="4c1bd-128">Il terzo comando recupera il certificato identificato dall'impronta digitale in $Thumbprint e lo archivia in $Certificate.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-128">The third command gets the certificate identified by the thumbprint in $Thumbprint, and stores it in $Certificate.</span></span>

<span data-ttu-id="4c1bd-129">Il quarto comando imposta la sottoscrizione su Subscription07 e il quinto comando seleziona la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-129">The fourth command sets the subscription to be Subscription07, and the fifth command selects that subscription.</span></span>

<span data-ttu-id="4c1bd-130">Il comando finale crea un contesto nella sottoscrizione corrente per il server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-130">The final command creates a context in the current subscription for the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="4c1bd-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c1bd-131">PARAMETERS</span></span>

### <span data-ttu-id="4c1bd-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="4c1bd-132">-Credential</span></span>
<span data-ttu-id="4c1bd-133">Specifica un oggetto credenziali che fornisce SQL Server'autenticazione per l'accesso al server.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-133">Specifies a credential object that provides SQL Server authentication for you to access the server.</span></span>

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

### <span data-ttu-id="4c1bd-134">-FullyQualifiedServerName</span><span class="sxs-lookup"><span data-stu-id="4c1bd-134">-FullyQualifiedServerName</span></span>
<span data-ttu-id="4c1bd-135">Specifica il nome di dominio completo (FQDN) per il server di SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-135">Specifies the fully qualified domain name (FQDN) name for the Azure SQL Database server.</span></span>
<span data-ttu-id="4c1bd-136">Ad esempio, Server02.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-136">For example, Server02.database.windows.net.</span></span>

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

### <span data-ttu-id="4c1bd-137">-ManageUrl</span><span class="sxs-lookup"><span data-stu-id="4c1bd-137">-ManageUrl</span></span>
<span data-ttu-id="4c1bd-138">Specifica l'URL che questo cmdlet usa per accedere al portale DatabaseManagement di Azure SQL per il server.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-138">Specifies the URL that this cmdlet uses to access the Azure SQL DatabaseManagement Portal for the server.</span></span>

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

### <span data-ttu-id="4c1bd-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="4c1bd-139">-Profile</span></span>
<span data-ttu-id="4c1bd-140">Specifica il profilo di Azure da cui viene letto questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4c1bd-141">Se non si specifica un profilo, questo cmdlet legge dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4c1bd-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4c1bd-142">-ServerName</span></span>
<span data-ttu-id="4c1bd-143">Specifica il nome del server di database.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-143">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="4c1bd-144">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4c1bd-144">-SubscriptionName</span></span>
<span data-ttu-id="4c1bd-145">Specifica il nome della sottoscrizione di Azure che questo cmdlet usa per creare il contesto di connessione.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-145">Specifies the name of the Azure subscription that this cmdlet uses to create the connection context.</span></span>
<span data-ttu-id="4c1bd-146">Se non si specifica alcun valore per questo parametro, il cmdlet usa la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-146">If you do not specify a value for this parameter, the cmdlet uses the current subscription.</span></span>
<span data-ttu-id="4c1bd-147">Eseguire il cmdlet Select-AzureSubscription per modificare l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-147">Run the Select-AzureSubscription cmdlet to change the current subscription.</span></span>

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

### <span data-ttu-id="4c1bd-148">-UseSubscription</span><span class="sxs-lookup"><span data-stu-id="4c1bd-148">-UseSubscription</span></span>
<span data-ttu-id="4c1bd-149">Indica che questo cmdlet usa la sottoscrizione di Azure per creare il contesto di connessione.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-149">Indicates that this cmdlet uses Azure subscription for creating the connection context.</span></span>

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

### <span data-ttu-id="4c1bd-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c1bd-150">CommonParameters</span></span>
<span data-ttu-id="4c1bd-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c1bd-152">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c1bd-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c1bd-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="4c1bd-153">INPUTS</span></span>

## <span data-ttu-id="4c1bd-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c1bd-154">OUTPUTS</span></span>

### <span data-ttu-id="4c1bd-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span><span class="sxs-lookup"><span data-stu-id="4c1bd-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span></span>

## <span data-ttu-id="4c1bd-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="4c1bd-156">NOTES</span></span>
* <span data-ttu-id="4c1bd-157">Se si esegue l'autenticazione senza specificare un dominio e si usa Windows PowerShell 2.0, il cmdlet Get-Credential restituisce una barra rovesciata ( ) anteposta al nome utente, ad esempio \\ \utente.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-157">If you authenticate without specifying a domain, and if you use Windows PowerShell 2.0, the Get-Credential cmdlet returns a backslash (\\) prepended to the username, for example, \user.</span></span> <span data-ttu-id="4c1bd-158">Windows PowerShell 3.0 non aggiunge la barra rovesciata.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-158">Windows PowerShell 3.0 does not add the backslash.</span></span> <span data-ttu-id="4c1bd-159">Questa barra rovesciata non viene riconosciuta dal parametro *Credential* del cmdlet **New-AzureSqlDatabaseServerContext.**</span><span class="sxs-lookup"><span data-stu-id="4c1bd-159">This backslash is not recognized by the *Credential* parameter of the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span> <span data-ttu-id="4c1bd-160">Per rimuoverla, usare comandi simili ai seguenti:</span><span class="sxs-lookup"><span data-stu-id="4c1bd-160">To remove it, use commands similar to the following:</span></span>

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## <span data-ttu-id="4c1bd-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c1bd-161">RELATED LINKS</span></span>



[<span data-ttu-id="4c1bd-162">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4c1bd-162">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="4c1bd-163">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4c1bd-163">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="4c1bd-164">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4c1bd-164">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="4c1bd-165">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4c1bd-165">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


