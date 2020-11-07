---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
ms.openlocfilehash: 24249be1d2b5b203a207d72ebd29ec691a90c39a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857218"
---
# <span data-ttu-id="35e7b-101">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="35e7b-101">Set-AzSqlServer</span></span>

## <span data-ttu-id="35e7b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="35e7b-103">Modifica le proprietà di un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="35e7b-103">Modifies properties of a SQL Database server.</span></span>

## <span data-ttu-id="35e7b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35e7b-104">SYNTAX</span></span>

```
Set-AzSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35e7b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35e7b-105">DESCRIPTION</span></span>
<span data-ttu-id="35e7b-106">Il cmdlet **set-AzSqlServer** modifica le proprietà di un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="35e7b-106">The **Set-AzSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="35e7b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35e7b-107">EXAMPLES</span></span>

### <span data-ttu-id="35e7b-108">Esempio 1: reimpostare la password dell'amministratore</span><span class="sxs-lookup"><span data-stu-id="35e7b-108">Example 1: Reset the administrator password</span></span>
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

<span data-ttu-id="35e7b-109">Questo comando Reimposta la password di amministratore nel server AzureSQL denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="35e7b-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="35e7b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35e7b-110">PARAMETERS</span></span>

### <span data-ttu-id="35e7b-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="35e7b-111">-AssignIdentity</span></span>
<span data-ttu-id="35e7b-112">Genera e assegna un'identità di Azure Active Directory per questo server per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="35e7b-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="35e7b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35e7b-113">-DefaultProfile</span></span>
<span data-ttu-id="35e7b-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="35e7b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35e7b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="35e7b-115">-Force</span></span>
<span data-ttu-id="35e7b-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="35e7b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="35e7b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35e7b-117">-ResourceGroupName</span></span>
<span data-ttu-id="35e7b-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="35e7b-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="35e7b-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="35e7b-119">-ServerName</span></span>
<span data-ttu-id="35e7b-120">Specifica il nome del server che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="35e7b-120">Specifies the name of the server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="35e7b-121">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="35e7b-121">-ServerVersion</span></span>
<span data-ttu-id="35e7b-122">Specifica la versione a cui questo cmdlet modifica il server.</span><span class="sxs-lookup"><span data-stu-id="35e7b-122">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="35e7b-123">I valori accettabili per questo parametro sono: 2,0 e 12,0.</span><span class="sxs-lookup"><span data-stu-id="35e7b-123">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="35e7b-124">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="35e7b-124">-SqlAdministratorPassword</span></span>
<span data-ttu-id="35e7b-125">Specifica una nuova password, come **SecureString** , per l'amministratore del server di database.</span><span class="sxs-lookup"><span data-stu-id="35e7b-125">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="35e7b-126">Per ottenere una **SecureString** , usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="35e7b-126">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="35e7b-127">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="35e7b-127">For more information, type `Get-Help
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

### <span data-ttu-id="35e7b-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="35e7b-128">-Tags</span></span>
<span data-ttu-id="35e7b-129">Specifica un dizionario di tag che questo cmdlet associa al server.</span><span class="sxs-lookup"><span data-stu-id="35e7b-129">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="35e7b-130">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="35e7b-130">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="35e7b-131">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="35e7b-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="35e7b-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="35e7b-132">-Confirm</span></span>
<span data-ttu-id="35e7b-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35e7b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35e7b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35e7b-134">-WhatIf</span></span>
<span data-ttu-id="35e7b-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35e7b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35e7b-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35e7b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35e7b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35e7b-137">CommonParameters</span></span>
<span data-ttu-id="35e7b-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35e7b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35e7b-139">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35e7b-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35e7b-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35e7b-140">INPUTS</span></span>

### <span data-ttu-id="35e7b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="35e7b-141">System.String</span></span>

## <span data-ttu-id="35e7b-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35e7b-142">OUTPUTS</span></span>

### <span data-ttu-id="35e7b-143">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="35e7b-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="35e7b-144">Note</span><span class="sxs-lookup"><span data-stu-id="35e7b-144">NOTES</span></span>

## <span data-ttu-id="35e7b-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35e7b-145">RELATED LINKS</span></span>

[<span data-ttu-id="35e7b-146">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="35e7b-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
