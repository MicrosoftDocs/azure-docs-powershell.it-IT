---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 0b1759d6c2dc364904c50df010e6151351999f8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974205"
---
# <span data-ttu-id="8527a-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="8527a-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="8527a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8527a-102">SYNOPSIS</span></span>
<span data-ttu-id="8527a-103">Recupera l'autenticazione di Azure AD solo per una SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8527a-103">Gets Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="8527a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8527a-104">SYNTAX</span></span>

### <span data-ttu-id="8527a-105">UseResourceGroupAndServerNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="8527a-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8527a-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8527a-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8527a-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8527a-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8527a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8527a-108">DESCRIPTION</span></span>
<span data-ttu-id="8527a-109">Il cmdlet **Get-AzSqlServerActiveDirectoryOnlyAuthentication** ottiene il requisito di autenticazione di Azure Active Directory (Azure AD) solo per un server AzureSQL nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="8527a-109">The **Get-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="8527a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8527a-110">EXAMPLES</span></span>

### <span data-ttu-id="8527a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8527a-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="8527a-112">Questo comando ottiene solo il requisito di autenticazione di Azure Active Directory (Azure AD) per un server AzureSQL denominato Server01 associato a un gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="8527a-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="8527a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8527a-113">PARAMETERS</span></span>

### <span data-ttu-id="8527a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8527a-114">-DefaultProfile</span></span>
<span data-ttu-id="8527a-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8527a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8527a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8527a-116">-InputObject</span></span>
<span data-ttu-id="8527a-117">Oggetto SQL server da usare.</span><span class="sxs-lookup"><span data-stu-id="8527a-117">The SQL server object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8527a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8527a-118">-ResourceGroupName</span></span>
<span data-ttu-id="8527a-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8527a-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8527a-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8527a-120">-ResourceId</span></span>
<span data-ttu-id="8527a-121">ID risorsa dell'istanza da usare</span><span class="sxs-lookup"><span data-stu-id="8527a-121">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8527a-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8527a-122">-ServerName</span></span>
<span data-ttu-id="8527a-123">Il nome dell'account Azure SQL Server'autenticazione di Azure Active Directory è in.</span><span class="sxs-lookup"><span data-stu-id="8527a-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8527a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8527a-124">-Confirm</span></span>
<span data-ttu-id="8527a-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8527a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8527a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8527a-126">-WhatIf</span></span>
<span data-ttu-id="8527a-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8527a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8527a-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8527a-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8527a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8527a-129">CommonParameters</span></span>
<span data-ttu-id="8527a-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8527a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8527a-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8527a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8527a-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="8527a-132">INPUTS</span></span>

### <span data-ttu-id="8527a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8527a-133">System.String</span></span>

## <span data-ttu-id="8527a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8527a-134">OUTPUTS</span></span>

### <span data-ttu-id="8527a-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="8527a-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="8527a-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="8527a-136">NOTES</span></span>

## <span data-ttu-id="8527a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8527a-137">RELATED LINKS</span></span>

[<span data-ttu-id="8527a-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="8527a-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="8527a-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="8527a-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="8527a-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8527a-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="8527a-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8527a-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="8527a-142">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="8527a-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)