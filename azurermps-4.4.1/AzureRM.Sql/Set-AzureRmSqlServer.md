---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
ms.openlocfilehash: 9eb0e0503d1a7a7b71cac8f9f71a7c2f18847bca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512800"
---
# <span data-ttu-id="24609-101">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="24609-101">Set-AzureRmSqlServer</span></span>

## <span data-ttu-id="24609-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24609-102">SYNOPSIS</span></span>
<span data-ttu-id="24609-103">Modifica le proprietà di un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="24609-103">Modifies properties of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24609-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24609-104">SYNTAX</span></span>

```
Set-AzureRmSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24609-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24609-105">DESCRIPTION</span></span>
<span data-ttu-id="24609-106">Il cmdlet **set-AzureRmSqlServer** modifica le proprietà di un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="24609-106">The **Set-AzureRmSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="24609-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24609-107">EXAMPLES</span></span>

### <span data-ttu-id="24609-108">Esempio 1: reimpostare la password dell'amministratore</span><span class="sxs-lookup"><span data-stu-id="24609-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="24609-109">Questo comando Reimposta la password di amministratore nel server AzureSQL denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="24609-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="24609-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24609-110">PARAMETERS</span></span>

### <span data-ttu-id="24609-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="24609-111">-AssignIdentity</span></span>
<span data-ttu-id="24609-112">Genera e assegna un'identità di Azure Active Directory per questo server per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="24609-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="24609-113">-Force</span><span class="sxs-lookup"><span data-stu-id="24609-113">-Force</span></span>
<span data-ttu-id="24609-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="24609-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="24609-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24609-115">-ResourceGroupName</span></span>
<span data-ttu-id="24609-116">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="24609-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="24609-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="24609-117">-ServerName</span></span>
<span data-ttu-id="24609-118">Specifica il nome del server che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="24609-118">Specifies the name of the server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="24609-119">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="24609-119">-ServerVersion</span></span>
<span data-ttu-id="24609-120">Specifica la versione a cui questo cmdlet modifica il server.</span><span class="sxs-lookup"><span data-stu-id="24609-120">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="24609-121">I valori accettabili per questo parametro sono: 2,0 e 12,0.</span><span class="sxs-lookup"><span data-stu-id="24609-121">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="24609-122">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="24609-122">-SqlAdministratorPassword</span></span>
<span data-ttu-id="24609-123">Specifica una nuova password, come **SecureString** , per l'amministratore del server di database.</span><span class="sxs-lookup"><span data-stu-id="24609-123">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="24609-124">Per ottenere una **SecureString** , usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="24609-124">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="24609-125">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="24609-125">For more information, type `Get-Help
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

### <span data-ttu-id="24609-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="24609-126">-Tags</span></span>
<span data-ttu-id="24609-127">Specifica un dizionario di tag che questo cmdlet associa al server.</span><span class="sxs-lookup"><span data-stu-id="24609-127">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="24609-128">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="24609-128">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="24609-129">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="24609-129">For example:</span></span>

<span data-ttu-id="24609-130">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="24609-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="24609-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="24609-131">-Confirm</span></span>
<span data-ttu-id="24609-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24609-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24609-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24609-133">-WhatIf</span></span>
<span data-ttu-id="24609-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24609-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24609-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24609-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24609-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24609-136">-DefaultProfile</span></span>
<span data-ttu-id="24609-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24609-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24609-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24609-138">CommonParameters</span></span>
<span data-ttu-id="24609-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24609-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24609-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24609-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24609-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24609-141">INPUTS</span></span>

## <span data-ttu-id="24609-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24609-142">OUTPUTS</span></span>

### <span data-ttu-id="24609-143">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="24609-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="24609-144">Note</span><span class="sxs-lookup"><span data-stu-id="24609-144">NOTES</span></span>

## <span data-ttu-id="24609-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24609-145">RELATED LINKS</span></span>

[<span data-ttu-id="24609-146">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="24609-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
