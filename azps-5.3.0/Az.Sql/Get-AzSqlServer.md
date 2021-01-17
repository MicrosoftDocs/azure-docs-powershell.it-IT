---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
ms.openlocfilehash: 79577b9812f743035d90b2c4fe112dd9f2468fd2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475628"
---
# <span data-ttu-id="be7f9-101">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="be7f9-101">Get-AzSqlServer</span></span>

## <span data-ttu-id="be7f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be7f9-102">SYNOPSIS</span></span>
<span data-ttu-id="be7f9-103">Restituisce informazioni sui server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="be7f9-103">Returns information about SQL Database servers.</span></span>

## <span data-ttu-id="be7f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be7f9-104">SYNTAX</span></span>

```
Get-AzSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be7f9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be7f9-105">DESCRIPTION</span></span>
<span data-ttu-id="be7f9-106">Il cmdlet **Get-AzSqlServer** restituisce informazioni su uno o più server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="be7f9-106">The **Get-AzSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="be7f9-107">Specificare il nome di un server per visualizzare le informazioni solo per il server.</span><span class="sxs-lookup"><span data-stu-id="be7f9-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="be7f9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be7f9-108">EXAMPLES</span></span>

### <span data-ttu-id="be7f9-109">Esempio 1: ottenere tutte le istanze di SQL Server assegnate a un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="be7f9-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
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

<span data-ttu-id="be7f9-110">Questo comando consente di ottenere informazioni su tutti i server di database SQL di Azure assegnati al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="be7f9-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="be7f9-111">Esempio 2: ottenere informazioni su un server di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="be7f9-111">Example 2: Get information about an Azure SQL Database server</span></span>
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

<span data-ttu-id="be7f9-112">Questo comando consente di ottenere informazioni sul server di database SQL di Azure denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="be7f9-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="be7f9-113">Esempio 3: ottenere tutte le istanze di SQL Server nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="be7f9-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
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

<span data-ttu-id="be7f9-114">Questo comando consente di ottenere informazioni su tutti i server di database SQL di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="be7f9-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

### <span data-ttu-id="be7f9-115">Esempio 4: ottenere tutte le istanze di SQL Server assegnate a un gruppo di risorse tramite filtro</span><span class="sxs-lookup"><span data-stu-id="be7f9-115">Example 4: Get all instances of SQL Server assigned to a resource group using filtering</span></span>
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

<span data-ttu-id="be7f9-116">Questo comando consente di ottenere informazioni su tutti i server di database SQL di Azure assegnati al gruppo di risorse ResourceGroup01 che iniziano con "Server".</span><span class="sxs-lookup"><span data-stu-id="be7f9-116">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01 that start with "server".</span></span>

## <span data-ttu-id="be7f9-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be7f9-117">PARAMETERS</span></span>

### <span data-ttu-id="be7f9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be7f9-118">-DefaultProfile</span></span>
<span data-ttu-id="be7f9-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="be7f9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be7f9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be7f9-120">-ResourceGroupName</span></span>
<span data-ttu-id="be7f9-121">Specifica il nome del gruppo di risorse a cui sono assegnati i server.</span><span class="sxs-lookup"><span data-stu-id="be7f9-121">Specifies the name of the resource group to which servers are assigned.</span></span>

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

### <span data-ttu-id="be7f9-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="be7f9-122">-ServerName</span></span>
<span data-ttu-id="be7f9-123">Specifica il nome del server ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be7f9-123">Specifies the name of the server that this cmdlet gets.</span></span>

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

### <span data-ttu-id="be7f9-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="be7f9-124">-Confirm</span></span>
<span data-ttu-id="be7f9-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be7f9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be7f9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be7f9-126">-WhatIf</span></span>
<span data-ttu-id="be7f9-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be7f9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be7f9-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be7f9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be7f9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be7f9-129">CommonParameters</span></span>
<span data-ttu-id="be7f9-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be7f9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be7f9-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be7f9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be7f9-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be7f9-132">INPUTS</span></span>

### <span data-ttu-id="be7f9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="be7f9-133">System.String</span></span>

## <span data-ttu-id="be7f9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be7f9-134">OUTPUTS</span></span>

### <span data-ttu-id="be7f9-135">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="be7f9-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="be7f9-136">Note</span><span class="sxs-lookup"><span data-stu-id="be7f9-136">NOTES</span></span>

## <span data-ttu-id="be7f9-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be7f9-137">RELATED LINKS</span></span>

[<span data-ttu-id="be7f9-138">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="be7f9-138">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="be7f9-139">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="be7f9-139">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="be7f9-140">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="be7f9-140">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="be7f9-141">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="be7f9-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


