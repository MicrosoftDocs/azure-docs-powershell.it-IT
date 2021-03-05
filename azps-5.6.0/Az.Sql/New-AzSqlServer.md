---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: 182dfddf4acc294b2afb994b13db4f1644d95aab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977661"
---
# <span data-ttu-id="72816-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="72816-101">New-AzSqlServer</span></span>

## <span data-ttu-id="72816-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72816-102">SYNOPSIS</span></span>
<span data-ttu-id="72816-103">Crea un SQL server di database.</span><span class="sxs-lookup"><span data-stu-id="72816-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="72816-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72816-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-PublicNetworkAccess <String>]
 [-MinimalTlsVersion <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72816-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="72816-105">DESCRIPTION</span></span>
<span data-ttu-id="72816-106">Il cmdlet **New-AzSqlServer** crea un server di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="72816-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="72816-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72816-107">EXAMPLES</span></span>

### <span data-ttu-id="72816-108">Esempio 1: Creare un nuovo server di SQL Azure</span><span class="sxs-lookup"><span data-stu-id="72816-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="72816-109">Questo comando crea una versione 12 di Azure SQL server di database.</span><span class="sxs-lookup"><span data-stu-id="72816-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="72816-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72816-110">PARAMETERS</span></span>

### <span data-ttu-id="72816-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72816-111">-AsJob</span></span>
<span data-ttu-id="72816-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="72816-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="72816-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="72816-113">-AssignIdentity</span></span>
<span data-ttu-id="72816-114">Generare e assegnare un'identità di Azure Active Directory per questo server per l'uso con servizi di gestione delle chiavi come Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="72816-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="72816-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72816-115">-DefaultProfile</span></span>
<span data-ttu-id="72816-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="72816-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72816-117">-Location</span><span class="sxs-lookup"><span data-stu-id="72816-117">-Location</span></span>
<span data-ttu-id="72816-118">Specifica la posizione del data center in cui questo cmdlet crea il server.</span><span class="sxs-lookup"><span data-stu-id="72816-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="72816-119">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="72816-119">-MinimalTlsVersion</span></span>
<span data-ttu-id="72816-120">Versione minima di TLS da applicare a Sql Server</span><span class="sxs-lookup"><span data-stu-id="72816-120">The minimal TLS version to enforce for Sql Server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72816-121">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="72816-121">-PublicNetworkAccess</span></span>
<span data-ttu-id="72816-122">Accetta un contrassegno, abilitato/disabilitato, per specificare se l'accesso alla rete pubblica al server è consentito o meno.</span><span class="sxs-lookup"><span data-stu-id="72816-122">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="72816-123">Se disabilitata, solo le connessioni effettuate tramite collegamenti privati possono raggiungere questo server.</span><span class="sxs-lookup"><span data-stu-id="72816-123">When disabled, only connections made through Private Links can reach this server.</span></span>

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

### <span data-ttu-id="72816-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72816-124">-ResourceGroupName</span></span>
<span data-ttu-id="72816-125">Specifica il nome del gruppo di risorse a cui il cmdlet assegna il server.</span><span class="sxs-lookup"><span data-stu-id="72816-125">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="72816-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72816-126">-ServerName</span></span>
<span data-ttu-id="72816-127">Specifica il nome del nuovo server.</span><span class="sxs-lookup"><span data-stu-id="72816-127">Specifies the name of the new server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72816-128">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="72816-128">-ServerVersion</span></span>
<span data-ttu-id="72816-129">Specifica la versione del nuovo server.</span><span class="sxs-lookup"><span data-stu-id="72816-129">Specifies the version of the new server.</span></span> <span data-ttu-id="72816-130">I valori accettabili per questo parametro sono: 2.0 e 12.0.</span><span class="sxs-lookup"><span data-stu-id="72816-130">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="72816-131">Specificare 2.0 per creare un server 11 o 12.0 per creare un server versione 12.</span><span class="sxs-lookup"><span data-stu-id="72816-131">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="72816-132">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="72816-132">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="72816-133">Specifica le credenziali SQL amministratore del server di database per il nuovo server.</span><span class="sxs-lookup"><span data-stu-id="72816-133">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="72816-134">Per ottenere un **oggetto PSCredential,** usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="72816-134">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="72816-135">Per altre informazioni, digitare `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="72816-135">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72816-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="72816-136">-Tags</span></span>
<span data-ttu-id="72816-137">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="72816-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="72816-138">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="72816-138">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="72816-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72816-139">-Confirm</span></span>
<span data-ttu-id="72816-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72816-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72816-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72816-141">-WhatIf</span></span>
<span data-ttu-id="72816-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72816-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72816-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72816-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72816-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72816-144">CommonParameters</span></span>
<span data-ttu-id="72816-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72816-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72816-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="72816-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72816-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="72816-147">INPUTS</span></span>

### <span data-ttu-id="72816-148">System.String</span><span class="sxs-lookup"><span data-stu-id="72816-148">System.String</span></span>

## <span data-ttu-id="72816-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72816-149">OUTPUTS</span></span>

### <span data-ttu-id="72816-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="72816-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="72816-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="72816-151">NOTES</span></span>

## <span data-ttu-id="72816-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72816-152">RELATED LINKS</span></span>

[<span data-ttu-id="72816-153">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="72816-153">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="72816-154">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="72816-154">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="72816-155">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="72816-155">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="72816-156">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="72816-156">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="72816-157">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="72816-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
