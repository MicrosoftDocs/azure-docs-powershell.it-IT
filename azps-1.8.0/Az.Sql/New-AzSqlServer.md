---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: 0d5eb08c938fe17e4270cd66038a738341937cb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676843"
---
# <span data-ttu-id="59434-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="59434-101">New-AzSqlServer</span></span>

## <span data-ttu-id="59434-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59434-102">SYNOPSIS</span></span>
<span data-ttu-id="59434-103">Crea un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="59434-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="59434-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59434-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59434-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59434-105">DESCRIPTION</span></span>
<span data-ttu-id="59434-106">Il cmdlet **New-AzSqlServer** crea un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="59434-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="59434-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59434-107">EXAMPLES</span></span>

### <span data-ttu-id="59434-108">Esempio 1: creare un nuovo server di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="59434-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="59434-109">Questo comando crea un server di database SQL di una versione 12 Azure.</span><span class="sxs-lookup"><span data-stu-id="59434-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="59434-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59434-110">PARAMETERS</span></span>

### <span data-ttu-id="59434-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59434-111">-AsJob</span></span>
<span data-ttu-id="59434-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="59434-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59434-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="59434-113">-AssignIdentity</span></span>
<span data-ttu-id="59434-114">Genera e assegna un'identità di Azure Active Directory per questo server per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="59434-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="59434-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59434-115">-DefaultProfile</span></span>
<span data-ttu-id="59434-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="59434-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59434-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="59434-117">-Location</span></span>
<span data-ttu-id="59434-118">Specifica la posizione del centro dati in cui questo cmdlet crea il server.</span><span class="sxs-lookup"><span data-stu-id="59434-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="59434-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59434-119">-ResourceGroupName</span></span>
<span data-ttu-id="59434-120">Specifica il nome del gruppo di risorse a cui questo cmdlet assegna il server.</span><span class="sxs-lookup"><span data-stu-id="59434-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="59434-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="59434-121">-ServerName</span></span>
<span data-ttu-id="59434-122">Specifica il nome del nuovo server.</span><span class="sxs-lookup"><span data-stu-id="59434-122">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="59434-123">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="59434-123">-ServerVersion</span></span>
<span data-ttu-id="59434-124">Specifica la versione del nuovo server.</span><span class="sxs-lookup"><span data-stu-id="59434-124">Specifies the version of the new server.</span></span> <span data-ttu-id="59434-125">I valori accettabili per questo parametro sono: 2,0 e 12,0.</span><span class="sxs-lookup"><span data-stu-id="59434-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="59434-126">Specificare 2,0 per creare un server versione 11 o 12,0 per creare un server versione 12.</span><span class="sxs-lookup"><span data-stu-id="59434-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="59434-127">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="59434-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="59434-128">Specifica le credenziali di amministratore del server di database SQL per il nuovo server.</span><span class="sxs-lookup"><span data-stu-id="59434-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="59434-129">Per ottenere un oggetto **PSCredential** , usa il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="59434-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="59434-130">Per altre informazioni, digitare `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="59434-130">For more information, type `Get-Help
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

### <span data-ttu-id="59434-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="59434-131">-Tags</span></span>
<span data-ttu-id="59434-132">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="59434-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="59434-133">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="59434-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="59434-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="59434-134">-Confirm</span></span>
<span data-ttu-id="59434-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59434-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59434-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59434-136">-WhatIf</span></span>
<span data-ttu-id="59434-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59434-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59434-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59434-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59434-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59434-139">CommonParameters</span></span>
<span data-ttu-id="59434-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59434-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59434-141">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59434-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59434-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59434-142">INPUTS</span></span>

### <span data-ttu-id="59434-143">System. String</span><span class="sxs-lookup"><span data-stu-id="59434-143">System.String</span></span>

## <span data-ttu-id="59434-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59434-144">OUTPUTS</span></span>

### <span data-ttu-id="59434-145">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="59434-145">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="59434-146">Note</span><span class="sxs-lookup"><span data-stu-id="59434-146">NOTES</span></span>

## <span data-ttu-id="59434-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59434-147">RELATED LINKS</span></span>

[<span data-ttu-id="59434-148">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="59434-148">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="59434-149">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="59434-149">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="59434-150">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="59434-150">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="59434-151">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="59434-151">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="59434-152">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="59434-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
