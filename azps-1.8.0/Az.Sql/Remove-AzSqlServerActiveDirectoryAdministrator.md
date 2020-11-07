---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 333b2d2e8bab14798e7c5809590814e4a189b555
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676795"
---
# <span data-ttu-id="035eb-101">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="035eb-101">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="035eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="035eb-102">SYNOPSIS</span></span>
<span data-ttu-id="035eb-103">Rimuove un amministratore di Azure AD per SQL Server.</span><span class="sxs-lookup"><span data-stu-id="035eb-103">Removes an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="035eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="035eb-104">SYNTAX</span></span>

```
Remove-AzSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="035eb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="035eb-105">DESCRIPTION</span></span>
<span data-ttu-id="035eb-106">Il cmdlet **Remove-AzSqlServerActiveDirectoryAdministrator** rimuove un amministratore di Azure Active Directory (Azure ad) per il server AzureSQL nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="035eb-106">The **Remove-AzSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="035eb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="035eb-107">EXAMPLES</span></span>

### <span data-ttu-id="035eb-108">Esempio 1: rimuovere un amministratore</span><span class="sxs-lookup"><span data-stu-id="035eb-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="035eb-109">Questo comando rimuove l'amministratore di Azure AD per il server denominato Server01 associato al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="035eb-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="035eb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="035eb-110">PARAMETERS</span></span>

### <span data-ttu-id="035eb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="035eb-111">-DefaultProfile</span></span>
<span data-ttu-id="035eb-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="035eb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="035eb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="035eb-113">-Force</span></span>
<span data-ttu-id="035eb-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="035eb-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="035eb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="035eb-115">-ResourceGroupName</span></span>
<span data-ttu-id="035eb-116">Specifica il nome del gruppo di risorse a cui è assegnato SQL Server.</span><span class="sxs-lookup"><span data-stu-id="035eb-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="035eb-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="035eb-117">-ServerName</span></span>
<span data-ttu-id="035eb-118">Specifica il nome di SQL Server per cui questo cmdlet rimuove un amministratore.</span><span class="sxs-lookup"><span data-stu-id="035eb-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="035eb-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="035eb-119">-Confirm</span></span>
<span data-ttu-id="035eb-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="035eb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="035eb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="035eb-121">-WhatIf</span></span>
<span data-ttu-id="035eb-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="035eb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="035eb-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="035eb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="035eb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="035eb-124">CommonParameters</span></span>
<span data-ttu-id="035eb-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="035eb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="035eb-126">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="035eb-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="035eb-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="035eb-127">INPUTS</span></span>

### <span data-ttu-id="035eb-128">System. String</span><span class="sxs-lookup"><span data-stu-id="035eb-128">System.String</span></span>

## <span data-ttu-id="035eb-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="035eb-129">OUTPUTS</span></span>

### <span data-ttu-id="035eb-130">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="035eb-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="035eb-131">Note</span><span class="sxs-lookup"><span data-stu-id="035eb-131">NOTES</span></span>

## <span data-ttu-id="035eb-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="035eb-132">RELATED LINKS</span></span>

[<span data-ttu-id="035eb-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="035eb-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="035eb-134">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="035eb-134">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="035eb-135">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="035eb-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

