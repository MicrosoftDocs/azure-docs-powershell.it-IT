---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: 6b9fa4c7fff426f9af19484c7576b9dee341a82e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686292"
---
# <span data-ttu-id="b149c-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b149c-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="b149c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b149c-102">SYNOPSIS</span></span>
<span data-ttu-id="b149c-103">Crea un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="b149c-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b149c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b149c-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b149c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b149c-105">DESCRIPTION</span></span>
<span data-ttu-id="b149c-106">Il cmdlet **New-AzureRmSqlServer** crea un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b149c-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="b149c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b149c-107">EXAMPLES</span></span>

### <span data-ttu-id="b149c-108">Esempio 1: creare un nuovo server di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="b149c-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="b149c-109">Questo comando crea un server di database SQL di una versione 12 Azure.</span><span class="sxs-lookup"><span data-stu-id="b149c-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="b149c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b149c-110">PARAMETERS</span></span>

### <span data-ttu-id="b149c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b149c-111">-AsJob</span></span>
<span data-ttu-id="b149c-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b149c-112">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="b149c-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b149c-113">-AssignIdentity</span></span>
<span data-ttu-id="b149c-114">Genera e assegna un'identità di Azure Active Directory per questo server per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="b149c-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="b149c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b149c-115">-DefaultProfile</span></span>
<span data-ttu-id="b149c-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b149c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b149c-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b149c-117">-Location</span></span>
<span data-ttu-id="b149c-118">Specifica la posizione del centro dati in cui questo cmdlet crea il server.</span><span class="sxs-lookup"><span data-stu-id="b149c-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b149c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b149c-119">-ResourceGroupName</span></span>
<span data-ttu-id="b149c-120">Specifica il nome del gruppo di risorse a cui questo cmdlet assegna il server.</span><span class="sxs-lookup"><span data-stu-id="b149c-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b149c-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b149c-121">-ServerName</span></span>
<span data-ttu-id="b149c-122">Specifica il nome del nuovo server.</span><span class="sxs-lookup"><span data-stu-id="b149c-122">Specifies the name of the new server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b149c-123">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b149c-123">-ServerVersion</span></span>
<span data-ttu-id="b149c-124">Specifica la versione del nuovo server.</span><span class="sxs-lookup"><span data-stu-id="b149c-124">Specifies the version of the new server.</span></span> <span data-ttu-id="b149c-125">I valori accettabili per questo parametro sono: 2,0 e 12,0.</span><span class="sxs-lookup"><span data-stu-id="b149c-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

<span data-ttu-id="b149c-126">Specificare 2,0 per creare un server versione 11 o 12,0 per creare un server versione 12.</span><span class="sxs-lookup"><span data-stu-id="b149c-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="b149c-127">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="b149c-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="b149c-128">Specifica le credenziali di amministratore del server di database SQL per il nuovo server.</span><span class="sxs-lookup"><span data-stu-id="b149c-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="b149c-129">Per ottenere un oggetto **PSCredential** , usa il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="b149c-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="b149c-130">Per altre informazioni, digitare `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="b149c-130">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b149c-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="b149c-131">-Tags</span></span>
<span data-ttu-id="b149c-132">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b149c-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b149c-133">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="b149c-133">For example:</span></span>

<span data-ttu-id="b149c-134">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b149c-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b149c-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b149c-135">-Confirm</span></span>
<span data-ttu-id="b149c-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b149c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b149c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b149c-137">-WhatIf</span></span>
<span data-ttu-id="b149c-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b149c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b149c-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b149c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b149c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b149c-140">CommonParameters</span></span>
<span data-ttu-id="b149c-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b149c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b149c-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b149c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b149c-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b149c-143">INPUTS</span></span>

### <span data-ttu-id="b149c-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b149c-144">None</span></span>
<span data-ttu-id="b149c-145">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b149c-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b149c-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b149c-146">OUTPUTS</span></span>

### <span data-ttu-id="b149c-147">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="b149c-147">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="b149c-148">Note</span><span class="sxs-lookup"><span data-stu-id="b149c-148">NOTES</span></span>

## <span data-ttu-id="b149c-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b149c-149">RELATED LINKS</span></span>

[<span data-ttu-id="b149c-150">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b149c-150">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="b149c-151">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b149c-151">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="b149c-152">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b149c-152">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="b149c-153">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b149c-153">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="b149c-154">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="b149c-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
