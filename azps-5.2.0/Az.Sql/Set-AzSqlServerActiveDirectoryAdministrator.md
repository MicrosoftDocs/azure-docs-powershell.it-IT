---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: d450fa7795a530106a72180210d9cb133c7d3047
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355087"
---
# <span data-ttu-id="47074-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="47074-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="47074-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47074-102">SYNOPSIS</span></span>
<span data-ttu-id="47074-103">Viene previsto un amministratore di Azure AD per SQL Server.</span><span class="sxs-lookup"><span data-stu-id="47074-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="47074-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47074-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47074-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47074-105">DESCRIPTION</span></span>
<span data-ttu-id="47074-106">Il cmdlet **set-AzSqlServerActiveDirectoryAdministrator** consente di applicare un amministratore di Azure Active Directory (Azure ad) per il server AzureSQL nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="47074-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="47074-107">È possibile eseguire il provisioning di un solo amministratore alla volta.</span><span class="sxs-lookup"><span data-stu-id="47074-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="47074-108">I membri seguenti di Azure AD possono essere provisionati come amministratore di SQL Server:</span><span class="sxs-lookup"><span data-stu-id="47074-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="47074-109">Membri nativi di Azure AD</span><span class="sxs-lookup"><span data-stu-id="47074-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="47074-110">Membri federati di Azure AD</span><span class="sxs-lookup"><span data-stu-id="47074-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="47074-111">Membri importati da altri annunci di Azure che sono membri nativi o federati</span><span class="sxs-lookup"><span data-stu-id="47074-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="47074-112">I gruppi di Azure AD creati come gruppi di sicurezza gli account Microsoft, ad esempio quelli nei domini Outlook.com, Hotmail.com o Live.com, non sono supportati come amministratori.</span><span class="sxs-lookup"><span data-stu-id="47074-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="47074-113">Gli altri account Guest, ad esempio quelli presenti nei domini Gmail.com o Yahoo.com, non sono supportati come amministratori.</span><span class="sxs-lookup"><span data-stu-id="47074-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="47074-114">Ti consigliamo di eseguire il provisioning di un gruppo di annunci Azure dedicato come amministratore.</span><span class="sxs-lookup"><span data-stu-id="47074-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="47074-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47074-115">EXAMPLES</span></span>

### <span data-ttu-id="47074-116">Esempio 1: eseguire il provisioning di un gruppo di amministratori per un server</span><span class="sxs-lookup"><span data-stu-id="47074-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="47074-117">Questo comando serve un gruppo di amministratori di Azure AD denominato DBA per il server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="47074-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="47074-118">Questo server è associato al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="47074-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="47074-119">Esempio 2: eseguire il provisioning di un utente di amministratore per un server</span><span class="sxs-lookup"><span data-stu-id="47074-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

<span data-ttu-id="47074-120">Questo comando serve un utente di Azure AD come amministratore per il server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="47074-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="47074-121">Esempio 3: eseguire il provisioning di un gruppo di amministratori specificando il relativo ID</span><span class="sxs-lookup"><span data-stu-id="47074-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="47074-122">Questo comando serve un gruppo di amministratori di Azure AD denominato DBA per il server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="47074-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="47074-123">Il comando specifica un ID per il parametro *ObjectID* .</span><span class="sxs-lookup"><span data-stu-id="47074-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="47074-124">In questo modo si verifica che il comando abbia esito positivo anche se il nome visualizzato del gruppo non è univoco.</span><span class="sxs-lookup"><span data-stu-id="47074-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="47074-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47074-125">PARAMETERS</span></span>

### <span data-ttu-id="47074-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47074-126">-DefaultProfile</span></span>
<span data-ttu-id="47074-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="47074-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47074-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="47074-128">-DisplayName</span></span>
<span data-ttu-id="47074-129">Specifica il nome visualizzato dell'amministratore di Azure AD specificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47074-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47074-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="47074-130">-ObjectId</span></span>
<span data-ttu-id="47074-131">Specifica l'ID univoco dell'amministratore di Azure AD che questo cmdlet prevede.</span><span class="sxs-lookup"><span data-stu-id="47074-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="47074-132">Se il nome visualizzato non è univoco, devi specificare un valore per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="47074-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47074-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47074-133">-ResourceGroupName</span></span>
<span data-ttu-id="47074-134">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="47074-134">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="47074-135">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="47074-135">-ServerName</span></span>
<span data-ttu-id="47074-136">Specifica il nome di SQL Server per cui questo cmdlet prevede un amministratore.</span><span class="sxs-lookup"><span data-stu-id="47074-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47074-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="47074-137">-Confirm</span></span>
<span data-ttu-id="47074-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47074-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47074-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47074-139">-WhatIf</span></span>
<span data-ttu-id="47074-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47074-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47074-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47074-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47074-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47074-142">CommonParameters</span></span>
<span data-ttu-id="47074-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47074-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47074-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47074-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47074-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47074-145">INPUTS</span></span>

### <span data-ttu-id="47074-146">System. String</span><span class="sxs-lookup"><span data-stu-id="47074-146">System.String</span></span>

### <span data-ttu-id="47074-147">System. Guid</span><span class="sxs-lookup"><span data-stu-id="47074-147">System.Guid</span></span>

## <span data-ttu-id="47074-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47074-148">OUTPUTS</span></span>

### <span data-ttu-id="47074-149">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="47074-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="47074-150">Note</span><span class="sxs-lookup"><span data-stu-id="47074-150">NOTES</span></span>

## <span data-ttu-id="47074-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47074-151">RELATED LINKS</span></span>

[<span data-ttu-id="47074-152">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="47074-152">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="47074-153">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="47074-153">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="47074-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="47074-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="47074-155">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="47074-155">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


