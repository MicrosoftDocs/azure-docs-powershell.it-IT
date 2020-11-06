---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 76d5c2fc90b4e0e518aa022a97c6b9ce369715db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518280"
---
# <span data-ttu-id="dfda7-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="dfda7-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="dfda7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dfda7-102">SYNOPSIS</span></span>
<span data-ttu-id="dfda7-103">Viene previsto un amministratore di Azure AD per SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dfda7-103">Provisions an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfda7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfda7-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfda7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfda7-105">DESCRIPTION</span></span>
<span data-ttu-id="dfda7-106">Il cmdlet **set-AzureRmSqlServerActiveDirectoryAdministrator** consente di applicare un amministratore di Azure Active Directory (Azure ad) per il server AzureSQL nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="dfda7-106">The **Set-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

<span data-ttu-id="dfda7-107">È possibile eseguire il provisioning di un solo amministratore alla volta.</span><span class="sxs-lookup"><span data-stu-id="dfda7-107">You can provision only one administrator at a time.</span></span>

<span data-ttu-id="dfda7-108">I membri seguenti di Azure AD possono essere provisionati come amministratore di SQL Server:</span><span class="sxs-lookup"><span data-stu-id="dfda7-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>

- <span data-ttu-id="dfda7-109">Membri nativi di Azure AD</span><span class="sxs-lookup"><span data-stu-id="dfda7-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="dfda7-110">Membri federati di Azure AD</span><span class="sxs-lookup"><span data-stu-id="dfda7-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="dfda7-111">Membri importati da altri annunci di Azure che sono membri nativi o federati</span><span class="sxs-lookup"><span data-stu-id="dfda7-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="dfda7-112">Gruppi di Azure AD creati come gruppi di sicurezza</span><span class="sxs-lookup"><span data-stu-id="dfda7-112">Azure AD groups created as security groups</span></span>

<span data-ttu-id="dfda7-113">Gli account Microsoft, ad esempio quelli nei domini Outlook.com, Hotmail.com o Live.com, non sono supportati come amministratori.</span><span class="sxs-lookup"><span data-stu-id="dfda7-113">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="dfda7-114">Gli altri account Guest, ad esempio quelli presenti nei domini Gmail.com o Yahoo.com, non sono supportati come amministratori.</span><span class="sxs-lookup"><span data-stu-id="dfda7-114">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>

<span data-ttu-id="dfda7-115">Ti consigliamo di eseguire il provisioning di un gruppo di annunci Azure dedicato come amministratore.</span><span class="sxs-lookup"><span data-stu-id="dfda7-115">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="dfda7-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfda7-116">EXAMPLES</span></span>

### <span data-ttu-id="dfda7-117">Esempio 1: eseguire il provisioning di un gruppo di amministratori per un server</span><span class="sxs-lookup"><span data-stu-id="dfda7-117">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="dfda7-118">Questo comando serve un gruppo di amministratori di Azure AD denominato DBA per il server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="dfda7-118">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="dfda7-119">Questo server è associato al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="dfda7-119">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="dfda7-120">Esempio 2: eseguire il provisioning di un utente di amministratore per un server</span><span class="sxs-lookup"><span data-stu-id="dfda7-120">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="dfda7-121">Questo comando serve un utente di Azure AD come amministratore per il server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="dfda7-121">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="dfda7-122">Esempio 3: eseguire il provisioning di un gruppo di amministratori specificando il relativo ID</span><span class="sxs-lookup"><span data-stu-id="dfda7-122">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="dfda7-123">Questo comando serve un gruppo di amministratori di Azure AD denominato DBA per il server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="dfda7-123">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="dfda7-124">Il comando specifica un ID per il parametro *ObjectID* .</span><span class="sxs-lookup"><span data-stu-id="dfda7-124">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="dfda7-125">In questo modo si verifica che il comando abbia esito positivo anche se il nome visualizzato del gruppo non è univoco.</span><span class="sxs-lookup"><span data-stu-id="dfda7-125">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="dfda7-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dfda7-126">PARAMETERS</span></span>

### <span data-ttu-id="dfda7-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dfda7-127">-DisplayName</span></span>
<span data-ttu-id="dfda7-128">Specifica il nome visualizzato dell'amministratore di Azure AD specificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfda7-128">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="dfda7-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dfda7-129">-ObjectId</span></span>
<span data-ttu-id="dfda7-130">Specifica l'ID univoco dell'amministratore di Azure AD che questo cmdlet prevede.</span><span class="sxs-lookup"><span data-stu-id="dfda7-130">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="dfda7-131">Se il nome visualizzato non è univoco, devi specificare un valore per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="dfda7-131">If the display name is not unique, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="dfda7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfda7-132">-ResourceGroupName</span></span>
<span data-ttu-id="dfda7-133">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="dfda7-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="dfda7-134">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="dfda7-134">-ServerName</span></span>
<span data-ttu-id="dfda7-135">Specifica il nome di SQL Server per cui questo cmdlet prevede un amministratore.</span><span class="sxs-lookup"><span data-stu-id="dfda7-135">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="dfda7-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dfda7-136">-Confirm</span></span>
<span data-ttu-id="dfda7-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfda7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfda7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfda7-138">-WhatIf</span></span>
<span data-ttu-id="dfda7-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfda7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfda7-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfda7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfda7-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfda7-141">-DefaultProfile</span></span>
<span data-ttu-id="dfda7-142">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dfda7-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfda7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfda7-143">CommonParameters</span></span>
<span data-ttu-id="dfda7-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfda7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfda7-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfda7-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfda7-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dfda7-146">INPUTS</span></span>

## <span data-ttu-id="dfda7-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfda7-147">OUTPUTS</span></span>

### <span data-ttu-id="dfda7-148">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="dfda7-148">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="dfda7-149">Note</span><span class="sxs-lookup"><span data-stu-id="dfda7-149">NOTES</span></span>

## <span data-ttu-id="dfda7-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfda7-150">RELATED LINKS</span></span>

[<span data-ttu-id="dfda7-151">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="dfda7-151">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="dfda7-152">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="dfda7-152">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="dfda7-153">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="dfda7-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


