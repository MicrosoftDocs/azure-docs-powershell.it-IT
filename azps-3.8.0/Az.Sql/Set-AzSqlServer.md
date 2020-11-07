---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
ms.openlocfilehash: f408edfa0bcdff88fe7577a7cdb6549dcd722dc2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864346"
---
# <span data-ttu-id="f673c-101">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="f673c-101">Set-AzSqlServer</span></span>

## <span data-ttu-id="f673c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f673c-102">SYNOPSIS</span></span>
<span data-ttu-id="f673c-103">Modifica le proprietà di un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="f673c-103">Modifies properties of a SQL Database server.</span></span>

## <span data-ttu-id="f673c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f673c-104">SYNTAX</span></span>

```
Set-AzSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-MinimalTlsVersion <String>] [-PublicNetworkAccess <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f673c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f673c-105">DESCRIPTION</span></span>
<span data-ttu-id="f673c-106">Il cmdlet **set-AzSqlServer** modifica le proprietà di un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="f673c-106">The **Set-AzSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="f673c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f673c-107">EXAMPLES</span></span>

### <span data-ttu-id="f673c-108">Esempio 1: reimpostare la password dell'amministratore</span><span class="sxs-lookup"><span data-stu-id="f673c-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="f673c-109">Questo comando Reimposta la password di amministratore nel server AzureSQL denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="f673c-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="f673c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f673c-110">PARAMETERS</span></span>

### <span data-ttu-id="f673c-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f673c-111">-AssignIdentity</span></span>
<span data-ttu-id="f673c-112">Genera e assegna un'identità di Azure Active Directory per questo server per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f673c-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="f673c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f673c-113">-DefaultProfile</span></span>
<span data-ttu-id="f673c-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f673c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f673c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f673c-115">-Force</span></span>
<span data-ttu-id="f673c-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f673c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f673c-117">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="f673c-117">-PublicNetworkAccess</span></span>
<span data-ttu-id="f673c-118">Prende un contrassegno, abilitato/disabilitato, per specificare se l'accesso alla rete pubblica al server è consentito o meno.</span><span class="sxs-lookup"><span data-stu-id="f673c-118">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="f673c-119">Quando è disabilitata, solo le connessioni effettuate tramite collegamenti privati possono raggiungere il server.</span><span class="sxs-lookup"><span data-stu-id="f673c-119">When disabled, only connections made through Private Links can reach this server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f673c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f673c-120">-ResourceGroupName</span></span>
<span data-ttu-id="f673c-121">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="f673c-121">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f673c-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="f673c-122">-ServerName</span></span>
<span data-ttu-id="f673c-123">Specifica il nome del server che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="f673c-123">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f673c-124">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="f673c-124">-ServerVersion</span></span>
<span data-ttu-id="f673c-125">Specifica la versione a cui questo cmdlet modifica il server.</span><span class="sxs-lookup"><span data-stu-id="f673c-125">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="f673c-126">I valori accettabili per questo parametro sono: 2,0 e 12,0.</span><span class="sxs-lookup"><span data-stu-id="f673c-126">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f673c-127">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="f673c-127">-SqlAdministratorPassword</span></span>
<span data-ttu-id="f673c-128">Specifica una nuova password, come **SecureString** , per l'amministratore del server di database.</span><span class="sxs-lookup"><span data-stu-id="f673c-128">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="f673c-129">Per ottenere una **SecureString** , usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="f673c-129">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="f673c-130">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="f673c-130">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f673c-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="f673c-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="f673c-132">Versione TLS minima da applicare per SQL Server</span><span class="sxs-lookup"><span data-stu-id="f673c-132">The minimal TLS version to enforce for Sql Server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f673c-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="f673c-133">-Tags</span></span>
<span data-ttu-id="f673c-134">Specifica un dizionario di tag che questo cmdlet associa al server.</span><span class="sxs-lookup"><span data-stu-id="f673c-134">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="f673c-135">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="f673c-135">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="f673c-136">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f673c-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f673c-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f673c-137">-Confirm</span></span>
<span data-ttu-id="f673c-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f673c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f673c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f673c-139">-WhatIf</span></span>
<span data-ttu-id="f673c-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f673c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f673c-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f673c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f673c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f673c-142">CommonParameters</span></span>
<span data-ttu-id="f673c-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f673c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f673c-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f673c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f673c-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f673c-145">INPUTS</span></span>

### <span data-ttu-id="f673c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f673c-146">System.String</span></span>

## <span data-ttu-id="f673c-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f673c-147">OUTPUTS</span></span>

### <span data-ttu-id="f673c-148">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="f673c-148">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="f673c-149">Note</span><span class="sxs-lookup"><span data-stu-id="f673c-149">NOTES</span></span>

## <span data-ttu-id="f673c-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f673c-150">RELATED LINKS</span></span>

[<span data-ttu-id="f673c-151">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="f673c-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
