---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: e5460fcbc48d36dab6309891247315f0539ff7ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200149"
---
# <span data-ttu-id="1f592-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="1f592-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="1f592-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f592-102">SYNOPSIS</span></span>
<span data-ttu-id="1f592-103">Ottiene l'autenticazione solo di Azure AD per un determinato SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1f592-103">Gets Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="1f592-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f592-104">SYNTAX</span></span>

### <span data-ttu-id="1f592-105">UseResourceGroupAndServerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1f592-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f592-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f592-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f592-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f592-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f592-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f592-108">DESCRIPTION</span></span>
<span data-ttu-id="1f592-109">Il cmdlet **Get-AzSqlServerActiveDirectoryOnlyAuthentication** ottiene solo Azure Active Directory (Azure ad) solo un requisito di autenticazione per un server AzureSQL nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="1f592-109">The **Get-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="1f592-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f592-110">EXAMPLES</span></span>

### <span data-ttu-id="1f592-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1f592-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="1f592-112">Questo comando ottiene solo Azure Active Directory (Azure AD) solo il requisito di autenticazione per un server AzureSQL denominato Server01 associato a un gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="1f592-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="1f592-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f592-113">PARAMETERS</span></span>

### <span data-ttu-id="1f592-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f592-114">-DefaultProfile</span></span>
<span data-ttu-id="1f592-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f592-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f592-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f592-116">-InputObject</span></span>
<span data-ttu-id="1f592-117">Oggetto di SQL Server da usare.</span><span class="sxs-lookup"><span data-stu-id="1f592-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="1f592-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f592-118">-ResourceGroupName</span></span>
<span data-ttu-id="1f592-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1f592-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="1f592-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f592-120">-ResourceId</span></span>
<span data-ttu-id="1f592-121">ID risorsa dell'istanza da usare</span><span class="sxs-lookup"><span data-stu-id="1f592-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="1f592-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="1f592-122">-ServerName</span></span>
<span data-ttu-id="1f592-123">Nome di Azure SQL Server in cui è presente solo l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1f592-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="1f592-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f592-124">-Confirm</span></span>
<span data-ttu-id="1f592-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f592-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f592-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f592-126">-WhatIf</span></span>
<span data-ttu-id="1f592-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f592-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f592-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f592-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f592-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f592-129">CommonParameters</span></span>
<span data-ttu-id="1f592-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f592-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f592-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f592-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f592-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f592-132">INPUTS</span></span>

### <span data-ttu-id="1f592-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1f592-133">System.String</span></span>

## <span data-ttu-id="1f592-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f592-134">OUTPUTS</span></span>

### <span data-ttu-id="1f592-135">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="1f592-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="1f592-136">Note</span><span class="sxs-lookup"><span data-stu-id="1f592-136">NOTES</span></span>

## <span data-ttu-id="1f592-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f592-137">RELATED LINKS</span></span>

[<span data-ttu-id="1f592-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="1f592-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="1f592-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="1f592-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="1f592-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="1f592-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="1f592-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="1f592-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="1f592-142">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="1f592-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)