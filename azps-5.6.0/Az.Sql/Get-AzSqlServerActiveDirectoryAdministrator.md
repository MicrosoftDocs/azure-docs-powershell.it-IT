---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 09b7ebf1f88479bca847566b2da93feb83b18571
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974221"
---
# <span data-ttu-id="280af-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="280af-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="280af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="280af-102">SYNOPSIS</span></span>
<span data-ttu-id="280af-103">Recupera informazioni su un amministratore di Azure AD per SQL Server.</span><span class="sxs-lookup"><span data-stu-id="280af-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="280af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="280af-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="280af-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="280af-105">DESCRIPTION</span></span>
<span data-ttu-id="280af-106">Il cmdlet **Get-AzSqlServerActiveDirectoryAdministrator** ottiene informazioni su un amministratore di Azure Active Directory (Azure AD) per un server AzureSQL nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="280af-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="280af-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="280af-107">EXAMPLES</span></span>

### <span data-ttu-id="280af-108">Esempio 1: ottiene informazioni su un amministratore per un server</span><span class="sxs-lookup"><span data-stu-id="280af-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b true
```

<span data-ttu-id="280af-109">Questo comando ottiene informazioni su un amministratore di Azure AD per un server denominato Server01 associato a un gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="280af-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="280af-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="280af-110">PARAMETERS</span></span>

### <span data-ttu-id="280af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="280af-111">-DefaultProfile</span></span>
<span data-ttu-id="280af-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="280af-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="280af-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="280af-113">-ResourceGroupName</span></span>
<span data-ttu-id="280af-114">Specifica il nome del gruppo di risorse a cui è SQL Server risorsa.</span><span class="sxs-lookup"><span data-stu-id="280af-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="280af-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="280af-115">-ServerName</span></span>
<span data-ttu-id="280af-116">Specifica il nome della SQL Server per cui il cmdlet riceve informazioni.</span><span class="sxs-lookup"><span data-stu-id="280af-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="280af-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="280af-117">-Confirm</span></span>
<span data-ttu-id="280af-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="280af-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="280af-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="280af-119">-WhatIf</span></span>
<span data-ttu-id="280af-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="280af-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="280af-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="280af-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="280af-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="280af-122">CommonParameters</span></span>
<span data-ttu-id="280af-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="280af-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="280af-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="280af-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="280af-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="280af-125">INPUTS</span></span>

### <span data-ttu-id="280af-126">System.String</span><span class="sxs-lookup"><span data-stu-id="280af-126">System.String</span></span>

## <span data-ttu-id="280af-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="280af-127">OUTPUTS</span></span>

### <span data-ttu-id="280af-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="280af-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="280af-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="280af-129">NOTES</span></span>

## <span data-ttu-id="280af-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="280af-130">RELATED LINKS</span></span>

[<span data-ttu-id="280af-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="280af-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="280af-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="280af-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="280af-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="280af-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="280af-134">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="280af-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


