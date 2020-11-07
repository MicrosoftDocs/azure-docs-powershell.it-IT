---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 0dd74526adbc821fe3e256d2fb59850d5bf72943
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686671"
---
# <span data-ttu-id="e1b56-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e1b56-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="e1b56-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1b56-102">SYNOPSIS</span></span>
<span data-ttu-id="e1b56-103">Rimuove un amministratore di Azure AD per SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e1b56-103">Removes an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1b56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1b56-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1b56-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1b56-105">DESCRIPTION</span></span>
<span data-ttu-id="e1b56-106">Il cmdlet **Remove-AzureRmSqlServerActiveDirectoryAdministrator** rimuove un amministratore di Azure Active Directory (Azure ad) per il server AzureSQL nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e1b56-106">The **Remove-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="e1b56-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1b56-107">EXAMPLES</span></span>

### <span data-ttu-id="e1b56-108">Esempio 1: rimuovere un amministratore</span><span class="sxs-lookup"><span data-stu-id="e1b56-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="e1b56-109">Questo comando rimuove l'amministratore di Azure AD per il server denominato Server01 associato al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="e1b56-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="e1b56-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1b56-110">PARAMETERS</span></span>

### <span data-ttu-id="e1b56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1b56-111">-DefaultProfile</span></span>
<span data-ttu-id="e1b56-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e1b56-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1b56-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e1b56-113">-Force</span></span>
<span data-ttu-id="e1b56-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e1b56-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e1b56-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1b56-115">-ResourceGroupName</span></span>
<span data-ttu-id="e1b56-116">Specifica il nome del gruppo di risorse a cui è assegnato SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e1b56-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="e1b56-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="e1b56-117">-ServerName</span></span>
<span data-ttu-id="e1b56-118">Specifica il nome di SQL Server per cui questo cmdlet rimuove un amministratore.</span><span class="sxs-lookup"><span data-stu-id="e1b56-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1b56-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e1b56-119">-Confirm</span></span>
<span data-ttu-id="e1b56-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1b56-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1b56-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1b56-121">-WhatIf</span></span>
<span data-ttu-id="e1b56-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1b56-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1b56-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1b56-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1b56-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1b56-124">CommonParameters</span></span>
<span data-ttu-id="e1b56-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1b56-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1b56-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1b56-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1b56-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1b56-127">INPUTS</span></span>

### <span data-ttu-id="e1b56-128">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="e1b56-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="e1b56-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1b56-129">OUTPUTS</span></span>

### <span data-ttu-id="e1b56-130">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="e1b56-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="e1b56-131">Note</span><span class="sxs-lookup"><span data-stu-id="e1b56-131">NOTES</span></span>

## <span data-ttu-id="e1b56-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1b56-132">RELATED LINKS</span></span>

[<span data-ttu-id="e1b56-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e1b56-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="e1b56-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e1b56-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="e1b56-135">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="e1b56-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

