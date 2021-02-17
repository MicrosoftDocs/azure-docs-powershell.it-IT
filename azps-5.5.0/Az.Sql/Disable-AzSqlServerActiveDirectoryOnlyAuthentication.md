---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 8d9214b44d5e408717968d042a1cdb86cd25130a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196191"
---
# <span data-ttu-id="96752-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="96752-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="96752-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96752-102">SYNOPSIS</span></span>
<span data-ttu-id="96752-103">Disabilita l'autenticazione di Azure AD solo per una specifica SQL Server.</span><span class="sxs-lookup"><span data-stu-id="96752-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="96752-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96752-104">SYNTAX</span></span>

### <span data-ttu-id="96752-105">UseResourceGroupAndServerNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="96752-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96752-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96752-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96752-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96752-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96752-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="96752-108">DESCRIPTION</span></span>
<span data-ttu-id="96752-109">Il cmdlet **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** disabilita il requisito di autenticazione di Azure Active Directory (Azure AD) solo per un server AzureSQL nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="96752-109">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="96752-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96752-110">EXAMPLES</span></span>

### <span data-ttu-id="96752-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="96752-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   False
```

<span data-ttu-id="96752-112">Questo comando disabilita il requisito di autenticazione di Azure Active Directory (Azure AD) solo per un server AzureSQL denominato Server01 associato a un gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="96752-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="96752-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96752-113">PARAMETERS</span></span>

### <span data-ttu-id="96752-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96752-114">-DefaultProfile</span></span>
<span data-ttu-id="96752-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96752-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96752-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96752-116">-InputObject</span></span>
<span data-ttu-id="96752-117">Oggetto SQL server da usare.</span><span class="sxs-lookup"><span data-stu-id="96752-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="96752-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96752-118">-ResourceGroupName</span></span>
<span data-ttu-id="96752-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="96752-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="96752-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96752-120">-ResourceId</span></span>
<span data-ttu-id="96752-121">ID risorsa dell'istanza da usare</span><span class="sxs-lookup"><span data-stu-id="96752-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="96752-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="96752-122">-ServerName</span></span>
<span data-ttu-id="96752-123">Il nome dell'account Azure SQL Server'autenticazione di Azure Active Directory è in.</span><span class="sxs-lookup"><span data-stu-id="96752-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="96752-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96752-124">-Confirm</span></span>
<span data-ttu-id="96752-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96752-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96752-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96752-126">-WhatIf</span></span>
<span data-ttu-id="96752-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96752-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96752-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96752-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96752-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96752-129">CommonParameters</span></span>
<span data-ttu-id="96752-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96752-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96752-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="96752-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96752-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="96752-132">INPUTS</span></span>

### <span data-ttu-id="96752-133">System.String</span><span class="sxs-lookup"><span data-stu-id="96752-133">System.String</span></span>

## <span data-ttu-id="96752-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96752-134">OUTPUTS</span></span>

### <span data-ttu-id="96752-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="96752-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="96752-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="96752-136">NOTES</span></span>

## <span data-ttu-id="96752-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96752-137">RELATED LINKS</span></span>

[<span data-ttu-id="96752-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="96752-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="96752-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="96752-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="96752-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="96752-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="96752-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="96752-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="96752-142">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="96752-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)