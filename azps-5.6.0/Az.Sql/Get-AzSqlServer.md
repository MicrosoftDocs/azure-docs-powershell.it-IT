---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
ms.openlocfilehash: 26a1e7dab44f71aa14990fe4e46a2f79a24e9067
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999261"
---
# <span data-ttu-id="27602-101">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="27602-101">Get-AzSqlServer</span></span>

## <span data-ttu-id="27602-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27602-102">SYNOPSIS</span></span>
<span data-ttu-id="27602-103">Restituisce informazioni sui server SQL database.</span><span class="sxs-lookup"><span data-stu-id="27602-103">Returns information about SQL Database servers.</span></span>

## <span data-ttu-id="27602-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27602-104">SYNTAX</span></span>

```
Get-AzSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27602-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="27602-105">DESCRIPTION</span></span>
<span data-ttu-id="27602-106">Il cmdlet **Get-AzSqlServer** restituisce informazioni su uno o più server di database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="27602-106">The **Get-AzSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="27602-107">Specificare il nome di un server per visualizzare le informazioni solo per tale server.</span><span class="sxs-lookup"><span data-stu-id="27602-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="27602-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27602-108">EXAMPLES</span></span>

### <span data-ttu-id="27602-109">Esempio 1: Ottenere tutte le istanze SQL Server assegnate a un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="27602-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="27602-110">Questo comando ottiene informazioni su tutti i server di SQL database di Azure assegnati al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="27602-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="27602-111">Esempio 2: Ottenere informazioni su un server di SQL Azure</span><span class="sxs-lookup"><span data-stu-id="27602-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="27602-112">Questo comando recupera informazioni sul server di SQL azure denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="27602-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="27602-113">Esempio 3: Recuperare tutte le istanze SQL Server'abbonamento</span><span class="sxs-lookup"><span data-stu-id="27602-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server03.database.windows.net
```

<span data-ttu-id="27602-114">Questo comando ottiene informazioni su tutti i server di SQL di Azure nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="27602-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

### <span data-ttu-id="27602-115">Esempio 4: Ottenere tutte le istanze di SQL Server assegnate a un gruppo di risorse usando il filtro</span><span class="sxs-lookup"><span data-stu-id="27602-115">Example 4: Get all instances of SQL Server assigned to a resource group using filtering</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "server*"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="27602-116">Questo comando ottiene informazioni su tutti i server di SQL database di Azure assegnati al gruppo di risorse ResourceGroup01 che iniziano con "server".</span><span class="sxs-lookup"><span data-stu-id="27602-116">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01 that start with "server".</span></span>

## <span data-ttu-id="27602-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27602-117">PARAMETERS</span></span>

### <span data-ttu-id="27602-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27602-118">-DefaultProfile</span></span>
<span data-ttu-id="27602-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="27602-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27602-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27602-120">-ResourceGroupName</span></span>
<span data-ttu-id="27602-121">Specifica il nome del gruppo di risorse a cui sono assegnati server.</span><span class="sxs-lookup"><span data-stu-id="27602-121">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27602-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="27602-122">-ServerName</span></span>
<span data-ttu-id="27602-123">Specifica il nome del server che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27602-123">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27602-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27602-124">-Confirm</span></span>
<span data-ttu-id="27602-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27602-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27602-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27602-126">-WhatIf</span></span>
<span data-ttu-id="27602-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27602-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27602-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27602-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27602-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27602-129">CommonParameters</span></span>
<span data-ttu-id="27602-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27602-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27602-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="27602-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27602-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="27602-132">INPUTS</span></span>

### <span data-ttu-id="27602-133">System.String</span><span class="sxs-lookup"><span data-stu-id="27602-133">System.String</span></span>

## <span data-ttu-id="27602-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27602-134">OUTPUTS</span></span>

### <span data-ttu-id="27602-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="27602-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="27602-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="27602-136">NOTES</span></span>

## <span data-ttu-id="27602-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27602-137">RELATED LINKS</span></span>

[<span data-ttu-id="27602-138">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="27602-138">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="27602-139">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="27602-139">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="27602-140">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="27602-140">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="27602-141">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="27602-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


