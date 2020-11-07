---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 030a5ed61b4faafb47e8cba808dada484180a01c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688506"
---
# <span data-ttu-id="c747d-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c747d-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="c747d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c747d-102">SYNOPSIS</span></span>
<span data-ttu-id="c747d-103">Rimuove un amministratore di Azure AD per SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c747d-103">Removes an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c747d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c747d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c747d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c747d-105">DESCRIPTION</span></span>
<span data-ttu-id="c747d-106">Il cmdlet **Remove-AzureRmSqlServerActiveDirectoryAdministrator** rimuove un amministratore di Azure Active Directory (Azure ad) per il server AzureSQL nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="c747d-106">The **Remove-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="c747d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c747d-107">EXAMPLES</span></span>

### <span data-ttu-id="c747d-108">Esempio 1: rimuovere un amministratore</span><span class="sxs-lookup"><span data-stu-id="c747d-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="c747d-109">Questo comando rimuove l'amministratore di Azure AD per il server denominato Server01 associato al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="c747d-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="c747d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c747d-110">PARAMETERS</span></span>

### <span data-ttu-id="c747d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c747d-111">-Force</span></span>
<span data-ttu-id="c747d-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c747d-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c747d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c747d-113">-ResourceGroupName</span></span>
<span data-ttu-id="c747d-114">Specifica il nome del gruppo di risorse a cui è assegnato SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c747d-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="c747d-115">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="c747d-115">-ServerName</span></span>
<span data-ttu-id="c747d-116">Specifica il nome di SQL Server per cui questo cmdlet rimuove un amministratore.</span><span class="sxs-lookup"><span data-stu-id="c747d-116">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="c747d-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c747d-117">-Confirm</span></span>
<span data-ttu-id="c747d-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c747d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c747d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c747d-119">-WhatIf</span></span>
<span data-ttu-id="c747d-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c747d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c747d-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c747d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c747d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c747d-122">-DefaultProfile</span></span>
<span data-ttu-id="c747d-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c747d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c747d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c747d-124">CommonParameters</span></span>
<span data-ttu-id="c747d-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c747d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c747d-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c747d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c747d-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c747d-127">INPUTS</span></span>

### <span data-ttu-id="c747d-128">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="c747d-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="c747d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c747d-129">OUTPUTS</span></span>

### <span data-ttu-id="c747d-130">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="c747d-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="c747d-131">Note</span><span class="sxs-lookup"><span data-stu-id="c747d-131">NOTES</span></span>

## <span data-ttu-id="c747d-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c747d-132">RELATED LINKS</span></span>

[<span data-ttu-id="c747d-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c747d-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="c747d-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c747d-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="c747d-135">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="c747d-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


