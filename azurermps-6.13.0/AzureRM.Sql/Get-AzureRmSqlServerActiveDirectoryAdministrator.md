---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 1ccc18aa77327878d151b888253e68478da29fbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686038"
---
# <span data-ttu-id="935b3-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="935b3-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="935b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="935b3-102">SYNOPSIS</span></span>
<span data-ttu-id="935b3-103">Ottiene informazioni su un amministratore di Azure AD per SQL Server.</span><span class="sxs-lookup"><span data-stu-id="935b3-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="935b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="935b3-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="935b3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="935b3-105">DESCRIPTION</span></span>
<span data-ttu-id="935b3-106">Il cmdlet **Get-AzureRmSqlServerActiveDirectoryAdministrator** ottiene le informazioni su un amministratore di Azure Active Directory (Azure ad) per un server AzureSQL nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="935b3-106">The **Get-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="935b3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="935b3-107">EXAMPLES</span></span>

### <span data-ttu-id="935b3-108">Esempio 1: ottiene informazioni su un amministratore per un server</span><span class="sxs-lookup"><span data-stu-id="935b3-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="935b3-109">Questo comando consente di ottenere informazioni su un amministratore di Azure AD per un server denominato Server01 associato a un gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="935b3-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="935b3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="935b3-110">PARAMETERS</span></span>

### <span data-ttu-id="935b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935b3-111">-DefaultProfile</span></span>
<span data-ttu-id="935b3-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="935b3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="935b3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="935b3-113">-ResourceGroupName</span></span>
<span data-ttu-id="935b3-114">Specifica il nome del gruppo di risorse a cui è assegnato SQL Server.</span><span class="sxs-lookup"><span data-stu-id="935b3-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="935b3-115">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="935b3-115">-ServerName</span></span>
<span data-ttu-id="935b3-116">Specifica il nome di SQL Server per cui questo cmdlet ottiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="935b3-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="935b3-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="935b3-117">-Confirm</span></span>
<span data-ttu-id="935b3-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="935b3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="935b3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="935b3-119">-WhatIf</span></span>
<span data-ttu-id="935b3-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="935b3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="935b3-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="935b3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="935b3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935b3-122">CommonParameters</span></span>
<span data-ttu-id="935b3-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="935b3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935b3-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="935b3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935b3-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="935b3-125">INPUTS</span></span>

### <span data-ttu-id="935b3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="935b3-126">System.String</span></span>

## <span data-ttu-id="935b3-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="935b3-127">OUTPUTS</span></span>

### <span data-ttu-id="935b3-128">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="935b3-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="935b3-129">Note</span><span class="sxs-lookup"><span data-stu-id="935b3-129">NOTES</span></span>

## <span data-ttu-id="935b3-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="935b3-130">RELATED LINKS</span></span>

[<span data-ttu-id="935b3-131">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="935b3-131">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="935b3-132">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="935b3-132">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="935b3-133">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="935b3-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


