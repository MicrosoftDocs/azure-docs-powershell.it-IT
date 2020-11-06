---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
ms.openlocfilehash: a3af56ab78cd31dde30939901eaff12fff78ffa2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519847"
---
# <span data-ttu-id="fe3fc-101">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="fe3fc-101">Get-AzureRmSqlServer</span></span>

## <span data-ttu-id="fe3fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe3fc-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3fc-103">Restituisce informazioni sui server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="fe3fc-103">Returns information about SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe3fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe3fc-104">SYNTAX</span></span>

```
Get-AzureRmSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe3fc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe3fc-105">DESCRIPTION</span></span>
<span data-ttu-id="fe3fc-106">Il cmdlet **Get-AzureRmSqlServer** restituisce informazioni su uno o più server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="fe3fc-106">The **Get-AzureRmSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="fe3fc-107">Specificare il nome di un server per visualizzare le informazioni solo per il server.</span><span class="sxs-lookup"><span data-stu-id="fe3fc-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="fe3fc-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe3fc-108">EXAMPLES</span></span>

### <span data-ttu-id="fe3fc-109">Esempio 1: ottenere tutte le istanze di SQL Server assegnate a un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fe3fc-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="fe3fc-110">Questo comando consente di ottenere informazioni su tutti i server di database SQL di Azure assegnati al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="fe3fc-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="fe3fc-111">Esempio 2: ottenere informazioni su un server di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="fe3fc-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="fe3fc-112">Questo comando consente di ottenere informazioni sul server di database SQL di Azure denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="fe3fc-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="fe3fc-113">Esempio 3: ottenere tutte le istanze di SQL Server nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="fe3fc-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmSqlServer
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

<span data-ttu-id="fe3fc-114">Questo comando consente di ottenere informazioni su tutti i server di database SQL di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="fe3fc-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

## <span data-ttu-id="fe3fc-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe3fc-115">PARAMETERS</span></span>

### <span data-ttu-id="fe3fc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3fc-116">-DefaultProfile</span></span>
<span data-ttu-id="fe3fc-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fe3fc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe3fc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe3fc-118">-ResourceGroupName</span></span>
<span data-ttu-id="fe3fc-119">Specifica il nome del gruppo di risorse a cui sono assegnati i server.</span><span class="sxs-lookup"><span data-stu-id="fe3fc-119">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe3fc-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="fe3fc-120">-ServerName</span></span>
<span data-ttu-id="fe3fc-121">Specifica il nome del server ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe3fc-121">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe3fc-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fe3fc-122">-Confirm</span></span>
<span data-ttu-id="fe3fc-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe3fc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe3fc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe3fc-124">-WhatIf</span></span>
<span data-ttu-id="fe3fc-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe3fc-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe3fc-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe3fc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe3fc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3fc-127">CommonParameters</span></span>
<span data-ttu-id="fe3fc-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe3fc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3fc-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe3fc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3fc-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe3fc-130">INPUTS</span></span>

### <span data-ttu-id="fe3fc-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fe3fc-131">None</span></span>
<span data-ttu-id="fe3fc-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="fe3fc-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe3fc-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe3fc-133">OUTPUTS</span></span>

### <span data-ttu-id="fe3fc-134">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="fe3fc-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="fe3fc-135">Note</span><span class="sxs-lookup"><span data-stu-id="fe3fc-135">NOTES</span></span>

## <span data-ttu-id="fe3fc-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe3fc-136">RELATED LINKS</span></span>

[<span data-ttu-id="fe3fc-137">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="fe3fc-137">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="fe3fc-138">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="fe3fc-138">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="fe3fc-139">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="fe3fc-139">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="fe3fc-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="fe3fc-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


