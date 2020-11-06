---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
ms.openlocfilehash: f2d687ce10edf56fc424c03873c733971f70e546
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519957"
---
# <span data-ttu-id="06c5f-101">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="06c5f-101">Get-AzureRmSqlServer</span></span>

## <span data-ttu-id="06c5f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="06c5f-103">Restituisce informazioni sui server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="06c5f-103">Returns information about SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06c5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06c5f-104">SYNTAX</span></span>

```
Get-AzureRmSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06c5f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06c5f-105">DESCRIPTION</span></span>
<span data-ttu-id="06c5f-106">Il cmdlet **Get-AzureRmSqlServer** restituisce informazioni su uno o più server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="06c5f-106">The **Get-AzureRmSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="06c5f-107">Specificare il nome di un server per visualizzare le informazioni solo per il server.</span><span class="sxs-lookup"><span data-stu-id="06c5f-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="06c5f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06c5f-108">EXAMPLES</span></span>

### <span data-ttu-id="06c5f-109">Esempio 1: ottenere tutte le istanze di SQL Server assegnate a un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="06c5f-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLoginSqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="06c5f-110">Questo comando consente di ottenere informazioni su tutti i server di database SQL di Azure assegnati al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="06c5f-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="06c5f-111">Esempio 2: ottenere informazioni su un server di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="06c5f-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="06c5f-112">Questo comando consente di ottenere informazioni sul server di database SQL di Azure denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="06c5f-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="06c5f-113">Esempio 3: ottenere tutte le istanze di SQL Server nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="06c5f-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="06c5f-114">Questo comando consente di ottenere informazioni su tutti i server di database SQL di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="06c5f-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

## <span data-ttu-id="06c5f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06c5f-115">PARAMETERS</span></span>

### <span data-ttu-id="06c5f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06c5f-116">-ResourceGroupName</span></span>
<span data-ttu-id="06c5f-117">Specifica il nome del gruppo di risorse a cui sono assegnati i server.</span><span class="sxs-lookup"><span data-stu-id="06c5f-117">Specifies the name of the resource group to which servers are assigned.</span></span>

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

### <span data-ttu-id="06c5f-118">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="06c5f-118">-ServerName</span></span>
<span data-ttu-id="06c5f-119">Specifica il nome del server ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06c5f-119">Specifies the name of the server that this cmdlet gets.</span></span>

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

### <span data-ttu-id="06c5f-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06c5f-120">-Confirm</span></span>
<span data-ttu-id="06c5f-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06c5f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06c5f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06c5f-122">-WhatIf</span></span>
<span data-ttu-id="06c5f-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06c5f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06c5f-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06c5f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06c5f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06c5f-125">-DefaultProfile</span></span>
<span data-ttu-id="06c5f-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06c5f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06c5f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c5f-127">CommonParameters</span></span>
<span data-ttu-id="06c5f-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06c5f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c5f-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06c5f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c5f-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06c5f-130">INPUTS</span></span>

## <span data-ttu-id="06c5f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06c5f-131">OUTPUTS</span></span>

### <span data-ttu-id="06c5f-132">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="06c5f-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="06c5f-133">Note</span><span class="sxs-lookup"><span data-stu-id="06c5f-133">NOTES</span></span>

## <span data-ttu-id="06c5f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06c5f-134">RELATED LINKS</span></span>

[<span data-ttu-id="06c5f-135">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="06c5f-135">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="06c5f-136">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="06c5f-136">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="06c5f-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="06c5f-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="06c5f-138">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="06c5f-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


