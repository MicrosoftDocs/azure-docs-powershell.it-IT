---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: a754ff33cba0bcf6324be0eb947b592b8fd4a622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686556"
---
# <span data-ttu-id="d2ed0-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="d2ed0-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="d2ed0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ed0-103">Crea un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2ed0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2ed0-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2ed0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2ed0-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ed0-106">Il cmdlet **New-AzureRmSqlServer** crea un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="d2ed0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2ed0-107">EXAMPLES</span></span>

### <span data-ttu-id="d2ed0-108">Esempio 1: creare un nuovo server di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="d2ed0-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="d2ed0-109">Questo comando crea un server di database SQL di una versione 12 Azure.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="d2ed0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2ed0-110">PARAMETERS</span></span>

### <span data-ttu-id="d2ed0-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d2ed0-111">-AssignIdentity</span></span>
<span data-ttu-id="d2ed0-112">Genera e assegna un'identità di Azure Active Directory per questo server per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="d2ed0-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d2ed0-113">-Location</span></span>
<span data-ttu-id="d2ed0-114">Specifica la posizione del centro dati in cui questo cmdlet crea il server.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-114">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="d2ed0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ed0-115">-ResourceGroupName</span></span>
<span data-ttu-id="d2ed0-116">Specifica il nome del gruppo di risorse a cui questo cmdlet assegna il server.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-116">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="d2ed0-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="d2ed0-117">-ServerName</span></span>
<span data-ttu-id="d2ed0-118">Specifica il nome del nuovo server.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-118">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="d2ed0-119">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="d2ed0-119">-ServerVersion</span></span>
<span data-ttu-id="d2ed0-120">Specifica la versione del nuovo server.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-120">Specifies the version of the new server.</span></span> <span data-ttu-id="d2ed0-121">I valori accettabili per questo parametro sono: 2,0 e 12,0.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-121">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

<span data-ttu-id="d2ed0-122">Specificare 2,0 per creare un server versione 11 o 12,0 per creare un server versione 12.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-122">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="d2ed0-123">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="d2ed0-123">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="d2ed0-124">Specifica le credenziali di amministratore del server di database SQL per il nuovo server.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-124">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="d2ed0-125">Per ottenere un oggetto **PSCredential** , usa il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-125">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="d2ed0-126">Per altre informazioni, digitare `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="d2ed0-126">For more information, type `Get-Help
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

### <span data-ttu-id="d2ed0-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="d2ed0-127">-Tags</span></span>
<span data-ttu-id="d2ed0-128">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d2ed0-129">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="d2ed0-129">For example:</span></span>

<span data-ttu-id="d2ed0-130">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d2ed0-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d2ed0-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d2ed0-131">-Confirm</span></span>
<span data-ttu-id="d2ed0-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2ed0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2ed0-133">-WhatIf</span></span>
<span data-ttu-id="d2ed0-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2ed0-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2ed0-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ed0-136">-DefaultProfile</span></span>
<span data-ttu-id="d2ed0-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ed0-138">CommonParameters</span></span>
<span data-ttu-id="d2ed0-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ed0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ed0-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ed0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ed0-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2ed0-141">INPUTS</span></span>

## <span data-ttu-id="d2ed0-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2ed0-142">OUTPUTS</span></span>

### <span data-ttu-id="d2ed0-143">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="d2ed0-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="d2ed0-144">Note</span><span class="sxs-lookup"><span data-stu-id="d2ed0-144">NOTES</span></span>

## <span data-ttu-id="d2ed0-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2ed0-145">RELATED LINKS</span></span>

[<span data-ttu-id="d2ed0-146">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="d2ed0-146">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="d2ed0-147">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="d2ed0-147">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="d2ed0-148">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="d2ed0-148">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="d2ed0-149">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d2ed0-149">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="d2ed0-150">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="d2ed0-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
